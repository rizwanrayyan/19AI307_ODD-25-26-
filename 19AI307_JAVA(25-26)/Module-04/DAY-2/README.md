# Ex.No:4(B)  IMPLEMENT SOLID PRINCIPLES IN JAVA PROGRAM 

## QUESTION:
Design a microservices-based system where multiple services (AuthService, UserService, OrderService, etc.) must log system events using a centralized Singleton Logger. Every service logs messages in the format:

"[Service] [LEVEL]: message"

Log levels: INFO, WARNING, ERROR

After each log entry, print the entire log history.

## AIM:
To implement the Singleton Design Pattern in Java to maintain a centralized logger that stores and prints logs from multiple services.


## ALGORITHM :
1. Start the program.

2. Import necessary packages (java.util.*).

3. Create a Logger class:

    - Make the constructor private.

    - Provide a static getInstance() method.

    - Store logs in an ArrayList.

    - Add a method log(service, level, message) to format and store logs.

4. After adding a new log, print:

    - The newly added log

    - The entire log history in numbered format

5. In main():

    - Read number of logs n

    - For each log, read service name, level, and message

    - Call the Singleton logger to add the log

6. Stop the program.




## PROGRAM:
 ```
/*
Program to implement a SOLID Principles in Java Program
Developed by: RIZWAN T
Register Number: 212222040134
*/
```

## SOURCE CODE:
```
import java.util.*;

class Logger {
    private static Logger instance;
    private List<String> logs = new ArrayList<>();

    private Logger() {}

    public static Logger getInstance() {
        if (instance == null) {
            instance = new Logger();
        }
        return instance;
    }

    public void log(String service, String level, String message) {
        String logEntry = service + " " + level + ": " + message;
        logs.add(logEntry);
        System.out.println(logEntry);
        System.out.println("Current Logs:");
        for (int i = 0; i < logs.size(); i++) {
            System.out.println((i + 1) + ". " + logs.get(i));
        }
        System.out.println();
    }
}

public class MicroserviceLogger {
    public static void main(String[] args) {
        Scanner sc = new Scanner(System.in);
        int n = Integer.parseInt(sc.nextLine());
        Logger logger = Logger.getInstance();
        for (int i = 0; i < n; i++) {
            String[] input = sc.nextLine().split(" ", 3);
            String service = input[0];
            String level = input[1];
            String message = input[2];
            logger.log(service, level, message);
        }
        sc.close();
    }
}
```







## OUTPUT:
<img width="969" height="243" alt="Screenshot 2025-11-20 at 11 13 55 AM" src="https://github.com/user-attachments/assets/cc6cd280-a5f9-4511-a4a7-a125db8352f3" />


## RESULT:
Thus, a centralized logging system using the Singleton Design Pattern was successfully implemented in Java, and logs were maintained and displayed in sequential order.



