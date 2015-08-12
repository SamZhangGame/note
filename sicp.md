# SICP Notes

## Procedures and the Processes They Generate
### 1.2.1 Linear Recursion and Iteration
``` lisp
(define (factorial n)
  (if (= n 1)
      1
      (* n (factorial (- n 1)))))
```

![alt text](http://mitpress.mit.edu/sicp/full-text/book/ch1-Z-G-7.gif)

``` lisp
(define (factorial n)
  (fact-iter 1 1 n))

(define (fact-iter product counter max-count)
  (if (> counter max-count)
      product
      (fact-iter (* counter product)
                 (+ counter 1)
                 max-count)))
```

![alt text]http://mitpress.mit.edu/sicp/full-text/book/ch1-Z-G-10.gif)
