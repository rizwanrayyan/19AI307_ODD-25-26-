# Ex.No:3(E) INNER CLASS

## QUESTION:
Write a Java program to check if a number is an Armstrong number using Math.pow(), the Integer wrapper class, and an Inner Class.

## AIM:
To implement a Java program that uses an Inner Class to determine whether a number entered by the user is an Armstrong number.

## ALGORITHM :
1. Start the program.

2. Import the necessary package java.util.

3. Create an outer class ArmstrongChecker.

4. Inside it, define an inner class Calculator that checks if the number is Armstrong.

5. Use Integer.toString() to find the number of digits.

6. Use Math.pow() to compute digit powers and sum them.

7. Compare the sum with the original number.

8. Display if the number is an Armstrong number or not.

9.End the program.




## PROGRAM:
 ```
/*
Program to implement a InnerClass using Java
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
        int num = sc.nextInt();
        int temp = num;
        int digits = Integer.toString(num).length();
        int sum = 0;

        while (temp > 0) {
            int digit = temp % 10;
            sum += Math.pow(digit, digits);
            temp /= 10;
        }

        if (sum == num)
            System.out.println(num + " is an Armstrong number.");
        else
            System.out.println(num + " is not an Armstrong number.");

        sc.close();
    }
}
```





## OUTPUT:
<img width="688" height="300" alt="Screenshot 2025-11-20 at 10 54 43 AM" src="https://github.com/user-attachments/assets/06e98f53-4aaa-4e11-9861-6ad514aa7d47" />



## RESULT:
Thus, the program to implement an Inner Class in Java and check for an Armstrong number was executed successfully.


