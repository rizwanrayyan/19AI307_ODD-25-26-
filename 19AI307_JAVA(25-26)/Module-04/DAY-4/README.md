# Ex.No:4(D) DESIGN PATTERN -- ABSTRACT FACTORY

## QUESTION:
Create a program that sends different types of notifications: "email", "sms", and "push". Use the Factory Pattern to generate the appropriate notification sender and call its notifyUser() method.


## AIM:
To implement the Abstract Factory Design Pattern in Java by creating a NotificationFactory that returns specific notification objects (Email, SMS, Push) based on user input.

## ALGORITHM :
1. Start the program.

2. Import the necessary package java.util.

3. Create a Notification interface with the method notifyUser().

4. Create concrete classes:

    - EmailNotification

    - SMSNotification

    - PushNotification

5. Create NotificationFactory with a method to return the correct notification object.

6. In main, repeatedly take input from the user: "email", "sms", "push" or "exit".

7. Use factory to generate the object and call notifyUser().

8. Stop the program.


## PROGRAM:
 ```
/*
Program to implement a Abstract Factory Pattern using Java
Developed by: RIZWAN T
Register Number: 212222040134
*/
```

## SOURCE CODE:
```
import java.util.Scanner;
interface Notification {
    void notifyUser();
}
class EmailNotification implements Notification {
    public void notifyUser() {
        System.out.println("Sending Email Notification");
    }
}
class SMSNotification implements Notification {
    public void notifyUser() {
        System.out.println("Sending SMS Notification");
    }
}
class PushNotification implements Notification {
    public void notifyUser() {
        System.out.println("Sending Push Notification");
    }
}
class NotificationFactory {
    public Notification createNotification(String input) {
        if (input.equalsIgnoreCase("email")) {
            return new EmailNotification();
        } else if (input.equalsIgnoreCase("sms")) {
            return new SMSNotification();
        } else if (input.equalsIgnoreCase("push")) {
            return new PushNotification();
        }
        return null;
    }
}
public class Main {
    public static void main(String[] args) {
        Scanner sc = new Scanner(System.in);
        NotificationFactory factory = new NotificationFactory();
        while (true) {
            String input = sc.nextLine();
            if (input.equalsIgnoreCase("exit")) break;
            Notification n = factory.createNotification(input);
            if (n != null) n.notifyUser();
            else System.out.println("Invalid notification type: " + input);
        }
    }
}
```



## OUTPUT:
<img width="741" height="351" alt="Screenshot 2025-11-20 at 11 28 42 AM" src="https://github.com/user-attachments/assets/927bb6ff-8391-40b1-9602-1c58adbeb922" />



## RESULT:
Thus, the Java program implementing the Abstract Factory Pattern to generate different types of notifications was executed successfully.


