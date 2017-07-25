---
layout: pattern
title: Bridge
folder: bridge
permalink: /patterns/bridge/
pumlid: BSR14SCm20J0Lf82BFxf1akCJ4R26ZZYzkE7zxLljJgoIVfu7S2A3v7pLRhYo3r3l9u6CPHwJjAH5uETllpZhKbejsqn86v1a-CExQwj2mdgqv8-oyev_W00
categories: Structural
tags:
 - Java
 - Gang Of Four
 - Difficulty-Intermediate
---

## Also known as
Handle/Body

## Intent
Decouple an abstraction from its implementation so that the two can
vary independently.

将抽象部分与它的实现部分分离，使它们都可以独立地变化。

![alt text](./etc/bridge.png "Bridge")

## Applicability
Use the Bridge pattern when

* you want to avoid a permanent binding between an abstraction and its implementation. This might be the case, for example, when the implementation must be selected or switched at run-time.
* both the abstractions and their implementations should be extensible by subclassing. In this case, the Bridge pattern lets you combine the different abstractions and implementations and extend them independently
* changes in the implementation of an abstraction should have no impact on clients; that is, their code should not have to be recompiled.
* you have a proliferation of classes. Such a class hierarchy indicates the need for splitting an object into two parts. Rumbaugh uses the term "nested generalizations" to refer to such class hierarchies
* you want to share an implementation among multiple objects (perhaps using reference counting), and this fact should be hidden from the client. A simple example is Coplien's String class, in which multiple objects can share the same string representation.

你不希望在抽象和它的实现部分之间有一个固定的绑定关系。例如这种情况可能是因为，在程序运行时刻实现部分应可以被选择或者切换。
类的抽象以及它的实现都应该可以通过生成子类的方法加以扩充。这时Bridge模式使你可以对不同的抽象接口和实现部分进行组合，并分别对它们进行扩充。
对一个抽象的实现部分的修改应对客户不产生影响，即客户的代码不必重新编译。
有许多类要生成。这样一种类层次结构说明你必须将一个对象分解成两个部分。Rumbaugh称这种类层次结构为?嵌套的普化?（nested generalizations ）。
你想在多个对象间共享实现（可能使用引用计数），但同时要求客户并不知道这一点。一个简单的例子便是Coplien的String类，在这个类中多个对象可以共享同一个字符串表示。

## Credits

* [Design Patterns: Elements of Reusable Object-Oriented Software](http://www.amazon.com/Design-Patterns-Elements-Reusable-Object-Oriented/dp/0201633612)
