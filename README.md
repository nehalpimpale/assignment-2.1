# assignment-2.1


Q1.

public class acad 
{
  public static void main(String[] args)
  {
    int a=25;                              //Value is assigned to variable a
    int b=50;                              //value is assigned to variable b
    System.out.println(a+b);             //(a+b) is displayed on console
  }
}


Q2.

import java.util.Scanner;
public class acad 
{
  public static void main(String[] args)
  {
    Scanner in=new Scanner(System.in);
    int x=in.nextInt();                //value is read from console and assigned to variable x
    int y=in.nextInt();                //value is read from console and assigned to variable y
    System.out.println(x+y);          //displaying x+y on console
    in.close();
  }
}


Q3.

import java.util.Scanner;
public class acad 
{
	public static void main(String[] args)
	{
		Scanner sc=new Scanner(System.in);
		int x=sc.nextInt();         //value is read from console and assigned to variable x
		int y=sc.nextInt();        //value is read from console and assigned to variable x
		System.out.println("First number is:"+x);
		System.out.println("Second number is:"+y);
		sum(x,y);
		sc.close();
	}
	public static void sum(int a,int b) 			//method for calculating and displaying the sum
	{
		System.out.println("Sum is:"+(a+b));
	}
}


Q4.

import java.util.ArrayList;
import java.util.Scanner;


public class acad 
{
	public static void main(String[] args)
	{
		Scanner sc=new Scanner(System.in);
		int a=sc.nextInt();            
		int b=sc.nextInt();            
		ArrayList<Integer> odd=new ArrayList<Integer>();     //ArrayList preferred over array as the size is dynamic
		ArrayList<Integer> even=new ArrayList<Integer>();    //ArrayList preferred over array as the size is dynamic
		for(int i=a;i<=b;i++)
		{
			if(i%2==0)
				even.add(i);                                 //adding even numbers in ArrayList
			else
				odd.add(i);                                  //adding odd numbers in ArrayList
		}
		System.out.println();
		System.out.println("Odd numbers are:");
		for(int i:odd)
			System.out.print(i+" ");
		System.out.println();
		System.out.println("\nEven numbers are:");
		for(int i:even)
			System.out.print(i+" ");
		sc.close();
	}
}


Q5.

import java.util.Scanner;

public class acad 
{
	public static void main(String[] args)
	{
		Scanner sc=new Scanner(System.in);
		int n=sc.nextInt();                                     //accepting the number from console
		System.out.println("Input: "+n);
		System.out.println("O/p:");
		for(int i=1;i<=10;i++)
		{
			System.out.println(n+" * "+i+" = "+(n*i));            //displaying table of given number on console
		}
		sc.close();
	}
}



Q6.


import java.util.Scanner;


public class acad 
{
	public static void sum()																	                  //sum method with no arguments
	{
		int x=5;
		int y=10;
		System.out.println("Sum is (method with no arguments):"+(x+y));
	}
	public static void sum(int a,int b)   														           //sum method with 2 arguments       
	{
		System.out.println("Sum of first 2 numbers is (method with 2 arguments):"+(a+b));
	}
	public static void sum(int a,int b,int d,int e)												      //sum method with 4 arguments       
	{
		System.out.println("Sum of all 3 numbers is (method with 4 arguments):"+(a+b+d+e));
	}
	
	public static void main(String[] args)
	{
		Scanner sc=new Scanner(System.in);
		int a=sc.nextInt();      
		int b=sc.nextInt();
		int d=sc.nextInt();
		int e=sc.nextInt();
		sum();
		sum(a,b);
		sum(a,b,d,e);
		sc.close();
	} 
	
}


Q7.


The return value alone is not sufficient for the compiler to figure out which function to call:

public int foo() {...}
public float foo() {..}
...
foo(); // which one?
So while overloading a method the return type should be same. We can overload method in 2 ways
1.different type of method arguments
2.different number of method arguments

To avoid the ambiguity of compiler the return type of overloaded method should be same.

overloading with different return type will give following error

class A{
static int add(int a,int b){return a+b;}
static double add(int a,int b){return a+b;}
}
class B{
public static void main(String[] args){
System.out.println(Adder.add(11,11));   //ambiguity
}}
In this when code is compiled it will show error as:
Overloading3.java:3: error: method add(int,int) is already defined in class A
static double add(int a,int b){return a+b;}


Q8.


import java.util.Arrays;
import java.util.Scanner;


public class acad 
{
	public static void main(String[] args)
	{
		Scanner sc=new Scanner(System.in);
		int n=sc.nextInt();                   //size of array
		int[] arr=new int[n];
		int[] arr1=new int[n];
		for(int i=0;i<n;i++)
		{
			arr[i]=sc.nextInt();
		}
		Arrays.sort(arr);
		int j=0;                            //sorting array in ascending order
		for(int i=arr.length-1;i>=0;i--)
		{
			arr1[j]=arr[i];					//Storing elements in reverse order(Descending)
			j++;
		}
		for(int x : arr1)
			System.out.println(x);			//Displaying array elements in descending order
		sc.close();
	}
}


