---
layout: pattern
title: Flyweight
folder: flyweight
permalink: /patterns/flyweight/
pumlid: HSV94S8m3030Lg20M7-w4OvYAoCh7Xtnq3ty-Eq-MQlaJcdow17JNm26gpIEdkzqidffa4Qfrm2MN1XeSEADsqxEJRU94MJgCD1_W4C-YxZr08hwNqaRPUQGBm00
categories: Structural
tags:
 - Java
 - Gang Of Four
 - Difficulty-Intermediate
 - Performance
---

## Intent
Use sharing to support large numbers of fine-grained objects
efficiently.

运用共享技术有效地支持大量细粒度的对象。

![alt text](./etc/flyweight_1.png "Flyweight")

## Applicability
The Flyweight pattern's(享元模式) effectiveness depends heavily on how
and where it's used. Apply the Flyweight pattern when all of the following are
true

* an application uses a large number of objects
* storage costs are high because of the sheer quantity of objects
* most object state can be made extrinsic
* many groups of objects may be replaced by relatively few shared objects once extrinsic state is removed
* the application doesn't depend on object identity. Since flyweight objects may be shared, identity tests will return true for conceptually distinct objects.

一个应用程序使用了大量的对象。
完全由于使用大量的对象，造成很大的存储开销。
对象的大多数状态都可变为外部状态。
如果删除对象的外部状态，那么可以用相对较少的共享对象取代很多组对象。
应用程序不依赖于对象标识。由于flyweight对象可以被共享，对于概念上明显有别的对象，标识测试将返回真值。

## Real world examples

* [java.lang.Integer#valueOf(int)](http://docs.oracle.com/javase/8/docs/api/java/lang/Integer.html#valueOf%28int%29) and similarly for Byte, Character and other wrapped types.

## Credits

* [Design Patterns: Elements of Reusable Object-Oriented Software](http://www.amazon.com/Design-Patterns-Elements-Reusable-Object-Oriented/dp/0201633612)
