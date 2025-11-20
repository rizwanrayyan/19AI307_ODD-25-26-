# Ex.No:1(E) STRINGS AND MATH FUNCTION

## QUESTION:
Write a Java program to count the number of vowels in a given string.
## AIM:
To write a Java program that reads a string from the user and counts the total number of vowels present in it.

## ALGORITHM :
1. Start the program.

2. Import the necessary package java.util.*.

3. Read a string input from the user.

4. Convert the string to lowercase to make comparison easy.

5. Initialize a counter for vowels.

6. Traverse each character of the string:

   - If the character is ‘a’, ‘e’, ‘i’, ‘o’, or ‘u’, increment the vowel count.

8. Print the total number of vowels.

9. End the program.

## PROGRAM:
 ```
/*
Program to implement a Strings and Math Function using Java
Developed by: RIZWAN T
Register Number: 212222040134
*/
```

## SOURCE CODE:
```
import java.io.BufferedReader;
import java.io.InputStreamReader;
public class VowelCount {
    public static void main(String[] args) throws Exception {
        BufferedReader br = new BufferedReader(new InputStreamReader(System.in));
        String input = br.readLine().toLowerCase();
        int count = 0;
        for (int i = 0; i < input.length(); i++) {
            char ch = input.charAt(i);
            if (ch == 'a' || ch == 'e' || ch == 'i' || ch == 'o' || ch == 'u') {
                count++;
            }
        }
        System.out.println("Number of vowels: " + count);
    }
}

```

## OUTPUT:
<img width="690" height="260" alt="Screenshot 2025-11-19 at 6 46 13 PM" src="https://github.com/user-attachments/assets/b6230f3f-76c7-465c-a8dd-aea5727d35b8" />



## RESULT:
Thus, the Java program to count the number of vowels in a string was successfully written, executed, and verified.











