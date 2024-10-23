<br>

---

<br>

```cpp
#include <iostream>

int main() {
	std::cout << "Hello, World!" << '\n';
	return 0;
}
```

<br>

---

<br>

## Breakdown

<br>

```cpp
#include <iostream>
```

> **Explanation**: 
> - This line includes the `iostream` library, which provides functionality for input and output, such as reading from the keyboard or printing to the console.

<br>

```cpp
int main() {
```

> **Explanation**:
> - This is the starting point of every C++ program. 
> - The `main` function is where the execution begins. 
> - The `int` indicates that the function returns an integer value (typically used to signal success or failure to the operating system).

<br>

```cpp
std::cout << "Hello, World!" << '\n';
```

> **Explanation**: 
> - `std::cout` is an object that represents the standard output stream (usually the console).
> - The `<<` operator is used to send data to the output stream (in this case, the string `"Hello, World!"`).
> - `'\n'` is a newline character, which moves the cursor to the next line in the console after the text is printed.

<br>

```cpp
return 0;
```

> **Explanation**: 
> - This line returns the value `0` from the `main` function, which indicates to the operating system that the program executed successfully.

<br>

```cpp
}
```

> **Explanation**: 
> - This closing curly brace marks the end of the `main` function.

<br>

---

<br>

### Summary:

This simple program includes the necessary header for input/output, defines a `main` function, prints "Hello, World!" to the console, and returns `0` to indicate successful completion.