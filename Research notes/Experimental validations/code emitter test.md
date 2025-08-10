
This plugin allows code blocks to be executed interactively like in Jupyter Notebooks. It has no external environment requirements (such as system installations of compilers), because code execution works via local sandboxes using JavaScript or WebAssembly technology, or network requests to online Playgrounds. This means it can support all platforms supported by Obsidian.


Supported languages:

| Language   | Provider                                                                                       |
| ---------- | ---------------------------------------------------------------------------------------------- |
| C/C++      | [Sololearn](https://www.sololearn.com/)                                                        |
| C#         | [Sololearn](https://www.sololearn.com/)                                                        |
| Go         | [Sololearn](https://www.sololearn.com/)                                                        |
| Haskell    | [https://play.haskell.org](https://play.haskell.org/)                                          |
| HTML & CSS | [Shadow DOM](https://developer.mozilla.org/en-US/docs/Web/API/Web_components/Using_shadow_DOM) |
| Java       | [Sololearn](https://www.sololearn.com/)                                                        |
| JavaScript | JS Sandbox ([qiankun](https://github.com/umijs/qiankun/blob/master/src/sandbox/index.ts))      |
| Kotlin     | [https://play.kotlinlang.org](https://play.kotlinlang.org/)                                    |
| Python     | WebAssembly ([Pyodide](https://github.com/pyodide/pyodide))                                    |
| R          | [Sololearn](https://www.sololearn.com/)                                                        |
| Rust       | [https://play.rust-lang.org](https://play.rust-lang.org/)                                      |
| Swift      | [Sololearn](https://www.sololearn.com/)                                                        |
| TypeScript | [TypeScript](https://www.typescriptlang.org/) Compiler + JS Sandbox                            |
| V          | [https://play.vosca.dev/](https://play.vosca.dev/)                                             |
| Wenyan     | [Wenyan](https://github.com/wenyan-lang/wenyan) Compiler + JS Sandbox                          |

Note

Only `Python`, `TypeScript`, and `JavaScript` are run in a local sandbox (JS/WebAssembly). Others will send code to third-party website to evaluate the results (e.g.: [https://play.kotlinlang.org](https://play.kotlinlang.org/), [https://play.rust-lang.org](https://play.rust-lang.org/)). Please take care to avoid sending your potentially-sensitive source code.


### Python

[](https://github.com/mokeyish/obsidian-code-emitter#python)

Install `numpy` through `micropip`


```python
import micropip
await micropip.install('numpy')  
import numpy as np
a = np.random.rand(3,2)
b = np.random.rand(2,5)

print(a@b)

```



#### Using `matplotlib`

[](https://github.com/mokeyish/obsidian-code-emitter#using-matplotlib)

```python
import micropip
await micropip.install('matplotlib')

import matplotlib.pyplot as plt

fig, ax = plt.subplots()             # Create a figure containing a single Axes.
ax.plot([1, 2, 3, 4], [1, 4, 2, 3])  # Plot some data on the Axes.
plt.show()                           # Show the figure.
```


### Python

Test a loop and conditional logic.

```python
numbers = [1, 5, 8, 12, 3, 9]
even_sum = 0
odd_count = 0

for num in numbers:
    if num % 2 == 0:
        even_sum += num
    else:
        odd_count += 1

print(f"Sum of even numbers: {even_sum}")
print(f"Count of odd numbers: {odd_count}")
```

Test dictionary operations.

```python
student = {
    "name": "Alice",
    "age": 20,
    "major": "Computer Science",
    "gpa": 3.8
}

print(f"Student Name: {student['name']}")
print(f"Student Major: {student.get('major', 'Unknown')}")

student["gpa"] = 3.9
student["city"] = "New York"

print("Updated student info:")
for key, value in student.items():
    print(f"{key}: {value}")
```



### HTML & CSS

```html
<div><span class="h">Hello</span><span class="w">world</span></div>

<style>
.h {
  color: red;
}
.w {
  color: green;
}
</style>
```



### Any languages that support CORS


Here is the example to support Ruby.

```ts
const url = 'https://api2.sololearn.com/v2/codeplayground/v2/compile';

const runCode = async (code: string, lang: 'cpp' | 'go' | 'c' | 'java' | 'cs' | 'swift' | 'rb') => {
  const header = {
    'User-Agent': 'Obsidian Code Emitter/0.1.0 (If this is not allowed, please let me know)',
    'Accept': 'application/json, text/plain, */*',
    'Accept-Language': 'en-US',
    'Content-Type': 'application/json',
  };

  const res = await fetch(url, {
    'headers': header,
    'body': JSON.stringify({
      'code': code,
      'codeId': null,
      'input': '',
      'language': lang
    }),
    'method': 'POST',
  });
  return (await res.json()) as {
    success: boolean,
    errors: string[],
    data: {
      sourceCode: number,
      status: number,
      errorCode: number,
      output: string,
      date: string,
      language: string,
      input: string,
    }
  };
};

const ruby_code = `
puts "Hello World12"
`;


console.log((await runCode(ruby_code, 'rb')).data.output);
```




### JavaScript

Assuming a standard JavaScript environment (like Node.js or browser console).

```javascript
function factorial(n) {
  if (n < 0) return "Factorial is not defined for negative numbers";
  if (n === 0 || n === 1) return 1;
  let result = 1;
  for (let i = 2; i <= n; i++) {
    result *= i;
  }
  return result;
}

console.log("Factorial of 5:", factorial(5));
console.log("Factorial of 0:", factorial(0));
console.log("Factorial of -3:", factorial(-3));
```

Test array methods.

```javascript
const fruits = ["apple", "banana", "cherry", "date"];

console.log("Original array:", fruits);
console.log("First fruit:", fruits[0]);
console.log("Array length:", fruits.length);

fruits.push("elderberry");
console.log("After push:", fruits);

const removed = fruits.pop();
console.log("Removed:", removed);
console.log("After pop:", fruits);

const sliced = fruits.slice(1, 3);
console.log("Sliced (index 1 to 3):", sliced);

const mapped = fruits.map(fruit => fruit.toUpperCase());
console.log("Mapped (uppercase):", mapped);
```

### Java

Requires a Java Development Kit (JDK) environment.

```java
public class HelloWorld {
    public static void main(String[] args) {
        System.out.println("Hello from Java!");
        int sum = 0;
        for (int i = 1; i <= 10; i++) {
            sum += i;
        }
        System.out.println("Sum of 1 to 10: " + sum);
    }
}
```

### C++

Requires a C++ compiler (like g++).

```cpp
#include <iostream>
#include <vector>
#include <numeric>

int main() {
    std::cout << "Hello from C++!" << std::endl;
    std::vector<int> numbers = {10, 20, 30, 40, 50};
    double average = std::accumulate(numbers.begin(), numbers.end(), 0.0) / numbers.size();
    std::cout << "Average of numbers: " << average << std::endl;
    return 0;
}
```

### Go

Requires a Go environment.

```go
package main

import "fmt"

func main() {
	fmt.Println("Hello from Go!")
	x := 10
	y := 20
	sum := x + y
	fmt.Printf("The sum of %d and %d is %d\n", x, y, sum)
}
```

### R

Requires an R environment.

```r
# Hello from R
message("Hello from R!")

# Create a vector
data <- c(15, 22, 18, 25, 30)

# Calculate mean and median
mean_val <- mean(data)
median_val <- median(data)

cat("Data:", data, "\n")
cat("Mean:", mean_val, "\n")
cat("Median:", median_val, "\n")
```

### SQL

Requires a SQL database connection or interpreter. This example assumes a generic SQL syntax.

```sql
-- Create a simple table
CREATE TABLE Employees (
    EmployeeID INT PRIMARY KEY,
    FirstName VARCHAR(50),
    LastName VARCHAR(50),
    Department VARCHAR(50)
);

-- Insert some data
INSERT INTO Employees (EmployeeID, FirstName, LastName, Department) VALUES
(1, 'John', 'Doe', 'Sales'),
(2, 'Jane', 'Smith', 'Marketing'),
(3, 'Peter', 'Jones', 'Sales');

-- Select all employees
SELECT * FROM Employees;

-- Select employees in the Sales department
SELECT FirstName, LastName FROM Employees WHERE Department = 'Sales';
```

### Shell (Bash)

Requires a shell environment.

```bash
#!/bin/bash
echo "Hello from Bash!"
current_dir=$(pwd)
echo "Current directory: $current_dir"
ls -l
```

### Examples for Error Handling

Test a syntax error (Python).

```python
print("This is valid syntax")
  print("This is invalid syntax" # IndentationError
```

Test a runtime error (JavaScript).

```javascript
console.log("Starting calculation...");
let result = 10 / 0; // Division by zero
console.log("Result:", result); // This line might not be reached depending on how errors are handled
```

Test an undefined variable (Python).

```python
x = 10
print(y) # NameError: name 'y' is not defined
```

### Example with Larger Output

Test printing many lines (Python).

```python
for i in range(100):
    print(f"Line number {i+1}")
```

These examples cover basic syntax, common data structures, loops, conditionals, and potential error cases across several languages.
