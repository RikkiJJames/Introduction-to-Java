# Introduction-to-Java
An introductory guide into Python

 ## Contents

 * [Section 1 - Java Programme Structure](#section-1---java-programme-structure)
   * [The Programme Container](#the-programme-container)
   * [The Main Method](#the-main-method)
 * [Section 2 - Variables](#section-2---variables)
   * [Data Types](#data-types)
   * [The Main Method](#the-main-method)
 * [Section 3 - Operators](#section-3---operators)
   * [Arithmetic Operators](#arithmetic-operators)
   * [Assignment Operators](#assignment-operators)
   * [Comparison Operators](#comparison-operators)
   * [Logical Operators](#logical-operators)
   * [Conditional Operator](#conditional-operator)
 * [Section 4 - Conditional Statements](#section-4---conditional-statements)
   * [if Statements](#if-statements) 
   * [else Statements](#else-statements)
   * [else if Statements](#else-if-statements)
   * [switch Statements](#switch-statements)


 
 ## Section 1 - Java Programme Structure
 
 ### The Programme Container 
 
 
All Java files are compiled into class files so that they can be run. The programme name is declared following the class keyword and all of the code that defines the class is contained within curly braces. 
The class names should always begin with an uppercase letter as shown below:
 
  ```java
 class Hello 
 {
 
 }
 ```
 
 ### The Main Method
 
 Within the curly the main method should be defined. This is the starting point for all Java programmes. The keywords will be defined later in the guide. But the method is defined below:
 
   ```java
 class Hello 
 {
  public static void main (String [] args){    }
 }
 ```
 
 To print out a text output, the "System.out.println()" function is used:
 
```java
 class Hello 
 {
  public static void main (String [] args){ 
  System.out.println("Hello World")
  }
 }
 ```
 
  ## Section 2 - Variables
  
  A variable is a container that stores a value. Variables are created by specifying the type of data being stored and then a name for that variable.
  
  ### Data Types
  
 | Data Type | Description | Example |
 |    :-:    |     :-:     |   :-:   |
 |    char   | A single Unicode character. Written between single quotes | 'a' or '/u002B' |
 |   String  | Any number of Unicode characters | "My String" |
 |    byte   | Integer number ranging from -128 to 127  | 12 |
 |   short   | Integer number ranging from -32,768 to 32,767  | 2000 or 2_000 |
 |    int    | An integer number, ranging from -2.14 billion to 2.14 billion | 20000 or 20_000 |
 |   long    | An integer number, exceeding +/- 2.14 billion | 20000 or 20_000 |
 |   float   | A floating-point number, with a decimal point. Must have an 'f' suffix to ensure it's treated as a float| 3.141f |
 |   double  | Extremely long floating point number. Should have 'd' suffix to ensure readability| 3.14159265d |
 |  boolean  | A logical value if either true or false | true or false |
 
 ### Defining Variables
 
 Variables can be defined as shown below:
 
 ```java
 class Main 
 {
  public static void main (String [] args){ 
  
  // Underscores can be used for large numbers for increased readability
  int myValue = 10_000
  System.out.println(myValue)
  // Prints 10000
  }
 }
 ```
 
 ### Casting Variables
 
 To convert the result of an expression from one variable type to another, it must be cast. This is done by putting the data type you wish to cast to in brackets beside the expression.
 
  ```java
 class Main 
 {
    public static void main (String [] args){ 


    byte myMinByteValue = Byte.MIN_VALUE;
    /*
    Expression below defaults to an int. Must be cast to byte to work correctly.
    byte myNewByteValue = (myMinByteValue / 2); Required Type byte, provided int.
    */
    byte myNewByteValue = (byte) (myMinByteValue / 2); 
    System.out.println(myNewByteValue)
    // Prints -64
    }
 }
 ```
 
 Examples on the mentioned data types can be found below:
 * [Bytes, Shorts, Ints & Longs](Variables/ByteShortIntLong)
 * [Char & Booleans](Variables/CharAndBoolean)
 * [Float & Double](Variables/FloatAndDouble)
 * [String](Variables/String)
 
 ## Section 3 - Operators
 
 
  Operators are used to perform operations on variables and their are four types:
 * Arithmetic
 * Assignment
 * Comparison
 * Logical 

 #### Arithmetic Operators
 
 Used to create expressions in Java programmes and perform common mathematical operations

 |Operator|Name| Description|
 | :-:|:-:|:-:|
 |+| Addition| Adds two values. Also used to concatenate String values|
 |-| Subtraction| Subtracts two values|
 |* | Multiplication| Multiplies two values|
 |/| Division | Divides one value by another|
 |%| Modulus | Returns the remainder of a division operation| 
 |++| Increment| Increases the value of a variable by 1|
 |--| Decrement|Decreases the value of a variable by 1|
 
 ### Assignment Operators
 
 Used to assign the result of an expression. There are also shorthand versions of longer equivalent expressions:
 
 |Operator|Example| Equivalent |
 | :-:|:-:|:-:|
 |=| a = b| a = b|
 |+=| a += b| a = a + b |
 |-= | a -= b| a = a - b|
 | *= | a *= b | a = a * b|
 | /= | a /= b | a = a / b| 
 | %= | a %= b| a = a % b|

 ### Comparison Operators
 
 Comparisson operators are used to compare two values in an expression and return a boolean value of true or false.
 
 |Operator|Comparison|
 | :-:|:-:|
 |== | Equality|
 | != | Inequality |
 |>| Greater than|
 | >=| Greater than, or equal to | 
 | < | Less than | 
 | <= | Less than, or equal to|
 
 ### Logical Operators

Logical operators are used to combine multiple expressions that each return a boolean value, into a complex expression that returns a single boolean value.

 |Operator|Operation|
 | :-:|:-:|
 | && | Logical AND|
 | || | Logical OR |
 |!| Logical NOT|

### Conditional Operator

The Tenary Operator evaluates an expression for a true or false value and returns one of the given operands depending on the result. It's syntax looks like this:

( boolean-expression ) ? if-true-return-this : if-false-return-this;

An example can be seen below:

 ```java
 class Main 
 {
  public static void main (String [] args){ 
  
 int age = 21;
 
 boolean isAdult = (age > 18) ? true : false;
 // isAdult resolves to true
  }
 }
 ```

## Section 4 - Conditional Statements

### if Statements 

The 'if' statement performs a conditional test to evaluate an expression for a boolean value. The statements following the expression will only be executed when the expression is true. The if statement syntax cam be seen below:

if (test-expression) code-to-be-executed-when-true:

An Example can be seen below:

 ```java
 class Main 
 {
  public static void main (String [] args){ 
  
    if (2 > 1){
       System.out.println("Five is greater than one")
    }
  }
 }
 ```
 
### else Statements

The 'else' statement is used in conjunction with the "if" keyword to create "if else" statements. This creates alternative branches for a program to pusue according to the evaluation of the tested expression. This enables an alternative statement to be executed when the first statement fails:

```java
 class Main 
 {
  public static void main (String [] args){ 
  
    int hours = 11;

    if (hours <= 12){
     System.print.ln("It is morning") 
    }
    else {
     System.print.ln("It is no longer morning") 
    }
  }
 }

```

### else if Statements

Else If Statements
The 'else if' operator used to specify a new condition to test, if the first condition is false.

 
 ```java
 class Main 
 {
  public static void main (String [] args){ 
  
    int hours = 11;

    if (hours <= 12){
     System.print.ln("Good morning") 
    } else if (hours < 18){
     System.print.ln("Good afternoon") 
    } else {
      System.print.ln("Good evening") 
    }
   }
 }

```

### switch Statements

A 'switch' statement is used to specify many alternative blocks of code to be executed. It evaluates a statement once and compares the output of the expression against each 'case'. If the output matches a case then its corresponding code block will be run. An example can be seen below:

```java
 class Main 
 {
  public static void main (String [] args){ 
  
    int day = 2;
        switch (day) {
            case 1:
                System.out.println("Monday");
                break; // used to signify end of case
            case 2:
                System.out.println("Tuesday"); // print Tuesday as the day number is 2
                break;
            case 3:
                System.out.println("Wednesday");
                break;
            case 4:
                System.out.println("Thursday");
                break;
            case 5:
                System.out.println("Friday");
                break;
            case 6:
                System.out.println("Saturday");
                break;
            case 7:
                System.out.println("Sunday");
                break;
            default: // triggers when the input doesn't match any case
                System.out.println("Sorry that's not a valid input");
        }
    }
}
        
```

A more detailed example on operators & conditional statements can be found [here](ConditionalStatements/IfThenStatements)

