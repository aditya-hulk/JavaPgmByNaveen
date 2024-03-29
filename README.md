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

		//Squar rooot
		System.out.println(Math.sqrt(-1)); //NAN sqrt of negative number is not defined

		//Integer
		System.out.println(Math.sqrt(-1));// NAN
		System.out.println(Math.sqrt(0)); // 0.0
		System.out.println(Math.sqrt(1));// 1.0

		//Float
		System.out.println(Math.sqrt(0.0F)); //0.0		
		System.out.println(Math.sqrt(-1.0F)); //NaN		
		System.out.println(Math.sqrt(1.0F)); //1.0
		
		//Double
		System.out.println(Math.sqrt(0.0D)); //0.0		
		System.out.println(Math.sqrt(-1.0D)); //NaN		
		System.out.println(Math.sqrt(1.0D)); //1.0
		

		//Mod
	
		System.out.println(1 % 0);// Exception in main thread
		System.out.println(0 % 0);//  Exception in main thread
		System.out.println(-1 % 0);//  Exception in main thread

		System.out.println(-2.1F % 0);// NAN	
		System.out.println(0.0F % 0); // NaN
		System.out.println(2.1F % 0); // NaN
		
		System.out.println(-2.1D % 0);// NAN	
		System.out.println(0.0D % 0); // NaN
		System.out.println(2.1D % 0); // NaN

//  % by 0.0
			System.out.println(1 % 0.0);// NAN
		System.out.println(0 % 0.0);//  NAN
		System.out.println(-1 % 0.0);//  NAN
		
		System.out.println(-2.1F % 0.0);// NAN	
		System.out.println(0.0F % 0.0); // NaN
		System.out.println(2.1F % 0.0); // NaN
		
		System.out.println(-2.1D % 0.0);// NAN	
		System.out.println(0.0D % 0.0); // NaN
		System.out.println(2.1D % 0.0); // NaN

		
		
		
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

		//Divide Integer number by 0	
		//Integer
		//System.out.println(-1/0);  Exception in thread "main" java.lang.ArithmeticException: / by zero
//		System.out.println(9/0);  Exception in thread "main" java.lang.ArithmeticException: / by zero		
//		System.out.println(0/0); Exception in thread "main" java.lang.ArithmeticException: / by zero		
		
		
		//Floatig or Double		
		//A floating or double number if divide by 0 or 0.0 it will give infinity
		System.out.println(-9.0 / 0);//-Infinity
		System.out.println(9.0 / 0); //Infinity		
		System.out.println(9.1F/0); // Infinity		
		System.out.println(91.99D / 0); //Infinity		
		
		
		System.out.println(0.0 /0); //NaN 0.0 is undefined number

//Divide number by 0.0
		System.out.println(10 /0.0); // Infinity
		System.out.println(0 / 0.0);//NaN
		System.out.println(-11 /0.0); // -Infinity

		System.out.println(9.0 / 0.0); // Infinity
		System.out.println(-9.0F / 0.0);// -Infinity
		
		System.out.println(9.0F / 0.0);// Infinity
		System.out.println(9.0D / 0.0);// Infinity
		System.out.println(-9.0D / 0.0);// -Infinity

		
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
		age =34; // we can easily initialize static variable inside static block
		
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
	
	public static final int x = 20;
	
	public static void main(String ar[]) {
		System.out.println(Demo.x); // 20
		//This is called compiler optimization, Compiler will do performance activity here. 
		//In order to improve performance Demo.x is replace by 20 at compile time in dot class 
		//file  since  x is final static in nature.
		
	}
}
```
### 2nd
```java
package com.adi;

public class Demo {

	//static block
	static {
		System.out.println("Static block");		
	}
	
	public static  int x = 20; // it's not final it's static in nature and whenever you try to approach this variable, the static block also get  executed.

	
	public static void main(String ar[]) {
		System.out.println(Demo.x); 
	}
	static block
	20
}
```
### 3rd
```java
package com.adi;

public class Demo {

	//static block
	static {
		System.out.println("Static block");		
	}
	
	public final  int x = 30;
	
	public static void main(String ar[]) {
		System.out.println(new Demo().x);  //In order to call x, class is need to load by calling constructor so definately static block is going to execute.
	}
	
	Static block
	30
}
```
## Following output

```java
package com.adi;

public class Demo {

	//static block
	static {
		System.out.println("Static block");		
	}
	
	//instance initialization block
	{
		System.out.println("Instance block");
	}
	
	//constructor
	Demo(){
		System.out.println("Constructor");
	}
	
	public static void main(String ar[]) {
		System.out.println("Main method"); //I am not creating the object of this class so constructor and instance block has not chance 
		//so technically no instance is created so either constructor or instance block will not be executed here.
		
	}
	
	Static block
	Main method
}
```
### 2nd
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
		new Demo(); //Now you are creating object of this class so construtor and instance block will be executed.

		// first instance block is geeting executed and then constructor this is order
	}
}
Static block
Main method
Instance block
Constructor

```
# 14. How System.out.println() works internally in java?
![Alt text](image-11.png)

## 1st part
System is a class  
out is a refrence variable of PrintStream class  
println() is a method of PrintStream class  

out is a static variable so you can call via class name
and you pass string arrgument
![Alt text](image-12.png)

## 2nd part :- How println() method work in PrintStream class?

println() method -> internally calls writeln() method 

writeln() method -> intrenally calls newLine() method

newLine() method -> intrenally calls flushBuffer()  method and all stuffs.

So in this way output is going to printed.

## 3rd part:- Can we create an object of System class?
![Alt text](image-13.png)
No, Since  Not only System class is a final class  but also its constructor is also private.

All the refrence variable present in System class are static in nature. So they can call directly with respect to class name.

And  also variable are final in nature, so that once you assigned value to it no one can change.

Eg: PrintStream in, PrintStream out and PrintStream err are static and final refrence variable present in System class.

 	 public static final PrintStream err = null;
	  public static final PrintStream out = null;
	   public static final InputStream in = null;

## 4rth part:- 
	public static final PrintStream out = null;   
***Observe this :   out is set to null by default,
so when you write System.out.println() it's null.sth leads to Null Pointer Exception. But in our case the value is going to printed***

### So where out variable is getting initialized?
The out variable is initialized internally by Jvm.

In System class we have methods like   

		setIn() for inputStream in and
	     setOut()  for PrintStream out

***When System class is loaded all it's refrence variable is loaded, then in order to initialize out variable Jvm internally calls setOut() method.By passing out variable as paramater.***

The setOut() method interanally calls -> setOut0() method.

the setOut0() method is a native method. A native method is sth which is written in C language.

And the setOut0() method is called by JvmJni(java native interface ) in order to initialize out variable.

# 15. Maximum number of method parameter allow in java.

Limit of parameter   
For  datatypes byte, short, int, float, boolean, classtype ->  limit is 254(non static method) or 255(static method)

![Alt text](image-14.png)
![Alt text](image-15.png)

