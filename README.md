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

### 25 - Find the odd numbers
Difficulty:	Easy
Topics:	seqs

Write a function which returns only the odd numbers from a sequence.
```Clojure
(= (__ #{1 2 3 4 5}) '(1 3 5))
(= (__ [4 2 1 6]) '(1))
(= (__ [2 2 4 6]) '())
(= (__ [1 1 1 3]) '(1 1 1 3))
```
Solution
```Clojure
#(filter odd? %)
```

### 30 Compress a Sequence

Difficulty:	Easy
Topics:	seqs

Write a function which removes consecutive duplicates from a sequence.
```Clojure	
(= (apply str (__ "Leeeeeerrroyyy")) "Leroy")
(= (__ [1 1 2 3 3 2 2 3]) '(1 2 3 2 3))
(= (__ [[1 2] [1 2] [3 4] [1 2]]) '([1 2] [3 4] [1 2]))
```

One posible solution
```clojure
#(map first (partition-by identity %))
```
