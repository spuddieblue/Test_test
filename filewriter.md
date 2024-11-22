# FileWriter vs PrintWriter: Concise Guide

## FileWriter

### Use When:
- You need **basic writing capabilities**.
- Writing **raw characters or simple strings** without advanced formatting.
- You want **minimal overhead** and don’t need buffering or advanced features.

### Key Features:
- Writes **raw characters or strings**.
- Does **not auto-flush** (relies on the OS to handle writes).
- Requires manual addition of **line breaks** (`\n`).
- Interprets `write(int)` as a Unicode code point (not the number itself).

### Example:
```java
FileWriter writer = new FileWriter("example.txt");
writer.write("Hello, FileWriter!\n");
writer.write("Another line.\n");
writer.write(String.valueOf(56));  // Converts number to a string manually
writer.close();
```
## Comparison Table

| **Feature**           | **FileWriter**                  | **PrintWriter**                 |
|-----------------------|----------------------------------|---------------------------------|
| **Ease of Use**       | Basic                           | Advanced                        |
| **Formatting**        | Manual (e.g., concatenation)    | Built-in with `printf()`        |
| **Line Breaks**       | Must add `\n` manually          | Automatic with `println()`      |
| **Data Type Support** | Strings and single characters   | Handles all types (`int`, etc.) |
| **Buffered Output**   | Relies on OS buffering          | Adds Java-level buffering       |
| **Error Checking**    | No direct support               | Built-in with `checkError()`    |
| **Best Use Case**     | Lightweight, raw writing        | Structured, formatted writing   |

## When to Choose One

### Choose FileWriter:
- For **basic, minimalistic file writing** with no need for formatting or data type conversion.
- When you want **lower overhead** for performance-critical tasks.

### Choose PrintWriter:
- For **convenience, flexibility, and formatted output**.
- When you need to handle **multiple data types** or want easy-to-read, maintainable code.



