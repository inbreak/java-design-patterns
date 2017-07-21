---
layout: pattern
title: Prototype
folder: prototype
permalink: /patterns/prototype/
pumlid: HSV13OCm30NGLM00udktCS62eCInxE-YRj_UUdjlRLfx7fBUbmkmU14vF-Lik7BF4AzJ8OfIvw3Mys6mqyrltWw9Tkfc38XhqE3uWSmd9Zuc9AZ_bVHHB4V_0W00
categories: Creational
tags: 
 - Java
 - Gang Of Four
 - Difficulty-Beginner
---

## Intent
Specify the kinds of objects to create using a prototypical
instance, and create new objects by copying this prototype.

用原型实例指定创建对象的种类，并且通过拷贝这些原型创建新的对象。

![alt text](./etc/prototype_1.png "Prototype")

## Applicability
Use the Prototype pattern when a system should be independent of how its products are created, composed and represented; and

* when the classes to instantiate are specified at run-time, for example, by dynamic loading; or
* to avoid building a class hierarchy of factories that parallels the class hierarchy of products; or
* when instances of a class can have one of only a few different combinations of state. It may be more convenient to install a corresponding number of prototypes and clone them rather than instantiating the class manually, each time with the appropriate state

当要实例化的类是在运行时刻指定时，例如，通过动态装载；或者
为了避免创建一个与产品类层次平行的工厂类层次时；或者
当一个类的实例只能有几个不同状态组合中的一种时。建立相应数目的原型并克隆它们可能比每次用合适的状态手工实例化该类更方便一些。

## Real world examples

* [java.lang.Object#clone()](http://docs.oracle.com/javase/8/docs/api/java/lang/Object.html#clone%28%29)

## Credits

* [Design Patterns: Elements of Reusable Object-Oriented Software](http://www.amazon.com/Design-Patterns-Elements-Reusable-Object-Oriented/dp/0201633612)
