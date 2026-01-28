# Recursive Comment Counter (Java)

## 📌 Project Overview
This Java program calculates the total number of comments and replies in a nested structure. It uses an `Object[]` array to simulate a real-world comment system where a comment can have multiple replies (nested arrays).

### Key Features:
* **Nested Array Handling**: Uses `Object[]` to store mixed types (String and Array).
* **Recursive Logic**: A recursive function traverses through multiple layers of replies.
* **Type Checking**: Uses `instanceof` to distinguish between a single comment and a reply thread.

## 💻 Code Snippet
The core logic uses a recursive method to "dive" into nested arrays:
```java
if (item instanceof String) {
    count++; // Direct Comment
} else if (item instanceof Object[]) {
    count += countAll((Object[]) item); // Nested Replies
}