## For static method
```java
package com.adi;

public class Demo {

	// Maximum number of parameter allow in java

	// Creating non static function
	// Q) how many parmeter will be allowed in it.
	public void testing( int a1, int a2, int a3, int a4, int a5, int a6, int a7, int a8, int a9, int a10,
			int a11, int a12, int a13, int a14, int a15, int a16, int a17, int a18, int a19, int a20, int a21, int a22,
			int a23, int a24, int a25, int a26, int a27, int a28, int a29, int a30, int a31, int a32, int a33, int a34,
			int a35, int a36, int a37, int a38, int a39, int a40, int a41, int a42, int a43, int a44, int a45, int a46,
			int a47, int a48, int a49, int a50, int a51, int a52, int a53, int a54, int a55, int a56, int a57, int a58,
			int a59, int a60, int a61, int a62, int a63, int a64, int a65, int a66, int a67, int a68, int a69, int a70,
			int a71, int a72, int a73, int a74, int a75, int a76, int a77, int a78, int a79, int a80, int a81, int a82,
			int a83, int a84, int a85, int a86, int a87, int a88, int a89, int a90, int a91, int a92, int a93, int a94,
			int a95, int a96, int a97, int a98, int a99, int a100, int a101, int a102, int a103, int a104, int a105,
			int a106, int a107, int a108, int a109, int a110, int a111, int a112, int a113, int a114, int a115,
			int a116, int a117, int a118, int a119, int a120, int a121, int a122, int a123, int a124, int a125,
			int a126, int a127, int a128, int a129, int a130, int a131, int a132, int a133, int a134, int a135,
			int a136, int a137, int a138, int a139, int a140, int a141, int a142, int a143, int a144, int a145,
			int a146, int a147, int a148, int a149, int a150, int a151, int a152, int a153, int a154, int a155,
			int a156, int a157, int a158, int a159, int a160, int a161, int a162, int a163, int a164, int a165,
			int a166, int a167, int a168, int a169, int a170, int a171, int a172, int a173, int a174, int a175,
			int a176, int a177, int a178, int a179, int a180, int a181, int a182, int a183, int a184, int a185,
			int a186, int a187, int a188, int a189, int a190, int a191, int a192, int a193, int a194, int a195,
			int a196, int a197, int a198, int a199, int a200, int a201, int a202, int a203, int a204, int a205,
			int a206, int a207, int a208, int a209, int a210, int a211, int a212, int a213, int a214, int a215,
			int a216, int a217, int a218, int a219, int a220, int a221, int a222, int a223, int a224, int a225,
			int a226, int a227, int a228, int a229, int a230, int a231, int a232, int a233, int a234, int a235,
			int a236, int a237, int a238, int a239, int a240, int a241, int a242, int a243, int a244, int a245,
			int a246, int a247, int a248, int a249, int a250, int a251,
			int a252, int a253, int a254) {
		
		

	}

	public static void main(String ar[]) {

	}
}
```
***For static method (int datatype) 254 parameter is allowed.***
#### If we try to add one more paramter
![Alt text](image-16.png)

![Alt text](image-17.png)

## For static method 
255 parameter is allowed (for datatype int)
![Alt text](image-18.png)

![Alt text](image-21.png)

![Alt text](image-22.png)


#### If we try to allowed 1 more parameter in static method then error
![Alt text](image-19.png)

## for double and long - - the maximum amount of parameter we pass is 127 only(including static and non static method).

![Alt text](image-23.png)

![Alt text](image-24.png)

Only 127 is allowed

## Tricky part
### How many bytes double will take?   
double/ long both takes 8 bytes

int  -> 4 bytes

So double can be replace by 2 int.

![Alt text](image-25.png)


the moment you add 1 more int parameter
![Alt text](image-26.png)

So you can create number of combinations of int and double just take care of bytes.

### classtypes means  object refrences
![Alt text](image-28.png)

![Alt text](image-27.png)

Any classtype you can pass here.

# 16 Find duplicate element in an Array.

## 1. via brute force mechanism
```java
package com.adi;

public class Demo {

	public static void main(String ar[]) {
		
		//String array
		String[] infra = {"Amazon","GCP","Azure","Amazon","Ali Baba","SauceLabs","Azure","GCP"};
		
		System.out.println("*********brute force***********");
		
		for(int i=0;i<infra.length;i++) {
			//here i will compare Amazon with GCP 
			//so i is 0(Amazon) and j is i+1(GCP)
			for(int j=i+1;j<infra.length;j++) {
				
				//if array[i] equals to arr[j] then duplicate element is found
				if(infra[i].equals(infra[j])) {
					System.out.println(infra[i]);
				}
			}
		}
	}
}
*********brute force***********
Amazon
GCP
Azure

```
Time Complexity is n2 (due to outer loop and inner loop)
## 2. via HashSet
```java
package com.adi;

import java.util.HashSet;
import java.util.Set;

public class Demo {

	public static void main(String ar[]) {
		
		//String array
		String[] infra = {"Amazon","GCP","Azure","Amazon","Ali Baba","SauceLabs","Azure","GCP"};
		
		System.out.println("*********Hash Set***********");
		
		//Create an object of Set
		Set<String> data = new HashSet<>();
		
		//iterate array via forEach
		for(String e : infra) {
			
			//Adds the specified element to this set if it is not already present 
			//adds the specified element e to this set if the set contains no element e2 such that Objects.equals(e, e2). 
			//If this set already contains the element, the call leaves the set unchanged and returns false
			
			//Means ye Set i.e data mein add() jab chalengi wo check karnega Amazon set mein add hai kya.. 
			//nhi hai to Add karke true return karnega
			//Next time jab Amazon aavenga.. wo Set mein add nhi kar pavenga... Aur false return karenga			
			if(data.add(e) == false) {
				System.out.println(e);
			}
		}
	
		//Remember HashSet do not store the duplicate elements.
		
	}
}
*********Hash Set***********
Amazon
Azure
GCP

```

## 3. via HashMap
HashMap store elements in Key-Value pair format.
```java
package com.adi;

import java.util.HashMap;
import java.util.Map;
import java.util.Map.Entry;
import java.util.Set;

public class Demo {

	public static void main(String ar[]) {
		
		//String array
		String[] infra = {"Amazon","GCP","Azure","Amazon","Ali Baba","SauceLabs","Azure","GCP"};
		
		System.out.println("*********Hash Map***********");
		
		//Key is store in the form of String
		//how many repetation i.e Value in the form of Integer
		Map<String, Integer> infraMap = new HashMap<String,Integer>();
		
		for(String e: infra) {
			
			//It HashMap(InfraMap) contains key then it will return it's value or null
			Integer count = infraMap.get(e);
			
			if(count == null) {
				//count = null means elment nahi hai HashMap mein so add it and value 1 dedo
				infraMap.put(e, 1);
			}else {
				// yaha par count null nahi hai so again add element and increment count 
				infraMap.put(e, ++count);
			}
			
		}
		
		//Print duplicate element
		//With this entrySet sari hashmap aa gyi
		//iteration ke liye achaa
		// entry set mein entry hoti hai
		Set<Entry<String, Integer>> entrySet = infraMap.entrySet();
		
		for(Entry<String, Integer> entry : entrySet) {
			
			//yadi value 1 se jayda hai so duplicate hai
			if(entry.getValue() > 1) {
				
				//print key
				System.out.println(entry.getKey());
			}
		}
		
	}
}
*********Hash Map***********
Azure
GCP
Amazon

```
## 4. via Stream  via Set & filter 
```java
package com.adi;

import java.util.Arrays;
import java.util.HashSet;
import java.util.Set;
import java.util.stream.Collectors;

public class Demo {

	public static void main(String ar[]) {
		
		//String array
		String[] infra = {"Amazon","GCP","Azure","Amazon","Ali Baba","SauceLabs","Azure","GCP"};
		
		System.out.println("*********Stream via Set & filter***********");
		
		//Maintain a HashSet
		//HashSet store unique elements
		Set<String> dataSet = new  HashSet<>(); 
		
				
		//Convert your String Array into list via asList() in order to apply Stream.
		// Stream is apply on Collection basically
		
		//Regarding filter 
		// hashSet(dataSet) has add() method
		//   which give boolean value 
		// if element is present then it will return false(not added that element)
		//if element is not present then it will return true(added that element into Set)		
		//			!dataSet.add(e) means add elements which are duplicate.
		//    since filter method is  performing intermediate operation
		
		//Regarding collect
		//  it perform terminal operation
		//   collect everything into Set
		
		Set<String> dupliSet = Arrays.asList(infra).stream()
					.filter(e -> !dataSet.add(e))
					.collect(Collectors.toSet());
		
		System.out.println(dupliSet);

		
	}
}
*********Stream via Set & filter***********
[Azure, GCP, Amazon]
```
## 5. Stream via groupingBy
```java
package com.adi;

import java.util.Arrays;
import java.util.Map;
import java.util.Set;
import java.util.function.Function;
import java.util.stream.Collector;
import java.util.stream.Collectors;

public class Demo {

	public static void main(String ar[]) {
		
		//String array
		String[] infra = {"Amazon","GCP","Azure","Amazon","Ali Baba","SauceLabs","Azure","GCP"};
		
		System.out.println("*********Stream via groupingBy***********");
		
		//Convert it into List
		// Since stream can be apply on collections
		
		//Here we use groupingBy- classifier
		// basically grouping object by some property
		
		// About Funciton.identity() 
		//  Returns a function that always returns its input argument.
		
		// About Collectors.counting()
		// Returns a Collector accepting elements of type T that counts the number of input elements.
		//   Basically it will count the number of elements
		
		// About entrySet() 
		//   covert everything into entrySet
		//    Remember in Key is unique in entrySet value means number of repeatation.
		
		//filter(e -> e.getValue()>1)
		//  compare entrySet value is greater than 1 then it's duplicate
		
		//map(Map.Entry::getKey);
		// satisfied condition fetch the key 
		
		// collect them in Set
		
		Set<String> eleSet = 
				Arrays.asList(infra)
				   .stream()
					.collect(Collectors.groupingBy(Function.identity(),Collectors.counting()))
					.entrySet()
					 .stream()
					  .filter(e -> e.getValue()>1)
					   .map(Map.Entry::getKey)
					    .collect(Collectors.toSet());
		
		
		System.out.println(eleSet);
		
		/*
		 * Convert your String[] i.e infra into ArrayList
		 *   Getting a list  then taking a stream
		 *    put a Collection over here
		 *  means grouping By Function.identity() means
		 *    from stream source keep collecting data and 
		 *      group on the basis of identity and keep counting it.
		 *    means it maintain the counting also( key(identity) and it's counting)
		 *      and then give me entrySet() out of it
		 *   it will generate internal map here containing (key and value)
		 *     use stream () on it and filter
		 *   filter you write on the basis of Stream e.getValue() > 1 means duplicate element
		 * we use map Map.Entry calling getKey which satisfy the condition
		 *   and finally collect the set over here.   		 *
		 * */
	}
}
*********Stream via groupingBy***********
[Azure, GCP, Amazon]

```
## 6. via Stream using frequency
```java
package com.adi;

import java.util.Arrays;
import java.util.Collections;
import java.util.List;
import java.util.Set;
import java.util.stream.Collectors;

public class Demo {

	public static void main(String ar[]) {
		
		//String array
		String[] infra = {"Amazon","GCP","Azure","Amazon","Ali Baba","SauceLabs","Azure","GCP"};
		
		System.out.println("*********Stream via frequency ***********");
		
		//Convert your array into list and apply Stream
		
		//About frequency()
		// Returns the number of elements in the specified collection equal to the specified
		//   object. 
		// returns the number of elements e in the collection 
		// Require 2 things
		//  collection on which frequency determine and  on which object e i.e  on all object
		//   if frequency is greater than 1
		
		// collect it into Set
		
		List<String> list = Arrays.asList(infra);
			  
		Set<String> eleList = 
				list.stream()
					 .filter(e -> Collections.frequency(list, e) > 1)
					  .collect(Collectors.toSet());
		
		System.out.println(eleList);
	}
}
*********Stream via frequency ***********
[Azure, GCP, Amazon]

```
# 17. Star pattern Logic- Part1
![Alt text](image-29.png)
![Alt text](image-30.png)

