# Java Chapter 2 Reference Sheet — Elementary Programming

## Console Input
```java
Scanner input = new Scanner(System.in);
double value = input.nextDouble();
```

## Variable Declarations
```java
int x;
double radius;
char a;
```

## Assignment Statements
```java
x = 1;
radius = 1.0;
a = 'A';
```

## Declare and Initialize in One Line
```java
int x = 1;
double d = 1.4;
```

## Constants
```java
final double PI = 3.14159;
final int SIZE = 3;
```

## Naming Conventions
- **Variables/Methods**: camelCase — `radius`, `computeArea`
- **Classes**: PascalCase — `ComputeArea`
- **Constants**: UPPER_CASE — `MAX_VALUE`

## Numeric Data Types and Ranges
| Type   | Range                                 | Size         |
|--------|----------------------------------------|--------------|
| byte   | -128 to 127                            | 8-bit        |
| short  | -32,768 to 32,767                      | 16-bit       |
| int    | -2^31 to 2^31–1                        | 32-bit       |
| long   | -2^63 to 2^63–1                        | 64-bit       |
| float  | ±1.4E–45 to ±3.4E+38                   | 32-bit IEEE  |
| double | ±4.9E–324 to ±1.8E+308                 | 64-bit IEEE  |

## Numeric Input Methods
- `nextByte()`, `nextShort()`, `nextInt()`, `nextLong()`
- `nextFloat()`, `nextDouble()`

## Arithmetic Operators
| Operator | Meaning      | Example       |
|----------|--------------|---------------|
| `+`      | Addition     | `34 + 1`      |
| `-`      | Subtraction  | `34.0 - 0.1`  |
| `*`      | Multiplication | `300 * 30`  |
| `/`      | Division     | `1.0 / 2.0`   |
| `%`      | Remainder    | `20 % 3`      |

## Integer Division
```java
5 / 2     // yields 2
5.0 / 2   // yields 2.5
5 % 2     // yields 1
```

## Exponentiation
```java
Math.pow(2, 3);     // 8.0
Math.pow(4, 0.5);   // 2.0
Math.pow(2.5, -2);  // 0.16
```

## Number Literals
```java
int i = 34;
long x = 1000000L;
double d = 5.0;
float f = 100.2f;
```

## Scientific Notation
```java
double d = 1.23456e+2;  // 123.456
```

## Augmented Assignment
```java
x += 8;   // x = x + 8;
x -= 2;   // x = x - 2;
x *= 3;   // x = x * 3;
x /= 4;   // x = x / 4;
x %= 5;   // x = x % 5;
```

## Increment/Decrement
```java
++i;  // pre-increment
i++;  // post-increment
--i;  // pre-decrement
i--;  // post-decrement
```

## Type Casting
```java
double d = 3;         // implicit widening
int i = (int)3.9;     // explicit narrowing → 3
```

## Expression Casting in Augmented Ops
```java
int sum = 0;
sum += 4.5;  // equivalent to: sum = (int)(sum + 4.5);
```

## Software Development Process (Phases)
- Requirement Specification
- System Analysis
- System Design
- IPO (Input-Process-Output)
- Implementation
- Testing
- Deployment
- Maintenance

## Common Errors and Pitfalls
- Undeclared/unused variables
- Integer overflow (`int value = 2147483647 + 1;` → wraps)
- Round-off errors (`1.0 - 0.9` ≠ `0.1`)
- Unintended integer division (`5 / 2` = `2`)
- Redundant Scanner objects (only create one)
