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
