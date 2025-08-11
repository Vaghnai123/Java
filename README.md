<!-- JDK VS JVM VS JRE -->

JDK :- It's a software development kit required to develop java applications.
JRE :- It's part of JDK that provides the libraries and other components to run applications.
JVM :- It's a part of JRE and responsible for executing the Java bytecode.

---------------------------------------------------------------------------------------------------------------
<!-- Showing Output -->

System.out.print("one"); <!-- Use when 2 or more output print in single line -->
System.out.println("Hello"); <!-- Use when 2 or more output print in multi line -->

<!-- Variable :- Variable are like containers used for storing data values Example :- int a = 5; -->

<!-- Hello world Program  -->

public class HelloWorld {
public static void main(String[] args) {
System.out.println("Hello, World!");
}
}

---------------------------------------------------------------------------------------------------------------
<!-- Data types-->

There are two data type in java

1. Primitive Data types ---> boolean, char, byte, short, int, long, float, double.
2. Non Primitive Data types ---> strings, arrays, objects, etc.
   Example :-
   Integer literals --> 10,5,-8, etc...
   Floating Point --> 1.2, 0.25, -1.999, etc..
   Boolean Literal --> true, false
   character literals --> 'a', 'A', 'N' , 'q' , etc...
   string literals --> "hi", "hello", "whats'up"

---------------------------------------------------------------------------------------------------------------
<!-- Naming Conversions -->

Camel case :- It is a style of writing where The first word starts with a lowercase letter. Every subsequent word starts with a capital letter  
Example :- myVariableName
Snake*case :- In snake_case, all letters are lowercase, and words are separated by underscores (*)
Example :- first_name, max_speed_limit.
Kebab-case :- kebab-case means all lowercase words separated by hyphens (-).  
Example :- my-variable-name

---------------------------------------------------------------------------------------------------------------
<!-- Escape Sequences -->

\n --> New line (The escape sequence \n is used to insert a new line in the output.)

<!-- Example --> System.out.println("Hello\nWorld");  --> Output :- Hello  World

\t --> Tab space (The escape sequence \t inserts a horizontal tab space in the output.)

<!-- Example --> System.out.println("Java\tRocks");  --> Output :- Java Rocks

\b --> backspace (The escape sequence \b is a backspace, which moves the cursor one character back and removes the previous character in output.)

<!-- Example --> System.out.println("Helloo\b");  --> Output :- Hello

\\ --> The escape sequence \\ is used to print a backslash (\) character itself.

<!-- Example --> System.out.println("This is a backslash: \\\\");  --> Output :- This is a backslash: \

\' --> The escape sequence \' is used to insert a single quote (') character in a string or character literal.

<!-- Example --> System.out.println("It\'s Java");  --> Output :- It's Java

\" --> The escape sequence \" is used to insert a double quote (") character inside a string.

<!-- Example --> System.out.println("She said \"Hello\""); --> Output :- She said "Hello"

---------------------------------------------------------------------------------------------------------------
<!-- Keywords -->

The complete list of Java keywords is:- abstract, assert, boolean, break, byte, case, catch, char, class, const, continue, default, do, double, else, enum, extends, final, finally, float, for, goto, if, implements, import, instanceof, int, interface, long, native, new, null, package, private, protected, public, return, short, static, strictfp, super, switch, synchronized, this, throw, throws, transient, try, void, volatile, and while.

---------------------------------------------------------------------------------------------------------------
<!-- Rules for Naming Identifiers -->

1. It Can only contain Letters (A-Z, a-z), Digits (0-9), Underscore (\_), Dollar sign ($)
2. Java identifiers cannot be keywords, meaning reserved words like int, class, or for cannot be used as names.
3. Identifier must start with a letter, an underscore (\_), or a dollar sign ($), but cannot start with a digit.
4. Java Identifier are Case-sensitive. Example :- total and Total are different identifiers.
5. An identifier cannot contain spaces; for example, first name is invalid, but firstName is valid.
6. Identifier can be of any length, but meaningful and readable names are recommended for better understanding.

---------------------------------------------------------------------------------------------------------------
<!--User Input -->

nextLine() --> It Reads the entire line Example :- Hello World from Java
nextInt() --> It Reads an integer Example :- 25
nextDouble() --> It Reads a double Example :- 5.6
nextFloat() --> It Reads a float Example :- 2.3
nextBoolean() --> It Reads boolean Example :- true

<!-- Example :- -->

import java.util.Scanner;
public class Main {
public static void main(String[] args) {
Scanner sc = new Scanner(System.in);

            System.out.print("Enter your full name: ");
            String fullName = sc.nextLine();

            System.out.print("Enter your age: ");
            int age = sc.nextInt();

            System.out.print("Enter your height (in meters): ");
            double height = sc.nextDouble();

            System.out.print("Enter a floating-point number: ");
            float number = sc.nextFloat();

            // Output the values
            System.out.println("\n--- User Details ---");
            System.out.println("Full Name: " + fullName);
            System.out.println("Age: " + age);
            System.out.println("Height: " + height);
            System.out.println("Float Number: " + number);

    }

}

---------------------------------------------------------------------------------------------------------------
<!-- Challenges :- -->

1. Create a program to input name of the person and respond with "welcome NAME to Coding"
   import java.util.Scanner;
   public class WelcomeProgram {
   public static void main(String[] args) {
   Scanner sc = new Scanner(System.in);

   System.out.print("Enter your name: ");
   String name = sc.nextLine(); // Reads complete name with spaces

   System.out.println("Welcome " + name + " to Coding");
   sc.close();
   }
   }
   Output :-
   Enter your name: Zeel Patel
   Welcome Zeel Patel to Coding

2. Create a program to add two numbers.
   import java.util.Scanner;
   public class AddTwoNumbers {
   public static void main(String[] args) {
   Scanner sc = new Scanner(System.in);

   System.out.print("Enter first number: ");
   double num1 = sc.nextDouble();

   System.out.print("Enter second number: ");
   double num2 = sc.nextDouble();

   double sum = num1 + num2;
   System.out.println("The sum is: " + sum);
   sc.close();
   }
   }
   Output :-
   Enter first number: 5
   Enter second number: 7
   The sum is: 12.0

---------------------------------------------------------------------------------------------------------------
<!-- Type Conversion and Casting :- -->

