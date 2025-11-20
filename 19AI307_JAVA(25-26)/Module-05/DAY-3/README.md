# Ex.No:5(C)  FILE HANDLING USING JAVA
## QUESTION:
Ask the user for name, age, and email address. Write the collected data into a file called userdata.txt in a structured format.



## AIM:
To write a Java program that collects user details such as name, age, and email from the user and stores them in a text file using FileWriter.

## ALGORITHM :
1. Start the program.

2. Import the necessary packages such as java.util.* and java.io.*.

3. Create a Scanner object to read user input.

4. Read the user's name, age, and email.

5. Create a FileWriter object to open (or create) the file userdata.txt.

6. Write the user information to the file in a structured format.

7. Close the file.

8. Display a success message.

9. Stop the program.


## PROGRAM:
 ```
/*
Program to implement a File Handling using Java
Developed by: RIZWAN T
Register Number: 212222040134
*/
```

## SOURCE CODE:
```
import java.io.FileWriter;
import java.io.IOException;
import java.util.Scanner;

public class UserDataFile {
    public static void main(String[] args) {
        Scanner sc = new Scanner(System.in);

        String name = sc.nextLine();
        int age = sc.nextInt();
        sc.nextLine(); 
        String email = sc.nextLine();

        try {
            FileWriter fw = new FileWriter("userdata.txt");

            fw.write("User Information\n");
            fw.write("================\n");
            fw.write("Name  : " + name + "\n");
            fw.write("Age   : " + age + "\n");
            fw.write("Email : " + email + "\n");

            fw.close();
            System.out.println("Data written successfully.");
        } 
        catch (IOException e) {
            System.out.println("An error occurred.");
        }
    }
}
```







## OUTPUT:
<img width="705" height="301" alt="Screenshot 2025-11-20 at 11 50 11 AM" src="https://github.com/user-attachments/assets/caebef73-7e35-40a7-8168-fe5082a045d9" />



## RESULT:
Thus, the Java program to collect user information and write it to a file using file handling concepts was executed successfully.

