# 1. Print from 1 to 100 without using numbers in your code.

## Print number form 1 to 100 with using numbers in for loop
```java
package com.adi;

public class PrintOneToHundred {

	public static void main(String[] args) {
		
		for(int i=1; i<=100;i++) {
			System.out.println(i);
		}
	}
}

```
    Output- Number for 1 to 100 is printed

## Pring from 1 to 100 without using number
```java
package com.adi;

public class PrintOneToHundred {

	public static void main(String[] args) {
	
		//Using character literal
		int one = 'A'/'A';  //1 
		
		String s1 = ".........."; //length of string is 10
		
		for(int i = one; i<= (s1.length()*s1.length());i++) {
			System.out.println(i);
		}
	}
}

```
    Output- Number for 1 to 100 is printed

## Another way via askii value
```java
package com.adi;

public class PrintOneToHundred {

	public static void main(String[] args) {	
		
		int one = 'A'/'A';  //1 
		
		for(int i = one; i<= 'd';i++) {
			System.out.println(i);
		}
	}
}
```
     Output- Number for 1 to 100 is printed

# 2. Print 1 to 100 whithout using for/while/do-while loop in code.

## via recursive function
```java
package com.adi;

public class PrintOneToHundred {

	public static void main(String[] args) {	
		
	//via recursive function - a function calling itself
		
		printNum(1);
	}
	
	public static void printNum(int num) {
		
		//maximum range of number is 100 
		if(num <= 100) {
				
			//print
			System.out.println(num); //1 2 3 4 .....100
			
			//increment
			num++;
			
			//calling same function
			printNum(num);
		}	
	}
}

```
     Output- Number for 1 to 100 is printed

## via recursive function but generic method
```java
package com.adi;

public class PrintOneToHundred {

	public static void main(String[] args) {	
		
	//via recursive function but generic method
		
		printNum(1,100);
	}
	
	public static void printNum(int startnum, int endNumber) {
		
		//maximum range of number is endNumber
		if(startnum <= endNumber) {
				
			//print
			System.out.println(startnum); 
			
			//increment
			startnum++;
			
			//calling same function
			printNum(startnum,endNumber);
		}	
	}
}

```
       Output- Number for 1 to 100 is printed
## Via Integer Stream
```java
package com.adi;

import java.util.stream.IntStream;

public class PrintOneToHundred {

	public static void main(String[] args) {

		// via Integer stream

		// IntStream having method range(startInclusive,endExclusive)
		
		IntStream.range(1, 101).forEach(i -> System.out.println(i));

	}

}
```
     Output- Number for 1 to 100 is printed
# 3. Print from 1 to 100 without using any loop or recursion.
## via Arrays.fill()
```java
package com.adi;

import java.util.Arrays;
import java.util.stream.IntStream;

public class PrintOneToHundred {

	public static void main(String[] args) {

		//via Arrays fill :
		
		//create a object array and giving it size as 100(since we have to print from 1 to 100
		Object num[] = new Object[100];
		
		// In Arrays we have fill() method containting 2 argument
		// 1st arg - > array to be filled 
		// 2nd arg - >value to be stored in all element of the array
		
		Arrays.fill(num, new Object() {
			
			int count =0; //maintian a variable
			
			
			// Returns an  object representing the specified integer and return as string
			@Override
			public String toString() {
				
				return Integer.toString(++count);
			}
		});
		
		//What we do in above method?
		// Take 1st variable ie. 0
		//  in 2nd case we filled it as 1
		
		//This process is repeated till
		// when 1st arg is 99 
		// value is filled with 100
		
		
		//For printing
		System.out.println(Arrays.toString(num));
		
		
	}

}
```
Output:
![Alt text](image.png)

## via BitSet
```java
package com.adi;

import java.util.BitSet;

public class PrintOneToHundred {

	public static void main(String[] args) {

		// via BitSet class

		// create an object of BitSet() import from util
		// you have to set some value {{}}

		// Sets the bit at the specified index to the specified value.
		// 	Parameters:
			// 1st arg -> bitIndex a bit index
			// 2nd arg -> value a boolean value to set

		// whatever value u set convert it to toString()

		String s = new BitSet() {
					{
						set(1, 101);
					}
				}.toString();
				
		// here we use append() containing 3 things
				// 1 st ->character sequence
				//2nd -> start
				//3rd -> end
		//  out.print(csq.subSequence(start, end).toString())
		// this method behave like this		
		
		System.out.append(s, 1, s.length());

	}

}
```
Output:
![Alt text](image.png)

