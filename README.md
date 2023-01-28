# Introduction-to-Java
An introductory guide into Java

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
 * [Section 6 - Strings](#section-6---strings)
   * [String Manipulation](string-manipulation)
     * [Print Formatting](#print-formatting)
       * [Format Specifiers](#format-specifiers) 
         * [Precision](#precision)  
         * [Width](#width)  
       * [String Formatting](#string-formatting)
      * [Text Blocks](#text-blocks)
 * [Section 7 - OOP](#section-7---oop)
   * [Creating Classes](#creating-classes)
   * [Packages](#packages)
   * [Encapsulation](#encapsulation)
     * [Access Modifiers](#access-modifiers)
   * [Class Fields](#class-fields)
     * [Default Values](#default-values)
   * [Class Methods](#class-methods)
     * [Setters & Getters](#setters--getters)
       * [this Keyword](#this-keyword)
     * [Constructors](#constructors)
       * [Constructor Overloading](#constructor-overloading)
       * [Constructor Chaining](#constructor-chaining)
   * [Static vs Instance](#static-vs-instance)
     * [Static variables](#static-variables)
     * [Static Methods](#static-methods)
     * [Instance variables](#instance-variables)
     * [Instance Methods](#instance-methods)
   * [Inheritance](#inheritance)
  * [Section 8 - Arrays](#section-8---arrays)


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
## Section 6 - Strings


Strings are objects that have over 60 methods available. The string is a sequence of characters, meaning its characters are ordered and indexed. The index starts at zero. The table below shows the indices above each character for the String "Hello World"

 | Index | 0 | 1 |  2 | 3 |  4 | 5 |  6 | 7 |  8 | 9 |  10 |
 |    :-:    |     :-:     |      :-:  |    :-:    |     :-:     |      :-:     |    :-:    |     :-:     |      :-:     | :-:     | :-:     | :-:     | 
 |    Character  | H | e |  l | l |  o |  |  W | o |  r | l |  d |
 
Characters can be identified through there position. "H" is at index 0 and "W" is at index 6. The length of the string is 11, but its last index is 10.

String methods can be split into three categories:

* String inspection methods - Provide info on Strings such as length & isEmpty
* Method for comparing string values - Usually return a boolean values e.g. false if string are not equal
* String Manipulation Methods - Transform one string value into another

### String Inspection Methods

| Method | Description |
|    :-:    |     :-:     |
|    length  | Returns the number of characters in the String|
|    charAt  | Returns the character at the index passed as an argument|
|    indexOf/lastIndexOf  | Returns an integer, representing the index in the sequence where the String of character passed can be located in the String|
|    isEmpty  | Returns true if the length is zero|
|    isBlank  | Returns true length is zero OR the string only contains whitespace characters (added in JDK 11)|

Examples can be seen below:

```java
public class Main {
    public static void main(String[] args) {
        printInformation("Hello World");
        printInformation("");
        printInformation("\t \n");

        String helloWorld = "Hello World";
        System.out.printf("Index of r = %d %n", helloWorld.indexOf("r")); // prints 8
        System.out.printf("Index of World = %d %n", helloWorld.indexOf("World")); // prints 6

        System.out.printf("Index of l = %d %n", helloWorld.indexOf("l")); // prints 2
        System.out.printf("Index of l = %d %n", helloWorld.lastIndexOf("l")); // prints 9

        // Find second l

        System.out.printf("Index of l = %d %n", helloWorld.indexOf("l",3)); // prints 3
        System.out.printf("Index of l = %d %n", helloWorld.lastIndexOf("l",8)); // prints 3
    }

    public static void printInformation(String string) {
        int length = string.length();
        System.out.printf("Length = %d %n", length); // Prints length of String

        if (string.isEmpty()) {
            System.out.println("String is Empty"); //returns if length is zero and no blank space
            return;
        }

        if (string.isBlank()){
            System.out.println("String is Blank"); // returns if length is zero with blank space
            return;
        }

        System.out.printf("First char = %c %n", string.charAt(0)); //%c character format specifier, prints first character

        System.out.printf("Last char = %c %n", string.charAt(length - 1)); // prints last character
    }
}

```


### String Comparison Methods

| Method | Description |
|    :-:    |     :-:     |
|    contentEquals  | Returns a boolean if the String's value is equal to the value of the argument passed. This method allows for arguments other than String, for any type that is a character sequence.|
|    equals  | Returns a boolean if the String's value is equal to the value of the argument passed|
|    equalsIgnoreCase  | Returns a boolean if the String's value is equal (ignoring case), to the value of the argument passed.|
|    contains  | Returns a boolean if the String contains the argument passed.|
|    endsWith/startsWith  | These return a boolean, and are much like the "contains" method, but more specific to the placement of the String |
|    regionMatches  | Returns a boolean, if defined sub-regions are matched.|


```java
public class Main {
    public static void main(String[] args) {

        String helloWorld = "Hello World";

        String helloWorldLower = helloWorld.toLowerCase(); //hello world

        if (helloWorld.equals(helloWorldLower)) {
            System.out.println("Values match exactly"); // Doesn't match exactly - no output
        }

        if (helloWorld.equalsIgnoreCase(helloWorldLower)) {
            System.out.println("Values match ignoring case"); // Prints value
        }

        if (helloWorld.contentEquals("Hello World")) {
            System.out.println("Values match exactly"); // Prints values match exactly
        }

        if (helloWorld.startsWith("Hello")) {
            System.out.println("String starts with Hello"); // Prints 
        }

        if (helloWorld.endsWith("World")) {
            System.out.println("String ends with World"); // Prints
        }

        if (helloWorld.contains("World")) {
            System.out.println("String contains World"); // Prints
        }

    }
}

```
### String Manipulation

There are two types of String manipulation methods, the first set, don't change the underlying meaning of the text value, but perform some kind of clean up

| Method | Description |
|    :-:    |     :-:     |
|    indent  | This method was added in JDK 15, adds or removes spaces from the beginning of lines in multi-line text|
|    strip/ stripLeading / stripTrailing/ trim  | The difference between the strip and trim method is that strip() supports a larger set of white space characters. It and the corresponding stripLeading and stripTrailing methods were added in JDK 11.|
|    toLowerCase/ toUpperCase   | Returns a new String, either in a lower case or upper case|

The second set transform the String value and return a String with a different meaning:

| Method | Description |
|    :-:    |     :-:     |
|    concat  | Similar to '+' operator for strings, it concatenates text to the String and returns a new String as the result.|
|    join  | Allows multiple strings to be concatenated together in a single method, specifying a delimiter|
|    repeat   | Returns the String repeated by the number of times specified in the argument.|
|    replace/ replaceAll/ replaceFirst   | These methods replace characters or substrings in the String, returning a new String with replacements made.|
|    substring/ subSequence   | These return a part of the String, its range defined by the start and end of the index specified|

```java
public class StringMethods {

    public static void main(String[] args) {
        String birthDate = "12/11/1994";
        int startingIndex = birthDate.indexOf("1994");

        System.out.printf("Starting Index = %d %n", startingIndex); // Prints 6
        System.out.printf("Birth Year = %s %n", birthDate.substring(startingIndex)); // Prints 1994

        System.out.printf("Month = %s %n", birthDate.substring(3,5)); // Prints 11

        String newDate = String.join("/", "25", "7", "1991");
        System.out.printf("New Date = %s %n", newDate); // Prints 25/7/1991

        newDate = "25"; // Can also be done with concat, but is very inefficiently
        newDate = newDate.concat("/");
        newDate = newDate.concat("7");
        newDate = newDate.concat("/");
        newDate = newDate.concat("1991");

        System.out.printf("New Date = %s %n", newDate); // Prints 25/7/1991

        // Concat using method chaining

        newDate = "25".concat("/").concat("7").concat("/").concat("1991");
        System.out.printf("New Date = %s %n", newDate); // Prints 25/7/1991

        System.out.printf("New Date = %s %n",newDate.replace("/", "-")); // replaces '/' with '-'
        System.out.printf("New Date = %s %n",newDate.replace("7", "07")); // replaces '7' with '07'

        System.out.printf("New Date = %s %n",newDate.replaceFirst("/", "-")); // replaces first '/' with '-'
        System.out.printf("New Date = %s %n",newDate.replaceAll("/", "---")); // replaces all '/' with '---'

        System.out.println("ABC\n".repeat(3));
        System.out.println("-".repeat(20));
    }
}
```
### The StringBuilder Class

Java provides a mutable class that lets us change its text value. The most efficient way to create regular string is to assign a literal to a String object.

There are four ways to create a new StringBuilder object, using the new keyword.

* Pass a String
* Pass no arguments
* Pass an integer value
* Pass another type of character sequence (like StringBuilder)

An example can be seen below:

```java
public class Main {
    public static void main(String[] args) {

        String helloWorld = "Hello" + " World";

        // StringBuilder helloWorldBuilder = "Hello" + "World"; Does not compile

        StringBuilder helloWorldBuilder = new StringBuilder("Hello" + " World");

        printInformation(helloWorld); //Prints Hello World
        printInformation(helloWorldBuilder); //Prints Hello World

        helloWorld.concat(" and Goodbye"); // returned value not reassigned to new variable
        helloWorldBuilder.append(" and Goodbye"); // appended value added to original string

        printInformation(helloWorld); //Prints Hello World
        printInformation(helloWorldBuilder); //Prints Hello World and Goodbye
    }

    public static void printInformation(String string) {

        System.out.printf("String = %s %n", string);
        System.out.printf("Length = %d %n", string.length());
    }

    public static void printInformation(StringBuilder builder) {

        System.out.printf("String = %s %n", builder);
        System.out.printf("Length = %d %n", builder.length());
    }
}
```

String methods create a new object in memory and return a reference to this new object. StringBuilder methods return a StringBuilder referenfce, but it's really a self reference.

The StringBuilder calss has many similar methods to Strings. But there are also methods unique to the StringBuilder class:

| Method | Description |
|    :-:    |     :-:     |
|    delete/ deleteCharAt  | Deletes a substring using indices to specify a range, or delete a single character at an index|
|    insert  | Inserts text at a specified position|
|    reverse   | Reverses the order of the characters in the sequence|
|    setLength   | Can be used to truncate the sequence, or include null sequences to "fill out" the sequence to that length|

```java
public class Main {
    public static void main(String[] args) {
    
        StringBuilder builderPlus = new StringBuilder("Hello World");
        builderPlus.append(" and Goodbye");

        builderPlus.deleteCharAt(16). insert(16, "g");
        System.out.println(builderPlus); // Hello World and goodbye

        builderPlus.replace(16,17, "G");
        System.out.println(builderPlus); // Hello World and Goodbye

        builderPlus.reverse().setLength(7);
        System.out.println(builderPlus); // Prints eybdooG
    }

    public static void printInformation(String string) {

        System.out.printf("String = %s %n", string);
        System.out.printf("Length = %d %n", string.length());
    }

    public static void printInformation(StringBuilder builder) {

        System.out.printf("String = %s %n", builder);
        System.out.printf("Length = %d %n", builder.length());
        System.out.printf("Capacity = %d %n", builder.capacity());
    }
}

```

#### Print Formatting

System.out.printf can be used to format the output of the string. The example below uses the format specifier "%d" to insert variables into the printed line. 

```java

public class Main {
    public static void main(String[] args) {
        int age = 35;
        System.out.printf("Your age is %d\n", age);

        int yearOfBirth = 2023 - age;
        System.out.printf("Age = %d, Birth year = %d", age, yearOfBirth);
    }
}
```

##### Format Specifiers

At their most complex, format specifiers take the following form.

%[argument_index$][flags][width][.precision]conversion

They start with a percent sign, end with a conversion symbol, and have lots of options inbetween.

The conversion type "d" is used for decimal integer values. Some common types are shown below

 | Conversion | Argument Category | Description |
 |    :-:    |     :-:     |      :-:     | 
 |    'b', 'B'  | general |If the argument (arg) is null, then the return is false. If arg is a boolean, then the result is the string returned by String.valueOf(arg). Otherwise the result is "true"|
 |   'd', 'D'  | floating point | The result is formatted as a decimal integer (short, int & long) |
 |   'e', 'E'  | floating point | The result is formatted as a decimal number in computerised scientific notation |
 |    'f', 'F'   | floating point | The result is formatted as a decimal number (floating point numbers, floats & doubles)|
 |    'n, 'N'   | line separator | The result is the platform-specific line separator (preferred)|
 |    't', 'T'   | date/time | Prefix for date and time conversion characters|

Using the example above, the "f" type can be used to output floating point numbers. The default precision is 6 d.p.

```java

public class Main {
    public static void main(String[] args) {
        int age = 35;
        System.out.printf("Your age is %f\n", (float) age); // Outputs 35.000000 (default precision)
    }
}
```
###### Precision

However, the precision can be modified by inputing (.precision) inbetween the % and the type as shown below.

```java

public class Main {
    public static void main(String[] args) {
        int age = 35;
        System.out.printf("Your age is %.2f\n", (float) age); // Outputs 35.00 (2 d.p)
    }
}
```

###### Width

The width of the output can be adjusted by inserting the desired width inbewteen the "%" and the type as shown below:

Without Formatting:

```java
public class Main {
    public static void main(String[] args) {

        for (int i = 1; i < 100_000; i *= 10 ) {
            System.out.printf("Printing %d %n", i);
        }
    }
}
```

Output:

Printing 1 
Printing 10 
Printing 100 
Printing 1000 
Printing 10000

With Formatting

```java
public class Main {
    public static void main(String[] args) {

        for (int i = 1; i < 100_000; i *= 10 ) {
            System.out.printf("Printing %6d %n", i); // Width of largest value (1000000) is 6
        }
    }
}
```
Output:

Printing      1 
Printing     10 
Printing    100 
Printing   1000 
Printing  10000 

##### String Formatting

In Java 15 String formatting was added so the string itself can be directly formatted using two different methods as shown below:

```java
public class Main {
    public static void main(String[] args) {
        int age = 35
        String formattedString = String.format("Your age is %d", age);
        System.out.println(formattedString); // Your age is 35
    }
}
```

```java
public class Main {
    public static void main(String[] args) {
        int age = 35
        String formattedString = "Your age is %d".formatted(age)
        System.out.println(formattedString); // Your age is 35
    }
}
```
#### Text Blocks

Some common escape sequences are shown below:

 | Escape Sequence | Description |
 |    :-:    |     :-:     | 
 |    \t   | Insert a tab character|
 |   \n  | Insert a new line character |
 |    \\"   | Insert a double quote character |
 |   \\\   | Insert a backslash character|
 
 Incorporating these characters and formatting with them can look quite complicated:
 
 ```java
 public class Main {
    public static void main(String[] args) {


        String bulleted = "Print a Bulleted List:\n" +
                "\t\u2022 First Point\n" +
                "\t\t\u2022 Second Point\n";


        System.out.println(bulleted);
    }
}

```

Output:

Print a Bulleted List:
  * First Point
    * Second Point
     
However, this can be easily replicated using a text block in Java 15.


```java
public class Main {
    public static void main(String[] args) {

        String textBlock = """
                    Print a Bulleted List:
                        \u2022 First Point
                            \u2022 Second Point""";

        System.out.println(textBlock);
    }
}

```

Print a Bulleted List:
  * First Point
    * Second Point
    
## Section 7 - OOP

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
 

### Encapsulation

Encapsulation in OOP has two meanings. One is bundling behaviour and attributes into a single object. The other is the practice of hiding fields and methods from public access. Usually the meaning is the latter and the method of doing this is using access modifiers.

#### Access Modifiers

There are many access modifiers that control where the class can be accessed from

 | Access Keyword | Description |
 |    :-:    |     :-:     |
 |       | When no modifier is specified, package access is granted and the class is accessible to classes in the same package |
 |    public   | any other class in any package can access this class |
 |  private  | No other class can access this member |

### Class Fields

Class fields are variables that are specific to the class and defined in the code block as opposed to inside a method. When an object is created from the class, the values assigned to these fields represent the state of the object. Unlike local variables, class variables should have some type of access modifier declared for it. If not Java will declare the default (package private) implicitly. Below is an example of a car class with its field all having private access:

```java
public class Car {

    private String make;
    private String model;
    private String colour;
    private int doors;
    private boolean convertible;


}
```

#### Default Values

Class fields can be given default values as shown below:

```java
public class Car {

    private String make = "BMW";
    private String model = "Model 3";
    private String colour = "Grey";
    private int doors = 2;
    private boolean convertible = false;
}
```
This means that every object that gets instantiated will have these as default values.

### Class Methods

Class methods are first defined using the access modifier, return type and user given name. This is then followed by parenthesis in which you'd specify the type and name of any method arguments and then enclose the method code within curly brackets. The method below prints out the details from the car class defined above:

```java
public void describeCar(){
        System.out.println(doors + "-Door " +
                colour + " " +
                make + " " +
                model + " " +
                (convertible ? "Convertable" : " "));

}

```
The access modifier is public, which means it can be called from other classes such as "Main" and the return type is void. Which means it doesn't return anything.


#### Setters & Getters

A setter is a method on a class that sets the value of a private field.
A getter is a method on a class that retrieves the value of a private field.

The purpose of these methods is to control, and protect, access to private fields.

An example to get and set the "make" field of the car class is shown below:

```java
    public String getMake(){
        return make;
    }
    
    public void setMake(String make) {
        this.make = make;
    }
```

Note - In IntelliJ alt+insert can be used to quickly create setters & getters 

Setters also allow validation. The example below only allows 3 OEM's to be accepted in the setMake method, if the argument passed in is anything else. The make is set to "Unsupported"

```java
public void setMake(String make) {

        if (make == null){
            make = "Unknown";
        }
        String lowercaseMake = make.toLowerCase();
        switch (lowercaseMake){
            case "mazda":
            case "mitsubishi":
            case "toyota":
                this.make = make;
                break;
            default:
                this.make = "Unsupported";
        }
    }
```

##### this Keyword

In the earlier example. The "this" keyword was used used in the setter method. The this keyword refers to the instance that was created when the object was instantiated. So "this" is a special reference name for the object or instance, which it can use to describe itself. and it can be used to access fields on the class.

#### Constructors

A class is just a template. To create an object (instance) of a class, you need a constructor. This is a special type of code block that has a specific name and parameters just like a method. It has the same name as the class itself and doesn't return any values. You never include a return value from a constructor, not even void. You can, and should also specify the access modifier, to control who should be able to create new instances of the class.

```java
public class Car{ // Class declaration
    public Car(){ // Constructor declaration
    }
}
```

If no constructor is declared. The Java implicitly creates a constructor. However, if a class contains any other constructor declarations, then a default constructor is NOT implicitly declared.

```java
Car car = new Car(); // Default constructor
car.desribeCar();
```

From here you can call the setters discussed previously to assign the fields of the car class.

```java
public static void main(String[] args) {
        Car firstCar = new Car();
        firstCar.setMake("Mazda");
        firstCar.setModel("3");
        firstCar.setDoors(4);
        firstCar.setColour("Black");
        firstCar.setConvertible(false);
    }
```

Instead of setting all of the fields individually. The constructor can be used to set all the fields by passing them in as arguments to the constructor:

```java
public Car(String make, String model, String colour, int doors, boolean convertible) {
        this.make = make;
        this.model = model;
        this.colour = colour;
        this.doors = doors;
        this.convertible = convertible;
    }

```

##### Constructor Overloading

Constructor overloading is declaring multiple constructors, with differeent formal parameters.
The number of parameters can be different between constructors. Or if the number of parameters is the same between constructors, their types of order of the types much differ.

```java
public Car(String make, String model, String colour, int doors, boolean convertible) {
        this.make = make;
        this.model = model;
        this.colour = colour;
        this.doors = doors;
        this.convertible = convertible;
    }

    public Car(String make, String model, String colour, int doors) { // Overloaded constructor
        this.make = make;
        this.model = model;
        this.colour = colour;
        this.doors = doors;
        this.convertible = false;
    }
```

##### Constructor Chaining

Constructor chaining is when one constructor explictly calls another overloaded constructor. You can only call a constructor from another constructor.
You must use the "this()" keyword to execute another constructor, passing it arguments if required. "this" must be the first executable statement, if it's used from another constructor.

```java
public Car(){
        this("Jaguar","I-Pace","Grey", 4, false);
        System.out.println("Empty constructor called, default values used");
    }

    public Car(String make, String model, String colour, int doors, boolean convertible) {
        this.make = make;
        this.model = model;
        this.colour = colour;
        this.doors = doors;
        this.convertible = convertible;
        System.out.println("Constructor with parameters called");
    }
```

The result of the code above would be:

* Constructor with parameters called
* Empty constructor called, default values used

### Static vs Instance

#### Static Variables

A static variable is declared using the keyword 'static'. Every instance of the class share the same static variable. Therefore - if a change is made to that variable, all other instances of that class will see the effect of the change. It is common practice to use the class name and not a reference variable to access a static variable. This makes it clear that the variable is shared with the class and not stored within the instance.

```java
class Dog {

    static String genus = "Canis";

    void printData() {
        Dog d = new Dog();
        System.out.println(d.genus); // Confusing
        System.out.println(Dog.genus); // Clearer
    }
}
```

Also an instance isn't required to exist to access the value of a static variable.

```java
class Dog {

    static String genus = "Canis";
}

class Main {
    public static void main(String [] args){
    System.out.orintln(Dog.genus); // No instance required to access static variable
    }
}
```

They can be used for:

* Storing counters
* Generating unique ids
* Storing a constant value that doesn't change, like PI for example.
* Creating and controlling access to a shared resource (database/log file)


#### Static Methods

Static methods are declared using the 'static' modifier. Static methods cannot access instance methods and instance variable directly. They're usually used for operations that don't require any data from an instance of the class (from 'this'). 

Therefore inside a static method - you cannot used the 'this' keyword.

Whenever you see a method that doesn;t use instance variables, that method should probably be declared as a static method.
For example, 'main' is a static method, and it's called by the Java virtual matchine when it starts the Java application.

```java

class Calculator {
    public static void printSum (int a, int b) {
        System.out.println("sum = " + (a + b));
    }
}

public class Main {

    public static void main (String [] args) {
        Calculator.printSum(5, 10); // Does not require an instance
        printHello();
    }
    
    public static void printHello(){
        System.out.println("Hello");
    } 
}

```

#### Instance Variables

Instance variables are also known as fields, or member variables and belong to a specific instance of a class.
Each instance has it's own copy of an instance variable that can have a different value.

#### Instance Methods

Instance methods belong to an instance of a class. To use an instance method, an instance must be created from the class, usually by using the new keyword.

Instance methods can access both static/instance variables and static/instance methods directly. 

```java
class Dog {

    public void bark() {
        System.out.println("woof");
    }
}

class Main {
    public static void main(String [] args){
    
    Dog rex = new Dog(); // Create instance
    rex.bark(); // Call instance method
    }
}
```

### Inheritance

Inheritance is a way to reuse code. It is a way to organise classes into a parent-child hierachy, which lets the child inherit, fields and methods from its parent.

The most generic (base class), starts at the top of the hierachy. Every class below it is a subclass. A parent can have multiple children. However, in Java a child can only have one parent. But it will also inherit from it's parent class's parent etc.

Below is an example of an animal class:

```java

public class Animal {

    private String type;
    private String size;
    private double weight;
    
    
    public Animal() {
    
    }
    
    public Animal(String type, String size, double weight) {
        this.type = type;
        this.size = size;
        this.weight = weight;
    }

    @Override
    public String toString() {
        return "Animal{" +
                "type='" + type + '\'' +
                ", size='" + size + '\'' +
                ", weight=" + weight +
                '}';
    }

    public void move(String speed){
        System.out.println(type + " moves " + speed);
    }

    public void makeNoise(){
        System.out.println(type + " makes some kind of noise ");
    }
}
```

#### super Keyword

super() is a lot like this(). It's a way to call a constructor on the super class, directly from the sub classes constructor. Like this(), it has to be the first statement of the constructor. Because of that rule, this() and super() can never be called from the same constructor.
If a explicit call to super() is not made, then Java does it for you using super's default constructor.
If the super class does not have a default constructor, then you must explicitly call super() in all of your constructors, passing the right arguments to that constructor.

#### Sub Classes

A Dog class has been created, as a dog "IS A" animal, it will inherit animal attributes (type, size and weight) as well as the animal methods. The Dog class can also be specialised with its own fields and behaviour. To make one class inherit from another, the "extends" keyword is used. This class calls the default constructor of the animal class and doesn't set values to any field methods. Therefore, type & size will be "null" and weight will be 0.0.


```java
public class Dog extends Animal {
    public Dog(){
        super();
    }
}
```

However, you can pass values into the Dog constructor to instantiate these values. The updated Dog class below now has two fields specific to it (ear & tail shape). As well as this it uses a ternary operator to pass the size into the super constructor and the toString() method calls the super.toString() method to print out all information.

```java
public class Dog extends Animal {

    private String earShape;
    private String tailShape;

    public Dog(String type, double weight){
        this(type,weight, "Perky", "Curled");
    }
    public Dog(String type, double weight, String earShape, String tailShape) {
        super(type, weight < 15 ? "small": (weight < 35 ? "medium" : "large"), weight);
        this.earShape = earShape;
        this.tailShape = tailShape;
    }

    @Override
    public String toString() {
        return "Dog{" +
                "earShape='" + earShape + '\'' +
                ", tailShape='" + tailShape + '\'' +
                "} " + super.toString();
    }
}

```

##### Overriding super class methods

Overriding a method is when you create a method on a subclass, which has the same signature as a method on a super class. This enables the child class to show different behaviour for that method.

See the example below where the makeNoise() method is overriden in the dog class and now has no output.

```java
class Dog {
    public void makeNoise() {

    }
}
```

Another way to ensure a method is overriden is with alt + insert in intelliJ. This includes the @Override symbol that tells you the method is overriding the parent method.

```java
class Dog {
    @Override
    public void makeNoise() {

    }
}
```

An overriden class can do one of three things

* it can implement completely different behaviour, overriding the behaviour of the parent.
* It can simply call the parents class method, which is somewhat redundant to do.
* It can call the parent class's method, including other code to run, so it can extend the functionality.


### Composition

Composition is another component of OOP. The difference between inheritance and composition is that inheritance defines an 'IS A' relationship. Whereas composition defines a 'HAS A' relationship. Composition allows the modelling of parts which make up a greater whole. The example below models a PC which is product comprised of a monitor, motherboard and case.

```java
public class Product {

    private String model;
    private String manufacturer;
    private int width;
    private int height;
    private int depth;

    public Product(String model, String manufacturer) {
        this.model = model;
        this.manufacturer = manufacturer;
    }
}

class PC extends Product {

    private ComputerCase computerCase;
    private Monitor monitor;
    private Motherboard motherboard;

    public PC(String model, String manufacturer, ComputerCase computerCase, Monitor monitor, Motherboard motherboard) {
        super(model, manufacturer);
        this.computerCase = computerCase;
        this.monitor = monitor;
        this.motherboard = motherboard;
    }

    public ComputerCase getComputerCase() {
        return computerCase;
    }

    public Monitor getMonitor() {
        return monitor;
    }

    public Motherboard getMotherboard() {
        return motherboard;
    }
}

class Monitor extends Product {

    private int size;
    private String resolution;


    public Monitor(String model, String manufacturer) {
        super(model, manufacturer);
    }

    public Monitor(String model, String manufacturer, int size, String resolution) {
        super(model, manufacturer);
        this.size = size;
        this.resolution = resolution;
    }

    public void drawPixelAt(int x, int y, String colour){
        System.out.println(String.format("Drawing pixel at %d, %d in colour %s ", x,y, colour));
    }
}

class Motherboard extends Product {

    private int ramSlots;
    private int cardSlots;
    private String bios;

    public Motherboard(String model, String manufacturer) {
        super(model, manufacturer);
    }

    public Motherboard(String model, String manufacturer, int ramSlots, int cardSlots, String bios) {
        super(model, manufacturer);
        this.ramSlots = ramSlots;
        this.cardSlots = cardSlots;
        this.bios = bios;
    }

    public void loadProgram(String programName){
        System.out.println(String.format("Program %d is now loading...", programName));
    }
}

class ComputerCase extends Product {

    private String powerSupply;

    public ComputerCase(String model, String manufacturer) {
        super(model, manufacturer);
    }

    public ComputerCase(String model, String manufacturer, String powerSupply) {
        super(model, manufacturer);
        this.powerSupply = powerSupply;
    }

    public void pressPowerButton(){
        System.out.println("Power button pressed");
    }
}
```
As a general rule composition should be looked at first when designing programs in Java:


* Composition is more flexible, parts can be added or removed. These changes are less likely to have a downstream effect.
* Composition provides functional reuse outside of the class hierachy, meaning classes can share attributes & behaviour, by having similar components, instead of inheriting functionality from a parent or base class.
* Java's inheritance breaks encapsulation, because subclasses may need direct access to a parent's state or behaviour.

On the other hand:

* Inheritance is less flexible
* Adding or removing a class from a class hierachy may impact all subclasses from that point.
* A new subclass may not need all the functionality or attributes of its parent class.

### Encapsulation

In Java, encapsulation means hiding things, by making them private or inaccessible.

Reasons being hiding things:

* Makes the interface simpler, we may want to hide unnecessary details
* Protects the integrity of data on an object, we may hide or restrict access to some of the data and operations
* To decouple the published interface from the internal details of the class, we may hide actual names and types of class members.

The interface here referres to the class members that can be accessed by calling code. Everything else is interal or private.
An application programming interface, or API, is the public contract, that tells others how to use the class.

To see why encapsulation is important, see the example below that does not use it.

```java
class Game {

    public static void main(String[] args) {
        Player player = new Player();

        player.name = "John"; // Can access fields directly
        player.health = 20;
        player.weapon = "Sword";

        int damage = 10;
        player.loseHealth(damage);
        System.out.printf("Remaining health = %d%n", player.healthRemaining()); // Remaining health = 10

        player.health = 200;
        player.loseHealth(11);
        System.out.printf("Remaining health = %d%n", player.healthRemaining()); // Remaining health = 189 exceeding max of 100
    }
}

public class Player {

    public String name; // Public access modifier
    public int health;
    public String weapon;

    public void loseHealth(int damage) {
        health -= damage;

        if (health <= 0) {
            System.out.println("Player knocked out of game");
        }
    }

    public int healthRemaining() {
        return health;
    }

    public void restoreHealth(int extraHealth) {
        health += extraHealth;

        if (health > 100) {
            System.out.println("Player restored to 100%");
            health = 100;
        }
    }
}

```

Allowing direct access to data on an object, can potentially bypass checks and additional processing that the class has in place to manage the data. It also prevents renaming or ammending variable names. For example:

```java
public class Player {

    public String fullName; // Member field updated from name to fullName
    public int health;
    public String weapon;
}
```
This would break the Game class that can no longer find those fields.

An encapsulated version can be seen below:

```java
class Game {

    public static void main(String[] args) {

        EnhancedPlayer enhancedPlayer = new EnhancedPlayer("John");
        System.out.printf("Initial health is %d %n", enhancedPlayer.getHealthPercentage()); //

        EnhancedPlayer enhancedPlayer2 = new EnhancedPlayer("Pete", 200, "Sword");
        System.out.printf("Initial health is %d %n", enhancedPlayer2.getHealthPercentage()); // Maximum health is still 100
    }
}

public class EnhancedPlayer {

    private String name;
    private int healthPercentage;
    private String weapon;

    public EnhancedPlayer(String name) {
        this(name, 100, "Sword");
    }

    public EnhancedPlayer(String name, int health, String weapon) {
        this.name = name;

        if (health <= 0 ) {
            this.healthPercentage = 1;
        } else if (health > 100) {
            this.healthPercentage = 100;
        } else {
            this.healthPercentage = health;
        }
        this.weapon = weapon;
    }

    public void loseHealth(int damage){
        this.healthPercentage -= damage;

        if (this.healthPercentage <=0){
            System.out.println("Player knocked out");
            // Reduce number of lives remaining
        }
    }

    public int getHealthPercentage(){
        return this.healthPercentage;
    }
}
```

The main benefit of encapsulation is you're not affecting any other code. Its acts as a black box

To create an encapsulated class:

* Create constructors for object initialisation, which enforces that only objects with valid data will get created.
* Use the private access modifier for your fields.
* Use setter and getter methods sparingly, and only as needed.
* Use access modifiers that are not private, only for the methods that the calling code needs to use.


### Polymorphism

Polymophism means many forms. This allows the writing of code to call a method, but at runtime, the method's behaviour can be different for different objects. This means the behaviour is dependent on the runtime type of the object which may be different from the declared type in the code.

The declared type has to have some kind of relationship to the runtime type. Inheritance is one way to establish this relationship. However, there are other ways.

```java
class Cinema {
    public static void main(String[] args) {
        Movie movie1 = new Adventure("Star Wars"); // Adventure is a type of movie
        movie1.watchMovie(); // Calls Adventure watch movie method

        Movie movie2 = new Comedy("Space Balls"); // Comedy is a type of movie
        movie2.watchMovie(); // Calls Comedy watch movie method

        Movie movie3 = Movie.getMovie("Adventure", "Iron Man"); // creates adventure type movie
        movie3.watchMovie();
    }
}

public class Movie {

    private String title;

    public Movie(String title) {
        this.title = title;
    }

    public void watchMovie() {
        String instanceType = this.getClass().getSimpleName();
        System.out.printf("%s is a %s film %n", title, instanceType);
    }

    public static Movie getMovie(String type, String title) { // returns new movie type depending on type

        switch (type.toUpperCase().charAt(0)) {
            case 'A':
                return new Adventure(title);
            case 'C':
                return new Comedy(title);
            default:
                return new Movie(title);
        }
    }
}

class Adventure extends Movie {

    public Adventure(String title) {
        super(title);
    }
    @Override
    public void watchMovie() {
        super.watchMovie();
        System.out.printf(".. %s%n".repeat(3),
                "Pleasant Scene",
                "Scary Music",
                "Something Bad Happens");

        System.out.println();
    }
}

class Comedy extends Movie {

    public Comedy(String title) {
        super(title);
    }
    @Override
    public void watchMovie() {
        super.watchMovie();
        System.out.printf(".. %s%n".repeat(3),
                "Something funny happens",
                "Something even funnier happens",
                "Happy Ending");

        System.out.println();
    }
}

```

#### Adding Interactivity

The Scanner class can be used to get input from the user.

```java
import java.util.Scanner;

class Cinema {
    public static void main(String[] args) {

        Scanner s = new Scanner(System.in); //Get user input

        while (true) {
            System.out.print("Enter Type (A for Adventure or C for Comedy, " +
                    "or Q to quit:");
            String type = s.nextLine();
            if ("Qq".contains(type)) { //checks if 'Q' or 'q' are entered
                break;
            }

            System.out.print("Enter Movie Title: ");
            String title = s.nextLine();
            Movie movie = Movie.getMovie(type, title);
            movie.watchMovie();
        }
    }
}

```

Polymorphism enables you to write generic code, based on the base class.

## Section 8 - Arrays

Arrays are a data structure that allows the storage and manipulation of multiple values of the same type.
Elements in an Array are 0 indexed.

### Declaring an Array

When you declare an array, first the type of elements in the array must be specified, followed by square brackets which is the key for Java to identify the variable as an Array. The square brackets can also be after the variable name:

```java

int [] integers;
String [] names;
double accountBalances [];
```

### Instantiating an Array

One way to instantiate an Array is with the new keyword and a pair of square brackets:

```java
int [] integers = new int [10]; // Array with a size of 10 elements
```

The size of an array, once created, is fixed. Elements can not be added or deleted. However, the existing elements in the array can be reassigned. An Array instantiation does not have a set of parentheses, meaning data cannot be passed to a constructor for an array.

#### The Array Initialiser

An Array initialiser makes instantiating and intialising a small Array easier:

```java
int [] integers = new int []{1, 2, 3, 4, 5}; // Array with 1, 2, 3, 4 & 5 as its elements
```

Because the values are specified, the length of the array can be determined. Therefore, they don't need to be declared in the square brackets. In fact the "new int[]" does not need to be specified. However, this is only the case during instantiation.

```java
int [] integers = {1, 2, 3, 4, 5}; // Array with 1, 2, 3, 4 & 5 as its elements
```

An example of Array initilisation and instantiations can be seen below:

```java
import java.util.Arrays;

public class Main {
    public static void main(String[] args) {

        int [] integers = new int [10]; // Integer Array with a size of 10 and values of 0
        integers[5] = 50; // sets 6th element to 50

        double [] doubles = new double [10]; // Double Array with size of 10 and values of 0.0
        doubles[2] = 3.5; // Third element set to 3.5

        System.out.println(Arrays.toString(integers)); // Prints out Array values [0, 0, 0, 0, 0, 50, 0, 0, 0, 0]
        System.out.println(Arrays.toString(doubles)); // [0.0, 0.0, 3.5, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0]

        int [] integers1 = new int []{1, 2, 3, 4, 5}; // Array with 1, 2, 3, 4 & 5 as its elements

        /*
        Compiler Error - Array initialiser is not allowed here
        int [] integers2;
        integers2 = {2, 4, 6, 8, 10};
        */

        int [] integers2;

        integers2 = new int []{1,2,3,4,5}; // Initialiser can be used with new int keywords
        int [] integers3 = {2, 4, 6, 8, 10}; // Array with 2, 4, 6, 8 & 10 as its elements

        for (int i = 0; i < integers2.length; i++){
            System.out.print(integers2[i] + " "); // Prints out Array values
        }
        System.out.println();

        System.out.println(Arrays.toString(integers1)); // [1, 2, 3, 4, 5]
        System.out.println(Arrays.toString(integers3)); // [2, 4, 6, 8, 10]


        System.out.printf("First Element= %d %n", integers1[0]); // Prints first element
        System.out.printf("Length of Array = %d %n", integers1.length); // Prints Length of Array
        System.out.printf("Last Element = %d %n", integers1[(integers1.length - 1)]); // Prints Last Element of Array
    }
}
```

Array is a special class in Java which like all other classes inherits from java.lang.Object.

#### Enhanced for Loops

The enhanced for loop/ the For Each loop. Was designed to walk through elements in an Array or any kind of collection. It processes one element at a time, from the first to the last. The syntax can be seen below:

```java

for (declaration : collection) {
    // block of statements
}
```

It's important to notice the seperator between components is a colon and not a semi-colon. The enhanced for loops also only has two components vs the three using the basic for loop. See below for an example:

```java
int [] integers1 = new int []{1, 2, 3, 4, 5}; // Array with 1, 2, 3, 4 & 5 as its elements

    for (int element: integers1) {
        System.out.print(element + " ");
    }
```
### Using java.util.Arrays

Arrays are used to manage many items of the same type. Some common behaviour for Arrays would be sorting, initialising values, copying the Array and finding an element. For an array, this bejaviour isn't on the Array instance itself, but with a helper class java.util.Arrays. Some examples on sorting, filling and copying can be seen below:

```java
import java.util.Arrays;
import java.util.Random;

public class Main {
    public static void main(String[] args) {

        int[] firstArray = getRandomArray(10);
        System.out.println("firstArray = " + Arrays.toString(firstArray));
        Arrays.sort(firstArray); // Sorts in place
        System.out.println("firstArray sorted = " + Arrays.toString(firstArray));

        int[] secondArray = new int[10];
        System.out.println("secondArray = " + Arrays.toString(secondArray));
        Arrays.fill(secondArray, 5); // Fills Array with specified value
        System.out.println("secondArray filled with 5's= " + Arrays.toString(secondArray));

        int[] thirdArray = getRandomArray(10);
        System.out.println("thirdArray = " + Arrays.toString(thirdArray));

        int[] fourthArray = Arrays.copyOf(thirdArray, thirdArray.length); //Copy entire Array
        System.out.println("fourthArray = " + Arrays.toString(thirdArray));

        Arrays.sort(fourthArray);
        System.out.println("thirdArray = " + Arrays.toString(thirdArray));
        System.out.println("fourthArray sorted= " + Arrays.toString(fourthArray));

        int[] smallerArray = Arrays.copyOf(thirdArray,5);
        System.out.println("smallerArray= " + Arrays.toString(smallerArray)); // Only copied first 5 values

        int[] largerArray = Arrays.copyOf(thirdArray,15);
        System.out.println("largerArray= " + Arrays.toString(largerArray)); // Adds 5 extra elements
    }

    public static int[] getRandomArray (int length) { //Returns Array with random values
        Random random = new Random();
        int[] newInt = new int[length];

        for (int i = 0; i < length; i++) {
            newInt[i] = random.nextInt(100);
        }

        return newInt;
    }
}
```

#### Searching and Matching

There are different algorithms for searching and matching elements in lists. Java includes many of the common search techniques such as binarySearch on many of its collections. However:

* The array has to be sorted
* If there are duplicate values in the array, there is no guarentee which one it'll match on.
* Elements must be comparable. Trying to compare instances of different types, may lead to errors and invalid results.

The binarySearch method returns:

* The position of a match if found
* A -1 when no match was found
* If the array has duplicates and you need to find the first element, other methods should be used.

An example can be found below:

```java
import java.util.Arrays;
import java.util.Random;

public class Main {
    public static void main(String[] args) {

        String[] sArray = {"Able", "Jane", "Mark", "Ralph", "David"};
        Arrays.sort(sArray);

        System.out.println(Arrays.toString(sArray));

        if (Arrays.binarySearch(sArray, "Mark") >= 0) {
            System.out.println("Found Mark");
        }
    }

    public static int[] getRandomArray(int length) {

        Random random = new Random();
        int [] newArray = new int[length];

        for (int i = 0; i < length; i++) {
            newArray[i] = random.nextInt(100);
        }

        return newArray;
    }
}
```

Two Arrays are considered equal if both Arrays have the same number of elements and all elements in the same position are equal. An example can be seen below:

```java
import java.util.Arrays;

public class Main {
    public static void main(String[] args) {

        int[] s1 = {1, 2, 3, 4, 5};
        int[] s2 = {1, 2, 3, 4, 5};
        int[] s3 = {5, 4, 3, 2, 1};
        int[] s4 = {1, 2, 3, 4, 5, 0};


        if (Arrays.equals(s1, s2)) {
            System.out.println("Arrays are equal"); // Prints as - Elements are the same
        } else {
            System.out.println("Arrays are not equal");
        }

        if (Arrays.equals(s1, s3)) {
            System.out.println("Arrays are equal");
        } else {
            System.out.println("Arrays are not equal"); // Prints as - Elements are not in the same order
        }

        if (Arrays.equals(s1, s4)) {
            System.out.println("Arrays are equal");
        } else {
            System.out.println("Arrays are not equal"); // Prints as - Elements are not the same length
        }


    }
}
```

### Array References

WHen an object is assigned to a variable, the variable becomes a reference to that object. This is true of Arrays. However, if the Array contains objects. Then every Array element is also a reference. One way to know if it's a reference type is the 'new' operator as that creates a new object in memory. 

Examples can be seen below:

```java 
import java.util.Arrays;

public class Main {
    public static void main(String[] args) {


        int[] myIntArray = new int[5];
        int[] anotherArray = myIntArray; // Holds the same reference address

        System.out.printf("myIntArray = %s %n", Arrays.toString(myIntArray)); // myIntArray = [0, 0, 0, 0, 0]
        System.out.printf("anotherArray = %s %n", Arrays.toString(myIntArray)); // anotherArray = [0, 0, 0, 0, 0]

        anotherArray[0] = 1;

        System.out.printf("myIntArray after change = %s %n", Arrays.toString(myIntArray)); // myIntArray = [1, 0, 0, 0, 0]
        System.out.printf("anotherArray after change = %s %n", Arrays.toString(myIntArray)); // anotherArray = [1, 0, 0, 0, 0]

        modifyArray(myIntArray); // Creates another reference
        System.out.printf("myIntArray after second change = %s %n", Arrays.toString(myIntArray)); // myIntArray = [1, 2, 0, 0, 0]
        System.out.printf("anotherArray after second change = %s %n", Arrays.toString(myIntArray)); // anotherArray = [1, 2, 0, 0, 0]

    }

    private static void modifyArray(int[] array) {

        array[1] = 2;
    }
}
```

#### Variable Arguments

The brackets in an Array method signnature can be replaced by three periods. This is a special designation for Java, that means it will take zero or many fields as arguments for the method and create an array to process them in the method.

```java
public class Main {
    public static void main(String... args) {
        System.out.println("Hello world!");

        String [] splitStrings = "Hello World Again".split(" ");
        printText(splitStrings);

        System.out.println("_".repeat(20));
        printText("Hello");

        System.out.println("_".repeat(20));
        printText("Hello", "World", "Again");

        System.out.println("_".repeat(20));
        printText();
        
        String[] sArray = {"first", "second", "third", "fourth", "fifth"};
        System.out.println(String.join(",", sArray));
    }

    private static void printText(String... textList){

        for (String t: textList){
            System.out.println(t);
        }
    }
}
```

There can only be one variable argument in a method. The variable argument must be the last argument.

### Multi-Dimensional Arrays

Nested Arrays occur when an Array element is an Array. A two dimensional array can be thought of as a table or matrix of values with rows and columns. An Array initialiser can be used for this:

```java

public class Main {
    public static void main(String[] args) {

        int[][] array = { // Multiline 2D Array
                {1, 2, 3},
                {11, 12, 13},
                {21, 22, 23}
        };

        int[][] array2 = {{1, 2, 3}, {11, 12, 13}, {21, 22, 23}}; // single line 2D Array
    }
}
```

Multi-Dimensional arrays do not have to be uniform matrixes and the nested Arrays can be different sized

```java
int[][] array = {{1, 2}, {11, 12, 13}, {21, 22, 23, 24, 25}};
```

Each element is an array of integers. 

You can also initialise a multi-dimensional Array and define the size of the nested Arrays:

```java
int[][] array = new int [3][3]; // [outer][inner]
```

The statement above says that the Array contains three nested arrays and each array will have three ints.

You can also not specify the size of the nested arrays and only specify the outer array size:

```java
int[][] array = new int [3][];
```

#### Declaring Two-Dimensional Arrays

There are many ways to declare a two-dimensional array:

```java
int[][] array; // Most common and clearest way
int[] array [];
```

#### Accessing Multi-Dimensional Arrays

```java
import java.util.Arrays;

public class Main {
    public static void main(String[] args) {

        int[][] array2 = new int[4][4];

        System.out.println(Arrays.toString(array2)); // Prints string references
        System.out.println("arrays2.length = " + array2.length);

        for (int[] outer: array2){
            System.out.println(Arrays.toString(outer)); // Prints element values
        }

        for (int i = 0; i < array2.length; i++) { // Prints individual element values
            var innerArray = array2[i];

            for (int j = 0; j < innerArray.length; j++) {
                System.out.print(array2[i][j] + " ");
            }
            System.out.println();
        }

        System.out.println();

        for (var outer: array2) { // Same as line above but with enhanced for loop
            for (var element: outer) {
                System.out.print(element + " ");
            }
            System.out.println();
        }

        for (int i = 0; i < array2.length; i++) { // Prints individual element values
            var innerArray = array2[i];

            for (int j = 0; j < innerArray.length; j++) {
                array2[i][j] = (i * 10) + (j + 1); //Assigns values
            }
        }
        
        System.out.println();

        System.out.println(Arrays.deepToString(array2)); // Prints whole Array

    }
}
```

```java
import java.util.Arrays;

public class Main {
    public static void main(String[] args) {


        int[][] array = new int[4][4];

        for (int i = 0; i < array.length; i++) {
            var outer = array[i];

            for (int j = 0; j < outer.length; j++) {
                array[i][j] = (i * 10) + (j + 1);
            }
        }

        System.out.println(Arrays.deepToString(array));

        /*
        array[1] = {10, 20, 30}; // Array initialiser cannot be used here
        System.out.println(Arrays.deepToString(array));
        */

        array[1] = new int[] {10, 20, 30}; //Replaces second Array element to [10, 20, 30]
        System.out.println(Arrays.deepToString(array));

        Object[] anyArray = new Object[3];
        System.out.println(Arrays.toString(anyArray)); // [null, null, null]

        anyArray[0] = new String[] {"a", "b", "c"};
        System.out.println(Arrays.deepToString(anyArray)); // [[a, b, c], null, null]

        anyArray[1] = new String[][] {
                {"1", "2"},
                {"3", "4", "5"},
                {"6", "7", "8", "9"}
        };

        System.out.println(Arrays.deepToString(anyArray)); // [[a, b, c], [[1, 2], [3, 4, 5], [6, 7, 8, 9]], null]

        anyArray[2] = new int[2][2][2];
        System.out.println(Arrays.deepToString(anyArray)); // [[a, b, c], [[1, 2], [3, 4, 5], [6, 7, 8, 9]], [[[0, 0], [0, 0]], [[0, 0], [0, 0]]]]


        for (Object element: anyArray) {
            System.out.printf("Element type = %s %n", element.getClass().getSimpleName());
            System.out.printf("Element toString() = %s %n", element);
            System.out.println(Arrays.deepToString((Object[]) element )); //Element casted to object Array type
        }
    }

    }


```

## Section 9 - Containers

### Lists

There are other data structures that allow the modification of the number of elements in an Array as well as many other improvements.

#### Array vs Lists

An Array is mutable and the values in an Array can be set or changed. However, the size of the Array cannot be changed. Java has several other classes where items can be add, removed and the container can be resized. These classes are said to implement a Lists behaviour. List is a special type in Java called an Interface. Interfaces describe a set of method signitures that all List classes are expected to have.

#### The ArrayList

The ArrayList is a class that maintains an array in memory, that's actually bigger than what is needeed is most cases. It keeps track of the capacity - the actual size of the array. But it also keeps track of the elements that have been assigned or set- the size of the ArrayList. As elements are added to the ArrayList, its capacity needs to grow, this all happens behind the scenes, which is why the ArrayList is resizable.

```java
import java.util.ArrayList;
import java.util.Arrays;

record GroceryItem(String name, String type, int count) {
    public GroceryItem(String name) {
        this(name,"DAIRY",1);
    }

    @Override
    public String toString(){
        return String.format("%d %s in %s", count, name.toUpperCase(), type);
    }
}
public class Main {
    public static void main(String[] args) {
        GroceryItem[] groceryArray = new GroceryItem[3];
        groceryArray[0] = new GroceryItem("milk");
        groceryArray[1] = new GroceryItem("apples","PRODUCE",6);
        groceryArray[2] = new GroceryItem("oranges", "PRODUCE", 5);

        System.out.println(Arrays.toString(groceryArray));

        ArrayList<GroceryItem> groceryList = new ArrayList<>();

        groceryList.add(new GroceryItem("Butter"));
        groceryList.add(new GroceryItem("Milk"));
        groceryList.add(new GroceryItem("oranges", "PRODUCE", 5));
        groceryList.add(0, new GroceryItem("apples", "PRODUCE", 6)); // add new element at specified index

        System.out.println(groceryList);

        groceryList.set(0, new GroceryItem("Bananas", "PRODUCE", 6)); // replace element at specified index
        System.out.println(groceryList);

        groceryList.remove(1); // Remove element at specified index
        System.out.println(groceryList);
    }
}
```

Adding, Modifying, Accessing & Converting ArrayLists

```java
import java.util.ArrayList;
import java.util.Arrays;
import java.util.Comparator;
import java.util.List;

public class MoreLists {

    public static void main(String[] args) {

        String[] items = {"apples", "bananas", "milk", "eggs"};

        List<String> list = List.of(items); // Transforms Array into List
        System.out.println(list);

        System.out.println(list.getClass().getName()); //Immutable List - java.util.ImmutableCollections$ListN
        // list.add("yogurt"); Does not work as class is immutable

        ArrayList<String> groceries = new ArrayList<>(list);
        groceries.add("yogurt");
        System.out.println(groceries);

        ArrayList<String> newList = new ArrayList<>(
                List.of("pickles", "mustard", "cheese")); //Adds list elements to ArrayList

        System.out.println(newList);

        groceries.addAll(newList); // Add other ArrayList elements
        System.out.println(groceries);

        System.out.println("Third item = " + groceries.get(2)); //Access ArrayList Elements

        if (groceries.contains("mustard")) {
            System.out.println("List contains mustard");
        }

        groceries.add("yogurt");
        System.out.println("first = " + groceries.indexOf("yogurt"));
        System.out.println("last = " + groceries.lastIndexOf("yogurt"));

        System.out.println("Grocery List = " + groceries);
        groceries.remove(1);
        System.out.println("Grocery List = " + groceries); // 2nd element removed ("bananas")
        groceries.remove("yogurt");
        System.out.println("Grocery List = " + groceries); // first "yogurt" removes

        groceries.add("apples");
        groceries.removeAll(List.of("apples", "eggs"));
        System.out.println("Grocery List = " + groceries); // All apples and eggs removed

        groceries.retainAll(List.of("apples", "milk", "mustard", "cheese")); // Only keeps elements in the List within the ArrayList
        System.out.println(groceries);

        groceries.clear(); // Empties ArrayList
        System.out.println(groceries);
        System.out.println("isEmpty = " + groceries.isEmpty());

        groceries.addAll(List.of("apples", "milk", "mustard", "cheese"));
        groceries.addAll(Arrays.asList("eggs", "pickles", "mustard", "ham"));
        System.out.println(groceries);

        groceries.sort(Comparator.naturalOrder()); // orders Strings alphabetically and number in size order
        System.out.println(groceries);

        groceries.sort(Comparator.reverseOrder()); // Reverses order
        System.out.println(groceries);

        var groceryArray = groceries.toArray(new String [groceries.size()]); // Converts ArrayList into Array
        System.out.println(Arrays.toString(groceryArray));
        
        var groceryList = Arrays.asList(groceries); // Converts ArrayList into List
        System.out.println(groceryList);
    }
}

```

##### Multi-dimensional ArrayLists

A multi-dimensional ArrayList simply has a type, which in itself is an ArrayList and then instantiating each element as an ArrayList.

```java
import java.util.ArrayList;

public class MultiDimensionalArrayList {

    public static void main(String[] args) {

        int size = 3;
        ArrayList<ArrayList<Integer>> coordinates = new ArrayList<>(size);

        for (int i = 0; i < size; i++) {
            coordinates.add(new ArrayList<>());
        }

        coordinates.get(0).add(1);
        coordinates.get(1).add(2);
        coordinates.get(2).add(0);

        coordinates.get(1).add(0);
        coordinates.get(2).add(1);
        coordinates.get(0).add(2);

        System.out.println(coordinates); // [[1, 2], [2, 0], [0, 1]]
    }
}

```
