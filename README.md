# carp-bitset

A high-performance dynamic bitset for the [Carp language](https://github.com/carp-lang/Carp).

Bitsets provide extremely space-efficient storage for boolean flags and enable fast set-algebraic operations via bitwise logic.

## Features

- **Dynamic Growth**: Automatically expands to accommodate any bit index.
- **Set Algebra**: High-speed `union`, `intersection`, `difference`, and `symmetric-difference`.
- **Efficient Membership**: $O(1)$ check, set, and clear.
- **Optimized Iteration**: Fast iteration over set bits using bit manipulation.
- **Memory Efficient**: Backed by `Uint64` blocks to minimize overhead.

## Installation

Add this to your project by loading `bitset.carp`.

```clojure
(load "path/to/carp-bitset/bitset.carp")
(use BitSet)
```

## Usage

```clojure
(use BitSet)

(let [bs (BitSet.new)]
  (do
    (BitSet.add! &bs 10)
    (BitSet.add! &bs 100)
    
    (IO.println &(str (BitSet.contains? &bs 10))) ; true
    (IO.println &(str (BitSet.count &bs)))        ; 2
    
    ;; Efficiently iterate over set indices
    (BitSet.for-each-set &(fn [idx] (IO.println &(str @idx))) &bs)
  ))
```

## Running Tests

```bash
carp -x test/bitset_test.carp
```

## License

MIT