# 4. Print HelloWorld without using semicolon in java.
## Print via semicolon
```java
package com.adi;

public class Demo {

	public static void main(String args[]) {
		
		System.out.println("Hello World!");
	}
}

```
    Output : Hello World!
## via Printf() method
```java
package com.adi;

public class Demo {

	public static void main(String args[]) {
		
		//Printf() get formatted String
        // formaatted -> the way in which something is arranged or set out:
		
		if(System.out.printf("Hello World!") == null) {
			
		}
		//Condition definately fail but out put is printed.
	}
}

```
    Output : Hello World!

## via append
```java
package com.adi;

public class Demo {

	public static void main(String args[]) {
		
		//via append
		
		if(System.out.append("Hello World!") == null) {
			
		}
		
	}
}

```
    Output : Hello World!
## samething via .equals method
```java
package com.adi;

public class Demo {

	public static void main(String args[]) {

		// via append
		if (System.out.append("Hello World!" + "\n").equals(null)) {

		}

		if (System.out.printf("Hello World!").equals(null)) {

		}

	}
}

```
    Output : same 
## via for loop
```java
package com.adi;

public class Demo {

	public static void main(String args[]) {

		// via for loop

		for (int i = 0; i < 1; System.out.println("Hello World!")) {

			i++;
		}
		
		//For printing we won't use semicolon here
	}
}

```
    Output : same

# 5. Compare two integer number(integer caching) in java

```java
package com.adi;

public class Demo {

	public static void main(String args[]) {

		Integer num1 = 100;
		Integer num2 = 100;
		
		if(num1 == num2) {
			System.out.println("both are equal");
		} else {
			System.out.println("both are not equal");
		}
		
		// == compare refrence 
		
		// num1 and num2 are totally different object & having diff refrence 
		// but o/p => both are equal
		
		System.out.println("=================");
		
		Integer num3 = 190;
		Integer num4 = 190;
		
		if(num3 == num4) {
			System.out.println("both are equal");
		} else {
			System.out.println("both are not equal");
		}
		
		// o/p => both are not equal
		
		//This is happen bcaz of Integer caching
		//Integer caching range is -128 to 127
		// If you give number in this range then Integer caching is happen
		
		
		Integer num5 = 120;
		Integer num6 = 120;
		
		if(num5 == num6) {
			System.out.println("both are equal");
		} else {
			System.out.println("both are not equal");
		}
		
		//O/p : Both are equal
		//Same thing happen for negative number
		
		//This feature was introduced in Java 5 in order to improve memory management. 
		// Java keeps holds variable value in integer cache in range of -128 to 127
		//This Integer Cache works only on autoboxing 
		
		
		int num7 = -128;
		int num8 = -128;
		
		if(num7 == num8) {
			System.out.println("both are equal");
		} else {
			System.out.println("both are not equal");
		}
		//autoboxing is there from java5 onwards
		//o/p : Both are equal
	}
}

```
# 6. What is NAN? Not a number, How nan is defined in diff language.

## What is Nan?
Not a number i.e undefined number  
When u perform floating point operation like sqrt of negative number, modulus, divide by 0.0

```java
package com.adi;

public class Demo {

	public static void main(String args[]) {

		//System.out.println(2/0); or 0/0  same result Exception in thread "main" java.lang.ArithmeticException: / by zero
		
		System.out.println(1.0 /0.0); // or 2.0/0.0 or 1/0.0    ===>  Infinity		
	
		System.out.println(0.0/0.0); // NaN    This number is actually not defined
		
		System.out.println(Math.sqrt(-1)); //NAN sqrt of negative number is not defined
		
		System.out.println(2.1 % 0); // NaN
		
    	//System.out.println(1 % 0); // Exception in thread "main" java.lang.ArithmeticException: / by zero
		
		
	}
}

```

```java
package com.adi;

public class Demo {

	public static void main(String args[]) {
		
		//Generate a NaN number
		System.out.println(Float.NaN); // NaN 
		
		//Compare NaN number with another one
		System.out.println(Float.NaN == Float.NaN); //false 2 NaN numbers are not equal
		
		System.out.println(Float.NaN != Float.NaN); //true
		
		double nan = 2.1 % 0;
		
		System.out.println((2.1 % 0) == nan); //false
		
		System.out.println(nan == nan); //false
		
		
	}
}
```
# 7. What will be the output when you divide the number by zero?

