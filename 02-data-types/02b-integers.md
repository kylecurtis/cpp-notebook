<br>

---

<br>

## Short

Typically 16-bit, no suffix required.

| Type | Size | Min | Max |
| :---: | :---: | :---: | :---: |
| Signed Short | at least 16-bit | -32,768 | 32,767 |
| Unsigned Short | at least 16-bit | 0 | 65,535 |

<br>

#### Signed Short

- Allows negative values.

```cpp
short short_num {-100};
```

<br>

#### Unsigned Short

- Does not allow negative values.

```cpp
unsigned short ushort_num {100};
```

<br>

---

<br>

## Integer

Typically 32-bit, no suffix required.

| Type | Size | Min | Max |
| :---: | :---: | :---: | :---: |
| Signed Int | at least 32-bit | -2,147,483,648 | 2,147,483,647 |
| Unsigned Int | at least 32-bit | 0 | 4,294,967,295 |

<br>

#### Signed Int

- Allows negative values.

```cpp
int int_num {-1000};
```

<br>

#### Unsigned Int

- Does not allow negative values.

```cpp
unsigned int uint_num {1000};
```

<br>

---

<br>

## Long

Typically 32-bit or 64-bit depending on the platform.

| Type | Size | Min | Max |
| :---: | :---: | :---: | :---: |
| Signed Long | at least 32-bit | -2,147,483,648 | 2,147,483,647 |
| Unsigned Long | at least 32-bit | 0 | 4,294,967,295 |

<br>

#### Signed Long

- Allows negative values.

```cpp
long long_num {-100000L};  // Suffix 'L' for long literal (optional)
```

<br>

#### Unsigned Long

- Does not allow negative values.

```cpp
unsigned long ulong_num {100000UL};  // Suffix 'UL' for unsigned long literal
```

<br>

---

<br>

## Long Long

Typically 64-bit.

| Type | Size | Min | Max |
| :---: | :---: | :---: | :---: |
| Signed Long Long | at least 64-bit | -9,223,372,036,854,775,808 | 9,223,372,036,854,775,807 |
| Unsigned Long Long | at least 64-bit | 0 | 18,446,744,073,709,551,615 |

<br>

#### Signed Long Long

- Allows negative values.

```cpp
long long ll_num {-100000LL};  // Suffix 'LL' for long long literal
```

<br>

#### Unsigned Long Long

- Does not allow negative values.

```cpp
unsigned long long ull_num {100000ULL};  // Suffix 'ULL' for unsigned long long literal
```

<br>

---

<br>

## Min and Max (Using `<limits>`)

You can determine the minimum and maximum values for each integer type by including the `<limits>` library header:

```cpp
#include <limits>
```

<br>

### Short

```cpp
std::cout << "short (min): " << std::numeric_limits<short>::min() << '\n';
std::cout << "short (max): " << std::numeric_limits<short>::max() << '\n';

std::cout << "unsigned short (min): " << std::numeric_limits<unsigned short>::min() << '\n';
std::cout << "unsigned short (max): " << std::numeric_limits<unsigned short>::max() << '\n';
```

<br>

### Int

```cpp
std::cout << "int (min): " << std::numeric_limits<int>::min() << '\n';
std::cout << "int (max): " << std::numeric_limits<int>::max() << '\n';

std::cout << "unsigned int (min): " << std::numeric_limits<unsigned int>::min() << '\n';
std::cout << "unsigned int (max): " << std::numeric_limits<unsigned int>::max() << '\n';
```

<br>

### Long

```cpp
std::cout << "long (min): " << std::numeric_limits<long>::min() << '\n';
std::cout << "long (max): " << std::numeric_limits<long>::max() << '\n';

std::cout << "unsigned long (min): " << std::numeric_limits<unsigned long>::min() << '\n';
std::cout << "unsigned long (max): " << std::numeric_limits<unsigned long>::max() << '\n';
```

<br>

### Long Long

```cpp
std::cout << "long long (min): " << std::numeric_limits<long long>::min() << '\n';
std::cout << "long long (max): " << std::numeric_limits<long long>::max() << '\n';

std::cout << "unsigned long long (min): " << std::numeric_limits<unsigned long long>::min() << '\n';
std::cout << "unsigned long long (max): " << std::numeric_limits<unsigned long long>::max() << '\n';
```

<br>

---

<br>

## Fixed-Width Integer Types

