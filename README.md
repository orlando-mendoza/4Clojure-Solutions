# 4Clojure-Solutions


### 22 - Count a Sequence

Difficulty:	Easy
Topics:	seqs core-functions


Write a function which returns the total number of elements in a sequence.

```clojure
(= (__ '(1 2 3 3 1)) 5)

(= (__ "Hello World") 11)

(= (__ [[1 2] [3 4] [5 6]]) 3)

(= (__ '(13)) 1)

(= (__ '(:a :b :c)) 3)
```

One possible solution:

```clojure
#(reduce (fn[c _] (inc c)) 0 %)
```

### 23 - Reverse a Sequence - Special Restrictions: `reverse` `rseq`

Difficulty:	Easy
Topics:	seqs core-functions


Write a function which reverses a sequence.
```clojure
(= (__ [1 2 3 4 5]) [5 4 3 2 1])
(= (__ (sorted-set 5 7 2 7)) '(7 5 2))
(= (__ [[1 2][3 4][5 6]]) [[5 6][3 4][1 2]])
```

One posible solution
```clojure
#(reduce conj () %)
```

