# Compilation
Compilation causes errors. Java is a **compiled programming language**, meaning the code we write in a .java file is transformed into byte code by a compiler before it is executed by the Java Virtual Machine on your computer.

**Steps of Java Compilation**
![stepsofjavacompilation](Images/javacompilationsteps.png)

A **compiler** is a program that translates human-friendly programming languages into other programming languages that computers can execute.<br/>
For example, with a file called Plankton.java, we could compile it with the terminal command:<br/>
`javac Plankton.java`</p>
A successful compilation produces a .class file: Plankton.class, that we execute with the terminal command:<br/>
`java Plankton` <br/>
An unsuccessful compilation produces a list of errors. No .class file is made until the errors are corrected and the compile command is run again. The compiling process catches mistakes before the computer runs our code. 

# Variables
We store information in variables, named locations in memory.
Naming a piece of information allows us to use that name later, accessing the information we stored.
Variables also give context and meaning to the data we’re storing. <br/>
In Java, we specify the type of information we’re storing. Primitive datatypes are types of data built-in to the Java system.
We must declare a variable to reference it within our program. Declaring a variable requires that we specify the type and name: <br/>
`// datatype variableName
int age;
double salaryRequirement;
boolean isEmployed;`

ints hold positive numbers, negative numbers, and zero. They do not store fractions or numbers with decimals in them.
The int data type allows values between -2,147,483,648 and 2,147,483,647, inclusive.
To declare a variable of type int, we use the intkeyword before the variable name: <br/>
`// int variable declaration
int yearJavaWasCreated;
// assignment
yearJavaWasCreated = 1996;`

Data Types:
* int    
   * Whole number, int primitive data type that hold positive numbers, negative numbers and zero. No decimals. The int data type allows values between -2,147,483,648 and 2,147,483,647, inclusive.
     * `int age;`   `int yearCodecademyWasFounded = 2011;`
* double
   * Double primitive data type can hold decimals plus very small and large numbers. The maximum value is 1.797,693,134,862,315,7 E+308, which is approximately 17 followed by 307 zeros. The minimum value is 4.9 E-324, which is 324 decimal places!
     * `double price = 8.99;`
* boolean - true or false. `boolean javaIsACompiledLanguage = true;`
* char - can hold any character, like a letter, space, or punctuation mark. It must be surrounded by single quotes, '. 
   * `char punctuation = '!';` `char grade = 'A';`
* String - object not primitive! `String greeting = "Hello World";`