we have to start with 2 outer loop, 1 is for row and anotherone is for column.

outer loop -set limit  
inner loop - always depend upon outer loop  

row is also increasing i.e i++  
if you see the dig- col is increase i.e j++

![Alt text](image-31.png)

```java
package com.adi;

public class Demo {

	public static void main(String ar[]) {
		
		for(int i=0; i<=4; i++) {
			for(int j=0; j<=i; j++) {
				System.out.print(" * ");
			}
			System.out.println();
		}
	}
}
Output:
 * 
 *  * 
 *  *  * 
 *  *  *  * 
 *  *  *  *  * 

```
## Wrong logic
![Alt text](image-32.png)

## Reverse pattern
![Alt text](image-33.png)

![Alt text](image-34.png)

![Alt text](image-35.png)

```java
package com.adi;

public class Demo {

	public static void main(String ar[]) {
		
		for(int i=0; i<=4; i++) {
			for(int j=4; j>=i; j--) {
				System.out.print(" * ");
			}
			System.out.println();
		}
	}
}
Output:
 *  *  *  *  * 
 *  *  *  * 
 *  *  * 
 *  * 
 * 

```
## Require this pattern:
![Alt text](image-36.png)

slightly change in code.
![Alt text](image-37.png)

# 18 star patter part-2
![Alt text](image-38.png)

![Alt text](image-39.png)

![Alt text](image-40.png)

![Alt text](image-41.png)

```java
package com.adi;

public class Demo {

	public static void main(String ar[]) {
		
		
		for(int i=1; i<=4; i++) {
			
			for(int j=3; j >=i; j--) {
				
				System.out.print("-");
			}
			
			for(int k=1;k<=i;k++) {
				System.out.print("*");
			}
			
			System.out.println();
		}

	}
}
Output:
---*
--**
-***
****


```

# 19. Pyramid pattern logic
![Alt text](image-42.png)
![Alt text](image-44.png)

![Alt text](image-43.png)

![Alt text](image-45.png)

# 20. Alphabetic pattern logic
![Alt text](image-46.png)

![Alt text](image-47.png)

```java
package com.adi;

public class Demo {

	public static void main(String ar[]) {

		int alpha = 65;
		for (int i = 0; i <= 5; i++) {

			for (int j = 0; j <= i; j++) {

				System.out.print((char) (alpha + j) + " ");
			}

			System.out.println();
		}

	}
}
Ouput:
A 
A B 
A B C 
A B C D 
A B C D E 
A B C D E F 

```
## If you want to print pyramid having small a
```java
package com.adi;

public class Demo {

	public static void main(String ar[]) {

		int alpha = 97;
		for (int i = 0; i <= 5; i++) {

			for (int j = 0; j <= i; j++) {

				System.out.print((char) (alpha + j) + " ");
			}

			System.out.println();
		}

	}
}
Output:
a 
a b 
a b c 
a b c d 
a b c d e 
a b c d e f 

```
# 23. Alphabetic logic pattern Part-5

![Alt text](image-48.png)

![Alt text](image-49.png)

![Alt text](image-50.png)

```java
package com.adi;

public class Demo {

	public static void main(String ar[]) {

		int alpha = 65;
		for (int i = 0; i <= 5; i++) {

			for (int j = 0; j <= i; j++) {

				System.out.print((char) (alpha) + " ");
			}
			
			alpha++;
			
			System.out.println();
		}

	}
}
Output:
A 
B B 
C C C 
D D D D 
E E E E E 
F F F F F F 
```

## If you won't increment alpha what happened
![Alt text](image-51.png)

![Alt text](image-52.png)

![Alt text](image-53.png)

## A-Z Askii range - 65 to 90  
## a-z range is 97 to 122 

# 21. How to print count of duplicate character from String?  Hackerrank
![Alt text](image-54.png)

3 important condition  
1) when string is null
2) when given string is empty
3) when given string has 1 character or lenght is 1 then return nothing.

```java
package com.adi;

import java.util.HashMap;
import java.util.Map;
import java.util.Map.Entry;
import java.util.Set;

public class Demo {

	public static void main(String ar[]) {

		printDuplicateCharacters("JavavavaJJ");
		printDuplicateCharacters(null);
		printDuplicateCharacters("A");
		printDuplicateCharacters("");
	}
	
	public static void printDuplicateCharacters(String str) {
		
		if(str == null) {
			System.out.println("Null String");
			return ; // return nothing
		}
		
		if(str.isEmpty()) {
			System.out.println("Empty String");
			return ;
		}
		
		if(str.length() == 1) {
			System.out.println("Single char String");
			return ;
		}
		
		// To find duplicate character in a string
		//convert it into Character array by toCharArray()
		
		char[] wordsArray = str.toCharArray();
		
		
		//Creating HashMap where as key is Character and Value(how many time the character apperas) as Integer
		
		Map<Character, Integer> charMap = new HashMap<>();
		
		
		//Travers charArray via for loop
		
		for(Character ch : wordsArray) {
			//map has containsKey() 
			//Returns true if this map contains a mapping for the specified key.
			
			if(charMap.containsKey(ch)) {
				
				// map.get(key) return value 
				// whatever value return increment it by 1.
				charMap.put(ch, charMap.get(ch) + 1);
			}
			else {
				charMap.put(ch, 1);
			}
		}
		
		
		//print here
		// take entrySet out of Map
		Set<Map.Entry<Character, Integer>> entrySet = charMap.entrySet();
		
		//Take 1 entry out of  set of entrySet
		for(Map.Entry<Character, Integer> en : entrySet) {
			
			if(en.getValue() > 1) {
				System.out.println(en.getKey() + " : " + en.getValue());
			}
		}
		
		
	}
}
Ouptut:
a : 4
v : 3
J : 3
Null String
Single char String
Empty String
```

