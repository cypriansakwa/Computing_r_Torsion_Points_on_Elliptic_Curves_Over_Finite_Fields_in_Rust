# Elliptic Curve $r$-Torsion Points Finder

This Rust program computes all $r$-torsion points on an elliptic curve defined over a finite field $\mathbb{F}_m$. A point $P$ is an $r$-torsion point if $rP = \mathcal{O}$, where $\mathcal{O}$ is the point at infinity.

## Features

- Defines elliptic curve points with support for the point at infinity.
- Implements modular arithmetic for point addition and scalar multiplication on elliptic curves.
- Enumerates all points on the curve and checks if they satisfy the $r$-torsion condition.
- Outputs all $r$-torsion points, including the point at infinity.

## How It Works

1. **Elliptic Curve Definition**:
   - The elliptic curve is defined by the equation $y^2 \equiv x^3 + ax + b \mod m$.

2. **Key Functions**:
   - `is_on_curve`: Checks if a point lies on the curve.
   - `elliptic_add`: Adds two points on the curve.
   - `scalar_mult`: Computes $nP$ for a point $P$ using double-and-add.
   - `find_r_torsion_points`: Finds all points $P$ such that $rP = \mathcal{O}$.

3. **Input Parameters**:
   - Coefficients `a` and `b` of the elliptic curve.
   - Modulus `m` defining the finite field $\mathbb{F}_m$.
   - Integer `r` specifying the torsion subgroup order.

4. **Output**:
   - Prints all $r$-torsion points on the curve.

## Usage

1. Install Rust from [rust-lang.org](https://www.rust-lang.org/).
2. Clone or download this repository.
3. Run the program using `cargo run`.

## Example

For the elliptic curve $y^2 \equiv x^3 + x + 1 \mod 5$, the program computes the $3$-torsion points:

### Input
```rust
let a = 1;
let b = 1;
let m = 5;
let r = 3;
```
### 3-torsion points on the curve:
```rust
(2, 1)
(2, 4)
Point at infinity
```
## How to Run
1. Update the parameters `a`, `b`, `m`, and `r` in the main function.
2. Build and execute the program:
```
cargo run
```

