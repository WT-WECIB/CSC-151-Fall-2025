# Java Chapter 3 Reference Sheet — Selections

## Boolean Logic and Relational Operators

| Concept              | Syntax / Example           |
|----------------------|----------------------------|
| Boolean variable     | `boolean b = true;`        |
| Relational operators | `==`, `!=`, `<`, `<=`, `>`, `>=` |
| Boolean expression   | `boolean b = (x > y);`     |

---

## Selection Statements

### One-Way `if`
```java
if (condition) {
    // Code runs if condition is true
}
```

### Two-Way `if-else`
```java
if (condition) {
    // true branch
} else {
    // false branch
}
```

### Multi-Way `if-else`
```java
if (cond1) {
    ...
} else if (cond2) {
    ...
} else {
    ...
}
```

---

## Common `if` Errors

- Semicolon after `if`:
  ```java
  if (x > 0); // ← BAD
  ```

---

## Random Numbers

```java
int num = (int)(Math.random() * 10); // Generates 0–9
```

---

## Logical Operators

| Operator | Description             | Example                            |
|----------|-------------------------|------------------------------------|
| `&&`     | AND (short-circuit)     | `(x > 0 && y > 0)`                 |
| `||`     | OR (short-circuit)      | `(x > 0 || y > 0)`                 |
| `!`      | NOT                     | `!(x > 0)`                         |
| `^`      | XOR                     | `(x % 2 == 0) ^ (x % 3 == 0)`      |
| `&`      | AND (no short-circuit)  | `(x > 1) & (x++ < 10)`             |
| `|`      | OR (no short-circuit)   | `(x == 1) | (x++ < 10)`            |

---

## `switch` Statement

```java
switch (status) {
    case 0: System.out.println("Single"); break;
    case 1: System.out.println("Married"); break;
    default: System.out.println("Invalid"); break;
}
```

---

## Java 14 Enhancements

### Arrow Case Syntax

```java
switch (day) {
    case 1 -> System.out.println("One");
    case 2 -> System.out.println("Two");
    default -> System.out.println("Other");
}
```

### `switch` Expression with `yield`

```java
String result = switch (month) {
    case 2 -> {
        if (isLeapYear(year)) yield "29 days";
        else yield "28 days";
    }
    default -> "30 or 31 days";
};
```

### Combining Cases

```java
int day = 1;
System.out.println(
    switch (day) {
        case 1, 2, 3 -> day + " ";
        default -> " ";
    }
);
```

---

## Conditional (Ternary) Operator

```java
y = (x > 0) ? 1 : -1;

System.out.println(
    (num % 2 == 0) ? "Even" : "Odd"
);
```

---

## Operator Precedence (Selected)

| Precedence (High → Low)   | Operators                              |
|---------------------------|----------------------------------------|
| 1st (postfix)             | `++`, `--`                             |
| 2nd (unary)               | `+`, `-`, `!`                          |
| 3rd                       | `*`, `/`, `%`                          |
| 4th                       | `+`, `-` (binary)                      |
| 5th                       | `<`, `<=`, `>`, `>=`                   |
| 6th                       | `==`, `!=`                             |
| 7th                       | `^`                                    |
| 8th                       | `&&`                                   |
| 9th                       | `||`                                   |
| 10th (assignment)         | `=`, `+=`, `-=`, `*=`, `/=`, `%=`      |

---

## Debugging Techniques

- Logic errors are called bugs
- Use:
  - Hand-tracing
  - `System.out.println(...)` to inspect variables
  - Debugger to:
    - Step through code
    - Set breakpoints
    - View and modify variables
    - Inspect call stack