```java
package com.adi;

public class Demo {

	public static void main(String args[]) {
		
		//Number  = Integer , Double , Float
		
		//Arithmetic exception happen only in case of Integer		
		//Integer
//		System.out.println(9/0);  Exception in thread "main" java.lang.ArithmeticException: / by zero		
//		System.out.println(0/0); Exception in thread "main" java.lang.ArithmeticException: / by zero		
		System.out.println(10 /0.0); // Infinity
		
		//Floatig or Double		
		//A floating or double number if divide by 0 or 0.0 it will give infinity
		System.out.println(9.0 / 0); //Infinity		
		System.out.println(9.1F/0); // Infinity		
		System.out.println(91.99D / 0); //Infinity		
		System.out.println(9.0 / 0.0); // Infinity
		
		System.out.println(0.0 /0); //NaN 0.0 is undefined number
		System.out.println(0.0 /0.0); //NaN	
		
	}
}
```
# 8. What's output when print a long number with L or without L suffix in Java?
```java
package com.adi;

public class Demo {

	public static void main(String args[]) {
		
		// 1000 * 60 * 60 * 24 * 365 = 31536000000
		
		long longNumberWithoutL = 1000*60*60*24*365;
		long longNumberWithL = 1000*60*60*24*365L;
		
		System.out.println(longNumberWithoutL);//1471228928
		
		System.out.println(longNumberWithL);//31536000000
		
				
		// 31536000000 -- 36 bits representation
			//Decimal to binary conversion
			//11101010111101100010010110000000000   
		
		// Max limit of integer : 2147483647 i.e 32 bits
//		System.out.println(Integer.MAX_VALUE);2147483647
		
		//so it will cut 4 bits from left side in above binary number 
		//java will truncate 4 Most significant bits in order to get 32 bits
		// 1010111101100010010110000000000  i.e 1471228928
		
	}
}

```
# 9. What is the MIN_Value of Double and Float in java?
```java
package com.adi;

public class Demo {

	public static void main(String args[]) {
	
		//In case of Double or Float their minimum value is positive number
		System.out.println(Double.MIN_VALUE);// 4.9E-324  is a positive number		
		System.out.println(Float.MIN_VALUE);//1.4E-45 is a positive number
		
		System.out.println(Long.MIN_VALUE); // -9223372036854775808  is a negative number
		System.out.println(Integer.MIN_VALUE); // -2147483648 is a negative number
		
		
		//Compare Double.MIN_VALUE with 0.0d which one is lowest?
		System.out.println(Math.min(Double.MIN_VALUE, 0.0d)); // 0.0 The Double.MIN_VALUE is greater than 0.0d
		System.out.println(Math.min(Float.MIN_VALUE, 0.0f));// 0.0
		
		//Compare Integer min value with 0
		System.out.println(Math.min(Integer.MIN_VALUE, 0));// -2147483648  0 is greater in case of Integer
		
		
		//Which one is bigger Double.MIN_VALUE or NEGATIVE_INFINITY
		
		System.out.println(Double.NEGATIVE_INFINITY); // -Infinity
		System.out.println(Math.min(Double.MIN_VALUE, Double.NEGATIVE_INFINITY)); // -Infinity
		
	}
}

```

# 10. Will Static Block be executed with final Variable?
![Alt text](image-1.png)

```java
package com.adi;

public class Demo {

	public static void main(String args[]) {
	
		System.out.println(Main.x);
	}	
}

class Main{
	
	public static int x = 100;
	
	static {
		System.out.println("Main- class Static block...");
	}
}
```
## What will be the output in above case?
Will static block execute along with variable or what

    Output: 
    Main- class Static block...
    100

## What happen in case of static final keyword?
![Alt text](image-2.png)
 IN order to improve performance   
 this Main.x is final so it's actually replaced with 100   in dot class file or byte code  
		so it is represent 100   
		It will directly take value of x

It will not  load the main class

![Alt text](image-3.png)

![Alt text](image-4.png)

Check via online code decompiler

# 11. How many String Objects will be created? String Object and String Constant pool

You can create String object via  2 types. 
1) via String literals
2) via String objects

## Via String Objects
![Alt text](image-5.png)

