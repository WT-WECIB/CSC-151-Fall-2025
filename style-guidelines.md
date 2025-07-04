
# Java I Style Guidelines  

---

## 1. File Header

Every `.java` file MUST start with:

```java
/**
 * Your Name
 * Course: Java I
 * Date: MM/DD/YYYY
 *
 * Brief description of the class or program.
 */
```

---

## 2. Class, Method, and Variable Naming Requirements

| Element         | Format                  | Example         |
|-----------------|------------------------|-----------------|
| Class Names     | PascalCase              | `StudentInfo`   |
| Method Names    | camelCase               | `calculateTotal()` |
| Variable Names  | camelCase               | `totalScore`    |
| Constants       | ALL_CAPS_WITH_UNDERSCORES | `MAX_ATTEMPTS` |

Do NOT use single-letter variable names unless inside simple loops:

```java
for (int i = 0; i < 10; i++) {
    sum += i;
}
```

---

## 3. Indentation and Braces

Use **4 spaces** for indentation (NO tabs).  
Left brace `{` on the same line, right brace aligned:

```java
public class Example {

    public static void main(String[] args) {
        System.out.println("Hello World");
    }
}
```

---

## 4. Spacing

Use spaces for readability:

```java
int total = 0;
if (score > 90) {
    total += score;
}
```

Incorrect:

```java
int total=0;
if(score>90){
    total+=score;
}
```

---

## 5. Comments

Every class and method should have a Javadoc-style comment:

```java
/**
 * Calculates area of a rectangle.
 * @param width The width of the rectangle.
 * @param height The height of the rectangle.
 * @return The area.
 */
public int calculateArea(int width, int height) {
    return width * height;
}
```

Use `//` for short, in-line comments.

---

## 6. Method Structure

- Keep methods short and focused - **one task per method**.  
- Use clear, meaningful parameter names and return types.

---

## 7. Constants Over Magic Numbers

Never hardcode unexplained numbers. Always use a constant. Example below:

```java
public static final int MAX_RETRIES = 3;
```

---

## 8. Readability

Use blank lines to separate logical blocks of code.  
Keep lines under 100 characters in length for readability.
Incorrect spelling will result in a points deduction.

---

## 9. Error Handling

Use `try-catch` when appropriate.  
**Always validate user input**.

---

## 10. Compilation and Submission

✔ Code must compile with **no errors or warnings**. If code does not compile, the grade will be **zero**.  
✔ Follow these style rules - violations will lose points.  
✔ Submit all files with correct headers.

---

## 11. Example Template

```java
/**
 * Purple Folder
 * Java I
 * 08/15/2025
 *
 * Simple program to greet the user.
 */
public class HelloWorld {

    public static void main(String[] args) {
        System.out.println("Hello, World!");
    }
}
```
