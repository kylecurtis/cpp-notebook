<br>

---

<br>

## Mathematical Operators

<br>

#### Addition (+)

- Adds two numbers.

```cpp
int addition {10 + 2};  // 12
```

<br>

#### Subtraction (-)

- Subtracts the second number from the first.

```cpp
int subtraction {10 - 2};  // 8
```

<br>

#### Multiplication (*)

- Multiplies two numbers.

```cpp
int multiplication {10 * 2};  // 20
```

<br>

#### Division (/)

- Divides the first number by the second. For integers, the result is truncated to an integer.

```cpp
int division {10 / 2};  // 5
```

- For floating-point division, use decimal values to get accurate results.

```cpp
double decimal_div {10.0 / 2.0};  // 5.0
```

<br>

#### Modulus (%)

- Returns the remainder of division between two integers.

```cpp
int modulus {10 % 2};  // 0
```

<br>

---

<br>

## Increment and Decrement Operators

<br>

#### Increment Operator (++)

- Increases the value of a variable by 1.
  
  - **Post-increment** (`x++`): Increments after using the current value.

  ```cpp
  int x {10};
  int y {x++};  // x = 11, y = 10
  ```

  - **Pre-increment** (`++x`): Increments before using the current value.

  ```cpp
  int x {10};
  int y {++x};  // x = 11, y = 11
  ```

<br>

#### Decrement Operator (--)

- Decreases the value of a variable by 1.
  
  - **Post-decrement** (`x--`): Decrements after using the current value.

  ```cpp
  int x {10};
  int y {x--};  // x = 9, y = 10
  ```

  - **Pre-decrement** (`--x`): Decrements before using the current value.

  ```cpp
  int x {10};
  int y {--x};  // x = 9, y = 9
  ```

<br>

---

<br>

## Order of Operations

- Multiplication (`*`) and Division (`/`) have a higher precedence than Addition (`+`) and Subtraction (`-`).
- Operations with the same precedence are performed left-to-right.

```cpp
int result {10 + 2 * 5};  // result = 20 (multiplication first, then addition)
```

<br>

---

<br>

## The `<cmath>` Library

To use the math functions provided by the library, include the header at the beginning of your program:

```cpp
#include <cmath>
```

<br>

---

<br>

## Power Functions

<br>

#### pow(base, exponent)

- Raises a number to the power of another number.
  
```cpp
double result = std::pow(2, 3);  // 2^3 = 8
```

<br>

#### sqrt(x)

- Returns the square root of a number.
  
```cpp
double root = std::sqrt(16);  // 4
```

<br>

#### cbrt(x)

- Returns the cube root of a number.

```cpp
double cuberoot = std::cbrt(27);  // 3
```

<br>

---

<br>

## Trigonometric Functions

<br>

#### sin(x), cos(x), tan(x)

- These functions return the sine, cosine, and tangent of an angle (in radians).
  
```cpp
double sine = std::sin(3.14159 / 2);  // sin(π/2) = 1
double cosine = std::cos(3.14159);    // cos(π) = -1
double tangent = std::tan(0);         // tan(0) = 0
```

<br>

#### asin(x), acos(x), atan(x)

- These return the inverse sine (arcsin), inverse cosine (arccos), and inverse tangent (arctan), with the result in radians.

```cpp
double angle = std::asin(1);  // arcsin(1) = π/2
```

<br>

#### atan2(y, x)

- Returns the angle (in radians) between the positive x-axis and the point `(x, y)`.

```cpp
double angle = std::atan2(1, 1);  // atan2(1, 1) = π/4 (45 degrees)
```

<br>

---

<br>

## Logarithmic and Exponential Functions

<br>

#### log(x)

- Returns the natural logarithm (base e) of `x`.

```cpp
double result = std::log(2.71828);  // ≈ 1 (ln(e) = 1)
```

<br>

#### log10(x)

- Returns the base-10 logarithm of `x`.

```cpp
double result = std::log10(100);  // 2
```

<br>

#### exp(x)

- Returns `e` raised to the power of `x` (exponential function).

```cpp
double result = std::exp(1);  // ≈ 2.71828 (e^1 = e)
```

<br>

---

<br>

## Rounding and Absolute Value Functions

<br>

#### round(x), floor(x), ceil(x)

- **`round(x)`**: Rounds `x` to the nearest integer.
- **`floor(x)`**: Rounds `x` down to the nearest integer.
- **`ceil(x)`**: Rounds `x` up to the nearest integer.

```cpp
double rounded = std::round(3.6);  // 4
double floored = std::floor(3.6);  // 3
double ceiled = std::ceil(3.2);    // 4
```

<br>

#### abs(x)

- Returns the absolute value of an integer or floating-point number.

```cpp
int absolute = std::abs(-10);  // 10
double abs_double = std::fabs(-3.14);  // 3.14
```

<br>

---

<br>

## Min and Max Functions

<br>

#### fmin(x, y) / fmax(x, y)
- Returns the smaller or larger of the two values, respectively.

```cpp
double minimum = std::fmin(3.2, 4.5);  // 3.2
double maximum = std::fmax(3.2, 4.5);  // 4.5
```

<br>

---

<br>

## Angle Conversion

If you're working with degrees instead of radians, you can convert between the two using constants like `M_PI` or manually converting:

### Degrees to Radians

```cpp
double radians = degrees * (M_PI / 180.0);
```

### Radians to Degrees

```cpp
double degrees = radians * (180.0 / M_PI);
```

<br>

---

<br>