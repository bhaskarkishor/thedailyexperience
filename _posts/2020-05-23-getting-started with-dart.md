---
tags: [Web Development]
layout: post
title: Getting Started with Dart
image: images/dart-logos.png
---


> Dart is a client-optimized language for fast apps on any platform.

This is the official introduction on official [site](https://dart.dev) for dart. Dart is a language introduced by Google to specifically address the problem of fast app development on any platform. This specififc language together with set of tools(flutter) aims to have a single code base for different platforms, be it android, ios or web.

This effort is commendable as it would definitly reduce the development time for development groups maintaining separate codebases for web app and native apps.

### First eye opinion of Dart
To someone who already has some experience in C, javascript, python, java etc. Dart seems to be a derivative of C and java and javascript incorporating good elements of all. It is staticly typed language but it also provides developers with dynamic behaviour in case needed.
```dart
void main(){
    print('something);
}
```

### Static vs dynamic typed language
Static language: The datatype of the variable is defined at the time of variable declaration, unlike python. Also, the datatype of a variable cannot be changed once declared, unlike python. This has a inherent advantage of having less bugs.
```dart
void main(){
    int age = 12;
    print(age);
    age = '12'; //this produces error as age has to be integer
}
```
Dynamic language: The datatype of variable can be changed at any point of time. This behaviour can be found in python and javascript. This may accelerate the developement time in short run by a small margin but the code is more prone to bugs. 

```dart
void main(){
    dynamic age = 12;
    print(age);
    age = '12';
    print(age); //this is explicitly forcing dynamic behaviour on age varibale
}
```
### Available Datatypes
The Data types are quite similar to other programming language. Such as int, float, bool, String, List