### Always handle null check at first place immediately.

# 22. Count the occurences of a charcter in a String.

String str = "I love coding";  
how many time o comes  
o : 2  
I : 1  

## Here you can add null check, empty string, also single char string.
## via charArray  --- for loops

```java
package com.adi;

public class Demo {

	public static void main(String ar[]) {

		String str = "I love coding";
		
		//maintain 1 character count
		int count = 0;
		
		for(char ch : str.toCharArray()){
			
			if(ch == 'o') {
				count++;
			}
		}
		
		System.out.println("o : "+ count); //o : 2
		
	}		
}
```
```java
package com.adi;

public class Demo {

	public static void main(String ar[]) {
		String str = "I love coding";
		
		getCharOccurence(str, 'o'); //o : 2

	}
	
	public static void getCharOccurence(String str, char value) {

		// maintain 1 character count
		int count = 0;

		for (char ch : str.toCharArray()) {

			if (ch == value) {
				count++;
			}
		}

		System.out.println(value + " : " + count);
	}

}
```

## via str.len -- charAt(i)
```java
package com.adi;

public class Demo {

	public static void main(String ar[]) {
		String str = "I love coding and testing";

		getCharCount(str, 'i'); // i : 2
	}

	public static void getCharCount(String str, char value) {

		int count = 0; // maintain a counter

		for (int i = 0; i < str.length(); i++) {

			if (str.charAt(i) == value) {
				count++;
			}
		}

		System.out.println(value + " : " + count);
	}
}
```
## via streams
```java
package com.adi;

public class Demo {

	public static void main(String ar[]) {
		String str = "I love coding and testing";

		// String.char() method give IntStream (integer stream- primitive stream)
		//  since we can't apply Stream on String so we need to convert them to Collections
		
		//mapToObject() - It will map object to Stream
		//Returns an object-valued Stream consisting of the results 
		  //of applying the given function to the elements of this stream. 
		
		//String.valueOf()
		  //Returns the string representation of the Object argument.
		//String.valueOf(iNum): Returns the string representation of int iNum.
		
		//typecaset means e is not object , e is charcter and 
		// we convert charcter into String.
		
		//then filter it e.equals("i") 
		//here  e is object it's value is i and 
		//"i" --> String  i.e object whose value is i
		// so compare and  count it.
		
		long count = str.chars()
			.mapToObj(e -> String.valueOf((char)e))
				.filter(e -> e.equals("i"))
				 .count();
		 
		System.out.println( " i : " + count); // i : 2

	}

}
```

```java
package com.adi;

public class Demo {

	public static void main(String ar[]) {
		String str = "I love coding and testing";

		getCharCountUsingStreams(str,"i"); //i : 2

	}

	public static void getCharCountUsingStreams(String str,String value) {
		
		long count = str.chars()
				.mapToObj(e -> String.valueOf((char)e))
					.filter(e -> e.equals(value))
					 .count();
			 
			System.out.println(value + "  : " + count); 
		
	}
}
```

## via ApacheCommon StringUtils 
we require apache commons lib

jar file issue... so i used maven project and add this dependency
![Alt text](image-55.png)

```java
package com.adi.rest;

import org.apache.commons.lang3.StringUtils;

public class Test {
	public static void main(String a[]) {
		
		String str = "I love coding";
		
		int count = StringUtils.countMatches(str, "o");
		
		System.out.println("o : "+ count); // o:2
	}
}

```
# 24. What will be the output for the following?

```java
package com.adi;

public class Test {

	public static void main(String arg[]) {

		int i = (byte) + (char) - (int) + (long) - 1;
		
		/*
		 * here it will start from right to left
		 * 
		 * 	(byte) + (char) - (int) + (long) - 1;
		 *    long - 1 ==> -1 is casted into long ()  so it will give  -`1
		 *    
		 *    (byte) + (char) - (int)  - 1;
		 *    int - 1 ==> again 1 is converted into int so -1
		 *    
		 *    (byte) + (char) - * - 1
		 *    (byte) + (char) + 1
		 *    char -1 * -1 = char + 1 ==> + 1 not harm anything 1
		 *    
		 *    (byte)  + 1
		 *    byte + 1 ==> 1 only given 
		 * */
		System.out.println(i); // 1
		
		long j = (long) - 1;
		System.out.println(j); // -1 
		
		int k = - (int) - 1;
		System.out.println(k); //1 
		
		int l = (int) - 1;
		System.out.println(l); // -1 
		
		int m = (char) + 1;
		System.out.println(m); // 1
		
		int n = (byte) + 1;
		System.out.println(n); // 1 
		
		
	}
}

```

# 25. How to escape special characters in java?
```java
package com.adi;

public class Demo {

	public static void main(String ar[]) {
	
		// 1)  Print /"hello"/
		
//		System.out.println("/"hello"/"); // Invalid Assignment operator
		System.out.println("/\"hello\"/"); //   /"hello"/
		
		// 2) print /'hello'/
		System.out.println("/'hello'/");  // /'hello'/		
		// 3) print '/'hello'/'
		System.out.println("'/'hello'/'"); //  '/'hello'/'
		
		//4) "/'hello'/"
		System.out.println("\"/'hello'/\"");  // "/'hello'/"
		
		//5) "hello"
		System.out.println("\"hello\""); // "hello"
		
		// 6) I love "java" & "programming"
		System.out.println("I love \"java\" & \"programming\""); // I love "java" & "programming"
		
		//7) 'I love "java" & "ram"'
		System.out.println("'I love \"java\" & \"ram\"'"); // 'I love "java" & "ram"'
		
		//8) //input[@id='name'] for method
		System.out.println(getXpath("Aditya")); // input[@id='name']
		
		//9) //input[@id='name'] for method
		System.out.println(getXXpath("Aditya")); // input[@id='Aditya']
	}
	
	public static String getXpath(String name) {
		String xpath = "//input[@id='name']";
		
		return xpath;		
	}
	
	public static String getXXpath(String name) {
		String xpath = "//input[@id='"+name+"']";
		
		return xpath;		
	}

}
```
# 26. Create a language Translator & Autobots || Reflection in java

English to German tranlate  
Hello Aditya  - Hallo Aditya  
Good morning Aditya - Guten Morgen Aditya

if you write sth it will reply you back.


### This code is won't work in java 17. we have run it in older version currently exception happen. Try will lower version.

```javapackage com.adi;

import java.lang.reflect.Field;

public class Demo {

	// create a field variable here
	// use reflection
	// fetch String class value
	// setAccessible() value true
	// so that you can change the value of string
	static {

		try {
			Field value = String.class.getDeclaredField("value");

			value.setAccessible(true);

			value.set("Hello Aditya", value.get("Hallo Aditya"));

		} catch (NoSuchFieldException e) {
			e.printStackTrace();
		} catch (SecurityException e) {
			e.printStackTrace();
		} catch (IllegalArgumentException e) {
			e.printStackTrace();
		} catch (IllegalAccessException e) {
			e.printStackTrace();
		}
	}

	public static void main(String ar[]) {

		System.out.println("Hello Aditya");

	}
}
Output:

Hallo Aditya but we face an exception

```

# 27. Can we executes comments in java?

![Alt text](image-56.png)

![Alt text](image-57.png)

![Alt text](image-58.png)

unicode character - carriage return representing new line

# 28. What will be the output when you compare site url with it's ip address.

```java
package com.adi;

