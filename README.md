<div align="center">

![learn-dart-hero-image](https://user-images.githubusercontent.com/194400/84486386-40790900-ac95-11ea-916b-e27c1d141056.png "Learn Dart intro image")

Learn the [`Dart`](https://dart.dev) programming language 
to build cross-platform Native (Mobile, Web and Desktop) Apps 
with [`Flutter`](https://github.com/dwyl/learn-flutter)!

<br />
</div>

## Why?

`Dart` is a general purpose programming language
that can be used for Servers, Client Apps, Native Mobile Apps
and _everything_ in between!
Google uses `Dart` for several of their high profile products/projects
including Google Assistant (Client), Google Home Hub
and the Google Ads Platform (_their main money maker_).

`Dart` lets you build Apps for _any_ platform
with a native interface/experience and performance.
If you want to build cross-platform _Native_ Mobile Apps 
that don't waste memory or drain the devices' battery,
use `Dart` and `Flutter`.


According to GitHub in 2019, the biggest developer community,
`Dart` is fastest growing programming language:
https://octoverse.github.com/#top-languages

![github-top-programming-languages](https://user-images.githubusercontent.com/194400/84571947-b44b0c80-ad8e-11ea-8089-de0672e9e6d1.png)

This is because, as of 2019, `Flutter` was the second fastest growing project on GitHub:
https://octoverse.github.com/#top-and-trending-projects

![flutter-to-trending-project](https://user-images.githubusercontent.com/194400/84572723-e3b04800-ad93-11ea-85e2-19e9693e5a26.png)

In 2019, `Flutter` has inclusively 
overtaken React Native
in Google search frequency and
has maintained this trend ever since:
[https://trends.google.com/trends/explore](https://trends.google.com/trends/explore?date=today%205-y&q=%2Fg%2F11f03_rzbg,react%20native)

<img width="1373" alt="google-trends-graph-flutter-v-react-native" src="https://user-images.githubusercontent.com/17494745/198244948-29e5d3a5-1b2b-4d1f-a434-d4eee2a5799c.png">


The Flutter GitHub repository: https://github.com/flutter/flutter has more Starts (_a good measure of popularity_):

Flutter Stars           |  Flutter Languages
:-------------------------:|:-------------------------:
![flutter_stars](https://user-images.githubusercontent.com/17494745/198246297-2aafe6ea-0810-4c3a-b864-653ae3f72546.png)  |  ![flutter_languages](https://user-images.githubusercontent.com/17494745/198246641-792d7f4a-d025-4035-a204-3289962bade4.png)


Additionally an important metric to consider 
is the fact that **99%** of the code for `Flutter`
is written in `Dart` which means anyone who knows `Dart` 
can read, understand and _contribute_ to it.

By contrast React Native https://github.com/facebook/react-native 
has fewer stars (_even though it's been available for longer_):

React Native Stars           |  React Native Languages
:-------------------------:|:-------------------------:
![rn_stars](https://user-images.githubusercontent.com/17494745/198247220-6f9d44c0-bfbb-4850-a47a-6459798b3285.png)  |  ![rn_languages](https://user-images.githubusercontent.com/17494745/198247332-d986d36c-d354-4367-a7bf-7c7bb0a8856c.png)


And RN is written in 5 programming languages! 
So anyone wanting to contribute a truly cross-platform UI feature 
needs to know at least `JavaScript`, `Java` and `Objective-C`.
But since there are two _other_ flavours of `C` (namely `C++` and `Objective-C++`)
used in RN, you will need to go digging for whichm one. 
If you need to _debug_ why a particular UI does not work _consistenly_
across various Android versions or between iOS devices,
you need to dig into the `Objective-C` to understand it.

You don't have that headache in `Flutter`, everything is written in `Dart`.
The comparatively _tiny_ amount of `Java` and `Objective-C`

It's a _no-brainer_ to Learn `Dart` and `Flutter`. 
`Flutter` will _inevitably_ win the Cross-platform Native Mobile App "war"
because it has `Dart` as it's foundation. 






It's worth paying attention to these growth stats.



Let's face it, you're not reading this because you want
to learn another general purpose language. 
For that you would learn/use `Python` or `JavaScript`.
You are here for the same reason as we are,
to learn `Dart` as fast as possible,
so that you can use `Flutter` to build Native Apps. 



You are here for the same reason as us,
to learn `Dart` as fast as possible,
so that you can build `Flutter` Apps.

Because you very few people are using `Dart` outside of `Flutter`;
anyone that needs _general purpose_ programming laguage uses `Python`.
If you want to build `Flutter` Apps, learn `Dart`;
this tutorial is the perfect place to start.


## What ?

`Dart` is an open-source general-purpose programming language.
It can be compiled to run as high performance JavaScript in web browsers,
or as a native app on mobile (iOS + Android)
and desktop.
Is an object-oriented language with C-style syntax
familiar to all developers who have used
an Object Oriented Programming (OOP) 
language (e.g. `JavaScript`, `Java`, `C++`, `C#`, `Go`, etc.).
It supports a varied range of programming aids like interfaces,
classes, collections, generics, and optional typing.
Don't worry if these terms are unfamilar right now,
you will learn their use through examples below.

`Dart` was created by Lars Bak and Kasper Lund
while working for Google.
`Dart` was made an official standard by
the European Computer Manufacturers Association
[ECMA 408](https://www.ecma-international.org/publications/standards/Ecma-408.htm) in 2015.
The language syntax and semantics are **stable**.




Read more:

+ Official guides:
https://dart.dev/guides
+ Wikipedia article has the history:
https://en.wikipedia.org/wiki/Dart_(programming_language)


## Who?

This tutorial is for anyone who wants to learn `Dart` from scratch
without any prior knowledge of other programming languages.

Learning `Dart` is a prerequisite 
for building cross-platform native mobile/desktop/web Apps 
with `Flutter`.


<br />

## How?

We recommend that you `clone` this Git repository 
so that you can follow along on your `localhost`
_offline_:

```sh
git clone git@github.com:dwyl/learn-dart.git && cd learn-dart
```

> **Note**: If you are unable to run code on your device 
(e.g. you're reading this on an iPad), <br />
all examples have a link to 
**Dart Pad** so you can try them online:
https://dartpad.dartlang.org


<br />

### Install `Dart`

The official installation instructions are:
https://dart.dev/get-dart


### Mac

The recommended approach is to use Homebrew 
[brew.sh](https://brew.sh)

```sh
brew tap dart-lang/dart
brew install dart
```

### Linux

Follow the official instructions 
for your version of Linux: 
https://dart.dev/get-dart


### Windows?

Install the Flutter SDK which includes Dart:
https://flutter.dev/docs/get-started/install/windows

<!-- 
We don't *want* detailed Windows installation instructions 
because we don't *use* windows for any development work. 
Read: https://www.gnu.org/proprietary/malware-microsoft.html
Anyone using Windows for should install/dual-boot Linux. 
Yes, Mac is also proprietary, but it's not actively malicious.
-->

<br />

Once you have `Dart` installed, 
if you run the following terminal command:

```sh
dart --version
```

You should see something similar to:

```sh
Dart VM version: 2.8.4 (stable) (Wed Jun 3 12:26:04 2020 +0200) on "macos_x64"
```

> You may have more _recent_ version of `Dart`; that's fine!


<br />

## Hello World!

Once you have installed `Dart` on your `localhost` 
(_or opened [Dart Pad](https://dartpad.dartlang.org) 
if you are unable to install it on your mobile device_),
open your text 
[editor of choice](https://github.com/dwyl/dev-setup/issues/37),
create a directory called [`/examples`]()
and _inside_ that directory,
create a file with path 
[`examples/hello.dart`]()

Then _type_ the following code:

```dart
main() {
  print('Hello World!');
}
```

e.g: 


This code creates a function called `main` 
which calls `print` 
with our desired `String` `'Hello World!'`.
The function does not _return_ anything 


Now in your terminal window,
execute the program by typing: 

```sh
dart examples/hello.dart
```

You should see:

```
Hello World!
```

> Try it: https://dartpad.dartlang.org/fa6f6e5a7b9406e88b31a17e82655ef8

![dart-pad-hello-world-example](https://user-images.githubusercontent.com/194400/84514887-a54b5800-acc3-11ea-80bf-4ca4f39d1869.png)


<br />

By convention, you will often see the `main` function 
prefixed with the `void` keyword/type, e.g:

```dart
void main() {
  print('Hello World!');
}
```

This just means that our `main` function will not return anything.
In this case it's safe to ommit the `void` keywork 
as it is in _inferred_ by the compiler.
We checked: 
https://stackoverflow.com/questions/62346301/does-dart-main-function

> If see the `void` keyword and are curious about it, read: <br />
> + https://en.wikipedia.org/wiki/Void_type
> + https://medium.com/flutter-community/the-curious-case-of-void-in-dart-f0535705e529
> + https://medium.com/dartlang/dart-2-legacy-of-the-void-e7afb5f44df0

<br />

## Variables

The next thing you need to know in `Dart` 
is how to create variables (_or constants_)
to store your data.

### Using the `var` Keyword

The most basic way of defining variables 
is using the `var` keyword.
Create a new file with the path:
[`examples/var.dart`]()
and type the following code in it:

```dart
main() {
  var name = 'Alex'; // or whatever your name is! 
  print('Hello $name'); 
}
```
Change the _value_ `name` to whatever your name is.

Once you have saved the file,
run it with the command:

```sh
dart examples/var.dart
```

You should see output similar to the following:

```
Hello Alex!
```

> Try it: https://dartpad.dartlang.org/560f88da44b108ffe34e6979079246ea

![dart-pad-variables-example](https://user-images.githubusercontent.com/194400/84532536-4e9f4780-acde-11ea-9bfd-7f6f0c8bcb1b.png)


_Explanation_ of the code:
+ `main() {` - is familiar from the previous example,
it's the top-level function that dart invokes to run the program.
+ `var name = 'Alex';` - this is our variable definition using the `var` keyword. We _assign_ the value `'Alex'` 
to the variable `name`. 
+ `print('Hello $name');` - prints the `String` `'Hello` 
followed by the variable `name` we defined on the previous line.
The inclusion of the `$` (dollar sign) in the `$name` 
is the way to include a variable inside the `String`.
This is knonw as 
[String interpolation](https://dart.dev/guides/language/language-tour#strings).


## `Dart` Syntax:

Syntax is reasonably concise compared to other languages like `Java` or `JavaScript`.

defines a set of rules for writing programs.
A `Dart` program is composed of:

+ Variables and Operators
+ Classes
+ Functions
+ Expressions and Programming Constructs
+ Decision Making and Looping Constructs
+ Comments
+ Libraries and Packages

<br />

### Variables

There are several ways to define variables in Dart:

#### The keyword `var`

```dart
var a;
a = 42;
```

In this example the variable `a` is first declared,
then initialised on the next line.

In the following example we attempt to
re-assign the variable `a` to a `String`,
however since
`Dart`
[statically typed](https://dart.dev/faq#q-is-dart-a-statically-typed-language),
the code won't compile.
`a` is initialised as an `int`,
so attempting to reassign it as `String`
on the next line will fail:

**error**
```dart
var a = 42;
a = 'hello';
```

You will see the following error:

```dart
Error: A value of type 'String' can't be assigned to a variable of type 'int'.
  a = 'hello';
      ^
Error: Compilation failed.
```

e.g: https://dartpad.dartlang.org/bea94fb6dec3a69799f1f040135489a0

#### Types

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

However `Dart` will produce an error if multiple assignements are done
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

### main() function

The main function is a top-level function (a function created outside of a class) which is required in all Dart programs.
It is the starting point of your program. It usually has the type void.

void main() {
  print('hello');
}
The main function can take a list of string as a parameter.

### Arrow functions

Arrow functions is a syntactic sugar expression to create one statement function.

```dart
String hello() => 'hello'
```

is the same as

```dart
String hello() {
    return 'hello';
}
```

Arrow functions can also be used to create anonymous functions:

```dart
void main() {
    var hello = () => 'hello';
    print(a());
}
```

### Named parameters

Named parameters make it easier to understand which value is assigned to the argumment of a function.
Positional parameters rely on the order of the parameters given to the function. Named parameter instead rely on the name given to the parameter,
and discard the order.
You define the parameters inside `{}` and when the function is called assign the values to the paremeters with ':':

'''dart
String hello({String firstName, String lastName}) {
  return '$firstName $lastName';
}

void main() {
    var myName = hello(firstName: 'bob', lastName: 'Smith');
    var myNameAgain = hello(lastName: 'smith', firstName: 'bob'); // the order of the paramter doesn't matter
    print(myName);
}
'''

By default named parameters are optional:

'''dart
String hello({String firstName, String lastName}) {
  return '$firstName $lastName';
}

void main() {
    var myName = hello(firstName: 'bob');
    print(myName); // print 'bob null'
}
'''

If you want a parameter to be mandatory you can anotate it with `@required`.
You need first to import the 'meta' package which contains this anotation:
`import 'package:meta/meta.dart';`

Flutter also contains this anotation in the foundation.dart package:
`import 'package:flutter/foundation.dart';`

Select one of these two import depending if your project is a Flutter application or just a Dart program.

## Asynchronous events

`Dart` provides the `Future` class to represent asynchronous events.
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

`Dart` is an Object-Oriented language.#
Object Orientation is a software development paradigm that follows real-world modelling.
Object Orientation considers a program as a collection of objects that communicate with each other via mechanism called methods.

- Object
- State
- Behavior
- Identity
- Class
- Method

### Constructor

Constructors let you create an instance of a class.
When creating a class, Dart will provide a default constructor for this class.

```dart
class Car {
    String engine;
}

void main() {
  Car myCar = Car(); //The Car() constructor is provided automatically
  print(myCar); // print Instance of 'Car'
}
```

You can also create a named constructor with the syntax `ClassName.constructorName`:

```dart
 class Car {
     String engine;

     Car.withEngine(String engine) {
         this.engine ='engine $engine';
     }
 }
```

Dart also provides a syntax sugar for a constructor which assigned instance variable:

```dart
class Car {
    String engine;

    Car(this.engine); // Create a constructor which defined the engine value
}

void main() {
    Car c = Car('electric');
    print(c.engine);
}
```

### Initializer list

Initializer list are used to assigned values to instance variables:

```dart
class Pet {
    final String name;
    final int age;


    Pet.initialise() : this.name = 'Bob', this.age = 2; // assigned default values to final variables

    String getInfo() {
        return 'name: $name, age: $age';
    }
}

void main() {
    Pet p = Pet.initialise();
    print(p.getInfo());
}
```

Initializer list can also be used to redirect a contstructor of a class to another one:

```dart
class Pet {
    String name;

    Pet(this.name); // create a constructor which set the name variable

    Pet.setName(String name) : this(name); // redirect the setName constructor to the Pet(name) constructor
}

void main() {
    Pet p = Pet.setName('Bob');
    print(p.name);
}
```

### inheritance

A class can `extends` another class to create a sub class.
A sub class can only extends one class only.

```dart
class Pet {
    String name;

    Pet() : name = 'Mike';
}

class Cat extends Pet {
    Cat() {
        name = 'Dave';
    }
}

void main() {
  Pet p = Pet();
  Cat c = Cat();
  print(p.name); // print Mike 
  print(c.name); // print Dave
}
```

If you want to redefine a method in a sub class, you can use the `@override` annotation:

```dart
 class Pet {
     String name;
   
     Pet(this.name);

     String getName() {
        return 'the pet name is: $name';
     }
 }

 class Cat extends Pet {
     Cat(String name) : super(name);

     @override
     String getName() {
         return 'the cat name is: $name';
     }
 }

void main() {
  Cat c = Cat('Bob');
  print(c.getName()); // print the cat name is: Bob
}
```

### abstract class

If the parent class is created with the `abstract` keyword then only a child class can 
create an object instance as abstract class can't be instantiated.

```dart
abstract class Pet {
    String name;
}

class Cat extends Pet {
    Cat() {
        name = 'Dave';
    }
}

void main() {
  Pet p = Pet(); // error, Pet is an abstract class
  Cat c = Cat();
  print(c.name); // print Dave
}
```

Unlike "normal" class, an abstract class can contain methods without bodies.
The idea is to let the sub class implement the logic of the method:

```dart
abstract class Pet {
  void printMessage();
}

class Cat extends Pet {
  @override
  void printMessage() { // the printMessage implementation is required in subclass
    print('cat class');
  }
}

void main() {
  Cat c = Cat();
  c.printMessage(); // cat class
}
```


When creating an instance of an inherited class, first the initialiazer list is run (if any) then
the default constructor of the parent class and
finally the default constructor of the class:

```dart
class Pet {
    String name;

    Pet() : name = 'Dave'{
        print('Pet name: $name');
    }
}

class Cat extends Pet {
    Cat() {
        print('Cat name: $name');
    }
}

void main() {
  Cat c = Cat();
  // The name is set using the initializer list
  // then the parent constructor is run
  // then the cat constructor is run

  // print Pet name: Dave
  // then print Cat name: Dave
}
```

### Class interface with `implements`

Instead of using `extends` to inherite a behavior of a class,
Dart provides the `implements` keyword which allows you to use classes as interfaces
for another class. This class doesn't inherite any method logic but it will have to define
the types and method of the referenced classes.

```dart
class PetA {
    String name;
}

class PetB {
    int age;
}

class Cat implements PetA, PetB {
    @override
    String name;
    @override
    int age;
  
    Cat(this.name, this.age);
}
void main() {
    Cat c = Cat('Dave', 2);
    print(c.name);
    print(c.age);
}
```

## Effective Code in Flutter

This section is a summary of the Effective `Dart` in Flutter article by Google Developer Expert Katarina Sheremet:
https://medium.com/flutter-community/effective-code-in-your-flutter-app-from-the-beginning-e597444e1273

The `Dart` language is familiar to most developers used to object oriented programming.
There are a few best practices worth learning to ensure success.</br>
There are some tools that can make the process easier:


## Dartanalyzer

[`Dartanalyzer`](https://dart.dev/tools/dartanalyzer) is static analysis tool for `Dart`. It analyses your code for common mistakes and makes suggestions for how to simplify things. It corrects code before we run the application.</br>

This is an example of performing static analysis
over all the `Dart` files under the lib and test directories:
`dartanalyzer lib test`

## Pedantic Package

The [pedantic](https://pub.dev/packages/pedantic) package shows how static analysis is used internally at Google.
It contains pieces of `Dart` code that are used in best practices.</br>

To use this package just add a dependency in our pubspec.yaml:

```dart
pedantic: ^1.4.0
```
Then to update the dependencies just use the command:


```flutter packages get```



## `Dart` Testing

The purpose of automated software testing is quality assurance and system reliability.</br>
It gives _assurance_ that the features built in the application conform to the original specification and acceptance criteria.
Several tests can be created to test functionality, usability, performance or security.</br>

## Types of Tests

There are several types of software tests.
In `Dart` the most commonly used tests are unit, component and end-to-end; usually in that order.

### Unit Tests

Unit tests are test small parts of code, such as a function, a class, or a change made to the layout.
Every function must have at least one unit test.
A function with multiple possible outcomes must have multiple tests; one for each case.
Each function should be responsible for doing one thing.
If your function does multiple things or you use the word "and"
when describing what a function does,
that's usually a [bad sign](https://en.wikipedia.org/wiki/Code_smell).
We use small single responsibility tested functions to assemble a larger application.
See: https://en.wikipedia.org/wiki/Single_responsibility_principle
and https://blog.codinghorror.com/curlys-law-do-one-thing/

### Component Tests

Components are composed of several smaller functions once all the unit tests for those functions are passing.
Component tests test several functions or tasks assembled into a feature at the same time as a whole.

### End-To-End Tests

The end-to-end tests are used to test entire applications or most of them on real devices, or a browser.

## Useful libraries in Dart

There are also some libraries that can be useful when talking about Dart:

```package:test```

It helps us to have a perception of how we have to put the code, it serves to test small codes or big codes.

```package:mockito```

[Mockito](https://pub.dev/packages/mockito) is a mocking library that helps us to mock functionality where we don't want to perform a specific action. We try to _avoid_ using mocks as much as possible because they can inadvertently make our tests more complex with limited benefit.


## `Dart` VS Javascript:

Dart:

- Backed by Google
- In some instances, `Dart` is up to [twice the speed](https://benchmarksgame-team.pages.debian.net/benchmarksgame/fastest/dart.html) of JavaScript
- Quite scalable across projects
- Like Java
- Used extensively for the Flutter mobile UI framework

Javascript:

- Can be used on both front-end and back-end
- Used everywhere!
- Comes with lots of great and popular frameworks
- Fast, light-weight and flexible
- Can’t run a device which doesn’t use JavaScript today