So whenever we create String object via new keyword, One object is created in side heap memory and one object created inside SCP(provided it is not present earlier.)

SCP is created for memory optimization/ performance.

![Alt text](image-6.png)

SCP mein New World pehle se hai toh wapas se create nahi karenga n2 usme New World

## Via String literal
String s1 ="Hello World";

![Alt text](image-7.png)

When you create s3 = "Hello World"; It is already their in SCP so  it won't create.
Whenever you create object with string literal, the object is created in SCP but before that it will check inside SCP that the object is already present or not. And if present won't create if not then create.

```java
package com.adi;

public class Demo {

	public static void main(String args[]) {
	
		String s1 = "Hello World";
		String s2 = "Hello World";
		String s3 = s1;
		
		String n1 = new String("Hello World");
		String n2 = new String("Hello World");
		
		/*
		 * How many String object will be created?
		 *      3 (1 in SCP 2 in heap)
		 * */
		
		System.out.println(s1 == s2); // true
		System.out.println(s2 == s3); // true
		System.out.println(s1 == s3); // true

        System.out.println(n1 == n2); // false
        System.out.println(n1 == s3); // false

        // == operator compare refrences
	}	
}


```
![Alt text](image-8.png)

# 12. Pass null argument with method overloading of String and Object types

```java
package com.adi;

public class Demo {

	public static void main(String args[]) {
	
		// method overloading - With in same class - same method name but diff types of parameter
		//		sequence of parameter is also diff is called method overloading 
		
		
		Demo.test(1, 1.2F); // Hello test Int float
		Demo.test(3.4F, 1); // Hello test  float   Int
		
	}	
	
	public static void test(int a, float b) {
		System.out.println("Hello test Int float");
	}
	
	public static void test( float b, int a) {
		System.out.println("Hello test  float   Int");
	}
}

```

```java
package com.adi;

public class Demo {

	public static void test(Object o) {
		System.out.println("Object Argumnet");
	}
	
	public static void test(String s) {
		System.out.println("String Argumnet");
	}
	
	
	public static void main(String args[]) {
	
		//Object is superclass of String, and both can have null values
		
		test(null); // String Argumnet

		//For null String is quite obvious data type. So Compiler will go with String
	
	}	

}


```

## What happen with try to overload with StringBuffer or StringBuilder
![Alt text](image-9.png)

# 13. Top 10 Static & Instance block based interview question.

## Explain static block in java?

```java
package com.adi;

public class Demo {

	//static block is written using static keyword
	static {
		System.out.println("static block");
	}
	
	
	public static void main(String args[]) {	
		
	}	

}
```
    output: static block
When you run the main method of class. The class load itself and static block is execute.

```java
package com.adi;

public class Demo {

	//static block is written using static keyword
	static {
		System.out.println("static block");
	}
	
	
	public static void main(String args[]) {	
		
		System.out.println("Main method");
	}	

}
```
      Output : static block   
               Main method

Whenever Jvm load the class the static class is executed even before main method.

### Can we have n number of static block. Yes
```java
package com.adi;

public class Demo {

	
	static {
		System.out.println("static block 1");
	}
	static {
		System.out.println("static block 2");
	}
	
	
	public static void main(String args[]) {	
		
		System.out.println("Main method");
	}	

}

```
    Output : static block 1
             static block 2
                Main method

### static block is written anywhere in your class. The output is in what matter you written .
```java
package com.adi;

public class Demo {

	
	static {
		System.out.println("static block 5");
	}
	static {
		System.out.println("static block 2");
	}
	
	
	public static void main(String args[]) {	
		
		System.out.println("Main method");
	}	
	
	static {
		System.out.println("static block 1");
	}
	static {
		System.out.println("static block 3");
	}
}
static block 5
static block 2
static block 1
static block 3
Main method

```
## Q.2) How can we run a java program without making any object?
```java
package com.adi;

public class Demo {

//Static block is called when you load the class	
	static {
		System.out.println("Static block");
	}
	
//U need call explicitly to static method
	public static void test() {
		System.out.println("testing method");
	}

//This main() method will be called by Jvm
	public static void main(String arg[]) {
		System.out.println("main method");
	}
}
Static block
main method
```

```java
package com.adi;

public class Demo {


	static {
		System.out.println("Static block");
	}
	

	public static void test() {
		System.out.println("testing method");
	}


	public static void main(String arg[]) {
		System.out.println("main method");
		
		//IN order to call static method
		test(); // call direclty or with class name
		Demo.test();
	}
}
Static block
main method
testing method
testing method

```

