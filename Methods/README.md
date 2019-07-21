# Methods

You have defined and called constructor methods, which create an instance of a class. You have also defined main methods, which are the tasks that execute when the program is run. These are specific examples of methods. We can also define our own that will take input, do something with it, and return the kind of output we want.

What if it took 20 lines of code to make a sandwich? Our program would become very long very quickly if we were making multiple sandwiches. Methods are powerful because they allow us to create blocks of code that are repeatable and modular.

This method looks like:
```
public void startEngine() {
  System.out.println("Starting the car!");
  System.out.println("Vroom!");
}
```
The first line, public void startEngine(), is the **method signature**. It gives the program some information about the method:
* **public** means that other classes can access this method. 
* The **void** keyword means that there is no specific output from the method.
* startEngine() is the name of the method.

```
public void checkBalance(){
  System.out.println("Hello!");
  System.out.println("Your balance is " + balance);
}
```

# Calling Methods
Here is an example of calling a method on an object using the Car class:
```
class Car {

  String color;

  public Car(String carColor) {
    color = carColor;
  }

  public void startEngine() {
    System.out.println("Starting the car!");
    System.out.println("Vroom!");
  }

  public static void main(String[] args){
    Car myFastCar = new Car("red");
    myFastCar.startEngine();
  }
}
```

# Scope
A method is a task that an object of a class performs.
We mark the domain of this task using curly braces: {, and }. Everything inside the curly braces is part of the task. This domain is called the scope of a method.
We can’t access variables that are declared inside a method in code that is outside the scope of that method.
```
class Car {
  String color;
  int milesDriven;

  public Car(String carColor) {
    color = carColor;
    milesDriven = 0;         
  }

  public void drive() {
     String message = "Miles driven: " + milesDriven;
     System.out.println(message);
  }

  public static void main(String[] args){
     Car myFastCar = new Car("red");
     myFastCar.drive();
  }
}
```
The variable message, which is declared and initialized inside of drive, cannot be used inside of main()! It only exists within the scope of the drive() method.
However, milesDriven, which is declared at the top of the class, can be used inside all methods in the class, since it is in the scope of the whole class.

# Adding Parameters
```
class Car {

  String color;

  public Car(String carColor) {
    color = carColor;         
  }

  public void startRadio(String station) {
    System.out.println("Turning on the radio to " + station + "!");
    System.out.println("Enjoy!");
  }

  public static void main(String[] args){
    Car myCar = new Car("red");
    myCar.startRadio("Meditation Station");
  }
}
```
In this code, we create a startRadio() method that accepts an String parameter called station. In the main() method, we call the startRadio() method on the myCar object and provide an String parameter of"Meditation Station".

# Reassigning Instance Fields
```
public SavingsAccount{
  double balance;
  public SavingsAccount(double startingBalance){
    balance = startingBalance;
  }

  public void deposit(double amountToDeposit){
     //Add amountToDeposit to the balance
  }

  public void withdraw(double amountToWithdraw){
     //Subtract amountToWithdraw from the balance
  }

  public static void main(String[] args){

  }
}
```
These methods would change the value of the variable balance. We can reassign balance to be a new value by using our assignment operator, =, again.
```
public void deposit(double amountToDeposit){
  double updatedBalance = balance + amountToDeposit;
  balance = updatedBalance;
}
```
Now, when we call deposit(), it should change the value of the instance field balance:
```
public static void main(String[] args){
  SavingsAccount myAccount = new SavingsAccount(2000);
  System.out.println(myAccount.balance);
  myAccount.deposit(100);
  System.out.println(myAccount.balance);
}
```
This code first prints 2000, the initial value of myAccount.balance, and then prints 2100, which is the value of myAccount.balance after the deposit() method has run.

# Returns
Remember, variables can only exist in the scope that they were declared in.
We can use a value outside of the method it was created in if we return it from the method.
We return a value by using the keyword return:
```
public int numberOfTires() {
   int tires = 4;
   return tires;
}
```
This method, called numberOfTires, returns 4. **In past exercises, when creating new methods, we used the keyword void. Here, we are replacing void with int, to signify that the return type is an int.**
The **void keyword (which means “completely empty”)** indicates to the method that no value is returned after calling that method.
Alternatively, we can use datatype keywords (such as int, char, etc.) to specify that a method should return a value of that type.
```
public static void main(String[] args){
  Car myCar = new Car("red");
  int numTires = myCar.numberOfTires();
}
```
# The ToString() Method
When we print out Objects, we often see a String that is not very helpful in determining what the Object represents. In the last lesson, we saw that when we printed our Store objects, we would see output like:
Store@6bc7c054
where Store is the name of the object and 6bc7c054 is its position in memory.
This doesn’t tell us anything about what the Store sells, the price, or the other instance fields we’ve defined. We can add a method to our classes that makes this printout more descriptive.
```
class Car {

    String color;

    public Car(String carColor) {
        color = carColor;
    }

    public static void main(String[] args){
        Car myCar = new Car("red");
        System.out.println(myCar);
    }

   public String toString(){
       return "This is a " + color + " car!";
   }
}
```
Review:
Calling a method : Methods are invoked with a .and ()



