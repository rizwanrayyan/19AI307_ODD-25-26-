# Ex.No:1(B) CONDITIONAL STATEMENT

## QUESTION:
In a magical building, an elevator behaves oddly:

If the floor number is divisible by 3 and 5, it says "Skipped".

If the floor number is divisible by 3 only, it says "Beware!".

If the floor number is divisible by 5 only, it says "Blessings!".

Otherwise, it announces the floor number - print - "Floor {number}" .

Write a Java program to simulate this elevator logic for a given floor number.

## AIM:
To write a Java program using conditional statements to determine the elevator message based on the floor number.

## ALGORITHM :
1. Start the program.

2. Import the java.util.* package.

3. Create a Scanner object to read the floor number.

4. Read the floor number as an integer.

5. Check if the number is divisible by both 3 and 5: print "Skipped".

6. Else if divisible by 3 only: print "Beware!".

7. Else if divisible by 5 only: print "Blessings!".

8. Otherwise print "Floor {number}".

9. End the program.
## PROGRAM:
 ```
/*
Program to implement a conditional statement using Java
Developed by: RIZWAN T
Register Number: 212222040134
*/
```

## Sourcecode.java:
```
import java.util.Scanner;
public class MagicalElevator {
    public static void main(String[] args) {
        Scanner sc = new Scanner(System.in);
        int floor = sc.nextInt();
        
        if (floor % 3 == 0 && floor % 5 == 0) {
            System.out.println("Skipped");
        } else if (floor % 3 == 0) {
            System.out.println("Beware!");
        } else if (floor % 5 == 0) {
            System.out.println("Blessings!");
        } else {
            System.out.println("Floor " + floor);
        }
    }
}

```

## OUTPUT:

<img width="605" height="236" alt="Screenshot 2025-11-19 at 6 04 31 PM" src="https://github.com/user-attachments/assets/7933b082-0adc-42ac-9bd4-188802216889" />


## RESULT:
Thus, the Java program to simulate the magical elevator logic using conditional statements was successfully executed.








