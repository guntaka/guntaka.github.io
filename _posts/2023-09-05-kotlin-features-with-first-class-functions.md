---
layout: article
title: Productive Kotlin features based on first class functions
meta: Kotlin functional features
category: [tips, kotlin]
tags: [tips, kotlin, java]
---
With Kotlin's functional programming style, Java programmer get few more productive features. Having functions as first class citizens without complicated syntax is by far the most important design principle of Kotlin, in my view.

Some of the  benefits of first class functions:
### functions as parameters
You can pass a function object across multiple method calls, and only worry about invoking them where needed. Intermediate method calls just need to know about the function type, which can be aliased easily. The DZone article referred at the end of this article shows an example.
In Java, programmer need to change the functional interface even when  there is a change in number of paramemeters or change in return type.

### `.apply` operator
With `apply` and and other scope functions, you cna create/manupulate objects without intermediate variables, this may not improve the runtime performance, but it will make the programmer read less and use time more effectively, as long he/she is familiar with syntax.

### `internal` modifier
With `internal` visibility modifier, you can limit class/method/interface to the module it is located.

### coroutines
Coroutines are light weight threads implemented within JVM. Java threads corrsponds to operating system threads, and CPU does a lot of work to schedule and switch, and running large number of threads need huge CPU and Memory. On the otherhand, you can run millions of couroutines becuase the overhead is less. Newer Java versions will get these light weight treads, until then you can bebefit using Kotlin couroutines.


Reference: [Java vs. Kotlin: Lambdas and Functions](https://dzone.com/articles/java-vs-kotlin)