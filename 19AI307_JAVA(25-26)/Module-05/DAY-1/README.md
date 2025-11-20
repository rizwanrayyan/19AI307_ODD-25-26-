# Ex.No:5(A) INPUTSTREAMREADER 

## QUESTION:
Write a Java program to write text into a file using FileOutputStream.

## AIM:
To write a Java program that writes user-entered text into a specified file using FileOutputStream.

## ALGORITHM :
1. Start the program.

2. Import necessary packages (java.io.* and java.util.*).

3. Create a class for writing data into a file.

4. Read the filename and the text content from the user.

5. Create a FileOutputStream object using the filename.

6. Convert the text into bytes and write it into the file.

7. Close the FileOutputStream.

8. Print confirmation message.

9. End the program.




## PROGRAM:
 ```
/*
Program to implement a InputStreamReader using Java
Developed by: RIZWAN T
Register Number: 212222040134
*/
```

## SOURCE CODE:
```
import java.io.*;
import java.util.Scanner;
public class WriteUsingFileOutputStream {
    public static void main(String[] args) {
        try {
            Scanner sc = new Scanner(System.in);
            String fileName = sc.nextLine();
            String content = sc.nextLine();
            FileOutputStream fos = new FileOutputStream(fileName);
            fos.write(content.getBytes());
            fos.close();
            System.out.println("File written successfully.");
        } catch (IOException e) {
            System.out.println("Error: " + e.getMessage());
        }
    }
}
```





## OUTPUT:
![Screenshot 2025-11-20 at 11 41 48 AM](https://github.com/user-attachments/assets/aeb54860-f371-45a1-9b10-6cc573953e72)



## RESULT:
Thus, the Java program using FileOutputStream to write text into a file was executed successfully.

