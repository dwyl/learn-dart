## Publishing packages with Dart
The Dart ecosystem is made by packages 
and libraries that you can import in your
Dart-lang based projects. 
If you are creating a Flutter app,
you will notice you'll have a `pubspec.yaml`
file with the dependencies needed
to properly run it.

Luckily, publishing a package 
is fairly simple. 
All packages reside in https://pub.dev/
and this is the place we use to publish them.

## Before publishing
There are some constraints that 
ought to be met before publishing a package
in Dart.
Firstly, the project should have a 
`README.md`, a `CHANGELOG.md` and a
`pubspec.yaml` file 
(which is used to fill out the details 
about the package - these can be found
on the package's page, 
like in the picture below).

![package](https://user-images.githubusercontent.com/17494745/204871000-5e3f2b8b-9f43-4659-824d-3ce181a5d9f8.png)


Here's how the `pubspec.yaml` file
looks like for the 
[`dart_multihash`](https://github.com/dwyl/dart_multihash) 
package.

```yaml
name: dart_multihash
description: A dart-lang implementation of the Multihash protocol.
version: 0.0.1
homepage: https://github.com/dwyl/dart_multihash
repository: https://github.com/dwyl/dart_multihash
issue_tracker: https://github.com/dwyl/dart_multihash/issues

environment:
  sdk: '>=2.18.4 <3.0.0'

dependencies:
  buffer: ^1.1.1

dev_dependencies:
  lints: ^2.0.0
  crypto: ^3.0.2
  convert: ^3.1.1
  test: ^1.16.0
  collection: ^1.17.0
```

The `name`, `description`, `version`, 
`homepage`, `repository`, `issue tracker`,
amongst other properties effect the 
sidebar of the official page of the package
after publishing.

### Verified Publishers
If you have wondered about,
you might have noticed that 
lots of packages are published by
...well, publishers.

In the previous picture, 
regarding the `dart_multihash` package
you might have noticed that 
there's a [`dwyl.com`](https://pub.dev/publishers/dwyl.com/packages)
publisher associated.

There are a few advantages to
having a verified publisher.
The users *know* the package domain
is verified, know the organization 
behind it is trustworthy and can
safely use the package. 
Plus, you get a sweet 
![tick](https://dart.dev/assets/img/verified-publisher.svg)
icon!

If you are a person or a group of people
that is interested in publishing
under a single name, 
publishing through a verified publisher
is the way to go.

You will need your own domain and
**prove** Google that you own it. 
That is the domain the publisher
will be associated with.

For the steps to get this done,
do visit 
https://dart.dev/tools/pub/publishing#create-verified-publisher
.

## Publishing your package
So let's imagine you've 
completed your sweet Dart/Flutter
package and you want to share it
with the world! 

> There are some differences between
> Dart and Flutter packages,
> the main one being that the latter
> pertains to Flutter apps.
> Dart packages are more agnostic and
> not Flutter-specific.
> 
> If you were to use Visual Studio
> and `View -> Command Palette` and
> try to create a Flutter Package
> and a Dart Package, 
> although the project structure 
> is the same, there are two differences:
> **`pubspec.yaml` doesn't load 
> the Flutter SDK in the Dart's package**
> and the **`analysis_options.yaml` file
> imports different linting packages**.
> That's it. :smile:

Even if you are a publisher,
currently, you can't directly publish 
your package to your verified
publisher, you need to upload to your personal account
and then **transfer it** 
to the chosen verified publisher.

In your project root,
go to your terminal and type the following.

```sh
 dart pub publish --dry-run
```

This command will make sure
the package follows the 
[pubspec format](https://dart.dev/tools/pub/pubspec)
and [package layout conventions](https://dart.dev/tools/pub/package-layout).
If your package yields warnings,
don't worry! 
Just follow the suggestions 
(it's usually just linting or renaming files 
or specifying dependencies) 
and you should be good to go!

Once there are no issues 
and you feel you are ready to publish,
just run the following command!

```sh
 dart pub publish --dry-run
```

You should be prompted with the following output.

```
Publishing is forever; packages cannot be unpublished.
Policy details are available at https://pub.dev/policy

Do you want to publish dart_multihash 0.0.1 to https://pub.dartlang.org (y/N)?
```

Press `y`. 
You should now see the following.

```
Pub needs your authorization to upload packages on your behalf.
In a web browser, go to https://accounts.google.com/o/oauth2/auth?axxxx
Then click "Allow access".

Waiting for your authorization...
```

Your link will be custom.
If you visit it in your browser,
it will ask you to sign-in with your Google account.

![sign-in](https://user-images.githubusercontent.com/17494745/204876805-22f4d144-805a-4a2c-92b8-68df91734c1f.png)

After signing-in, you should be good to go!
You have now your own profile in https://pub.dev/!

If you authorize it,
your terminal should display the following.

```
Waiting for your authorization...
Authorization received, processing...

Successfully authorized.
Uploading... (2.2s)
```

This means your package has been published!
:tada:
Congrats!

## Transfering to a verified publisher
If you are part of an organization/verified publisher,
you can transfer your uploaded package
to it.
To do so, simply head to the package page
inside https://pub.dev/.
You will see something similar to this.

<img width="1312" alt="image" src="https://user-images.githubusercontent.com/17494745/204877380-de94c30f-b4ad-49b0-bd95-cf3d91aab8b8.png">

Inside the `Admin` tab, 
you can **change ownership**.
Simply select the publisher you want
and click on `Transfer to Publisher`.
**You have to be part of the 
organization/publisher to be able
to transfer ownership**.

And it's as simple as that! :smile:
