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
Output:
arduino
Copy code
Hello, FileWriter!
Another line.
56
PrintWriter
Use When:
You need advanced convenience and formatting capabilities.
Writing different data types (e.g., int, float, boolean) without manual conversion.
Automatically handling line breaks (println()).
You want additional tools like formatted output (printf) or error checking (checkError()).
Key Features:
Provides methods like println(), print(), and printf() for formatting and structured output.
Automatically converts data types to strings.
Supports buffering to minimize file operations.
Offers an optional checkError() method to verify errors.
Example:
java
Copy code
PrintWriter writer = new PrintWriter(new FileWriter("example.txt"));
writer.println("Hello, PrintWriter!");
writer.printf("Formatted number: %.2f%n", 56.78);
writer.println(56);  // Automatically converts the number to a string
writer.close