U don't require object in order to run the static method. And static block will be directly called at the time of class loading.

## What is the similarity between static block and static method.

### Similarity :
Both are static in nature.  
We don't need to create the object in order to call them.

### difference :
static block will be called in the moment when class is loaded.  
static method will not be called automatically, we need to call it explicitly either by direct calling or using by class name.

## can we call static method from another static method.
```java
package com.adi;

public class Demo {


	static {
		System.out.println("Static block");
	}
	

	public static void test() {
		System.out.println("testing method");
	}

	//Can we call static method i.e test() method inside another static i.e cover() method
	public static void cover() {
		System.out.println("Cover method");
		test();
	}


	public static void main(String arg[]) {
		System.out.println("main method");
	
		cover();
	}
}

Static block
main method
Cover method
testing method
```
## How can we create an objects if we make our constructor private.
We can do this via 1) static block 2) static mehtod

```java
package com.adi;

public class Demo {

	//How can we create an objects if we make our constructor private
	
	int age;
	
	//We can create object of this class inside this class since this constructor 
	// can only access within the class.
	// outside of the class it is not accessible.
	private Demo() {
		age =30;
	}
	
	public static void main(String arg[]) {
		
		Demo demo = new Demo();
		System.out.println(demo.age);
	}
}

30
```
### Can we access this object outside of class
![Alt text](image-10.png)

### via static method
```java
package com.adi;

public class Demo {

	
	int age;
	
	public static int createObject() {
		
		Demo demo = new Demo();
		demo.age=40;
		
		return demo.age;
	}

	private Demo() {
		age =30;
	}
	
	public static void main(String arg[]) {
	
	}
}
```
```java
package com.adi;

public class Test {
	
	public static void main(String arg[]) {
		
		int i = Demo.createObject();
		System.out.println(i);//40
		
	}
}

```
### via static block
```java
package com.adi;

public class Demo {

	
	 static int age;
	
	static {		
		age=50;
	}
	
	public static int createObject() {
		
		return age;
	}

	private Demo() {
		age =30;
	}
	
	public static void main(String arg[]) {
	
	}
}
```
```java
package com.adi;

public class Test {
	
	public static void main(String arg[]) {
		
		System.out.println(Demo.createObject());
	
	}
}

```
## Is it possible to compile and run java program without writing main() method?

```java
package com.adi;

public class Demo {

	//Is it possible to compile and run java program without writing main() method?
	//Yes
	//Here we create 2 static method.
	// If we need to compile and run this pgm then.
	
	static {
		System.out.println("Inside static block1");
	}
	
	static {
		System.out.println("Inside static block2");
	}
}
```
```java
package com.adi;

public class Test {
	
	public static void main(String arg[]) {
		
	Demo demo = new Demo();
	
	
	}
}
Inside static block1
Inside static block2
```
### another approach
```java
package com.adi;

public class Demo {

	static int age = 20;
	
	static {
		System.out.println("static 1");
	}
	
	static {
		System.out.println("static 2");
	}
}
```
```java
package com.adi;

//client class 
public class Test {
	
	public static void main(String arg[]) {
		
		System.out.println(Demo.age);
	
	
	}
}
static 1
static 2
20
```
## Can we initialize member variable within static block.
```java
package com.adi;

public class Demo {

	//Can we initialize member variable withing static block
	
	String name;
	
	static {
		
		Demo d = new Demo();
		d.name="ADitya"; // we can initialize memeber variable within static block.
	}
	
	public static void main(String ar[]) {
		
	}
}
```
```java
package com.adi;

public class Demo {
	
	String name;
	static int age;
	
	static {
		
		Demo d = new Demo();
		d.name="ADitya";
		age =34;
		
		System.out.println(d.name +", "+ age); //ADitya, 34
		
	}
	
	public static void main(String ar[]) {
		
	}
}
```

## What will be the output
```java
package com.adi;

public class Demo {

	//static block
	static {
		System.out.println("Static block");		
	}
	
	//instance block
	{
		System.out.println("Instance block");
	}
	
	//constructor
	Demo(){
		System.out.println("Constructor");
	}
	
	public static void main(String ar[]) {
		System.out.println("Main method");
		new Demo();
	}
}
Static block
Main method
Instance block
Constructor

```







