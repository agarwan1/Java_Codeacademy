# Conditional and Control Flow
```
if (true) {

  System.out.println("Hello World!");

}
```
If the condition is true, then the block is run. So Hello World! is printed.
But suppose the condition is different:
```
if (false) {

  System.out.println("Hello World!");

}
```
```
boolean isValidPassword = true;

if (isValidPassword) {

  System.out.println("Password accepted!");

}

// Prints "Password accepted!"

int numberOfItemsInCart = 9;

if (numberOfItemsInCart > 12) {

  System.out.println("Express checkout not available");

}
```
// Nothing is printed.
If a conditional is brief we can omit the curly braces entirely:
```
if (true) System.out.println("Brevity is the soul of wit");
```
Note: Conditional statements do not end in a semicolon.

```
if (hasPrerequisite) {

  // Enroll in course

} else {

  // Enroll in prerequisite

}
```

The conditional statement now has multiple conditions that are evaluated from the top down:
```
String course = "Theatre";

if (course.equals("Biology")) {

  // Enroll in Biology course

} else if (course.equals("Algebra")) {

  // Enroll in Algebra course

} else if (course.equals("Theatre")) {

  // Enroll in Theatre course

} else {

  System.out.println("Course not found!");
```
```
int testScore = 72;

if (testScore >= 90) {
  System.out.println("A");
} else if (testScore >= 80) {
  System.out.println("B");
} else if (testScore >= 70) {
  System.out.println("C");
} else if (testScore >= 60) {
  System.out.println("D");
} else {
  System.out.println("F");
}
// prints: C
```

# Switch
An alternative to chaining if-then-else conditions together is to use the switch statement. This conditional will check a given value against any number of conditions and run the code block where there is a match.
Here’s an example of our course selection conditional as a switch statement instead:
```
String course = "History";

switch (course) {
  case "Algebra": 
    // Enroll in Algebra
    break; 
  case "Biology": 
    // Enroll in Biology
    break;
  case "History": 
    // Enroll in History
    break;
  case "Theatre":
    // Enroll in Theatre
    break;
  default:
    System.out.println("Course not found");
}
```

