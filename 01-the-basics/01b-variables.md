<br>

---

<br>

## Declaration

Declaration is the process of specifying a variable's name and data type. It reserves a specific amount of memory for the variable, but does not assign it a value.

```cpp
int x;
```

<br>

---

<br>

## Default Initialization

If you declare a variable without an initializer, C++ applies **default initialization**:
   
- Fundamental types (e.g., `int`, `double`, `char`) are left **uninitialized** (undefined behavior).
- For user-defined types (like classes), the default constructor is called.

```cpp
int x;  // x is uninitialized (undefined)
std::string s;  // s is initialized as an empty string
```

<br>

### Benefits and Drawbacks:

| Benefits | Drawbacks |
| :--- | :--- |
| For class types, this allows you to rely on the default constructor to initialize the object. | For fundamental types, the variable will be uninitialized, which can lead to undefined behavior. |
| | It’s safer to always initialize variables explicitly to avoid undefined behavior. |

<br>

---

<br>

## Initialization

Initialization is the process of assigning a value to a variable. It's important to initialize variables before using them to avoid undefined behavior.

<br>

---

<br>

### Copy Initialization

This is the traditional way of initializing variables and is often used in older C++ codebases.

```cpp
int x = 10;  // Copy initialization
```

<br>

#### Benefits and Drawbacks:

| Benefits | Drawbacks |
| :--- | :--- |
| Familiar to most developers, especially those coming from C. | For objects, it can involve unnecessary copies if the compiler cannot optimize it out. |
| Works in most cases for primitive types and simple objects. | |

<br>

---

<br>

### Direct Initialization

This form directly calls the constructor of the variable type and avoids the creation of temporary objects. It's more efficient when working with classes or complex types.

```cpp
int x(10);  // Direct initialization
```

<br>

#### Benefits and Drawbacks:

| Benefits | Drawbacks |
| :--- | :--- |
| More efficient than copy initialization for user-defined types. | Slightly less common for fundamental types (but works the same). |
| No creation of temporary objects. | Can look odd in certain contexts compared to the `=` form. |

<br>

---

<br>

### Uniform Initialization (Brace Initialization)

Introduced in **C++11**, uniform initialization uses braces `{}` and provides a consistent way to initialize variables, arrays, containers, and even aggregate types (e.g., structs, classes).

```cpp
int x {10};  // recommended for modern C++
```

<br>

#### Benefits and Drawbacks:

| Benefits | Drawbacks |
| :--- | :--- |
| Prevents *narrowing conversions* (e.g., initializing `int` from `double`). | May be unfamiliar to developers not used to C++11 or later. |
| Works uniformly across all types, including arrays and user-defined types. | Brace-initialization can sometimes call `initializer_list` constructors instead of regular constructors. |
| Encouraged for modern C++ as it leads to clearer and safer code. | |
| Works with `std::initializer_list` (useful for collections like `std::vector`). | |

<br>

---

<br>

### List Initialization (C++11)

This is a special form of uniform initialization used specifically with aggregate types like arrays and structs.

```cpp
int arr[3] = {1, 2, 3};  // List initialization for arrays
std::vector<int> v = {1, 2, 3};  // Initializes vector using initializer_list
```

<br>

#### Benefits and Drawbacks:

| Benefits | Drawbacks |
| :--- | :--- |
| Simple and clear for initializing arrays and collections. | Only works with types that support `std::initializer_list`. |
| Prevents narrowing conversions, similar to uniform initialization. | |

<br>

---

<br>

### Value Initialization

Value initialization ensures that the variable is zero-initialized (set to zero for fundamental types or calls the default constructor for class types).

```cpp
int x{};  // Initializes `x` to 0
std::string s{};  // Initializes `s` to an empty string
```

<br>

#### Benefits and Drawbacks:

| Benefits | Drawbacks |
| :--- | :--- |
| Safe, ensures that variables are initialized even when the initial value isn't important. | Less familiar to developers who are not using C++11 or later. |
| Consistently works with both fundamental and user-defined types. | |
| Clean and modern syntax. | |

<br>

---

<br>

## Initializing Multiple Variables

Multiple variables of the same type can be declared and initialized on the same line:

```cpp
int min_num = 0, max_num = 10;
```

<br>

However, for better readability, it is often a good idea to declare and initialize each variable on its own line:

```cpp
int min_num = 0;
int max_num = 10;
```

<br>

---

<br>

## Constants

The `const` keyword is used to define variables whose values must remain constant throughout the program. Once initialized, their values cannot be changed. Constants must be initialized at the point of declaration:

```cpp
const int days_of_week = 7;
```

<br>

In C++17 and later, you can also use the `inline` keyword to declare constants inside headers without violating the One Definition Rule (ODR):

```cpp
inline const int months_in_year = 12;
```

<br>

---

<br>

## Naming Conventions

Variable naming conventions are important for readability and consistency. Here are some commonly used naming styles in C++:

```cpp
int file_size;  // Snake Case (recommended in C++)
int FileSize;   // Pascal Case (common in other languages, but less in C++)
int fileSize;   // Camel Case (often used in C++)
int iFileSize;  // Hungarian Notation (discouraged in modern C++)
```

<br>

---

<br>

## C++ Naming Best Practices

- Prefer **snake_case** or **camelCase** for variable names in C++.
- Avoid using Hungarian notation as it is considered outdated and can lead to less readable code.

<br>

---

<br>