# Ex.No:5(B) SERIALIZATION AND DESERIALIZATION 

## QUESTION:
Write a program to demonstrate reading UTF strings using DataInputStream.

## AIM:
To demonstrate how to read UTF-encoded strings from a file using the DataInputStream class in Java.

## ALGORITHM :
1. Start the program.

2. Import the necessary packages (java.io.*).

3. Create a file and write a UTF string using DataOutputStream.

4. Open the same file using DataInputStream.

5. Read the UTF string using readUTF().

6. Display the string on the screen.

7. Close all streams.

8. End the program.	





## PROGRAM:
 ```
/*
Program to implement a Serialization and Deserialization using Java
Developed by: RIZWAN T
Register Number: 212222040134
*/
```

## SOURCE CODE:
```
import java.io.*;
import java.util.Scanner;
public class ReadUTFDemo {
    public static void main(String[] args) {
        try {
            Scanner sc = new Scanner(System.in);
            String text = sc.nextLine();
            DataOutputStream dos = new DataOutputStream(new FileOutputStream("utf_data.txt"));
            dos.writeUTF(text);
            dos.close();
            DataInputStream dis = new DataInputStream(new FileInputStream("utf_data.txt"));
            String readText = dis.readUTF();
            dis.close();
            System.out.println("String read from file: " + readText);
        } catch (Exception e) {
            System.out.println("Error: " + e);
        }
    }
}
```





## OUTPUT:

<img width="709" height="301" alt="Screenshot 2025-11-20 at 11 46 40 AM" src="https://github.com/user-attachments/assets/c5b0d55b-3ea1-44ec-a331-ef5f3d818e94" />


## RESULT:
Thus, the Java program to read UTF strings from a file using DataInputStream was executed successfully.

