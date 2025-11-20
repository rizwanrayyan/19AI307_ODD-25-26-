# Ex.No:1(D) ARRAYS

## QUESTION:
Write a Java program to find the sum of even and odd elements in an array.

## AIM:
To write a Java program that reads an array of integers and calculates the sum of even elements and the sum of odd elements separately.

## ALGORITHM :
1. Start the program and read the size of the array n.

2. Read n integer elements into the array a[].

3. Initialize two variables:

   - evenSum = 0

   - oddSum = 0

4. Traverse the array from index 0 to n-1:

   - If a[i] is even, add it to evenSum.
     
   - Otherwise, add it to oddSum.
         
5. Print the sum of even elements.

6. Print the sum of odd elements.

7. End the program.
## PROGRAM:
 ```
/*
Program to implement a Array concept using Java
Developed by: RIZWAN T
Register Number: 212222040134
*/
```

## SOURCE CODE:
```
import java.util.Scanner;
public class SumEvenOdd {
    public static void main(String[] args) {
        Scanner sc = new Scanner(System.in);
        int n = sc.nextInt();
        int[] arr = new int[n];
        for (int i = 0; i < n; i++) {
            arr[i] = sc.nextInt();
        }
        int sumEven = 0, sumOdd = 0;
        for (int i = 0; i < n; i++) {
            if (arr[i] % 2 == 0) {
                sumEven += arr[i];
            } else {
                sumOdd += arr[i];
            }
        }
        System.out.println("Sum of even elements: " + sumEven);
        System.out.println("Sum of odd elements: " + sumOdd);
        sc.close();
    }
}
```

## OUTPUT:
<img width="666" height="481" alt="Screenshot 2025-11-19 at 6 39 38 PM" src="https://github.com/user-attachments/assets/ffb77632-b5e7-4be8-aeca-18f1018a00f5" />


## RESULT:
Thus, the Java program successfully calculates the sum of even and odd elements in an array.



















