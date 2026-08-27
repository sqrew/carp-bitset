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

## Examples

See [examples.md](examples.md) for usage examples.

## Running Tests

```bash
carp -x test/bitset_test.carp
```

## License

MIT
