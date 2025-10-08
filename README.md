Here are the questions and their correct answers from the images you provided, listed in a text format suitable for saving.

-----

## Object Oriented Programming Questions and Answers

### Question 6: Output of `switch` with `long`

**Code Snippet:**

```java
public class Main {
    public static void main(String[] args) {
        long key = 10;
        int x = 120;
        switch (key) {
            case 10: System.out.println("10");
            case 4: System.out.println(x);
        }
    }
}
```

**Correct Answer:** **Compilation Error.**
**Reason:** In Java, the `switch` statement expression cannot be of type `long`.

-----

### Question 7: Accessing Non-Static Member from Static Context

**Code Snippet:**

```java
public class ParkRanger {
    int birds = 10;
    public static void main(String[] data) {
        var trees = 5;
        System.out.println(trees + birds);
    }
}
```

**Correct Answer:** **C. It does not compile.**
**Reason:** The static `main` method cannot directly access the non-static (instance) variable `birds` without an object reference. This results in a compiler error: "non-static variable birds cannot be referenced from a static context."

-----

### Question 8: Try-Catch-Finally Execution Flow

**Code Snippet:**

```java
public class Football {
    public static void main(String[] args) {
        try {
            System.out.print('A');
            throw new ArrayIndexOutOfBoundsException();
        } catch (RuntimeException r) {
            System.out.print('B'); // Not executed due to re-throw
            throw r;
        } catch (Exception e) {
            System.out.print('C'); // Not executed, exception was re-thrown
        } finally {
            System.out.print('D');
        }
    }
}
```

**Correct Answer:** **AD**
**Reason:** 'A' is printed in the `try` block. The exception is caught by the first `catch` block which immediately re-throws it. The `finally` block executes next, printing 'D'. The program then terminates due to the uncaught re-thrown exception.

-----

### Question 9: Modifiers for an Abstract Method

**Question:** Which of the following modifiers can be applied to an abstract method? (Choose one)
**Options:** A. final, B. private, **C. public**, D. default, E. concrete
**Correct Answer:** **C. public**
**Note:** Abstract methods can be `public` or `protected`, but not `final` (must be overridden) or `private` (must be visible to subclasses).

-----

### Question 10: Type Inference with `var`

**Question:** Which is equivalent to `var q = 4.0f;`?
**Options:** A. float q = 4.0F;, **B. float q = 4.0f;**, C. double q = 4.0f;, D. double q = 4.0F;, E. Object q = 4.0f;
**Correct Answer:** **B. float q = 4.0f;**
**Reason:** The `f` suffix on the literal `4.0f` explicitly marks it as a `float` type, which the `var` keyword infers.

-----

### Question 11: Array Initialization (Corrected Syntax)

**Code Snippet (Assuming corrected syntax: `static int[][] array = new int[5][];`)**:

```java
public class Main {
    static int[][] array = new int[5][];
    public static void main(String[] args) {
        System.out.println(array[0]);
    }
}
```

**Correct Answer:** **NullPointerException** (at runtime)
**Reason:** The array is initialized only for the first dimension (`new int[5][]`). The elements `array[0]` through `array[4]` are references to arrays, which are initialized to `null`. Attempting to print the reference `array[0]` will print `null` (not a `NullPointerException`), *however*, the image is truncated and usually questions asking for output want to know what prints. If the output is simply the reference (which is `null`), then the correct answer is `null`. Based on similar test questions where printing an uninitialized array *reference* is expected to print **`null`**, and a `NullPointerException` only occurs if you try to dereference it (e.g., `array[0][0]`), the output would be **`null`**.

-----

### Question 12: Filling in Blanks (Logically Flawed Question)

**Question:** Given the following code, what values inserted in order into the blank lines, allow the code to compile? (Based on the code structure and `return 10;`)
**Code Snippet Implied:**

```java
// BLANK 1
public class Banker { // BLANK 2 likely for class/interface
    private static // BLANK 3 (Return Type) getMaxWithdrawal() {
        return 10;
    }
}
```

**Most Logically Consistent Answer (Though the original question is flawed):** **package, int, int** or **package, class, long**.
**Note:** If forced to choose from the common options, and recognizing the code returns an integer (`10`), the return type cannot be `void`. Since the question is inherently flawed, and a single definitive answer cannot be logically derived, no single option can be deemed **correct** based on strict Java rules for the entire program structure.

-----

### Question 13: String Concatenation and Equality

**Code Snippet:**

```java
String s1 = "hello java programming";
final String s2 = "hello java";
String s3 = s2 + " programming";
System.out.println(s3 == s1);
```

**Correct Answer:** **B) false**
**Reason:** `s1` is a literal in the String Pool. `s3` is created at **runtime** using string concatenation, so it is a new object on the heap. The `==` operator checks if they point to the same memory location (they don't), resulting in `false`.

-----

### Question 14: Unchecked Exceptions

**Question:** How many of these custom exceptions are unchecked exceptions?
**Exceptions:**

1.  `class ColoringException extends IOException {}`
2.  `class CursiveException extends WritingException {}`
3.  **`class DrawingException extends IllegalStateException {}`**
4.  **`class SketchingException extends DrawingException {}`**
5.  `class WritingException extends Exception {}`
    **Correct Answer:** **C. Two**
    **Reason:** Unchecked exceptions are those that extend `RuntimeException` or its subclasses. `IllegalStateException` is a subclass of `RuntimeException`. Therefore, `DrawingException` and its subclass `SketchingException` are unchecked. The others extend `Exception` or `IOException`, making them checked.

-----

### Question 17: Array Declaration Syntax

**Code Snippet:**

```java
public class Main {
    static int[] [] array;
    public static void main(String[] args) {
        System.out.println(array);
    }
}
```

**Correct Answer:** **Compilation Error.**
**Reason:** The array declaration `static int[] [] array;` has invalid syntax due to the space between the brackets. The correct syntax is `static int[][] array;`.

-----

### Question 18: StringBuffer `setCharAt`

**Code Snippet:**

```java
StringBuffer sb = new StringBuffer("ABCDE");
sb.setCharAt(2, 'X');
System.out.println(sb);
```

**Correct Answer:** **C) ABXDE**
**Reason:** `setCharAt(2, 'X')` replaces the character at index 2 (the third character, 'C') with 'X'.

-----

### Question 19: Array Access with Uninitialized Subarray

**Code Snippet (Assuming corrected syntax: `static int[][] array = new int[5][];`)**:

```java
public class Main {
    static int[][] array = new int[5][];
    public static void main(String[] args) {
        System.out.println(array[0]);
    }
}
```

**Correct Answer:** **B. null**
**Reason:** The line `new int[5][];` initializes `array` to hold 5 references to integer arrays, but these inner arrays are not created and are initially set to `null`. Printing the reference `array[0]` (which is a variable of type `int[]`) when its value is `null` will simply output the string "**null**" to the console.

-----

### Question 20: Accessing Instance Variables from Static Method

**Code Snippet (Interpreted):**

```java
public class RollerSkates {
    static int wheels = 1; 
    int tracks = 5; // Non-static instance variable
    public static void main(String[] arguments) {
        // ... (Object creation/assignments are syntactically incorrect)
        System.out.println(feet + tracks + s.wheels); // Accessing instance variables directly
    }
}
```

**Correct Answer:** **A. The code does not compile.**
**Reason:** The `main` method is `static` and cannot directly access the non-static instance variable `tracks` (and other variables/objects that are either undeclared or incorrectly accessed). The compiler will flag this as an error.