->Type conversion means changing one data type into another. In Java, this can happen automatically or manually.

-> There are Two main types of type conversion

1. Widening Conversion (Automatic / Implicit)
   -> It Happens automatically when you assign a smaller data type to a bigger data type.
   -> smallest to largest:- [byte->short->int->long->float->double]

2. Narrowing Conversion (Manual / Explicit)
   -> It Happens when you assign a bigger data type to a smaller data type.
   -> Largest to smallest:- [byte<-short<-int<-long<-float<-double]

<!-- Example :- -->
public class TypeConversionCasting {
public static void main(String[] args) {

        // -------- 1. Widening Conversion (Automatic / Implicit) --------
        int intNum = 100;           // int variable
        double doubleNum = intNum;  // int → double
        System.out.println("Widening Conversion (int → double): " + doubleNum);

        // -------- 2. Narrowing Conversion (Manual / Explicit) --------
        double doubleValue = 99.99;
        int intValue = (int) doubleValue; // double → int
        System.out.println("Narrowing Conversion (double → int): " + intValue);
    }

}
Output :-
Widening Conversion (int → double): 100.0
Narrowing Conversion (double → int): 99

---------------------------------------------------------------------------------------------------------------

                                     <!-- Operators, If-else  -->

1.  Arithmetic Operators :-
    -> It is Used for basic math operations.
    | Operator | Description | Example | Output |
    | -------- | ------------------- | ------- | -------------------- |
    | `+` | Addition | `5 + 3` | 8 |
    | `-` | Subtraction | `5 - 3` | 2 |
    | `*` | Multiplication | `5 * 3` | 15 |
    | `/` | Division | `5 / 2` | 2 (integer division) |
    | `%` | Modulus (Remainder) | `5 % 2` | 1 |
    <!-- Example :- -->
    public class Arithmetic {
    public static void main(String[] args) {
    int a = 20, b = 6;
    // Addition
    int sum = a + b;
    System.out.println("Addition (a + b): " + sum);

            // Subtraction
            int difference = a - b;
            System.out.println("Subtraction (a - b): " + difference);

            // Multiplication
            int product = a * b;
            System.out.println("Multiplication (a * b): " + product);

            // Division
            int quotient = a / b; // Integer division
            System.out.println("Division (a / b): " + quotient);

            // Modulus
            int remainder = a % b;
            System.out.println("Modulus (a % b): " + remainder);
        }

    }
    Output :-
    a = 20, b = 6
    Addition (a + b) : 26
    Subtraction (a - b) : 14
    Multiplication (a \* b) : 120
    Division (a / b) : 3
    Modulus (a % b) : 2
---------------------------------------------------------------------------------------------------------------
2.  Assignment (Shorthand) Operators :-
    -> It is Used to assign values to variables.
    | Operator | Example | Meaning |
    | -------- | -------- | ------------- |
    | `=` | `x = 5` | Assign 5 to x |
    | `+=` | `x += 3` | `x = x + 3` |
    | `-=` | `x -= 2` | `x = x - 2` |
    | `*=` | `x *= 4` | `x = x * 4` |
    | `/=` | `x /= 2` | `x = x / 2` |
    | `%=` | `x %= 3` | `x = x % 3` |
    <!-- Example :- -->

    public class AssignmentOperators {
    public static void main(String[] args) {

            int score = 50; // Initial value
            System.out.println("Initial Score: " + score);

            // Using += (Add and assign)
            score += 10; // score = score + 10
            System.out.println("After += 10: " + score);

            // Using -= (Subtract and assign)
            score -= 5; // score = score - 5
            System.out.println("After -= 5: " + score);

            // Using *= (Multiply and assign)
            score *= 2; // score = score * 2
            System.out.println("After *= 2: " + score);

            // Using /= (Divide and assign)
            score /= 4; // score = score / 4
            System.out.println("After /= 4: " + score);

            // Using %= (Modulus and assign)
            score %= 3; // score = score % 3
            System.out.println("After %= 3: " + score);
        }

    }
    Output :-
    Initial Score: 50
    After += 10: 60
    After -= 5: 55
    After \*= 2: 110
    After /= 4: 27
    After %= 3: 0
---------------------------------------------------------------------------------------------------------------
<!-- Challenge -->
1.  Write a program to swap two numbers :-
    import java.util.Scanner;
    public class SwapNumbers {
    public static void main(String[] args) {
    Scanner sc = new Scanner(System.in);

            System.out.print("Enter first number (a): ");
            int a = sc.nextInt();
            System.out.print("Enter second number (b): ");
            int b = sc.nextInt();

            System.out.println("\nBefore Swap:");
            System.out.println("a = " + a + ", b = " + b);

            // Swapping using a temporary variable
            int temp = a;
            a = b;
            b = temp;

            System.out.println("\nAfter Swap:");
            System.out.println("a = " + a + ", b = " + b);
            sc.close();
        }

    }
    Output :-
    Enter first number (a): 5
    Enter second number (b): 10

Before Swap:
a = 5, b = 10

After Swap:
a = 10, b = 5
---------------------------------------------------------------------------------------------------------------
3. Unary operators :-
   -> Unary operators in Java are operators that work on only one operand to perform an operation.

| Operator Type | Expression | Used Value | Final Value | Description
| Pre-increment | ++x | 6 | 6 |increment by 1 first and then use in statement
| Post-increment | x++ | 5 | 6 |use current value in statement then increment
| Pre-decrement | --x | 4 | 4 |decrement by 1 first and then use in statement
| Post-decrement | x-- | 5 | 4 |use current value in statement then decrement

