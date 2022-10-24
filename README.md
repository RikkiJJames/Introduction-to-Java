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
   * [Assignment Operators](#assignment-operators)
   * [Comparison Operators](#comparison-operators)
   * [Logical Operators](#logical-operators)
 
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
 
 ### Assignment Operators
 ### Comparison Operators
 ### Logical Operators