import java.net.MalformedURLException;
import java.net.URL;

public class Demo {

	public static void main(String ar[]) {

		try {
			
			//write proper url with proper ip address
			System.out.println(new URL("https://app.hubspot.com").equals(new URL("https://104.19.154.83"))); //true
			
		} catch (MalformedURLException e) {
			e.printStackTrace();
		}

	}
}
```
# 29. Find out missing number in an integer array.

humko ek integer array diya hai and find out which element is missing
![Alt text](image-59.png)

```java
package com.adi;

public class Demo {

	public static void main(String ar[]) {

		int num[] = { 1, 2, 3, 5 };

		int j = findMissingNumber(num, 5);
		
		System.out.println("Number missing is = "+j); //Number missing is = 4

	}

	// Give me array and give me total Number of count that i am expecting
	
	public static int findMissingNumber(int[] num, int totalCount) {

		int expectedSum = totalCount * ((totalCount + 1) / 2);

		int actualSum = 0;

		// traverse array in order to find summation.
		
		for (int i : num) {

			actualSum += i;
		}
		return expectedSum - actualSum;
	}
}
```
# 30. How to find length of String in java without using length() method.

## via toCharArray().length property
```java
package com.adi;

public class Demo {

	public static void main(String ar[]) {

		String str = "testing";
		
		//Convert String into Character array and use it's length property/variable. 
		System.out.println(str.toCharArray().length); // 7
	}

}
```

## via lastIndexOf() 
```java
package com.adi;

public class Demo {

	public static void main(String ar[]) {

		String str = "testing";
		
		//find lastIndexOf nothing can give you length of String
		
		System.out.println(str.lastIndexOf(""));//7
	}

}
```
## via Regular Expression
```java
package com.adi.rest;

import java.util.regex.Matcher;
import java.util.regex.Pattern;

public class Demo2 {

	public static void main(String[] args) {
	
		String str = "testing";
		
		//Compiles the given regular expression into a pattern.
		 // $ - Matches the end of input.
		
		// matcher = Creates a matcher that will match the given input 
		//   against this pattern
				
		Matcher matcher = Pattern.compile("$").matcher(str);

		
		//return true if, and only if, a subsequence of the input sequence 
		//    matches this matcher's pattern
		
		
		//If the match succeeds then more information can be obtained 
		   //via the start, end, and group methods. 
				
		matcher.find();
		
		//If matches then via end() we can find the length of String.
		int length = matcher.end();
		
		System.out.println("The length of String is : "+ length); //The length of String is : 7
		
		
	}

}
```

## via split() method
```java
package com.adi.rest;

public class Demo2 {

	public static void main(String[] args) {
	
		String str = "testing";
		
		//split on the basis of nothing
		// it will give you string array 
		// and via length property we can find length
		System.out.println(str.split("").length); // 7
	}

}

```

## via normal for-loop and count
```java
package com.adi.rest;

public class Demo2 {

	public static void main(String[] args) {
	
		String str = "testing";
		
		int count = 0;
		
		//str.toCharArray() return character array
		//  via forEach loop increase count 
		
		for(char ch : str.toCharArray()) {
			count ++;
		}
		
		System.out.println(count); // 7
	}

}

```
## via try-catch block use charAt() and while loop in  method
```java
package com.adi.rest;

public class Demo2 {

	public static void main(String[] args) {
	
		String str = "testing";
		
		int lenth = getLenth(str);
		
		System.out.println(lenth); // 7
	}
	
	public static int getLenth(String str) {
		
		int i = 0;
		
		try {
			while(true) {
				
				//charAt(index) - it will give charcter available at i position
				str.charAt(i);
				
				//i increase so when reach at end of String 
				// throw an IndexOutOfBoundException
				i++;
			}
		}catch (Exception e) {
				
			return i;
		}
		
	}

}

```

```java
package com.adi.rest;

public class Demo2 {

	public static void main(String[] args) {
	
		String str = "testing";
		
		 getLenth(str);
	}
	
	public static void getLenth(String str) {
		
		int i = 0;
		
		try {
			while(true) {
				
				//charAt(index) - it will give charcter available at i position
				str.charAt(i);
				
				//i increase so when reach at end of String 
				// throw an IndexOutOfBoundException
				i++;
			}
		}catch (Exception e) {
				
			System.out.println(i); //7
		}
		
	}

}

```

## via getBytes() method
```java
package com.adi.rest;

public class Demo2 {

	public static void main(String[] args) {

		String str = "testing";
		
		int leng = 0;
		
		try {
			//Encodes this String into a sequence of bytes using theplatform's
			 //   default charset, storing the result into a new byte array.
			
			//Big-Endian (BE) / Little-Endian (LE) are two ways to organize 
			   //multi-byte words  -- study require to dig deep.
			
			
			leng = str.getBytes("UTF-16BE").length/2;
			
		} catch (Exception e) {
			
		}
		
		System.out.println(leng); //7
	}
}

```
## via method use spilit()

```java
package com.adi.rest;

public class Demo2 {

	public static void main(String[] args) {

		String str = "testing";
	
		System.out.println(getStringLength(str)); // 7
	}
	
	public static int getStringLength(String str) {
		
		String[] st = str.split("");
		
		int count = 0;
		
		for(String s : st) {
			
			//It will give length of s everytime increase by 1
			count += s.toCharArray().length;
		}
		
		return count;
				
	}
}

```

```java
package com.adi.rest;

public class Demo2 {

	public static void main(String[] args) {

		String str = "testing";
	
		System.out.println(getStringLength(str)); // 7
	}
	
	public static int getStringLength(String str) {
		
		String[] st = str.split("");
		
		int count = 0;
		
		for(String s : st) {
			
			
			count ++;
		}
		
		return count;
				
	}
}

```

# 31. What is StringJoiner  or Combine multiple String in one.

```java
package com.adi.rest;

import java.util.StringJoiner;

public class Demo2 {

	public static void main(String[] args) {

		//Join Separate string in one by StringJoiner (1.8)
		//  combine diff list of emp name, stud name etc 
		// separte by delimeter
		
		//Tom,Lisa,Naveen
		
		StringJoiner joiner = new StringJoiner(",", "[", "]");
		
		joiner.add("Tom")
				.add("Lisa")
					.add("Naveen")
					 .add("Aditya");
		
		//To print use toString()method
		System.out.println(joiner.toString());
		
		
		
	}

}
Output:
[Tom,Lisa,Naveen,Aditya]
```

```java
package com.adi.rest;

import java.util.StringJoiner;

public class Demo2 {

	public static void main(String[] args) {

		StringJoiner joiner = new StringJoiner(";", "{", "]");

		joiner.add("Tom")
				.add("Lisa")
				  .add("Naveen").add("Aditya");

		System.out.println(joiner.toString()); // {Tom;Lisa;Naveen;Aditya]


	}

}

```
# 32. Count the number of occurence of a character in a String using java8 stream.

```java
package com.adi.rest;

public class Demo2 {

	public static void main(String[] args) {

		String str = "Testing solutions";
		
		//When you want to apply Stream on String use char() method
		   // It will return IntStream - now you perform your operation
		
		// In filter() 
		      // get any element 
		        // then convert it into charcter 
		// which occurence you are looking for compare that.
		
		long count = str.chars()
						  .filter(e ->(char)e == 'i')
						  	.count();
		
		System.out.println("i : "+ count); //i:2
		
	}

}

```
```java
package com.adi.rest;

public class Demo2 {

	public static void main(String[] args) {

		String str = "Testing solutions";
		
		//if you want to check multiple occurences
		long count = str.chars()
						  .filter(e ->(char)e == 'i' ||  (char)e == 's' )
						  	.count();
		
		System.out.println("i & s : "+ count); // i & s : 5
		
	}

}
```

## via generic method
```java
package com.adi.rest;

public class Demo2 {

	public static void main(String[] args) {

		String str = "Testing solutions";
		
		System.out.println(getCharCount(str, 'i')); // 2

	}

	public static long getCharCount(String str, char ch) {

		return str.chars()
					.filter(e -> (char) e == ch)
						.count();
				
	}
}

