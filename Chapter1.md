Building Abstractions with Procedures

**Computational Processes** are abstract beings that live inside our computers.

As *Processes* evolve they manipulate abstract things called **Data**. Their evolution is directed by a pattern of rules called a **Program**.
*People create programs to direct processes*

Why Lisp? Because *Procedures as Data*.
Above and beyond these considerations, programming in Lisp is great fun.

1.1 Elements of Programming
---------------------------

A powerfull provides three mechanisms for expressing ideeas about processes: 
  * **primitive abstraction** the simplest entities the language is concerned with
  * **means of combination** compound elements are build from simpler ones
  * **means of abstraction** compound elements can be named and manipulated as units ( Processes as Data? )
  
### 1.1.1 Expressions
```
123      // -> expression
+ | * -> // expression representing a primitive procedure
```

Combinations of expressions are called compound expressions and represent the application of a primitive procedure to some expressions. 
```
(+ 1 2) // Application of '+' to 1 and 2
```

### 1.1.2 Naming and the Env
**Define** allows us to keep track of results of compound expressions.

### 1.1.3 Evaluating Combination
