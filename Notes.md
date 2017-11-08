## Clojure notes

`->` operator

```clojure
user=> (def c 5)
user=> (-> c (+ 3) (/ 2) (- 1))                          
3

;; and if you are curious why
user=> (use 'clojure.walk)
user=> (macroexpand-all '(-> c (+ 3) (/ 2) (- 1)))
(- (/ (+ c 3) 2) 1)
```

```clojure
;; Be cautious with anonymous functions; they must be wrapped in an outer
;; pair of parens.
(-> 10
    #(/ % 2))
;; will throw an exception, but
(-> 10
    (#(/ % 2)))
;; will work fine. Similarly,
(-> 10
    (fn [n] (/ n 2)))
;; will throw an exception, but
(-> 10
    ((fn [n] (/ n 2))))
;; works as intended.
```