```

## overload this method
```java
package com.adi.rest;

public class Demo2 {

	public static void main(String[] args) {

		String str = "Testing solutions";
		
		System.out.println(getCharCount(str, 'i','s')); // 5

	}

	public static long getCharCount(String str, char ch) {

		return str.chars()
					.filter(e -> (char) e == ch)
						.count();
				
	}
	
	public static long getCharCount(String str, char ch1, char ch2) {

		return str.chars()
					.filter(e -> (char) e == ch1  || (char) e == ch2 )
						.count();
				
	}
}

```
# 33. Vowel count within a String; Via Java, Java8 streams, & Google Guvava

## via java
```java
package com.adi.rest;

public class Demo2 {

	public static void main(String[] args) {
		
		String str = "aeiouAEIOU";
		
		// we have to count the vovel in given string
		int count =0;
		
		for(int x=0; x< str.length(); x++) {
			
			if(isVovel(str.charAt(x))) {
				count ++;
			}
		}
		
		System.out.println(count); // 10
		
	}
	
	public  static boolean isVovel(char t) {
		
		return t=='a' || t=='e' || t=='i' || t=='o' || t=='u' 
		  || t == 'A' || t == 'E' || t == 'I' || t == 'O' || t == 'U';			
		
	}
}
```
## via Java8
```java
package com.adi.rest;

import java.util.function.IntPredicate;

public class Demo2 {

	public static void main(String[] args) {
		
		String str = "aeiouAEIOU";
		
		//Represents a predicate (boolean-valued function) of 
		    //  one int-valued argument
		
		IntPredicate vovel = new IntPredicate() {
			
			@Override
			public boolean test(int x) {
				
				//here we check vovels logic
				
				return x=='a' || x=='e' || x=='i' || x=='o' || x=='u' ||
						x=='A' || x=='E' || x=='I' || x=='O' || x=='U';				
			}
		};
		
		//give IntStream str.chars()
		long count = str.chars()
			             .filter(vovel)
			               .count();
		
		System.out.println(count); // 10
	}	
}

```
## via Google Guvava library
Add dependency
![Alt text](image-60.png)
```java
package com.adi.rest;

import com.google.common.base.CharMatcher;

public class Test1 {

	public static void main(String[] args) {
		

		String st = "Java example";
		
		// CharMatcher  = Determines a true or false value for any Java char value, just as Predicate does for any Object. 
		//  .anyOf()  = Returns a bogus matcher if the sequence contains supplementary characters.
		//    .countIn()  - Returns the number of matching chars found in a character sequence. 
	
		
		int countIn = CharMatcher.anyOf("aeiouAEIOU").countIn(st);

		System.out.println(countIn);  // 5 
	}

}

```

# 34. Join two arrays in java
![Alt text](image-61.png)

## via Java8
```java
package com.adi;

import java.util.Arrays;
import java.util.stream.Stream;

public class Demo {

	public static void main(String ar[]) {

		String[] batsman = {
					"Rohit",
					"Virat",
					"Dhawan",
					"Shreyas",
					"Rishabh",
					"Shubman" };
		
		String[] bowlers = {
					"Hardik",
					"Bhuvi",
					"Bumrah",
					"Chahal",
					"Jaddu" };
		
		
	//Convert array into Stream via Arrays.stream method
		
		Stream<String> sBat = Arrays.stream(batsman);
		Stream<String> sBow = Arrays.stream(bowlers);
		
		
	//Now concat it via Stream.concat()
	  //Then convert into combine array via toArray()
		// create a new String array by providing size to it
		
		String[] fullTeam = Stream.concat(sBat, sBow)
									.toArray(size -> new String[size]);
		
		
		//Print 
		for(String s : fullTeam) {
			System.out.println(s);
		}
	}

}
Output: 
Rohit
Virat
Dhawan
Shreyas
Rishabh
Shubman
Hardik
Bhuvi
Bumrah
Chahal
Jaddu
```
## via Goggle guvava lib - for object Arrays
```java
package com.adi.rest;

import com.google.common.collect.ObjectArrays;

public class Test1 {

	public static void main(String[] args) {
		
		String[] batsman = {
				"Rohit",
				"Virat",
				"Dhawan",
				"Shreyas",
				"Rishabh",
				"Shubman" };
	
	String[] bowlers = {
				"Hardik",
				"Bhuvi",
				"Bumrah",
				"Chahal",
				"Jaddu" };
	

	//concat require 3 things
		// 1st array 2nd array and type of final array
	
		String[] allTeam = ObjectArrays.concat(batsman, bowlers,String.class);
		
		for(String s : allTeam) {
			System.out.println(s);
		}
	}

}
Output:
Rohit
Virat
Dhawan
Shreyas
Rishabh
Shubman
Hardik
Bhuvi
Bumrah
Chahal
Jaddu
```
### what if primitive arrays
```java
package com.adi.rest;

import com.google.common.primitives.Ints;

public class Test1 {

	public static void main(String[] args) {
		
		int p1[] = {1,2,3,4,5};
		int p2[] = {6,7,8,9,10};
		
		//For concat this primitive arrays in google guvava
		
		int[] p3 = Ints.concat(p1,p2);
		
		//print
		for(int i :p3) {
			System.out.println(i);
		}
	}

}
Ouptut:
1
2
3
4
5
6
7
8
9
10

```
# 35. Calculate average of arrays using Simple loop, java8 & google guvava lib

![Alt text](image-62.png)

## via Simple loop
```java
package com.adi;

public class Demo {

	public static void main(String ar[]) {

		int num[] = {1,2,3,4,5,3,2,3,4};
		
		//Avg = Sum of all the number / array length
		
		int total = 0;
		
		for(int e : num) {
			total += e;			
		}
		
		System.out.println("total is : "+ total); // 27
		System.out.println("avg is : "+ (total/num.length)); // avg is : 3
	}
}
```
```java
package com.adi;

public class Demo {

	public static void main(String ar[]) {

		int num[] = {1,2,3,4,5,3,2,3,4};
		
		//Avg = Sum of all the number / array length
		
		double total = 0;
		
		for(int e : num) {
			total += e;			
		}
		
		System.out.println("total is : "+ total); // 27
		System.out.println("avg is : "+ (total/num.length)); // avg is : 3.0
	}
}
```
## via java8
```java
package com.adi;

import java.util.Arrays;
import java.util.OptionalDouble;

public class Demo {

	public static void main(String ar[]) {

		int num[] = {1,2,3,4,5,3,2,3,4};
		
		//Convert arrays in stream via Arrays.stream
		
		OptionalDouble average = Arrays.stream(num)
										 .average();
		
		System.out.println("avg is : "+ average); // avg is : OptionalDouble[3.0]
		
		System.out.println("avg is : "+ average.getAsDouble()); // avg is : 3.0
	}
}
```
## via google guvava lib
```java
package com.adi.rest;

import com.google.common.math.DoubleMath;

public class Test1 {

	@SuppressWarnings("deprecation")
	public static void main(String[] args) {
		
		int num[] = {1,2,3,4,5,3,2,3,4};
		
		//A class for arithmetic on doubles that is not covered by java.lang.Math.
		//Returns the arithmetic mean of values. 
		
		double avg = DoubleMath.mean(num);
		
		System.out.println("Avg is : "+avg); //Avg is : 3.0
	}

}

```

# 36. Get the count of words from Capitalize String.

![Alt text](image-63.png)

## 1st
```java
package com.adi;

public class Demo {

	public static void main(String ar[]) {
		
//Capitalized String - first leter is in Capital letter
		
		String str = "NaveenAutomationLabsYoutube";
		
		int count = 0;
		
		for(int i=0; i < str.length(); i++) {
			
			if(str.charAt(i) >= 'A' && str.charAt(i) <= 'Z') {
				count++;
			}
		}
		
		System.out.println(count); //4
		
	}
}
```

## 2nd via askii value
```java
package com.adi;

public class Demo {

