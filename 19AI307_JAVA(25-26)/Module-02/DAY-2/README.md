# Ex.No:2(B) METHODS

## QUESTION:
Write a method int cube(int x) that calls another method int square(int x) internally to compute the cube of a number as x * square(x).


## AIM:
To write a Java program that uses one method (square) inside another method (cube) to calculate the cube of a number.

## ALGORITHM :
1. Start the program.

2. Import the necessary package java.util.

3. Create a class CubeUsingSquare.

4. Inside the class, define a method square(int x) that returns x * x.

5. Define another method cube(int x) that returns x * square(x).

6. In the main method:

7. Create an object of the class.

8. Read an integer from the user.

9. Call cube(x) and display the result.

10. Stop the program.



## PROGRAM:
 ```
/*
Program to implement a Methods using Java
Developed by: RIZWAN T
Register Number: 212222040134
*/
```

## SOURCE CODE:
```
import java.util.*;
public class Main
{
    public static int square(int n){
        return n*n;
    }
    public static int cube(int n){
        return n*square(n);
    }
    public static void main(String[] args){
        Scanner sc=new Scanner(System.in);
        int n=sc.nextInt();
        int res=cube(n);
        System.out.print(res);
        
        
    }
}
```






## OUTPUT:
<img width="625" height="187" alt="Screenshot 2025-11-20 at 9 49 14 AM" src="https://github.com/user-attachments/assets/3e754904-b3c7-4e0a-8881-e45c0e4e68ea" />



## RESULT:
Thus, the Java program using method calling (cube calling square) was executed successfully.