<!-- Example :- -->
public class UnaryOperatorsExample {
public static void main(String[] args) {

        int a = 5;

        // 1. Unary Plus (+) and Minus (-)
        System.out.println("Unary plus (+a): " + (+a)); // keeps the value same
        System.out.println("Unary minus (-a): " + (-a)); // changes sign

        // 2. Increment Operators (++a, a++)
        System.out.println("Pre-increment (++a): " + (++a)); // increases first, then prints
        System.out.println("Post-increment (a++): " + (a++)); // prints first, then increases
        System.out.println("Value of a after post-increment: " + a);

        // 3. Decrement Operators (--a, a--)
        System.out.println("Pre-decrement (--a): " + (--a)); // decreases first, then prints
        System.out.println("Post-decrement (a--): " + (a--)); // prints first, then decreases
        System.out.println("Value of a after post-decrement: " + a);
    }

}
Output :-
Unary plus (+a): 5
Unary minus (-a): -5
Pre-increment (++a): 6
Post-increment (a++): 6
Value of a after post-increment: 7
Pre-decrement (--a): 6
Post-decrement (a--): 6
Value of a after post-decrement: 5
---------------------------------------------------------------------------------------------------------------
<!-- Challenges -->
1.  Create a program to calculate products of two floating point numbers.
    import java.util.Scanner;
    public class ProductOfNumbers {
    public static void main(String[] args) {
    Scanner sc = new Scanner(System.in);

            System.out.print("Enter first number: ");
            float num1 = sc.nextFloat();

            System.out.print("Enter second number: ");
            float num2 = sc.nextFloat();

            float product = num1 * num2;

            System.out.println("Product: " + product);

            sc.close();
        }

    }
    Output :- Enter first number: 2.5 Enter second number: 4.2 Product: 10.5
---------------------------------------------------------------------------------------------------------------
2. create a program to calculate the area of triangle. Area= 1/2*B*H.
   import java.util.Scanner;

public class AreaOfTriangle {
public static void main(String[] args) {
Scanner sc = new Scanner(System.in);

        System.out.print("Enter base of the triangle: ");
        float base = sc.nextFloat();

        System.out.print("Enter height of the triangle: ");
        float height = sc.nextFloat();

        float area = 0.5f * base * height;

        System.out.println("Area of the triangle: " + area);

        sc.close();
    }

}
Output :-
Enter base of the triangle: 5
Enter height of the triangle: 10
Area of the triangle: 25.0
---------------------------------------------------------------------------------------------------------------
3. create a program to calculate simple interest. interest=(PxTxR)/100
   import java.util.Scanner;

public class SimpleInterest {
public static void main(String[] args) {
Scanner sc = new Scanner(System.in);

        System.out.print("Enter Principal amount (P): ");
        float principal = sc.nextFloat();

        System.out.print("Enter Time in years (T): ");
        float time = sc.nextFloat();

        System.out.print("Enter Rate of Interest (R): ");
        float rate = sc.nextFloat();

        float interest = (principal * time * rate) / 100;

        System.out.println("Simple Interest: " + interest);

        sc.close();
    }

}
Output :-
Enter Principal amount (P): 10000
Enter Time in years (T): 2
Enter Rate of Interest (R): 5
Simple Interest: 1000.0
---------------------------------------------------------------------------------------------------------------
4. Create program to convert fahrenheit to celsius.

import java.util.Scanner;
public class FahrenheitToCelsius {
public static void main(String[] args) {
Scanner sc = new Scanner(System.in);

        System.out.print("Enter temperature in Fahrenheit: ");
        float fahrenheit = sc.nextFloat();

        float celsius = (fahrenheit - 32) * 5 / 9;

        System.out.println("Temperature in Celsius: " + celsius);

        sc.close();
    }

}
Output :-
Enter temperature in Fahrenheit: 98.6
Temperature in Celsius: 37.0
---------------------------------------------------------------------------------------------------------------
<!-- If Else -->
-> if and else are decision-making statements in Java.
-> They let your program choose which code block to run based on a condition.

Syntax :-
if (condition) {
    // Code runs if condition is true
} else {
    // Code runs if condition is false
}

<!-- Example :- -->
import java.util.Scanner;
public class VotingEligibility {
    public static void main(String[] args) {
        
        Scanner sc = new Scanner(System.in); // Create Scanner object for input

        System.out.print("Enter your age: ");
        int age = sc.nextInt(); // Read integer input
        
        if (age >= 18) {
            System.out.println("You are eligible to vote.");
        } else {
            System.out.println("You are NOT eligible to vote.");
        }
        
        sc.close(); 
    }
}
---------------------------------------------------------------------------------------------------------------
<!-- <Relational Operator> -->
-> Relational operators are used to compare two values.
-> Mostly used in conditions inside if, while, for, etc.
| Operator | Name                     | Meaning / Use                                          | Example  |  
| `==`     | Equal to                 | Checks if two values are equal                         | `5 == 5` | 
| `!=`     | Not equal to             | Checks if two values are different                     | `5 != 3` | 
| `>`      | Greater than             | Checks if left value is greater than right             | `7 > 5`  | 
| `<`      | Less than                | Checks if left value is less than right                | `4 < 9`  | 
| `>=`     | Greater than or equal to | Checks if left value is greater than or equal to right | `5 >= 5` | 
| `<=`     | Less than or equal to    | Checks if left value is less than or equal to right    | `3 <= 4` | 

Example :-
import java.util.Scanner;

public class RelationalExampleInput {
    public static void main(String[] args) {
        
        Scanner sc = new Scanner(System.in); // Create Scanner object

        System.out.print("Enter first number: ");
        int num1 = sc.nextInt();
        
        System.out.print("Enter second number: ");
        int num2 = sc.nextInt();
        
        System.out.println(num1 + " == " + num2 + " : " + (num1 == num2));
        System.out.println(num1 + " != " + num2 + " : " + (num1 != num2));
        System.out.println(num1 + " > " + num2  + " : " + (num1 > num2));
        System.out.println(num1 + " < " + num2  + " : " + (num1 < num2));
        System.out.println(num1 + " >= " + num2 + " : " + (num1 >= num2));
        System.out.println(num1 + " <= " + num2 + " : " + (num1 <= num2));
        
        sc.close(); 
    }
}
Output :-
Enter first number: 10
Enter second number: 20
10 == 20 : false
10 != 20 : true
10 > 20  : false
10 < 20  : true
10 >= 20 : false
10 <= 20 : true
---------------------------------------------------------------------------------------------------------------
<!-- Logical Operator -->
-> Logical operators are used to combine two or more conditions.
-> Mostly used in if, while, for statements for decision-making.

