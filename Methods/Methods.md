# Java Methods Programming Exercises

---

## Exercise 1: Basic Method Creation  

Create a class called `MathHelper` with the following methods:

```java
public class MathHelper {
    // TODO: Implement these methods
    
    // 1. Create a method called 'calculateSum' that takes two integers 
    //    and returns their sum
    
    // 2. Create a method called 'findMin' that takes two integers 
    //    and returns the smaller one
    
    // 3. Create a void method called 'printResult' that takes an integer 
    //    and prints "The result is: [number]"
    
    public static void main(String[] args) {
        // Test your methods here
        int sum = calculateSum(15, 25);
        int min = findMin(10, 20);
        printResult(sum);
        printResult(min);
    }
}
```

**Expected Output:**
```
The result is: 40
The result is: 10
```

---

## Exercise 2: Method Overloading  

Create a class called `Calculator` that demonstrates method overloading:

```java
public class Calculator {
    // TODO: Create multiple versions of a 'multiply' method that can handle:
    // 1. Two integers
    // 2. Three integers  
    // 3. Two double values
    // 4. An integer and a string (repeat the string that many times)
    
    public static void main(String[] args) {
        // Test all your overloaded methods
        System.out.println("Two ints: " + multiply(5, 3));
        System.out.println("Three ints: " + multiply(5, 3, 2));
        System.out.println("Two doubles: " + multiply(5.5, 3.2));
        System.out.println("Int and string: " + multiply(3, "Hi!"));
    }
}
```

**Expected Output:**
```
Two ints: 15
Three ints: 30
Two doubles: 17.6
Int and string: Hi!Hi!Hi!
```

---

## Exercise 3: Parameter Passing and Scope  

Create a class called `VariableScope` that demonstrates pass-by-value and variable scope:

```java
public class VariableScope {
    
    // 1. Create a method called 'tryToModify' that takes an integer parameter,
    //    adds 10 to it, and prints the value inside the method
    
    // 2. Create a method called 'processArray' that takes an integer array,
    //    doubles each element, and prints the array
    
    // 3. Create a method called 'demonstrateScope' that:
    //    - Declares a local variable 'x' with value 100
    //    - Uses a for loop (int i = 0; i < 3; i++)
    //    - INSIDE the for loop body, declare a variable 'y' with value i * 10
    //    - Prints both x and y inside the loop
    //    - Try to print y outside the loop (what happens?)
    
    public static void main(String[] args) {
        int number = 5;
        System.out.println("Before method call: " + number);
        tryToModify(number);
        System.out.println("After method call: " + number);
        
        int[] arr = {1, 2, 3, 4, 5};
        System.out.print("Before: ");
        for(int val : arr) System.out.print(val + " ");
        System.out.println();
        
        processArray(arr);
        
        System.out.print("After: ");
        for(int val : arr) System.out.print(val + " ");
        System.out.println();
        
        demonstrateScope();
    }
}
```

**Questions to answer:**
- Why doesn't the integer change after the method call?
- Why does the array change after the method call?
- What happens when you try to access `y` outside the loop?

---

## Bonus Challenge: Random Character Generator (Extra time)  

If you finish early, extend the RandomCharacter concept from the slides:

```java
public class PasswordGenerator {
    
    // Create methods to generate:
    // 1. A random lowercase letter
    // 2. A random uppercase letter  
    // 3. A random digit character
    // 4. A random special character from: !@#$%^&*
    // 5. A method that generates a password of specified length 
    //    containing a mix of all character types
    
    public static void main(String[] args) {
        System.out.println("Random lowercase: " + getRandomLower());
        System.out.println("Random uppercase: " + getRandomUpper());
        System.out.println("Random digit: " + getRandomDigit());
        System.out.println("Random special: " + getRandomSpecial());
        System.out.println("8-character password: " + generatePassword(8));
    }
}
```

---

## Submission Guidelines:
1. Create separate `.java` files for each exercise
2. Include comments explaining your logic
3. Post these files in one repo on your GitHub
4. Create one README file that answers the questions posted above
5. Submit a CLICKABLE LINK to your repo