	public static void main(String ar[]) {

		String str = "NaveenAutomationLabsYoutubeTestingJavaphython";

		int count = 0;

		for (int i = 0; i < str.length(); i++) {

			if (str.charAt(i) >= 65 && str.charAt(i) <= 90) {
				count++;
			}
		}

		System.out.println(count); // 6

	}
}
```

## 3rd via isUpperCase() in Character class
```java
package com.adi;

public class Demo {

	public static void main(String ar[]) {

		String str = "NaveenAutomationLabsYoutubeTestingJavaphython";

		int count = 0;

		for (int i = 0; i < str.length(); i++) {

			if(Character.isUpperCase(str.charAt(i))) {
				count++;
			}
		}

		System.out.println(count); // 6

	}
}
```
## 4rth via Streams
```java
package com.adi;

public class Demo {

	public static void main(String ar[]) {

		String str = "NaveenAutomationLabsYoutubeTestingJavaphython";

		//Convert string into Stream via chars()
		
		long count = str.chars()
						  .filter(e -> (e>=65 && e<=90))
						    .count();
		
		System.out.println(count); // 6

	}
}
```
## 5th 
```java
package com.adi;

public class Demo {

	public static void main(String ar[]) {

		String str = "NaveenAutomationLabsYoutubeTestingJavaphython";

		//Convert string into Stream via chars()
		
		long count = str.chars()
						  .filter(e -> Character.isUpperCase(e))
						    .count();
		
		System.out.println(count); // 6

	}
}
```

## 6th via regular expression
```java
package com.adi;

import java.util.regex.Matcher;
import java.util.regex.Pattern;

public class Demo {

	public static void main(String ar[]) {

		String str = "NaveenAutomationLabsYoutubeTestingJavaphython";

		//Take complete range from Capital A to Z [A-Z]
		// + any kind of character between A-Z i want
		String reg = "[A-Z]+";
		
		
		Pattern patternRef = Pattern.compile(reg);
		
		//match with this string 
		  //it will return mather Refrence
		Matcher matcher = patternRef.matcher(str);
		
		int count =0;
		
		//If this mathcher is available
		while(matcher.find()) {
			
			//Capturing groups are indexed from left to right, 
			  //starting at one.
			   //Group zero denotes the entire pattern, 
			count += matcher.group(0).length();
		}
		
		System.out.println(count); //6
	}
}
```

## what if there is a small String over begning
```java
package com.adi;

public class Demo {

	public static void main(String ar[]) {

		String str = "thisNaveenAutomationLabsYoutubeTestingJavaphython";

		//if small word is at the begining
		int count  =0;
		if(Character.isLowerCase(str.charAt(0))) {
			count++;
		}
		
		for(int i=0; i<str.length(); i++) {
			if(str.charAt(i) >='A' && str.charAt(i) <='Z') {
				count++;
			}
		}
		
		System.out.println(count); //7
	}
}
```
## if ther is space at begining 
```java
package com.adi;

public class Demo {

	public static void main(String ar[]) {

		String str = " thisNaveenAutomationLabsYoutubeTestingJavapop";

		
		int count  =0;
		if(Character.isLowerCase(str.trim().charAt(0))) {
			count++;
		}
		
		for(int i=0; i<str.length(); i++) {
			if(str.charAt(i) >='A' && str.charAt(i) <='Z') {
				count++;
			}
		}
		
		System.out.println(count); //7
	}
}
```

# 37. Check if subString is present in a given String.
![Alt text](image-64.png)

// U can split the string and iterate and find the desired thing

```java
package com.adi;

public class Demo {

	public static boolean isSubstring(String main, String sub) {
		
		// .* - start with anyString (.*)
		//and then sub string should be part of main String (.*) + sub
		// and end with anything
		return main.matches("(.*)" + sub + "(.*)");
	}
	
	public static void main(String ar[]) {

		System.out.println(isSubstring("naveen automation labs","labs"));//true
		
		System.out.println(isSubstring("naveen automation labs","testing"));//false
		
		System.out.println(isSubstring("naveen automation labs $$ special","$$"));//true
		
		System.out.println(isSubstring("automation","auto"));//true
		
		System.out.println(isSubstring("automation","to"));//true
		
		System.out.println(isSubstring("automation","a"));//true
		
		System.out.println(isSubstring("automation",null));//false
		
		//1 blank space
		System.out.println(isSubstring("automation labs"," "));//true
		
		//2 blank space
		System.out.println(isSubstring("automation labs","  "));//false
	}


}
```

## 3rd
```java
package com.adi;

public class Demo {

	public static boolean isSubstring(String main, String sub) {
		
		
		return main.contains(sub);
	}
	
	public static void main(String ar[]) {

		System.out.println(isSubstring("naveen automation labs","labs"));//true
		
		System.out.println(isSubstring("naveen automation labs","testing"));//false
		
		System.out.println(isSubstring("naveen automation labs $$ special","$$"));//true
		
		System.out.println(isSubstring("automation","auto"));//true
		
		System.out.println(isSubstring("automation","to"));//true
		
		System.out.println(isSubstring("automation","a"));//true
	
		
		//1 blank space
		System.out.println(isSubstring("automation labs"," "));//true
		
		//2 blank space
		System.out.println(isSubstring("automation labs","  "));//false
		
		System.out.println(isSubstring("automation",null));// Exception
		//contains null - leads to exception
	}


}
```

## 3rd
```java
package com.adi;

public class Demo {

	public static boolean isSubstring(String main, String sub) {
		
		//If substring is not available in main String it will return -1
		return main.indexOf(sub) != -1;
	}
	
	public static void main(String ar[]) {

		System.out.println(isSubstring("naveen automation labs","labs"));//true
		
		System.out.println(isSubstring("naveen automation labs","testing"));//false
		
		System.out.println(isSubstring("naveen automation labs $$ special","$$"));//true
		
		System.out.println(isSubstring("automation","auto"));//true
		
		System.out.println(isSubstring("automation","to"));//true
		
		System.out.println(isSubstring("automation","a"));//true
	
		
		//1 blank space
		System.out.println(isSubstring("automation labs"," "));//true
		
		//2 blank space
		System.out.println(isSubstring("automation labs","  "));//false
		
		System.out.println(isSubstring("automation",null));// Exception
		//contains null - leads to exception
	}


}
```

# 38. Why password should be stored in char[]
![Alt text](image-65.png)

Generally what we do.We create our password then we create there encrypted password. And via decryption we attain our account.



When you store password as String literal, it will store in heap memory and it's reference variable is store in stack memory.
![Alt text](image-66.png)

When we change password then refrence variable pointing to new password but the earlier password is not destroyed from SCP(String Constant pool). Since String is immutable. U can't change the string once created.
![Alt text](image-67.png)

If a hacker get your memory dump or heap dump he can easily access your earlier password.

U can say like garbace collector comes and destroy the value which have no refrence still the hacker has window to perform his operation.

When gc comes to destroy the unrefrence variable b4 that it will take dump.

https://docs.oracle.com/javase/8/docs/technotes/guides/security/crypto/CryptoSpec.html#PBEEx

![Alt text](image-68.png)

Now on we use char[] to store password. Once store we replace the password with nes one. If hacker take heap dump then he will get only new password not old one.


In String  accidently we store both things i.e earlier human readale password and encrypted password due to string immutability feature. &that is vulnerable things.  .  
So we use char array to store password things.

![Alt text](image-69.png)

Here if hacker take heap dump he won't harm our system.

```java
package com.adi;

public class Demo {

	public static void main(String ar[]) {

		// if we store password as string
		String pwd = "Naveen123";
		
		//With String
		//if accidently some one is printed the pwd it is visilbe 
		// on console log
		System.out.println("pwd is : "+ pwd); //pwd is : Naveen123
	}

}
```
```java
package com.adi;

public class Demo {

	public static void main(String ar[]) {

		// if we store password as char[]
		char pwd[] = {'a','b','c','1','2'};
		
		
		//if accidently some one is printed the pwd 
		
		System.out.println("pwd is : "+ pwd); //pwd is : [C@1cd072a9
		
		//It is not printed i.e hashvalue print
	}

}
```

## we can replace char[] value also with *
```java
package com.adi;

