# Ex.No:4(A) EXCEPTION HANDLING

## QUESTION:
If an Integer object is set to null, and you attempt to call .toString() on it, what happens? How can you prevent your code from throwing an exception in such cases?



## AIM:
To write a Java program that safely handles the case when an Integer object is null, preventing a NullPointerException by using a null check.

## ALGORITHM :
1. Start the program.

2. Import the required package java.util.*.

3. Declare an Integer variable and read user input.

4. If the input is 0, treat the Integer object as null.

5. Before calling .toString(), check whether the object is null.

6. If null, print "Null Integer"; otherwise print the integer value.

7. Stop the program.





## PROGRAM:
 ```
/*
Program to implement a Exception Handling using Java
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
        if (!sc.hasNextInt()) {
            System.out.println("Null Integer");
            return;
        }
        int value = sc.nextInt();
        Integer num = value == 0 ? null : value;
        if (num == null) {
            System.out.println("Null Integer");
        } else {
            System.out.println(num.toString());
        }
    }
}
```





## OUTPUT:
<img width="723" height="335" alt="Screenshot 2025-11-20 at 11 08 59 AM" src="https://github.com/user-attachments/assets/595c40bf-be52-4006-8886-848a4fb8a65b" />



## RESULT:
Thus, the Java program to safely handle null Integer objects and prevent NullPointerException using proper null checking was executed successfully.


