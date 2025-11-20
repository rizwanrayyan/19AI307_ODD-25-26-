# Ex.No:1(C) LOOPING STATEMENT

## QUESTION:
Write a Java program to reverse a number using a while loop. For example, if the input is 1234, the output should be 4321
## AIM:
To write a Java program using a while loop to reverse a given integer number.

## ALGORITHM :
1. Start the program.

2. Import the java.util.* package.

3. Create a Scanner object to read the number from the user.

4. Initialize a variable rev = 0 to store the reversed number.

5. Use a while loop that continues until the number becomes 0.

6. Extract the last digit using num % 10.

7. Update reversed number using rev = rev * 10 + digit.

8. Remove the last digit using num = num / 10.

9. After the loop ends, print the reversed number.

10. End the program.

## PROGRAM:
 ```
/*
Program to implement a Looping Statement using Java
Developed by: RIZWAN T
Register Number: 212222040134
*/
```

## SOURCE CODE:

```
import java.util.Scanner;
public class ReverseNumber {
    public static void main(String[] args) {
        Scanner sc = new Scanner(System.in);
        int num = sc.nextInt();
        sc.close();
        int reversed = 0;
        while (num != 0) {
            int digit = num % 10;
            reversed = reversed * 10 + digit;
            num /= 10;
        }
        System.out.println("Reversed number: " + reversed);
    }
}

```

## OUTPUT:
<img width="658" height="203" alt="Screenshot 2025-11-19 at 6 34 26 PM" src="https://github.com/user-attachments/assets/c05c2afa-2cd9-49c2-a691-6b5055540b46" />


## RESULT:
Thus, the Java program using a while loop to reverse a number was successfully written, executed, and verified.









