# Ex.No:3(F) WRAPPER CLASS

## QUESTION:
Write a Java program to find the square root of a number using the Double wrapper class.

## AIM:
To write a Java program that uses the Double wrapper class and Math.sqrt() to compute the square root of a given number.

## ALGORITHM :
1. Start the program.

2. Import the necessary package java.util.

3. Read a number from the user.

4. Convert the input value into a Double object.

5. Use Math.sqrt() to compute the square root.

6. Display the result.

7. End the program.



## PROGRAM:
 ```
/*
Program to implement a Wrapper Class using Java
Developed by: RIZWAN T
Register Number: 212222040134
*/
```

## SOURCE CODE:
```
import java.util.*;
public class Main {
    public static void main(String[] args) {
        Scanner sc = new Scanner(System.in);
        double num = sc.nextDouble();
        Double number = num; 
        Double sqrt = Math.sqrt(number);
        System.out.println("Square root of " + number + " is: " + sqrt);
        sc.close();
    }
}
```





## OUTPUT:
<img width="688" height="298" alt="Screenshot 2025-11-20 at 10 58 00 AM" src="https://github.com/user-attachments/assets/50b07a46-8003-4e38-b320-561bbc01dc05" />



## RESULT:
Thus, the program to compute the square root of a number using the Double wrapper class was executed successfully.


