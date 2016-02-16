## Procedures and Process they generate

### 1.2.1 Linear Recursion and Iteration

Exercise 1.10
```
(A 1 10)
(A 1 (A 1 9))
(A 1 (A 1 (A 1 8)))
(A 1 (A 1 (A 1 (A 1 7))))
(A 1 (A 1 (A 1 (A 1 (A 1 6)))))
(A 1 (A 1 (A 1 (A 1 (A 1 (A 1 5))))))
(A 1 (A 1 (A 1 (A 1 (A 1 (A 1 (A 1 4)))))))
(A 1 (A 1 (A 1 (A 1 (A 1 (A 1 (A 1 (A 1 3))))))))
(A 1 (A 1 (A 1 (A 1 (A 1 (A 1 (A 1 (A 1 (A 1 2)))))))))
(A 1 (A 1 (A 1 (A 1 (A 1 (A 1 (A 1 (A 1 (A 1 (A 1 1))))))))))
(A 1 (A 1 (A 1 (A 1 (A 1 (A 1 (A 1 (A 1 (A 0 2)))))))))
(A 1 (A 1 (A 1 (A 1 (A 1 (A 1 (A 1 (A 0 4))))))))
(A 1 (A 1 (A 1 (A 1 (A 1 (A 1 (A 0 8)))))))
(A 1 (A 1 (A 1 (A 1 (A 1 (A 0 16))))))
(A 1 (A 1 (A 1 (A 1 (A 0 32)))))
(A 1 (A 1 (A 1 (A 0 64))))
(A 1 (A 1 (A 0 128)))
(A 1 (A 0 256))
(A 0 512)
;; 1024
```

### 1.2.2 Tree recursion

Exercise 1.11
```
;; Recursive
(define (f n)
  (cond ((< n 3) n)
        (else (+ (f 
                  (- n 1)) 
                  (* 2 (f (- n 2)))
                  (* 3 (f (- n 3)))))))
```

```
;; Iterative
;; I don't understand this. It looks like a reverse of the recursive process.
(define (f n))

(define (f-iter a b c count)
  (cond ((= count 0) a)
        (f-iter b c (+ c (* 2 b) (* 3 a)) (- count 1))))
```

Exercise 1.12
```
;; rows are counted from 0 and columns are counted from 0 aswell
(define (pascal-triangle row column)
  (cond ( (or (> column row) (< column 0)) 0)
        ( (= column 0) 1)
        ( (+ 
            (pascal-triangle (- row 1) column) 
            (pascal-triangle (- row 1) column - 1))))
```

### 1.2.3 Order of Growth
