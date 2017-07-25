---
layout: pattern
title: Adapter
folder: adapter
permalink: /patterns/adapter/
pumlid: DSR14S8m30J0Lg20M7-wEMnDOiPMFDA9j0yyUEtUkzMHJTF7xI1NF4GSLzaxZtncgDVJgCPIpobzv0N2vOKtjgRHTziMI7KBcOXl10thfxB-Nz9dMJd71m00
categories: Structural
tags:
 - Java
 - Gang Of Four
 - Difficulty-Beginner
---

## Also known as
Wrapper

## Intent
Convert the interface of a class into another interface the clients
expect. Adapter lets classes work together that couldn't otherwise because of
incompatible interfaces.

将一个类的接口转换成客户希望的另外一个接口。Adapter模式使得原本由于接口不兼容而不能一起工作的那些类可以一起工作。

![alt text](./etc/adapter.png "Adapter")

## General usage of Adapter Pattern: 
+ Wrappers used to adopt 3rd parties libraries and frameworks - most of the applications using third party libraries use adapters as a middle layer between the application and the 3rd party library to decouple the application from the library. If another library has to be used only an adapter for the new library is required without having to change the application code.

## Applicability
Use the Adapter pattern when

* you want to use an existing class, and its interface does not match the one you need
* you want to create a reusable class that cooperates with unrelated or unforeseen classes, that is, classes that don't necessarily have compatible interfaces
* you need to use several existing subclasses, but it's impractical to adapt their interface by subclassing every one. An object adapter can adapt the interface of its parent class.

你想使用一个已经存在的类，而它的接口不符合你的需求。
你想创建一个可以复用的类，该类可以与其他不相关的类或不可预见的类（即那些接口可能不一定兼容的类）协同工作。
（仅适用于对象Adapter ）你想使用一些已经存在的子类，但是不可能对每一个都进行子类化以匹配它们的接口。对象适配器可以适配它的父类接口。

## Consequences:
Class and object adapters have different trade-offs. A class adapter

*	adapts Adaptee to Target by committing to a concrete Adaptee class. As a consequence, a class adapter won’t work when we want to adapt a class and all its subclasses.
*	let’s Adapter override some of Adaptee’s behavior, since Adapter is a subclass of Adaptee.
*	introduces only one object, and no additional pointer indirection is needed to get to the adaptee.

An object adapter	

*	let’s a single Adapter work with many Adaptees—that is, the Adaptee itself and all of its subclasses (if any). The Adapter can also add functionality to all Adaptees at once.
*	makes it harder to override Adaptee behavior. It will require subclassing Adaptee and making Adapter refer to the subclass rather than the Adaptee itself.


## Real world examples

* [java.util.Arrays#asList()](http://docs.oracle.com/javase/8/docs/api/java/util/Arrays.html#asList%28T...%29)
* [java.util.Collections#list()](https://docs.oracle.com/javase/8/docs/api/java/util/Collections.html#list-java.util.Enumeration-)
* [java.util.Collections#enumeration()](https://docs.oracle.com/javase/8/docs/api/java/util/Collections.html#enumeration-java.util.Collection-)
* [javax.xml.bind.annotation.adapters.XMLAdapter](http://docs.oracle.com/javase/8/docs/api/javax/xml/bind/annotation/adapters/XmlAdapter.html#marshal-BoundType-)


## Credits

* [Design Patterns: Elements of Reusable Object-Oriented Software](http://www.amazon.com/Design-Patterns-Elements-Reusable-Object-Oriented/dp/0201633612)
* [J2EE Design Patterns](http://www.amazon.com/J2EE-Design-Patterns-William-Crawford/dp/0596004273/ref=sr_1_2)
