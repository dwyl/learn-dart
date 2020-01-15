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
then on another line initialised.
On the last line the new `'hello'` value is assigned to `a`.

However because Dart is a [statically typed language](https://dart.dev/faq#q-is-dart-a-statically-typed-language),
the following code won't compile as `a` is now declared and initialised at the same time,
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
On this example `a` is declare with the type `int`,
then the value `42` is assigned to `a`.
On the last line another int value is assinged to `a`.

It is also possible to declare and assign at the same time the variable:

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

`final` can be used to create a constant variable.
The variable _has_ to be declared and initialised at the same time!

```dart
final a = 42;
```

**error**
```dart
final a;
a = 42;
```

The type of the variable can be also used with `final`:

```dart
final int a = 42;
```

Reassigning the variable created with `final` will produce an error:

**error**
```dart
final int a = 42;
a = 52; // error as the variable a is already defined
```

#### The `const` keyword

The `const` keyword is another way for creating constant value.
The difference with `final` is that the variable created with `const`
needs to be initialised at compile time.

```dart
const int a = 42;
```

**error**
```dart
const int a = 42;
a = 52;
```

#### The `dynamic` keyword

The `dynamic` keyword is used to create a variable that
can contain values of different types.

```dart
dynamic a;
a = 42;
a = 'hello'
```

Because the type of the variable can change,
we can't write the following:

```dart
dynamic int a;
a = 42;
```

## Object-Oriented Programming in Dart

Dart is an Object-Oriented language. Object Orientation is a software development paradigm that follows real-world modelling. Object Orientation considers a program as a collection of objects that communicate with each other via mechanism called methods.


- Object
- State
- Behavior
- Identity
- Class
- Method

## Dart VS Javascript:

Dart:

- Backed by Google
- Runs twice the speed of JavaScript
- Quite scalable across projects
- Like Java
- Used extensively for the Flutter mobile UI framework

Javascript:

- Can be used on both front-end and back-end
- Used everywhere!
- Comes with lots of great and popular frameworks
- Fast, light-weight and flexible
- Can’t run a device which doesn’t use JavaScript today















