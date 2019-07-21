# Arrays
We have seen how to store single pieces of data in variables. What happens when we need to store a group of data? What if we have a list of students in a classroom? Or a ranking of the top 10 horses finishing a horse race?
Java array to store the data as a list.
An array holds a fixed number of values of one type. Arrays hold doubles, ints, booleans, or any other primitives. Arrays can also contain Strings, or any other objects!
Each index of an array corresponds with a different value. Here is a diagram of an array filled with integer values:

# Creating an Array Explicitly
To create an array, we first declare the type of data it holds:
double[] prices;
Then, we can explicitly initialize the array to contain the data we want to store:
prices = {13.15, 15.87, 14.22, 16.66};
Just like with simple variables, we can declare and initialize in the same line:
double[] prices = {13.15, 15.87, 14.22, 16.66};
We can use arrays to hold Strings and other objects as well as primitives:
String[] clothingItems = {"Tank Top", "Beanie", "Funny Socks", "Corduroys"};

# Importing Arrays
When we printed out the array we created in the last exercise, we saw a memory address that did not help us understand what was contained in the array.
If we want to have a more descriptive printout of the array itself, we need a toString() method that is provided by the Arrays package in Java. <br/>
`import java.util.Arrays;`
We put this at the top of the file, before we even define the class!
When we import a package in Java, we are making all of the methods of that package available in our code.
The Arrays package has many useful methods, including Arrays.toString(). When we pass an array into Arrays.toString(), we can see the contents of the array printed out:
```
import java.util.Arrays;

public class Lottery(){

  public static void main(String[] args){
    int[] lotteryNumbers = {4, 8, 15, 16, 23, 42};
    String betterPrintout = Arrays.toString(lotteryNumbers);
    System.out.println(betterPrintout);
  }

}
```
This code will print:
`[4, 8, 15, 16, 23, 42]`

# Get Elements by Index
We use square brackets, [ and ], to access data at a certain index:
```
double[] prices = {13.1, 15.87, 14.22, 16.66};
System.out.println(prices[1]);
```
This command would print:
`15.87`

# Creating an Empty Array
We can also create empty arrays and then fill the items one by one. Empty arrays have to be initialized with a fixed size:
`String[] menuItems = new String[5];`
Once you declare this size, it cannot be changed! This array will always be of size 5.
After declaring and initializing, we can set each index of the array to be a different item:
```
menuItems[0] = "Veggie hot dog";
menuItems[1] = "Potato salad";
menuItems[2] = "Cornbread";
menuItems[3] = "Roasted broccoli";
menuItems[4] = "Coffee ice cream";
```
This group of commands has the same effect as assigning the entire array at once:
```
String[] menuItems = {"Veggie hot dog", "Potato salad", "Cornbread", "Roasted broccoli", "Coffee ice cream"};
```
We can also change an item after it has been assigned! Let’s say this restaurant is changing its broccoli dish to a cauliflower one:
`menuItems[3] = "Baked cauliflower";`
Now, the array looks like:
`["Veggie hot dog", "Potato salad", "Cornbread", "Baked cauliflower", "Coffee ice cream"]`

# Length
To get the length of an array, we can access the length field of the array object:
```
String[] menuItems = new String[5];
System.out.println(menuItems.length);
```
This command would print 5, since the menuItems array has 5 slots, even though they are all empty.
If we print out the length of the prices array:
```
double[] prices = {13.1, 15.87, 14.22, 16.66};
System.out.println(prices.length);
```
We would see 4, since there are four items in the prices array!

# String[] args
When we write main() methods for our programs, we use the parameter String[] args. Now that we know about array syntax, we can start to parse what this means.
A String[] is an array made up of Strings. Examples of String arrays:
```
String[] humans = {"Talesha", "Gareth", "Cassie", "Alex"};
String[] robots = {"R2D2", "Marvin", "Bender", "Ava"};
```
The args parameter is another example of a String array. In this case, the array args contains the arguments that we pass in from the terminal when we run the class file. (So far, args has been empty.)
So how can you pass arguments to main()? Let’s say we have this class HelloYou:
```
public class HelloYou {
  public static void main(String[] args) {
    System.out.println("Hello " + args[0]);  
  }
}
```
When we run the file HelloYou in the terminal with an argument of "Laura":
`java HelloYou Laura`
We get the *output*:
`Hello Laura`
The String[] args would be interpreted as an array with one element, "Laura".
When we use args[0] in the main method, we can access that element like we did in HelloYou.
You can check for equality in either of these ways here:
`this.equals(that);`
or
`this == that;`

# Review
* Creating arrays explicitly, using { and }.
* Accessing an index of an array using [ and ].
* Creating empty arrays of a certain size, and filling the indices one by one.
* Getting the length of an array using length.
* Using the argument array args that is passed into the main() method of a class.

review newsfeedemptyarray.java
		  public void setFavoriteArticle(int favoriteIndex, String newArticle){
    			favoriteArticles[favoriteIndex] = newArticle;
  		  }
review newsfeedelementbyindex.java
		





