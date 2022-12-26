# Introduction-to-Java
An introductory guide into Python

 ## Contents

 * [Section 1 - Java Programme Structure](#section-1---java-programme-structure)
   * [The Programme Container](#the-programme-container)
   * [The Main Method](#the-main-method)
   * [Comments](#comments)
     * [Single Line Comments](#single-line-comments) 
     * [Multiple Line Comments](#multiple-line-comments) 
 * [Section 2 - Variables](#section-2---variables)
   * [Data Types](#data-types)
   * [Defining Variables](#defining-variables)
   * [Defining Constants](#defining-constants)
   * [The Main Method](#the-main-method)
 * [Section 3 - Operators](#section-3---operators)
   * [Arithmetic Operators](#arithmetic-operators)
   * [Assignment Operators](#assignment-operators)
   * [Comparison Operators](#comparison-operators)
   * [Logical Operators](#logical-operators)
   * [Conditional Operator](#conditional-operator)
 * [Section 4 - Control Flow](#section-4---control-flow)
   * [Conditional Statements](#conditional-statements)
     * [if Statements](#if-statements) 
     * [else Statements](#else-statements)
     * [else if Statements](#else-if-statements)
     * [switch Statements](#switch-statements)
   * [Loops](#loops)
     * [for Loops](#for-loops)
     * [while Loops](#while-loops)
     * [do while Loops](#do-while-loops)
     * [Breaking Out of Loops](#breaking-out-of-loops)
       * [break](#break)
       * [continue](#continue)
 * [Section 5 - Methods](#section-5---methods)
   * [Returning Parameters](#returning-parameters)
   * [Overloading Methods](#overloading-methods)
 * [Section 6 - Classes](#section-6---classes)


 
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
 
 ### Comments
 
 When programming in any language it is good practice to add comments to explain each section. This makes the code more easily underrstood by other and yourself when revisiting code.
 
 #### Single Line Comments
 
Single Line comments can be added using the following syntax.

```java
 class Main 
 {
  public static void main (String [] args){ 
  // This is a comment
  }
 }
 ```
 
 
 #### Multiple Line Comments
 
 Single Line comments can be added using the following syntax.
 
 ```java
 class Main 
 {
  public static void main (String [] args){ 
  /* This is a 
  Multi Line
  Comment
  */
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
 
 ### Defining Constants
 
 The "final" keyword is a modifier that can be used to prevent any changes to the values initially assigned to them. This is useful when storing a fixed value in a program to avoid it being accidentally altered.
 The convention is to name constants in all uppercase characters to distinguish them from regular variables. See below:
 
  ```java
 class Main 
 {
  public static void main (String [] args){ 
  
  final double PI = 3.14159265359d;
  final double EULER = 2.71828;
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

## Section 4 - Control Flow

### Conditional Statements

#### if Statements 

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
 
#### else Statements

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

#### else if Statements

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

#### switch Statements

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

### Loops

A loop is a block of code that repeatedly executes the statement it contains until a tested condition is met.
#### for Loops

The most frequently used loop structure is the "for" loop which has the syntax below:

for ( initialiser; test-expression; updater )
{
  statements-to-be-executed-on-each-iteration;
}

The for loop must contain three parameters to control the loop

* Initialiser - assigns an initial value to a counter variable, which will track the number of iterations.
* Test expression - evaluated at the start of each iteration. When the evaluation returns true, the iteration proceeds. Else the loop is terminated
* Updater - changes the current value of the counter variable, started by the initialiser. Typically this will use i++ fir counting upm or i-- for counting down.

```java
 class Main 
 {
  public static void main (String [] args){ 
  
    for (int i = 1; i < 11; i++){
        System.out.println(i);
    }
    // Prints out 1 - 10
  }
 }
```

#### while Loops

An alternative to the for loop is the "while" loop, which has the syntax below:

while( test-expression )
{
    statements-to-be-executed-on-each-iteration;
}

Unlike the "for" loop the while loop does not contain an initialiser or updater. This means the test expression must evaluate a value that gets changed in the loop statements as the loop proceeds. Otherwise an infinite loop will be created. See below:

```java
public class Main {
    public static void main(String[] args) {

        int i = 1;
        while(i < 11){
            System.out.println(i);
            i++;
        }
    }
}
```

#### do while Loops

A variation of the "while" loop is the "do while" loop. This is created with the following syntax:

do 
{
    statements-to-be-executed-on-each-iteration;
} 
while (test-expression);

Like the "for" and "while" loops, a "do while" loop repeatedly executes the statemetns until the test-expression returns false. However, unlike the "while" loop. The test statement is only evaluatied at the end of each iteration. Therefore the loop is always executed at least once.

```java
public class Main {
    public static void main(String[] args) {

        int count = 1;
        do {
            System.out.println("Value is :" + count);
            count++;
        } while (count < 11);
        // Prints out 1 - 10. Always prints out initial value.
    }
}
```

#### Breaking Out of Loops

##### break
The "break" keyword can be used to prematurely terminate a loop once a specified condition is met. When a loop in a nested loop is broken out of it proceeds to the next iteration of its outer loop.

```java
public class Main {
    public static void main(String[] args) {
        int count = 0;

        while (count < 10){
            System.out.println(count);
            count++;
            if (count == 4){
                System.out.println("Breaking out of loop");
                break;
            }
        }
    }
}
```

##### continue

The "continue" keyword can be used to skip a single iteration of a loop when a specified condition is met.

```java
public class Main {
    public static void main(String[] args) {

        int count = 0;

        while (count < 11){
            count++;
            if (count % 2 != 0) {
                continue;
            }
            System.out.println(count);
            // Prints even numbers
        }
    }
}

```

## Section 5 - Methods

Programmes are typically split into seperate methods to create modules of code that each perform set tasks and can be called repeatedly throughout the programme as required.

After  the main method, more methods can be declared inside the curly brackets that define the class definition. Each new method must be given a new name. The syntax is shown below:

public static void secondMethod ( method-arguments ){ code-to-be-executed }

### Returning Parameters

When defining a method you may wish for it to return a value. This can be done with the third keyword in the method declaration. "void" means the function does not return anything. However this can be substituted with any data type. For instance the method "calculateScore" below returns an integer.

```java
public class Main {
    public static void main(String[] args) {

        boolean gameOver = true;
        int score = 10, levelCompleted = 2, bonus = 100;

        int highScore = calculateScore(gameOver, score, levelCompleted, bonus);

    }

    public static int calculateScore(boolean gameOver, int score, int levelCompleted, int bonus){

        if (gameOver){
            int finalScore = score +(levelCompleted * bonus);
            return finalScore;
        }

        return -1;
    }


```
### Overloading Methods

A class may contain multiple methods of the same name provided they have different a different number of arguments, or arguments of different data types. This is known as overloading. An example can be seen below:

```java
public class Main {
    public static void main(String[] args) {
        print(7);
        print(7, 3);
        print("Hello World");
    }

    public static void print(int value){
        System.out.println("Printing..." + value);
    }

    public static void print(int value1, int value2){
        System.out.println("Printing..." + value1 + " " + value2);
    }
    public static void print(String value){
        System.out.println("Printing..." + value);
    }
}
```

## Section 6 - Classes

Java uses OOP (Onject Orientated Programming) which is a technique to model objects that contain both data and code. The building block of Java that leads to Object-Oriented programming is a 'class' which describes the data (fields) and behaviour (methods) that are relevant to the object being described. Class members can be a field, method or any dependent element. If a field is static, there is only one copy in memory, and this value is associated with the class itself. If a field is not static, it is an instance field, and each object may have a different value stored for this field. A class is like a blueprint for an object and when an object is created, it inherits all the variables and functions from the class.

For example: in real life, a car is an object. The car has attributes, such as weight and color, and methods, such as drive and brake.

A class member. OOP has several advantages over procedural programming:

* OOP is faster and easier to execute
* OOP provides a clear structure for the programs
* OOP helps to prevent code repition and makes the code easier to maintain, modify and debug
* OOP makes it possible to create full reusable applications with less code and shorter development time

### Creating Classes

To create a class in Java, The syntax is to use the 'class' keyword with the class name having a capital letter, as shown below:

```java
public class Car {
}

```

### Packages

Classes can be organised into logical groupings called packages. You declare a package name in the class using the package statements. If no package is declared, the class implicitly belongs to the default package.

### Access Modifiers

There are many access modifiers that control where the class can be accessed from

 | Access Keyword | Description |
 |    :-:    |     :-:     |
 |       | When no modifier is specified, package access is granted and the class is accessible to classes in the same package |
 |    public   | any other class in any package can access this class |
 |  private  | No other class can access this member |
 

### Encapsulation

Encapsulation in OOP has two meanings. One is bundling behaviour and attributes into a single object. The other is the practice of hiding fields and methods from public access. Usually the meaning is the latter.


### Constructors

### Setters & Getters

