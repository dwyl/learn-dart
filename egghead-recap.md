ref: : https://egghead.io/courses/get-started-with-dart


## Control Flow

- `if/else` and ternary operator `<cond> ? <value-when-true> : <value-when-false>`

- `for/loop`
```dart
for (var i = 0; i < 3; i++) {
    print(i);
}
```

- `while`

```dart
var k = 0
while (k < 10) {
    print(k);
    k++;
}
```

```dart
do {
  print(k);
  k++;
} while( k < 10);
```

`break` and `continue` can be used in loop to skip or continue the flow

- `switch/case/break/default`

-  `assert`:

```dart
assert('', .isNotEmpty, 'The string is empty);
```

## Class and Inheeritance

Class define the structure of objects

```dart
Class Person {
    var name;
    var age;
    var _lastname # private property

    # getter and setter
    String get name => name;
    void set name(String newName) => name = newName;

    Person(naMe, age) { # can be replaced by Person(this.name, this.age);
        this.name = name;
        this.age = age;
    }

    # named constructor
    Person.fromJson(Map json) {
        name = json['name'];
        age = json['age'];
    }

    hello() {
        print('Hello $name');
    }
}
```

We can extend a class with the keyword `extends`

```dart
class Employee extends Person {
    int id;
    Employee(String name, int age, this.id): super(name, age);

    @override
    hello() {
        print('Id employee: $id');
    }
}
```

Cascade operator `..` chain functions on instance

## Interface, Mixins

create an interface with `abstract`

```dart
abstract class Person {
    String name;
    int age;
    void hello();
}
```

and implement the interface with `implements`

```dart
class Employee implements Person {
    String name;
    int age;
    Employee(this.name, this.age);

    void hello(){
        print('hello');
    }
}
```

- Mixin: allow to reuse a class code in other classes. Dart class can only have 1 parent.
Mixin allows to add code to a class and to keep 1 parent.

```dart

mixin OtherFeature {
    int height;
}

class Person with OtherFeature {
    ...
}
```

You can extend a mixin with another using the `on` keyword

```dart
mixin AnotherFeature on OtherFeature {

}

class Person with OtherFeature, AnotherFeature {

}
```

## Capture an dREturn Asynchronous values

Use `Futures` to manage asynchronous values
use the `then` keyword to capture the future value

```dart
void main() {
    var result = Future(() => 'Hello');
    result.then((str) => print(str));
}
```

Delay a reuslt
```dart
  var result = Future.delayed(Duration(seconds: 2), () => 'delayed string'))
  result.then((str) => print(str));
```

use `.catchError` on a future value to catch erros of the future

```dart
var error = true;
Future(() => error ? throw 'There is an error' : 'everythin ok')
  .then((str) => print(str))
  .catchError((err) => print(err))
```

use `Completer` to wrap async function (which are not Future) to a Future function

```dart
Future testAsFuture() {
    var completer = Completer();
    asyncfunc((val) => completer.complete(val));
    return completer.future;
}
```

use Future with `async/await` and `try/catch` to handle exception

```dart
Future asyncFct() async {
    try {
        var res = await futureFctCall();
        print(res);
    } catch (e) {
        print(e)
    }
}
```

## Capture and handle data streams

use a srtrean controller to manage the stream data.

```dart

void main() {
    StreamController<String> controller = StreamController<String>(); #<String> specify the type expected by the controller

    controller.stream.listen(
        (data) => print(data),
        onDone: () => print('done'),
        onError: (e) => print(e)
    );

    controller.add('hello');
    contoller.add('hello again');
    controller.addError('error!!!'); // trigger onError
    controller.close(); // trigger onDone. close returns a future
      .then((_) => print('controller process finished'));
}
```

use `asBrodcaseStream()` function to allow multiple listeners.

convert a Future to a stream with `Stream.fromFuture`

```dart
Future<String> result = HttpRequest.getString('https://dwyl.com');
Stream<String> resultStream = Stream.fromFuture(result);

resultStream.listen(
    (data) => print(data),
    onDone: () => print('done')
)
```