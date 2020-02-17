# learn-dart
Learn the Dart programming language to build cross-platform (Mobile, Web &amp; Desktop) Apps with Flutter!

## What ?

Dart is an open-source general-purpose programming language. It is originally developed by Google and later approved as a standard by ECMA.</br>
Dart is a new programming language meant for the server as well as the browser. Introduced by Google, the Dart SDK ships with its compiler – the Dart VM.</br>
The SDK also includes a utility -dart2js, a transpiler that generates JavaScript equivalent of a Dart Script.</br> 
Is an object-oriented language with C-style syntax which can optionally trans compile into JavaScript. It supports a varied range of programming aids like interfaces, classes, collections, generics, and optional typing.


## Who ?

This tutorial will be quite helpful for all those developers who want to develop single-page web applications using Dart. It is meant for programmers with a strong hold on object-oriented concepts.

## Why use Dart ?

### Pros And Cons:

Pros Include:
- Familiar language
- Built-in package manager
- Compiles to JavaScript
- Dart runs on the server, with bundles for http server, web sockets, files, directories, and more
- Full reflection API (mirrors)


Cons Include:
- Not as mature as Java
- Not as many packages as Node.js


## Dart Installation:

Install using Chocolatey.(https://chocolatey.org/).

First install Chocolatey, then go to your command line or to the powershell and run this command:

![Screen Shot 2020-01-09 at 14 55 49](https://user-images.githubusercontent.com/27420533/72078304-c06b0380-32f0-11ea-894b-9e5f1e58b882.png)

To upgrade the Dart SDK, run this command:

![Screen Shot 2020-01-09 at 14 56 38](https://user-images.githubusercontent.com/27420533/72078414-f1e3cf00-32f0-11ea-82b1-14f3d4979dc1.png)


Install using a setup wizard.
Alternatively, use the community-supported Dart SDK installer for Windows.(https://gekorm.com/dart-windows/).


![Screen Shot 2020-01-09 at 15 04 24](https://user-images.githubusercontent.com/27420533/72078636-60289180-32f1-11ea-91ed-46531d9c63c2.png)

On completion of the SDK installation, set the PATH environment variable to −


![Screen Shot 2020-01-09 at 15 08 03](https://user-images.githubusercontent.com/27420533/72078959-fbba0200-32f1-11ea-90c1-fb7a1912ccb4.png)

Verifying the Installation</br>
To verify if Dart has been successfully installed, open the command prompt and enter the following command −

![Screen Shot 2020-01-09 at 15 08 29](https://user-images.githubusercontent.com/27420533/72079018-14c2b300-32f2-11ea-98e3-87ba97f41faa.png)

## Dart Syntax:

Syntax defines a set of rules for writing programs. Every language specification defines its own syntax. 
A Dart program is composed of −

- Variables and Operators
- Classes
- Functions
- Expressions and Programming Constructs
- Decision Making and Looping Constructs
- Comments
- Libraries and Packages

### Variables

There are several ways to define variables in Dart:

#### The keyword `var`:

```dart
var a;
a = 42;
a = 'hello'
```

In this example the variable `a` is first declared,
then initialised on the next line.
On the last line the new `'hello'` value is assigned to `a`.

However because Dart is a [statically typed language](https://dart.dev/faq#q-is-dart-a-statically-typed-language),
the following code won't compile as `a` is declared and initialised at the same time,
i.e. `a` is created and linked to values with a specific type (_`int`_)

**error**
```dart
var a = 42;
a = 'hello'; //error as the variable a must have a value of type int
```

#### Type name

```dart
int a;
a = 42;
a = 52;
```

A type name can be used to create variables.
In this example `a` is declared with the type `int`,
then the value `42` is assigned to `a`.
On the last line `a` is assigned a new `int` value.

It is also possible to declare and assign a value to a variable at the same time:

```dart
int a = 42;
```

However Dart will produce an error if multiple assignements are done
with different type of values:

**error**
```dart
int a;
a = 42;
a = 'hello'; //error as a is defined to only be assigned with a value of type int
```

#### The `final` keyword

`final` can be used to create a constant.
A constant _must_ be declared and initialised at the same time 
and cannot be changed once it has been declared.

```dart
final a = 42;
```

**error**
```dart
final a;
a = 42;
```

The type of the variable/constant can be also used with `final`:

```dart
final int a = 42;
```

Attempting to reassign a constant created with `final` keyword will produce an error:

**error**
```dart
final int a = 42;
a = 52; // error as the variable a is already defined
```

#### The `const` keyword

The `const` keyword is another way for creating constant value.
The difference with `final` is that the variable created with `const`
must be initialised at ***compile time***, `const birth  = "2008/12/26"`
whereas a `final` value must be known at ***runtime***, `final birth  = getBirthFromDB()`. Neither can be changed after it has been initialised.

```dart
const int a = 42;
```

**error**
```dart
const int a = 42;
a = 52; // attempting to assign a new value to a constant. 
```

#### The `dynamic` keyword

The `dynamic` keyword is used to create a variable that
can contain values of different types. It should be used sparingly 
otherwise we lose the primary benefit of a statically typed language.

```dart
dynamic a;
a = 42;
a = 'hello'
```

Because the type of the variable can change,
we can't write the following:

```dart
dynamic int a; // https://repl.it/repls/GreenDeadMatch
a = 42;
```

## Asynchronous events

Dart provides the `Future` class to represent asynchronous events.
For example the following `hello` function will return a `String`  in a near future: 

```dart
Future<String> hello() { // The type parameter of Future is a String, represented by <String>
    return Future.delayed(Duration(seconds: 2), () => "hello"); // Using the Future.delayed function to create a time gap of 2 seconds
}
```

A function with a return type of `Future<T>` (where `T` represents any type) 
can have _three_ possible return states: 
`Uncompleted`, `Completed ` (_with_) ***success*** and `Completed` (_with_) ***error***
When completed the function will return the type `T`, in our case the `hello` function returns a `String`.
If an error occurs then the function will return an `Error`.

To be able to use the returned value of an asynchronus function we can use the `async` and `await` keywords.
We need first to describe the function using an asynchronous function by adding the `async` keyword before the body of the function.
Then we using the asynchronous function we prefix the call to the function with `await`. This will stop the process of the function
and wait for the future result. For example we can create a `main` function which will use our `hello` function:

```dart
void main() async {
    String hi = await hello();
    print(hi); // print "hello" after 2 seconds
}

Future<String> hello() { // The type parameter of Future is a String, represented by <String>
    return Future.delayed(Duration(seconds: 2), () => "hello"); // Use Future.delayed to delay execution by 2 sec.
}
```

To test this code you can copy/paste it and run it on dartpad: https://dartpad.dev/

If we do not add the `async/await` keywords, we can still call the asynchronous `hello` function,
however the result won't be ready and the `Future` instance will be returned instead of the String:

```dart
void main() {
    dynamic hi = hello();
    print(hi); // print "Instance of _Future<String>"
}

Future<String> hello() { // The type parameter of Future is a String, represented by <String>
    return Future.delayed(Duration(seconds: 2), () => "hello"); // Using the Future.delayed function to create a time gap of 2 seconds
}
```

We can also use the `then` function which takes a callback function to get the future value:


```dart
void main() {
    hello().then((futureValue) { // futureValue is the retuned value of the hello function
        print(futureValue); // print after 2 seconds "hello"
    });
}

Future<String> hello() { // The type parameter of Future is a String, represented by <String>
    return Future.delayed(Duration(seconds: 2), () => "hello"); // Using the Future.delayed function to create a time gap of 2 seconds
}
```

Compared to `await`, `then` will not stop the process of the function and continue the execution:

```dart
void main() {
    hello().then((futureValue) { // futureValue is the retuned value of the hello function
        print(futureValue); // print after 2 seconds "hello"
    });
    print('printed first'); // This print will be displayed before 'hello'
}

Future<String> hello() { // The type parameter of Future is a String, represented by <String>
    return Future.delayed(Duration(seconds: 2), () => "hello"); // Using the Future.delayed function to create a time gap of 2 seconds
}
```

## Object-Oriented Programming in Dart

Dart is an Object-Oriented language. Object Orientation is a software development paradigm that follows real-world modelling. Object Orientation considers a program as a collection of objects that communicate with each other via mechanism called methods.

- Object
- State
- Behavior
- Identity
- Class
- Method

## Effective Code in Flutter

Even though Flutter is a language that may seem familiar to many people, the "right" way to build an application to be a success is through the use of best practices.</br>
There are some tools that can make the process easier:


## Dartanalyzer

It's Dart analysis tool. It will make it easier for us because we don't need to rely on the IDE because Dart will correct the code even before we run the application.</br> 
It also makes it easier when we need to find a bug that has occurred.</br>

## Pedantic Package

The package that aims to document Google how Dart Analysis works.
It contains pieces of Dart code that are used in best practices.</br>

To use this package just add a dependency in our pubspec.yaml:

```dart
pedantic: ^1.4.0``
```
Then to update the dependencies just use the command:


```flutter packages get```



## Dart VS Javascript:

Dart:

- Backed by Google
- In some instances, Dart is up to [twice the speed](https://benchmarksgame-team.pages.debian.net/benchmarksgame/fastest/dart.html) of JavaScript
- Quite scalable across projects
- Like Java
- Used extensively for the Flutter mobile UI framework

Javascript:

- Can be used on both front-end and back-end
- Used everywhere!
- Comes with lots of great and popular frameworks
- Fast, light-weight and flexible
- Can’t run a device which doesn’t use JavaScript today