Fixed-width integers provide precise control over integer sizes across platforms using types from `<cstdint>`.

To use fixed-width integer types, include the `<cstdint>` header:

```cpp
#include <cstdint>
```

<br>

### 8-bit Integer Types

- **`std::int8_t`**: Signed 8-bit integer (range: -128 to 127).
- **`std::uint8_t`**: Unsigned 8-bit integer (range: 0 to 255).

```cpp
std::int8_t small_signed_num {-128};  // Signed 8-bit
std::uint8_t small_unsigned_num {255};  // Unsigned 8-bit
```

<br>

### 16-bit Integer Types

- **`std::int16_t`**: Signed 16-bit integer (range: -32,768 to 32,767).
- **`std::uint16_t`**: Unsigned 16-bit integer (range: 0 to 65,535).

```cpp
std::int16_t medium_signed_num {-32768};  // Signed 16-bit
std::uint16_t medium_unsigned_num {65535};  // Unsigned 16-bit
```

<br>

### 32-bit Integer Types

- **`std::int32_t`**: Signed 32-bit integer (range: -2,147,483,648 to 2,147,483,647).
- **`std::uint32_t`**: Unsigned 32-bit integer (range: 0 to 4,294,967,295).

```cpp
std::int32_t large_signed_num {-2147483648};  // Signed 32-bit
std::uint32_t large_unsigned_num {4294967295};  // Unsigned 32-bit
```

<br>

### 64-bit Integer Types

- **`std::int64_t`**: Signed 64-bit integer (range: -9,223,372,036,854,775,808 to 9,223,372,036,854,775,807).
- **`std::uint64_t`**: Unsigned 64-bit integer (range: 0 to 18,446,744,073,709,551,615).

```cpp
std::int64_t very_large_signed_num {-9223372036854775808LL};  // Signed 64-bit
std::uint64_t very_large_unsigned_num {18446744073709551615ULL};  // Unsigned 64-bit
```

<br>

### Notes:

- **Suffixes for literals**:
  - For **64-bit integers**, use the suffix `LL` for `std::int64_t` and `ULL` for `std::uint64_t` when initializing with literals to ensure the correct size.
- **Fixed-width types are ideal** for cases where the exact size of the integer matters, such as low-level programming, file I/O formats, and hardware interaction.

<br>

---

<br>

## Fixed-Width Integer Min/Max

<br>

### 8-bit Integers

```cpp
std::cout << "int8_t (min): " << +std::numeric_limits<std::int8_t>::min() << '\n';
std::cout << "int8_t (max): " << +std::numeric_limits<std::int8_t>::max() << '\n';

std::cout << "uint8_t (min): " << +std::numeric_limits<std::uint8_t>::min() << '\n';
std::cout << "uint8_t (max): " << +std::numeric_limits<std::uint8_t>::max() << '\n';
```

> **Note**: The `+` is used to promote `std::int8_t` and `std::uint8_t` to a larger type (like `int`), ensuring they are printed as numbers rather than characters.

<br>

### 16-bit Integers

```cpp
std::cout << "int16_t (min): " << std::numeric_limits<std::int16_t>::min() << '\n';
std::cout << "int16_t (max): " << std::numeric_limits<std::int16_t>::max() << '\n';

std::cout << "uint16_t (min): " << std::numeric_limits<std::uint16_t>::min() << '\n';
std::cout << "uint16_t (max): " << std::numeric_limits<std::uint16_t>::max() << '\n';
```

<br>

### 32-bit Integers

```cpp
std::cout << "int32_t (min): " << std::numeric_limits<std::int32_t>::min() << '\n';
std::cout << "int32_t (max): " << std::numeric_limits<std::int32_t>::max() << '\n';

std::cout << "uint32_t (min): " << std::numeric_limits<std::uint32_t>::min() << '\n';
std::cout << "uint32_t (max): " << std::numeric_limits<std::uint32_t>::max() << '\n';
```

<br>

### 64-bit Integers

```cpp
std::cout << "int64_t (min): " << std::numeric_limits<std::int64_t>::min() << '\n';
std::cout << "int64_t (max): " << std::numeric_limits<std::int64_t>::max() << '\n';

std::cout << "uint64_t (min): " << std::numeric_limits<std::uint64_t>::min() << '\n';
std::cout << "uint64_t (max): " << std::numeric_limits<std::uint64_t>::max() << '\n';
```

<br>

---

<br>