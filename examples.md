# Examples

## Basic Usage

Adding indices, checking membership, counting set bits, and iterating over set bits using `BitSet`:

```clojure
(use BitSet)

(defn main []
  (let [bs (BitSet.new)]
    (do
      (BitSet.add! &bs 10)
      (BitSet.add! &bs 100)
      
      (IO.println &(str (BitSet.contains? &bs 10))) ; true
      (IO.println &(str (BitSet.count &bs)))        ; 2
      
      ;; Efficiently iterate over set indices
      (BitSet.for-each-set &(fn [idx] (IO.println &(str @idx))) &bs))))
```
