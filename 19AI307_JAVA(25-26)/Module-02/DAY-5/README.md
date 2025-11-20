# Ex.No:2(E) ACCESS MODIFIERS

## QUESTION:
Create a class Calculator with:

One non-static method add(int a, int b) that returns the sum.

One static method info() that prints "Calculator is ready".

Read two numbers from the user and display the calculator message and the sum.


## AIM:
To write a Java program that demonstrates the use of static and non-static methods in a class.

## ALGORITHM :
1. Start the program.

2. Import the java.util package.

3. Create a class Calculator with:

    - A non-static method add(int a, int b) that returns a + b.

    - A static method info() that prints "Calculator is ready".

4. In the main method:

    - Read two integers from the user.

    - Call the static method info().

    - Create an object of Calculator.

    - Call the non-static method add() and display the sum.

5. Stop the program.



## PROGRAM:
 ```
/*
Program to implement a Access Modifiers using Java
Developed by: RIZWAN T
Register Number: 212222040134
*/
```

## SOURCE CODE:
```
import java.util.Scanner;

class Calculator {
   int a,b;
   int add(int a,int b){
       return a+b;
   }
   static void info(){
       System.out.println("Calculator is ready");
   }
}

class prog {
    public static void main(String[] args) {
        Scanner sc=new Scanner(System.in);
        int a=sc.nextInt();
        int b=sc.nextInt();
        Calculator c=new Calculator();
        Calculator.info();
        System.out.println("Sum: "+c.add(a,b));
    }
}
```






## OUTPUT:
<img width="691" height="329" alt="Screenshot 2025-11-20 at 10 06 26 AM" src="https://github.com/user-attachments/assets/943c18dd-a0a8-4eaa-9713-82ad5e71b82a" />



## RESULT:
Thus, the Java program using static and non-static methods was executed successfully.


