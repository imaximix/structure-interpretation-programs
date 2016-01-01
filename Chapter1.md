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
Evaluation has two simple rules: **evaluate the subexpressions of the combination** and **apply the procedure, value of the leftmost expression, to the arguments, that are the values of the other subexpressions**
```
(+ (* 2 3) 4)
```
There are exception to this rule.
```
(define x 5)
```
These are called **special forms**.

### 1.1.4 Compound Procedures
*Procedure definitions* a powerfull abstraction technique by which a compound procedure can pe given a name and then referred to as a unit.

Below is an example of **compund procedure**. It has the name **square**, and it represents the operation of multiplying something with itself.
```
(defn square [x] (* x x))
```
Thoughts: Compound procedures are just combinations of operations.

### 1.1.5 The substitution model for procedure application
There are two types of evaluation: *applicative-order evaluation* and *normal-order evaluation*

### 1.1.6 Conditional expressions and predicates

Exercises:
1.1
```
10 => **10**
(+ 5 3 4) => **12**
(- 9 1) => **8**
(/ 6 2) => **3**
(+ (* 2 4) (- 4 6)) => **6**
(define a 3) => **3**
(define b (+ a 1)) => **4**
(+ a b (* a b)) => **19**

(= a b) => **false**
(if (and (> b a) (< b (* a b)))
 b
 a) => **4**
 
(cond ((= a 4) 6)
 ((= b 4) (+ 6 7 a))
 (else 25)) => **16**
 
(+ 2 (if (> b a) b a)) => **6**

(* (cond ((> a b) a)
 ((< a b) b)
 (else -1))
 (+ a 1)) => **16**
```
1.2
```
(/ (+ 5 4 (- 2 (- 3 (+ 6 (/ 4 3))))) (* 3 (- 6 2) (- 2 7)))
```
1.3
```
(defn sum [& numbers]
 (map square (take-last 2 (order numbers))))
```
1.4
a and b get evaluated first, then the left most expressions gets evaluated and the params get applied to it.

1.5
