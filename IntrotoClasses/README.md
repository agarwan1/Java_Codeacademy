# Classes
All programs require one or more classes that act as a model for the world. 
For example, a program to track student test scores might have Student, Course, and Grade classes. Our real-world concerns, students and their grades, are inside the program as classes.
We represent each student as an **instance, or object,** of the Student class.
This is **object-oriented programming because programs are built around objects and their interactions. An object contains state and behavior.**
![stepsofjavacompilation](Images/classes.png)
**Classes are a blueprint for objects.** Blueprints detail the general structure. For example, all students have an ID, all courses can enroll a student, etc.
An **instance** is the thing itself. This student has an ID of 42, this course enrolled that student, etc.
![stepsofjavacompilation](Images/savingsaccount.png)

# Classes: Syntax
The fundamental concept of object-oriented programming is the class.
A class is the set of instructions that describe how an instance can behave and what information it contains.
Java has pre-defined classes such as System, which we’ve used in logging text to our screen, but we also need to write our own classes for the custom needs of a program.
```
public class Car {
// scope of Car class starts after curly brace

  public static void main(String[] args) {
    // scope of main() starts after curly brace

    // program tasks

  }
  // scope of main() ends after curly brace

}
```
// scope of Car class ends after curly brace
This example defines a class named Car. public is an access level modifier that allows other classes to interact with this class. For now, all classes will be public.
This class has a main() method, which lists the tasks performed by the program. main() runs when we execute the compiled Car.class file.

# Classes: Constructors