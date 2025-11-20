# Ex.No:1(A) INTRODUCTION TO JAVA PROGRAMMING, DATA TYPES, VARIABLES AND OPERATORS

## QUESTION:
Lovely is given a power level before entering a challenge room.
She receives 3 bonus potions (each adds +1 using ++)
She also steps on 2 traps (each reduces -1 using --)

But she doesn't want any logic or loops—just a step-by-step manual update of her power.

Write a program that:

Accepts her initial power level.

Increases it 3 times using ++.

Decreases it 2 times using --.

Displays the power level after each step.

Finally prints her final power level.
## AIM:
To write a Java program that demonstrates manual pre-increment (++) and pre-decrement (--) operations and prints the power after each step.

## ALGORITHM :
1. Start the program.

2. Import Scanner.

3. Read an integer input — the initial power.

4. Print the initial power.

5. Apply the first bonus: ++power and print.

6. Apply the second bonus: ++power and print.

7. Apply the third bonus: ++power and print.

8. Apply the first trap: --power and print.

9. Apply the second trap: --power and print.

10. Print the final power.

11. End the program.

## PROGRAM:
 ```
/*
Program to implement variables and Operators using Java
Developed by: RIZWAN T
Register Number: 212222040134
*/
```

## Sourcecode.java:
```
import java.util.Scanner;
public class Main {
    public static void main(String[] args) {
        Scanner sc = new Scanner(System.in);
        int power = sc.nextInt();
        System.out.println("Initial Power = " + power);
        power++;
        System.out.println("Power after Bonus 1 = " + power);
        power++;
        System.out.println("Power after Bonus 2 = " + power);
        power++;
        System.out.println("Power after Bonus 3 = " + power);
        power--;
        System.out.println("Power after Trap 1 = " + power);
        power--;
        System.out.println("Power after Trap 2 = " + power);
        System.out.println("Final Power = " + power);
        sc.close();
    }
}
```

## OUTPUT:
<img width="632" height="249" alt="Screenshot 2025-11-19 at 5 57 36 PM" src="https://github.com/user-attachments/assets/06bd1df1-1eee-4e2b-b6d0-24a380f41280" />



## RESULT:
The program demonstrates manual use of ++ and -- (pre-increment and pre-decrement) to update and display Lovely's power level step-by-step without any loops.






