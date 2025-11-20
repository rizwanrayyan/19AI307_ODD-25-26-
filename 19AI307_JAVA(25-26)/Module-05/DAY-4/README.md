# Ex.No:5(D) THREAD PRIORITY

## QUESTION:
Write a Java program to determine the priority and name of the current thread.
Note: Read the thread name from the user.

## AIM:
To write a Java program that sets and retrieves the name and priority of the current thread using Thread class methods.

## ALGORITHM :
1. Start the program.

2. Import the necessary package java.util.

3. Read the thread name from the user.

4. Get the current thread using Thread.currentThread().

5. Set the thread name with setName().

6. Retrieve thread priority using getPriority().

7. Display priority, name, and full thread details.

8. End the program.



## PROGRAM:
 ```
/*
Program to implement a Thread Priority Concept using Java
Developed by: RIZWAN T
Register Number: 212222040134
*/
```

## SOURCE CODE:
```
import java.util.Scanner;

public class ThreadDetails {
    public static void main(String[] args) {
        Scanner sc = new Scanner(System.in);
        String name = sc.nextLine();
        sc.close();

        Thread t = Thread.currentThread();
        t.setName(name);

        System.out.println("Priority of Thread: " + t.getPriority());
        System.out.println("Name of Thread: " + t.getName());
        System.out.println(t);
    }
}
```





## OUTPUT:
<img width="730" height="267" alt="Screenshot 2025-11-20 at 11 54 58 AM" src="https://github.com/user-attachments/assets/8772eb18-2ad0-4f67-b188-9924caacfceb" />



## RESULT:
Thus, the Java program to determine the priority and name of the current thread was executed successfully.

