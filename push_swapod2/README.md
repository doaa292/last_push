*This activity has been created as part of the 42 curriculum by oalabed, domansou.*

# Push_swap

## Description

Push_swap is a C program that sorts a list of integers using **two stacks** (`a` and `b`) and a limited set of operations. The goal is to sort the numbers in ascending order using the **minimum number of operations**.

---

## Usage

### Compile

```bash
make
```

### Run

```bash
./push_swap [OPTIONS] <numbers>
```

### Options

* `--simple` → O(n²)
* `--medium` → O(n√n)
* `--complex` → O(n log n)
* `--adaptive` → default (based on disorder)
* `--bench` → show performance info

---

## Rules

* Stack `a` starts filled, `b` is empty
* No duplicate numbers
* Allowed operations:
  `sa sb ss pa pb ra rb rr rra rrb rrr`
* Output = list of operations (one per line)
* Errors → print `Error`

---

## Algorithms

* **Simple (O(n²))** → basic sorting (e.g., selection)
* **Medium (O(n√n))** → chunk-based sorting
* **Complex (O(n log n))** → radix sort
* **Adaptive** → chooses strategy based on disorder:

| Disorder | Strategy   |
| -------- | ---------- |
| < 0.2    | O(n)       |
| 0.2–0.5  | O(n√n)     |
| ≥ 0.5    | O(n log n) |

---

## Benchmark (--bench)

Shows:

* Disorder %
* Strategy used
* Total operations
* Count of each operation

---

## Requirements

* No memory leaks
* No crashes
* Follow 42 Norm
* Provide Makefile (`all`, `clean`, `fclean`, `re`)

---
## Resources

Sorting algorithms (Radix, Insertion, Chunking)
Big-O complexity theory
42 subject PDF

## AI Usage

AI was used for:

Understanding algorithm strategies
Debugging ideas and edge cases
Improving test coverage

All code was written and fully understood before submission.

---
## Contributors

* `<oalabed>`
* `<domansou>`

