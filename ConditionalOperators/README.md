# Conditional Operators
Java includes operators that only use boolean values. These conditional operators help simplify complex boolean relationships by reducing multiple boolean values to a single value.
For example, what if we want to run a code block only if multiple conditions are true. We could use the ANDoperator: `&&`.
Or, we want to run a code block if at least one of two conditions are true. We could use the OR operator: `||`.
Finally, we can produce the opposite value, where truebecomes false and false becomes true, with the NOT operator: `!`.

# Conditional-And: &&
Here’s one way we could write the code:
```
if (tuitionPaid) {
  if (hasPrerequisite) {
    // enroll student
  }
}
```
We’ve nested two if-then statements. This does the job but we can be more concise with the AND operator:
```
if (tuitionPaid && hasPrerequisite) {
  // enroll student
}
```
The AND operator, &&, is used between two boolean values and evaluates to a single boolean value. If the values on both sides are true, then the resulting value is true, otherwise the resulting value is false.
This code illustrates every combination:
```
true && true
// true
false && true
// false
true && false
// false
false && false
// false
```

# Conditional-Or: ||
Here’s one way we could write the code:
if (hasAlgebraPrerequisite) {
  // Enroll in course
}

if (hasGeometryPrerequisite) {
  // Enroll in course
}
We’re using two different if-then statements with the same code block. We can be more concise with the ORoperator:
if (hasAlgebraPrerequisite || hasGeometryPrerequisite) {
  // Enroll in course
}
The OR operator, ||, is used between two boolean values and evaluates to a single boolean value. If either of the two values is true, then the resulting value is true, otherwise the resulting value is false.
This code illustrates every combination:
```
true || true
// true
false || true
// true
true || false
// true
false || false
// false
```

# Logical NOT: !
The unary operator NOT, !, works on a single value. This operator evaluates to the opposite boolean to which it’s applied:
```
!false
// true
!true
// false
```
```
if (hasPrerequisite) {
  // do nothing
} else {
  System.out.println("Must complete prerequisite course!");
}
```
This code does what we want but it’s strange to have a code block that does nothing!
The logical NOT operator cleans up our example:
```
boolean hasPrerequisite = false;

if (!hasPrerequisite) {
  System.out.println("Must complete prerequisite course!");
}
```

# Review
```
if (true && false) {
  System.out.println("You won't see me print!");
} else if (true && true) {
  System.out.println("You will see me print!");
}
```
Conditional-OR, ||, evaluates to true if one or both of the booleans on either side is true.
```
if (false || false) {
  System.out.println("You won't see me print!");
} else if (false || true) {
  System.out.println("You will see me print!");
}
```
Logical-NOT, !, evaluates to the opposite boolean value to which it is applied.
```
if (!false) {
  System.out.println("You will see me print!");
}
```