| Operator | Name        | Description                                          | Example                 | 
| `&&`     | Logical AND | True if both conditions are true                     | `(a > 5) && (b < 10)    | 
| `||`   | Logical OR  | True if at least one condition is true               | `(a > 5) || (b < 10)`   | 
| `!`      | Logical NOT | Reverses the result (true → false, false → true)     | `!(a > 5)`              | 

<!-- Example :- -->
import java.util.Scanner;

public class LogicalOperatorsExample {
    public static void main(String[] args) {
        
        Scanner sc = new Scanner(System.in);

        System.out.print("Enter your age: ");
        int age = sc.nextInt();

        System.out.print("Do you have a Voter ID? (true/false): ");
        boolean hasVoterID = sc.nextBoolean();

        // Logical AND (&&) → both conditions must be true
        if (age >= 18 && hasVoterID) {
            System.out.println("✅ You are eligible to vote.");
        } else {
            System.out.println("❌ You are NOT eligible to vote.");
        }

        // Logical OR (||) → at least one condition must be true
        if (age >= 18 || hasVoterID) {
            System.out.println("🙂 You meet at least one voting requirement.");
        } else {
            System.out.println("🙁 You meet no voting requirements.");
        }

        // Logical NOT (!) → reverses result
        boolean isAdult = age >= 18;
        System.out.println("Is adult? " + isAdult);
        System.out.println("Not adult? " + !isAdult);

        sc.close();
    }
}
Output :-
Enter your age: 20
Do you have a Voter ID? (true/false): true
✅ You are eligible to vote.
🙂 You meet at least one voting requirement.
Is adult? true
Not adult? false
---------------------------------------------------------------------------------------------------------------
<!-- Challenges :- -->
1. Create a program that determines if a number is positive , negative, or zero.

import java.util.Scanner;

public class NumberCheck {
    public static void main(String[] args) {
        
        Scanner sc = new Scanner(System.in); 

        System.out.print("Enter a number: ");
        double num = sc.nextDouble();

        if (num > 0) {
            System.out.println("The number is Positive.");
        } else if (num < 0) {
            System.out.println("The number is Negative.");
        } else {
            System.out.println("The number is Zero.");
        }

        sc.close(); 
    }
}
Output :-
Enter a number: 25
The number is Positive.
---------------------------------------------------------------------------------------------------------------
2. create a program that determines if a number is odd or even.
import java.util.Scanner;

public class OddEvenCheck {
    public static void main(String[] args) {
        
        Scanner sc = new Scanner(System.in); 

        System.out.print("Enter a number: ");
        int num = sc.nextInt();


        if (num % 2 == 0) {
            System.out.println("The number is Even.");
        } else {
            System.out.println("The number is Odd.");
        }

        sc.close(); 
    }
}
Enter a number: 10
The number is Even.
---------------------------------------------------------------------------------------------------------------
3. create a program that determines if a given year is a leap year.
import java.util.Scanner;

public class LeapYearCheck {
    public static void main(String[] args) {

        Scanner sc = new Scanner(System.in);

        // Take year input
        System.out.print("Enter a year: ");
        int year = sc.nextInt();

        // Leap year rules:
        // 1. Year divisible by 4 → possible leap year
        // 2. If divisible by 100 → must also be divisible by 400
        if ((year % 4 == 0 && year % 100 != 0) || (year % 400 == 0)) {
            System.out.println(year + " is a Leap Year.");
        } else {
            System.out.println(year + " is NOT a Leap Year.");
        }

        sc.close(); // Close scanner
    }
}
---------------------------------------------------------------------------------------------------------------
4. create a program that calculate grades based on marks. A--> above 90%  B--> above 75%  C --> above 60%   
D --> above 30%  F --> Below 30%
import java.util.Scanner;

public class GradeCalculator {
    public static void main(String[] args) {

        Scanner sc = new Scanner(System.in); 

        System.out.print("Enter your marks (0-100): ");
        int marks = sc.nextInt();

        if (marks > 90) {
            System.out.println("Grade: A");
        } else if (marks > 75) {
            System.out.println("Grade: B");
        } else if (marks > 60) {
            System.out.println("Grade: C");
        } else if (marks > 30) {
            System.out.println("Grade: D");
        } else {
            System.out.println("Grade: F");
        }

        sc.close(); 
    }
}
Output :-
Enter your marks (0-100): 95
Grade: A
---------------------------------------------------------------------------------------------------------------
5. Create a program that categorize a person into diffrent age groups.

Child --> below 13    Teen --> below 20    Adult --> below 60   Senior --> above 60
import java.util.Scanner;

public class AgeGroupCategorizer {
    public static void main(String[] args) {
        
        Scanner sc = new Scanner(System.in); 

        System.out.print("Enter your age: ");
        int age = sc.nextInt();

        if (age < 13) {
            System.out.println("Category: Child");
        } else if (age < 20) {
            System.out.println("Category: Teen");
        } else if (age < 60) {
            System.out.println("Category: Adult");
        } else {
            System.out.println("Category: Senior");
        }

        sc.close(); 
    }
}
---------------------------------------------------------------------------------------------------------------
<!-- Bitwise Operator -->
-> Bitwise operators work on the binary representation (bits) of numbers.
Operators :-
1. AND Operators (&) - Each bit of output is 1 if the corresponding bits of both operands are 1, otherwise 0.
2. OR Operators (|) - Each bit of output is 0 if the corresponding bits of both operands are 0, otherwise 1.
3. XOR Operators (^) - Each bit of output is 1 if the corresponding bits of operands are diffrent.
4. NOT Operators (~) - Performs Bitwise complement.
5. Left Shift Operator (<<) :- shift the left operand bits to left.
6. Right Shift Operator (>>) :- shift the left operand bits to Right.

<!-- Example --> Create a program that shows bitwise AND , OR, XOR, NOT, Left Shift, Right Shift.

public class BitwiseExample {
    public static void main(String[] args) {
        int a = 5; // Binary: 0101
        int b = 3; // Binary: 0011

        System.out.println("a & b  = " + (a & b)); // AND  // 0101 & 0011 = 0001 (1)
        System.out.println("a | b  = " + (a | b)); // OR   // 0101 | 0011 = 0111 (7)
        System.out.println("a ^ b  = " + (a ^ b)); // XOR  // 0101 ^ 0011 = 0110 (6)
        System.out.println("~a     = " + (~a));    // NOT  // ~0101 = 1010 (two's complement)
        System.out.println("a << 1 = " + (a << 1));// Left Shift  // 0101 << 1 = 1010 (10)
        System.out.println("a >> 1 = " + (a >> 1));// Right Shift // 0101 >> 1 = 0010 (2)
    }
}
Output :-
a & b  = 1      // 0101 & 0011 = 0001
a | b  = 7      // 0101 | 0011 = 0111
a ^ b  = 6      // 0101 ^ 0011 = 0110
~a     = -6     // ~0101 = 1010 (two's complement)
a << 1 = 10     // 0101 << 1 = 1010
a >> 1 = 2      // 0101 >> 1 = 0010
--------------------------------------------------------------------------------------------------------------
<!-- Example :- -->
4 & 1 → 100 & 001 → 000 → Even

7 & 1 → 111 & 001 → 001 → Odd

1. Write a program to check given number is even or odd using bitwise operator.

import java.util.Scanner;
public class EvenOddBitwise {
    public static void main(String[] args) {
        Scanner sc = new Scanner(System.in);

        // Taking input from the user
        System.out.print("Enter a number: ");
        int num = sc.nextInt();

        // Using bitwise AND to check even or odd
        if ((num & 1) == 0) {
            System.out.println(num + " is Even.");
        } else {
            System.out.println(num + " is Odd.");
        }

        sc.close();
    }
}
Output :-
Enter a number: 8
8 is Even.
---------------------------------------------------------------------------------------------------------------
<!-- Java Comments -->
It is used to add notes in java code

Syntax :-
1. Single Line :- //
2. Multi  Line :- /*  */
3. Java Docs :- /***/

<!-- Example :- -->
public class CommentExample {
    public static void main(String[] args) {
        
        // This is a single-line comment
        int a = 10; // You can also write it beside code

        /* This is a 
           multi-line comment
           explaining multiple steps */
        int b = 20;

        /**
         * This is a JavaDoc comment
         * It is used for generating official documentation
         */
        int sum = a + b;

        System.out.println("Sum: " + sum);
    }
}
---------------------------------------------------------------------------------------------------------------
<!-- Loop In Java -->
--> A loop is a programming structure that allows you to repeat a block of code multiple times until a certain condition is met.
--> They make programs shorter and easier to maintain.
--> Type of Loops are :- while, for , do-while.
                                        <!-- While Loop -->
–-> It Used when the number of iterations is unknown,and we check the condition before running the code
<!-- Example :- -->
public class WhileExample {
    public static void main(String[] args) {
        int i = 1; // Initial value
        while (i <= 5) { // Condition
            System.out.println("Number: " + i);
            i++; // Increment
        }
    }
}
<!-- Output :- -->
Number: 1
Number: 2
Number: 3
Number: 4
Number: 5
                                          <!-- do-While Loop -->
--> The do-while loop is used to execute a block of code at least once, and then repeatedly execute the block as long as the specified condition is true.

<!-- Example :- -->
import java.util.Scanner;
public class DoWhileInputExample {
    public static void main(String[] args) {
        Scanner scanner = new Scanner(System.in);
        int number;

        do {
            System.out.print("Enter a number (0 to exit): ");
            number = scanner.nextInt();
            System.out.println("You entered: " + number);
        } while (number != 0);

        System.out.println("Loop ended because you entered 0.");
        scanner.close();
    }
}

<!-- Output :- -->
Enter a number (0 to exit): 5
You entered: 5
Enter a number (0 to exit): 3
You entered: 3
Enter a number (0 to exit): 8
You entered: 8
Enter a number (0 to exit): 0
You entered: 0
Loop ended because you entered 0.

                                          <!-- For Loop -->
-->The for loop is used to run a block of code a specific number of times.
<!-- Syntax :- -->
for (initialization; condition; update) {
    // Code to execute repeatedly
}
<!-- Example :- -->
public class PivotPrint {
    public static void main(String[] args) {
        int start = 1;
        int end = 9;
        int pivot = 5;

        // Print from pivot down to start
        for (int i = pivot; i >= start; i--) {
            System.out.print(i);
        }

        // Print from pivot+1 to end
        for (int i = pivot + 1; i <= end; i++) {
            System.out.print(i);
        }
    }
}
Output :- 543216789
---------------------------------------------------------------------------------------------------------------
<!-- Functions in Java -->
--> A function is a block of code that performs a specific task.
--> In Java, functions cannot exist outside of a class; they must be inside a class.
--> A function that is declared as static can be called using the class name without creating an object.

<!-- Syntax :- -->
modifier static returnType functionName(parameter1Type parameter1Name, parameter2Type parameter2Name, ...) 
{
    // Body of the function
    // Statements to perform the task
    return value; // if returnType is not void
}

modifier → Access level of the function (public, private, protected, or default).

static → Makes the function belong to the class (can be called without creating an object).

returnType → The type of value the function will return (int, double, String, or void if nothing is returned).

functionName → Name of the function (should follow Java naming rules).

parameters → Input values the function accepts (optional; can be zero or more).

body → The code block inside { } that performs the task.

<!-- Example 1 :- -->
import java.util.Scanner; 
public class Demo {
    // Function to check if a number is positive, negative, or zero
    public static void checkNumber(int num) {
        if (num > 0) {
            System.out.println(num + " is Positive");
        } else if (num < 0) {
            System.out.println(num + " is Negative");
        } else {
            System.out.println("Number is Zero");
        }
    }

    public static void main(String[] args) {
        Scanner sc = new Scanner(System.in); 

        System.out.print("Enter a number: ");
        int number = sc.nextInt(); 

        checkNumber(number); 

        sc.close(); 
    }
}
<!-- Output :- -->
Enter a number: 5
5 is Positive


<!-- Example 2 :- -->
import java.util.Scanner;
public class PatternProgram {
    public static void printFirstPattern() {
    int rows = 0;  // Start with row 0

    while (rows < 5) {  // Outer loop for number of rows
        System.out.print("*");  // Print first star for the row

        int i = 0;  // Inner loop counter
        while (i < rows) {  // Inner loop for extra stars
            System.out.print(" *"); // Space + star
            i++;
        }

        System.out.println(); // Move to the next line
        rows++; // Increase row count
    }
}

    public static void main(String[] args) { 
        printFirstPattern();
    }
}
<!-- Output :- -->
*
* *
* * *
* * * *
* * * * *
---------------------------------------------------------------------------------------------------------------
<!-- Return Statement -->
--> The return statement is used to exit from a method and optionally send a value back to the method caller.

<!-- Example -->
public class Numbers{
public static void main(String[]args){
    int first = readNumber();
    int second = readNumber();
    int sum = first + second;
    System.out.println("Sum of the number is: " +sum);
}
public static int readNumber(){
    Scanner input = new Scanner(System.in);
    System.out.println("Please enter number");
    int number = input.nextInt();
    return number;
}
}
Output :-
Please enter number
5
Please enter number
7
Sum of the number is: 12
---------------------------------------------------------------------------------------------------------------
<!-- Argument and Parameters -->
--> A parameter is a variable that is declared in the method definition to receive input values.
--> An argument is the actual value or expression provided to a method when it is called.

<!-- Example :- -->
public class Demo {
    // 'x' and 'y' are parameters
    public static int add(int x, int y) {
        return x + y;
    }

    public static void main(String[] args) {
        int result = add(5, 3);  // 5 and 3 are arguments
        System.out.println(result);  // Output: 8
    }
}
---------------------------------------------------------------------------------------------------------------
<!-- Challenges -->
1. Develop a program that print the multiplication table of given number.

import java.util.Scanner;
public class Multiplication {
    public static void printMultiplication(int num) {
        int i = 1;
        while(i <= 10){
            System.out.println(num + " X " + i + " = " + (num * i));
            i++;
        }
    }
    public static void main(String[] args) {
        Scanner input = new Scanner(System.in);
        System.out.println("Please enter number");
        int num = input.nextInt();
        printMultiplication(num);
        input.close();
    }
}
Output :-
Please enter number
5
5 X 1 = 5
5 X 2 = 10
5 X 3 = 15
5 X 4 = 20
5 X 5 = 25
5 X 6 = 30
5 X 7 = 35
5 X 8 = 40
5 X 9 = 45
5 X 10 = 50
---------------------------------------------------------------------------------------------------------------
2. Create a program to sum all odd numbers from 1 to a specified number N.

import java.util.Scanner;
public class Multiplication {
    public static int oddSum(int num) {
        int sum = 0;
        int i = 1;
        while(i<=num){
            sum = sum + i;
            i += 2;
        }
        return sum;
    }
    public static void main(String[] args) {
        Scanner input = new Scanner(System.in);
        System.out.println("Please enter number : ");
        int num = input.nextInt();
        int sum = oddSum(num);
        System.out.println(" Odd Sum till " + num + " is " + sum);
    }
}
Output :-
Please enter number : 100
Odd Sum till 100 is 2500
---------------------------------------------------------------------------------------------------------------
3. write a function that calculates the factorial of a given number.

import java.util.Scanner;
public class Factorial {
    public static long factorial(int num) {
        if(num < 2){
            return 1;
        }
        long fact = 1;
        int i = 2;
        while (i<=num){
            fact *= i;
            i++;
        }
       return fact;
    }
    public static void main(String[] args) {
        Scanner input = new Scanner(System.in);
        System.out.println("Please enter number : ");
        int num = input.nextInt();
        long fact = factorial(num);
        System.out.println("Factorial is : " +fact);
        
    }
}
Output :-
Please enter number : 4
Factorial is : 24
---------------------------------------------------------------------------------------------------------------
4. create a program that computes the sum of the digits of an integer.

import java.util.Scanner;
public class Sum {
    public static int sumDigit(int num) {
        int sum = 0;
        while (num>0){
            sum += num % 10;
            num /= 10;
        }
        return sum;
    }
    public static void main(String[] args) {
        Scanner input = new Scanner(System.in);
        System.out.println("Please enter number : ");
        int num = input.nextInt();
        int sum = sumDigit(num);
        System.out.println("Sum of digits is : " +sum);
        
    }
}
Output :-
Please enter number : 123456
Sum of digit is : 21
---------------------------------------------------------------------------------------------------------------
5. create a program to find the least common multiple (LCM) of two numbers.

import java.util.Scanner;
public class LCM {
    public static int lcm(int first, int second) {
        int i = 1;
        while(true){
            int factor = first * i;
            if(factor % second == 0){
                return factor;
            }
            i++;
        }
    }

    public static void main(String[] args) {
        Scanner input = new Scanner(System.in);
        System.out.println("Please enter number 1 : ");
        int first = input.nextInt();
        System.out.println("Please enter number 2 : ");
        int second = input.nextInt();
        int lcm = lcm(first, second);
        System.out.println("lcm of the two number is : " +lcm);
        
    }
}
Output :-
Please enter number 1 : 2
Please enter number 2 : 4
lcm of the two number is : 4
---------------------------------------------------------------------------------------------------------------
6. create a program to find the Greatest common divisor (GCD) of two numbers.

import java.util.Scanner;
public class GCD {
    public static int gcd(int num1, int num2) {
        int gcd = 1;
        int i = 2;
        int least = least(num1, num2);
        while (i <= least) {
            if (num1 % i == 0 && num2 % i == 0) {
                gcd = i;
            }
            i++;
        }
        return gcd;
    }

    public static int least(int num1, int num2) {
        if (num1 < num2) {
            return num1;
        } else {
            return num2;
        }
    }

    public static void main(String[] args) {
        Scanner input = new Scanner(System.in);
        System.out.println("Please enter number 1: ");
        int num1 = input.nextInt();
        System.out.println("Please enter number 2: ");
        int num2 = input.nextInt();
        int gcdValue = gcd(num1, num2);
        System.out.println("GCD of " + num1 + " and " + num2 + " is: " + gcdValue);
    }
}
Output :-
Please enter number 1: 
15
Please enter number 2: 
20
GCD of 15 and 20 is: 5
---------------------------------------------------------------------------------------------------------------
7. Create a program to check whether given number is prime.

import java.util.Scanner;
public class Prime {
    public static boolean isPrime(int num) {
        int i = 2;
        while(i < num){
            if(num % i == 0){
                return false;
            }
            i++;
        }
        return true;
    }


    public static void main(String[] args) {
        Scanner input = new Scanner(System.in);
        System.out.println("Please enter number 1: ");
        int num1 = input.nextInt();
        boolean prime = isPrime(num1);
        if(prime){
            System.out.println("Your number is prime");
        }
        else{
            System.out.println("Your number is not prime");
        }
    }
}
Output :-
Please enter number 1: 23
Your number is prime
---------------------------------------------------------------------------------------------------------------
8. create a program to reverse the digits of a number.

import java.util.Scanner;
public class ReverseTheDigits {
    public static int reverse(int num) {
        int newNum = 0;
        while(num > 0){
            int digit = num % 10;
            newNum = newNum * 10 + digit;
            num /= 10;
        }
        return newNum;
    }


    public static void main(String[] args) {
        Scanner input = new Scanner(System.in);
        System.out.println("Please enter number : ");
        int num = input.nextInt();
        int reverse = reverse(num);
        System.out.println("Reverse of number is : " +reverse);
}
}
Output :-
Please enter number : 249
Reverse of number is : 942
---------------------------------------------------------------------------------------------------------------
9. create a program to print the fibonacci series up to a certain numbers.

import java.util.Scanner;
public class Fibonacci {

    public static void printFibonacci(int num) {
        if (num < 0) return;

        System.out.print("0 ");
        if (num == 0) return;

        System.out.print("1 ");

        int first = 0, second = 1;
        while (first + second <= num) {
            int third = first + second;
            System.out.print(third + " ");
            first = second;
            second = third;
        }
    }

    public static void main(String[] args) {
        Scanner input = new Scanner(System.in);
        System.out.println("Please enter number: ");
        int num = input.nextInt();

        System.out.println("Here is the Fibonacci series:");
        printFibonacci(num);
    }
}

Output :-
Please enter number:  200
Here is the Fibonacci series:
0 1 1 2 3 5 8 13 21 34 55 89 144 
---------------------------------------------------------------------------------------------------------------
10. create a program to check if number is an Armstrong number.

Example :- 153 is an Armstrong number because 1^3+5^3+3^3 = 153

import java.util.Scanner;
public class ArmstrongChecker {

    public static boolean isArmstrong(int num) { 
        int noOfDigits = noDigits(num);
        System.out.println("Number of digits : "+noOfDigits);
        int originalNum = num;
        int finalNumber = 0;

        while (num > 0) {
            int digit = num % 10;
            num /= 10;
            finalNumber += power(digit, noOfDigits);
        }
        System.out.println("Final Number is : "+finalNumber);
        return finalNumber == originalNum;
    }

    public static int power(int base, int exp) {
    int result = 1;
    int i = 0;
    while (i < exp) {
        result *= base;
        i++;
    }
    System.out.println("Power of " + base + " is " +result);
    return result;
}
    public static int noDigits(int num) {
        int digits = 0;
        while (num > 0) {
            digits++;
            num /= 10;
        }
        return digits;
    }

    public static void main(String[] args) {
        Scanner input = new Scanner(System.in);
        System.out.print("Enter a number: ");
        int number = input.nextInt();

        if (isArmstrong(number)) {
            System.out.println(number + " is an Armstrong number.");
        } else {
            System.out.println(number + " is NOT an Armstrong number.");
        }
    }
}
Output :-
Enter a number: 1
1 is an Armstrong number.
---------------------------------------------------------------------------------------------------------------
11. create a program to verify if a number is palindrome.

import java.util.Scanner;
public class Palindrome {
    public static boolean palindrome(int num) { 
        return num == reverse(num);
    }
    public static int reverse(int num) {
        int newNum = 0;
        while(num > 0){
            int digit = num % 10;
            newNum = newNum * 10 + digit;
            num /= 10;
        }
        return newNum;
    }

    public static void main(String[] args) {
        Scanner input = new Scanner(System.in);
        System.out.print("Enter a number: ");
        int number = input.nextInt();
        boolean palindrome = palindrome(number);
        if(palindrome){
            System.out.println("Your number is palindrome number");
        }
        else{
            System.out.println("Your number is not a palindrome number");
        }

    }
}
Output :-
Enter a number: 32123
Your number is palindrome number
---------------------------------------------------------------------------------------------------------------
12. Create a program that print patterns :-

Right Half Pyramid pattern :-
*
*  *
*  *  *
*  *  *  *
*  *  *  *  *
Reverse Right Half Pyramid pattern :-
*  *  *  *  *
*  *  *  *
*  *  *
*  *
*

Left Half Pyramid pattern :-
                *
             *  *
          *  *  *
       *  *  *  *
    *  *  *  *  *

<!-- Solution :- -->

import java.util.Scanner;
public class RightHalfPyramid {

    public static void printRightHalfPyramid(int maxRows) {
        System.out.println("Right Half Pyramid :-");
        int rows = 0;
        while (rows < maxRows) {
            int i = 0;
            while (i < rows) {
                System.out.print("*  ");
                i++;
            }
            System.out.println();
            rows++;
        }
    }

    public static void printReverseRightHalfPyramid(int maxRows) {
        System.out.println("Reverse Right Half Pyramid :-");
        int rows = maxRows;
        while (rows > 0) {
            int i = 0;
            while (i < rows) {
                System.out.print(" *");
                i++;
            }
            System.out.println();
            rows--;
        }
    }

    public static void printLeftHalfPyramid(int maxRows) {
        System.out.println("Left Half Pyramid :-");
        int rows = 1;
        while (rows <= maxRows) {
            // Print spaces
            int spaces = maxRows - rows;
            int j = 0;
            while (j < spaces) {
                System.out.print("  ");  // two spaces for alignment
                j++;
            }

            // Print stars
            int i = 0;
            while (i < rows) {
                System.out.print("* ");
                i++;
            }
            System.out.println();
            rows++;
        }
    }

    public static void main(String[] args) {
        Scanner input = new Scanner(System.in);
        System.out.print("Enter a number of Rows: ");
        int rows = input.nextInt();
        printRightHalfPyramid(rows);
        printReverseRightHalfPyramid(rows);
        printLeftHalfPyramid(rows);
    }
}
---------------------------------------------------------------------------------------------------------------
13. Write a Java program that prints numbers starting from a given pivot number down to a start number, and then continues from one more than the pivot number up to an end number.
For example, if start = 1, pivot = 5, and end = 9, the output should be: 543216789


public class PivotPrint {
    public static void main(String[] args) {
        int start = 1;
        int end = 9;
        int pivot = 5;

        // Print from pivot down to start
        int i = pivot;
        while (i >= start) {
            System.out.print(i);
            i--;
        }

        // Print from pivot+1 to end
        i = pivot + 1;
        while (i <= end) {
            System.out.print(i);
            i++;
        }
    }
}
Output :- 543216789
---------------------------------------------------------------------------------------------------------------
                                        <!-- Array In Java -->
--> An Array is a collection or container that stores multiple values of the same data type in a single variable.
--> Every element has a specific position called an index, which starts from 0.
--> Arrays are useful when you want to store lists of data, like scores, names, or any repeated items.
--> The size of an array is fixed when it is created and cannot be changed later.

<!-- Declaration and Creation :- -->
Syntax :-  dataType[] arrayName = new dataType[size];
Example :- int[] numbers = new int[5];  // Array to hold 5 integers

- dataType is the type of elements the array will hold (e.g., int, String).
- arrayName is the name you give to the array.
- size is the number of elements the array will hold.

<!-- Initializing an Array with Values (Directly) :- -->
Syntax :- dataType[] arrayName = {value1, value2, value3, ...};
Example :- int[] numbers = {10, 20, 30, 40, 50};

<!-- Accessing Array Elements :- -->
Syntax :- arrayName[index]
Example :- int firstNumber = numbers[0];  // Access first element

<!-- Changing Array Elements :- -->
Syntax :- arrayName[index] = newValue;
Example :- numbers[2] = 100;  // Change the third element to 100


<!-- Example :- -->
public class ArrayExample {
    public static void main(String[] args) {
        // 1. Declare and create an array of integers with size 5
        int[] numbers = new int[5];

        // 2. Initialize elements of the array
        numbers[0] = 10;
        numbers[1] = 20;
        numbers[2] = 30;
        numbers[3] = 40;
        numbers[4] = 50;

        // 3. Access and print elements using their indexes
        System.out.println("First element: " + numbers[0]);  // 10
        System.out.println("Third element: " + numbers[2]);  // 30

        // 4. Update an element in the array
        numbers[2] = 100;
        System.out.println("Updated third element: " + numbers[2]);  // 100

        // 5. You can also declare and initialize an array in one step:
        String[] fruits = {"Apple", "Banana", "Cherry"};

        System.out.println("First element: " + fruits[0]);

        // 6. Access value of Array using Loop :-
        int index = 0;
        while(index<5){
            System.out.println("Array of " + index + " index : " +numbers[index]);
            index++;

        // 7. Array Traversal in Loop :-
        int index = 0;
        while(index < numbers.length){
            System.out.println("Array of " + index + " index : " +numbers[index]);
            index++;

            }
        }
    }
}

Output :-
First element: 10
Third element: 30
Updated third element: 100
First element: Apple
Array of 0 index : 10
Array of 1 index : 20
Array of 2 index : 100
Array of 3 index : 40
Array of 4 index : 50
---------------------------------------------------------------------------------------------------------------
1. Write A program of Array Searching :-

import java.util.Scanner;
public class ArraySearching {
    public static void main(String[] args) {
        Scanner input = new Scanner(System.in);

        // Predefined array of integers
        int[] arr = {3, 6, 8, 87, 65, 4, 68, 23, 9, 98, 34};

        System.out.println("Enter the number you want to search:");
        int num = input.nextInt();

        // Call method to check if number exists in array
        boolean isFound = isFound(arr, num);

        if (isFound) {
            System.out.println("Your number was found in the array.");
        } else {
            System.out.println("Your number was not found in the array.");
        }
    }

    // Method to search for number in array using while loop
    public static boolean isFound(int[] arr, int num) {
        int index = 0;
        while (index < arr.length) {
            if (arr[index] == num) {
                return true;  // Found the number, return true
            }
            index++;
        }
        return false;  // Number not found after checking all elements
    }
}

Output :-
Enter the number you want to search : 98

Your number was found in the array.
---------------------------------------------------------------------------------------------------------------
                                            <!-- 2d Array-->
-->  A 2D array is like a table or matrix with rows and columns.

--> <!-- 1. Syntax (Combining Declaration and Creation) :- --> arrayName = new dataType[rows][columns];
--> Example :- int[][] matrix = new int[3][4];  // 3 rows and 4 columns

--> <!-- 2. Initializing a 2D Array with Values :-  -->
int[][] matrix = {
    {1, 2, 3, 4},
    {5, 6, 7, 8},
    {9, 10, 11, 12}
};

<!-- Example :- -->

<!-- 1. Declaration and Creation Array Example 1 :- -->
public class TwoDArrayWhile {
    public static void main(String[] args) {
        // Declare and create 2D array
        int[][] matrix = new int[3][4];

        // Assign some values
        matrix[0][0] = 10;
        matrix[0][1] = 20;
        matrix[1][0] = 30;
        matrix[2][3] = 40;

        // Print using while loops
        int i = 0;
        while (i < matrix.length) {
            int j = 0;
            while (j < matrix[i].length) {
                System.out.print(matrix[i][j] + " ");
                j++;
            }
            System.out.println();
            i++;
        }
    }
}

Output :-
10  20  0   0 
30  0   0   0 
0   0   0   40 


 <!-- 2. Creating, Initializing, and Printing a 2D Array Example 2 :- -->
public class TwoDArrayExample {
    public static void main(String[] args) {
        // Declare and initialize 2D array
        int[][] matrix = {
            {1, 2, 3},
            {4, 5, 6},
            {7, 8, 9}
        };

        int i = 0;  // row index
        while (i < matrix.length) {
            int j = 0;  // column index
            while (j < matrix[i].length) {
                System.out.print(matrix[i][j] + " ");
                j++;
            }
            System.out.println();  // move to next line after each row
            i++;
        }
    }
}
Output :-
1 2 3 
4 5 6 
7 8 9 
---------------------------------------------------------------------------------------------------------------
<!-- Challenges -->
1. Create a program to find the sum and average of all elements in an array.


2. create a program to find number of occurrences of an element in an array.


3. create a program to find the maximum and minimum element in an array.


4. create a program to check if the given array is sorted.


5. create a program to return a new array deleting specific element.


6. create a program to reverse array.


7. create a program to check is the array is palindrome or not.


8. create a program to merge two sorted array.


9. create a program to search an element in 2D-array.


10. create a program to sum and average of all element in a 2D-array.


11. create a program to find the sum of two diagonal elements.