import java.util.Arrays;

public class Demo {

	public static void main(String ar[]) {

	
		char pwd[] = {'a','b','c','1','2'};
		
		System.out.println("pwd is : "+ pwd); //pwd is : [C@1cd072a9
		
		//Replace char[] via *
		Arrays.fill(pwd, '*');
		
		for(int i=0; i<pwd.length; i++) {
			System.out.print(pwd[i]); // *****
		}
	}

}
```

## 1 hack
### If JVM is crash, it will generate the crash dump .

Aapne abhi change bhi nahi kiya hai char[] pwd ko and Jvm crash ho gya. So crash dump se old pwd nikal sakta Hacker ya wo banda jo monitor karenga crash dump.

# 39. Find Student name holding highest marks. List with object and streams.

![Alt text](image-70.png)

![Alt text](image-71.png)

```java
package com.adi;

public class Student {

	private String name;
	private int rollNum;
	private int marks;
	private int age;
	
	//When we create an object of class we use constructor so
	// no need to create the setters
	public Student(String name, int rollNum, int marks, int age) {
		this.name = name;
		this.rollNum = rollNum;
		this.marks = marks;
		this.age = age;
	}

	public String getName() {
		return name;
	}

	public int getRollNum() {
		return rollNum;
	}

	public int getMarks() {
		return marks;
	}

	public int getAge() {
		return age;
	}

	@Override
	public String toString() {
		return "Student [name=" + name + ", rollNum=" + rollNum + ", marks=" + marks + ", age=" + age + "]";
	}	
	
}

```
```java
package com.adi;

import java.util.ArrayList;
import java.util.List;

public class Demo {

	public static void main(String ar[]) {
		
		Student s1 = new Student("Tom", 1, 90, 15);
		Student s2 = new Student("Peter", 2, 80, 16);
		Student s3 = new Student("Lisa", 3, 95, 17);
		Student s4 = new Student("Robby", 4, 100, 15);
		Student s5 = new Student("Naveen", 5, 50, 14);
		
		//Add all the student into ArrayList
		List<Student> studentList = new ArrayList<>();
		
		studentList.add(s1);
		studentList.add(s2);
		studentList.add(s3);
		studentList.add(s4);
		studentList.add(s5);
		
		//Find Total Student - use list.size() method
		System.out.println("Total Students : "+ studentList.size());
		
		System.out.println("=======================");
		
		//Print all these students
		//via for looop(enhanced for loop)
		System.out.println("     Print via Enhanced for loop");
		
		for(Student stud : studentList) {
			System.out.println(stud);		}
		
		System.out.println("=======================");
		
		//Print all these students
		// via stream
		System.out.println("     Print via streams");
		
		studentList.stream()
					.forEach(s -> System.out.println(s));
		
		System.out.println("=======================");
		
		//Give me all student who achieve marks greater than 80
		System.out.println("     Print students whose marks > 80");
		
		studentList.stream()
					.filter(stud -> stud.getMarks() > 80)
					.forEach(stud -> System.out.println(stud.getName() + "    :    " + stud.getMarks()));
		
		System.out.println("=======================");
		
		//Name student who got highest marks
		System.out.println("     Print students who got highest marks");
		
		//Go for map not filter
		//  pass marks
		//   go for maximum out for it via max()
		//     what type of data max() have Integer 
		//      and call compare method
		//    fetch all this via get()
		Integer highestMarks = studentList.stream()
											.map(stud -> stud.getMarks())
												.max(Integer::compare)
													.get();
		System.out.println("Highest marks of student : " +highestMarks);
		
		studentList.stream()
					.filter(stud -> stud.getMarks()== highestMarks)
				     .forEach(s -> System.out.println("name who got hm : "+s.getName()));
	}
}
Output:
Total Students : 5
=======================
     Print via Enhanced for loop
Student [name=Tom, rollNum=1, marks=90, age=15]
Student [name=Peter, rollNum=2, marks=80, age=16]
Student [name=Lisa, rollNum=3, marks=95, age=17]
Student [name=Robby, rollNum=4, marks=100, age=15]
Student [name=Naveen, rollNum=5, marks=50, age=14]
=======================
     Print via streams
Student [name=Tom, rollNum=1, marks=90, age=15]
Student [name=Peter, rollNum=2, marks=80, age=16]
Student [name=Lisa, rollNum=3, marks=95, age=17]
Student [name=Robby, rollNum=4, marks=100, age=15]
Student [name=Naveen, rollNum=5, marks=50, age=14]
=======================
     Print students whose marks > 80
Tom    :    90
Lisa    :    95
Robby    :    100
=======================
     Print students who got highest marks
Highest marks of student : 100
name who got hm : Robby

```

# 40. Shift all zero to right side of the Array.
![Alt text](image-72.png)

### Solve via BruteForce
U can use brute force (where you compare first element with next
	and swap it 

## Another approach
we focus on non zero element and create a new array having same size. & fill new array with  nonzero element then the remaining spaces automatically fills with zeros.   
Since default value of integer is 0.

![Alt text](image-73.png)

```java
package com.adi;

import java.util.Arrays;

public class Test {

	public static void main(String arg[]) {

		int i[] = new int[] {1,0,2,0,3,0,0,0}; //1 2 3 0 0 0 0 0
		
		//print in console
		//how to print an array
		// Arrays.toString(provide array here)
		System.out.println(Arrays.toString(shiftZeroToRight(i))); //[1, 2, 3, 0, 0, 0, 0, 0]

		i = new int[] {1,2,3,0};
		System.out.println(Arrays.toString(shiftZeroToRight(i)));  //[1, 2, 3, 0]
		
		i = new int[] {1};
		System.out.println(Arrays.toString(shiftZeroToRight(i))); // [1]
		
		
		
	}

	public static int[] shiftZeroToRight(int[] intArray) {		
		//Cover all the scenario's 		
		//What happen if lenght of Array is = 1
		if(intArray.length == 1) {
			return intArray;
		}
		
		// if length is greater than 1 
		
		int newArray[] = new int[intArray.length];
		int count = 0;
		
		for(int num : intArray) {
			
			//Condition for non zero number
			if(num != 0) {
				newArray[count] = num;
				count++; // increase counter
			}			
		}		
		
		return newArray;
	}
}

```
## Some enhancements
```java
package com.adi;

import java.util.Arrays;

public class Test {

	public static void main(String arg[]) {

		int i[] = new int[] { 1, 0, 2, 0, 3, 0, 0, 0 }; 

		System.out.println(Arrays.toString(shiftZeroToRight(i)));// [1, 2, 3, 0, 0, 0, 0, 0]
		
		//if you require 0 in left side 
		// u need to sort it
		Arrays.sort(i); 
		System.out.println(Arrays.toString(i)); // [0, 0, 0, 0, 0, 1, 2, 3]

	}

	public static int[] shiftZeroToRight(int[] intArray) {

		if (intArray.length == 1) {
			return intArray;
		}

		int newArray[] = new int[intArray.length];
		int count = 0;

		for (int num : intArray) {

			if (num != 0) {
				newArray[count] = num;
				count++;
			}
		}

		return newArray;
	}
}

```

### Problem with this approach
```java
package com.adi;

import java.util.Arrays;

public class Test {

	public static void main(String arg[]) {

		int i[] = new int[] { 1, 0, 20, 0, 3, 0, 4, 0,90 }; 
		System.out.println(Arrays.toString(shiftZeroToRight(i)));// [1, 20, 3, 4, 90, 0, 0, 0, 0]

		Arrays.sort(i); 
		System.out.println(Arrays.toString(i)); // [0, 0, 0, 0, 1, 3, 4, 20, 90]

		//here wo khud hi sort kar raha.. 
		// jis order mein insert hai .. usme store nhi kar raha
		
	}

	public static int[] shiftZeroToRight(int[] intArray) {

		if (intArray.length == 1) {
			return intArray;
		}

		int newArray[] = new int[intArray.length];
		int count = 0;

		for (int num : intArray) {

			if (num != 0) {
				newArray[count] = num;
				count++;
			}
		}

		return newArray;
	}
}

```
# Abc
