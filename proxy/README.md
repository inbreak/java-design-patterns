---
layout: pattern
title: Proxy
folder: proxy
permalink: /patterns/proxy/
pumlid: 9SR13OCm30NGLM00udktCS62eCI9x6yesrEfx_Jcehd69c5rEe3X7oBZE-q5HwpXOhahH95oRrHgt0msEldYPHClkow30J5rQko_qB3-VKYG_qjXBOrezGK0
categories: Structural
tags:
 - Java
 - Gang Of Four
 - Difficulty-Beginner
---

## Also known as
Surrogate

## Intent
Provide a surrogate or placeholder for another object to control
access to it.

为其他对象提供一种代理以控制对这个对象的访问。

![alt text](./etc/proxy.png "Proxy")

## Applicability
Proxy is applicable whenever there is a need for a more
versatile or sophisticated reference to an object than a simple pointer. Here
are several common situations in which the Proxy pattern is applicable

* Remote proxy provides a local representative for an object in a different address space.
* Virtual proxy creates expensive objects on demand.
* Protection proxy controls access to the original object. Protection proxies are useful when objects should have different access rights.
//在需要用比较通用和复杂的对象指针代替简单的指针的时候，使用Proxy模式。
远程代理（Remote Proxy）为一个对象在不同的地址空间提供局部代表。
虚代理（Virtual Proxy）根据需要创建开销很大的对象
保护代理（Protection Proxy）控制对原始对象的访问。保护代理用于对象应该有不同 的访问权限的时候。

## Typical Use Case

* Control access to another object
* Lazy initialization
* Implement logging
* Facilitate network connection
* Count references to an object

## Tutorials
* [Controlling Access With Proxy Pattern](http://java-design-patterns.com/blog/controlling-access-with-proxy-pattern/)

## Presentations
* [Proxy](https://github.com/iluwatar/java-design-patterns/tree/master/proxy/etc/presentation.html)

## Real world examples

* [java.lang.reflect.Proxy](http://docs.oracle.com/javase/8/docs/api/java/lang/reflect/Proxy.html)
* [Apache Commons Proxy](https://commons.apache.org/proper/commons-proxy/)
* Mocking frameworks Mockito, Powermock, EasyMock

## Credits

* [Design Patterns: Elements of Reusable Object-Oriented Software](http://www.amazon.com/Design-Patterns-Elements-Reusable-Object-Oriented/dp/0201633612)
