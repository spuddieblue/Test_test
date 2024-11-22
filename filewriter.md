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

