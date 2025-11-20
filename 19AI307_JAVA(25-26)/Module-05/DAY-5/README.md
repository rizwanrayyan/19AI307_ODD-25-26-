# Ex.No:5(E) MULTITHREADING -SYNCHRONIZATION

## QUESTION:
Use a thread pool to calculate and print the square of each number from input.

## AIM:
To write a Java program that uses a Thread Pool (ExecutorService) to compute and print the square of each input number concurrently.

## ALGORITHM :
1. Start the program.

2. Import the necessary package java.util and java.util.concurrent.

3. Read the total count of numbers from the user.

4. Create a fixed thread pool using Executors.newFixedThreadPool().

5. For each input number, submit a task to the pool to compute its square.

6. Inside each task, calculate and print the square.

7. Shutdown the executor service.

8. End the program.




## PROGRAM:
 ```
/*
Program to implement a Synchronization concept using Java
Developed by: RIZWAN T
Register Number: 212222040134
*/
```

## SOURCE CODE:
```
import java.util.*;
import java.util.concurrent.*;
public class SquareThreadPool {
    public static void main(String[] args) throws Exception {
        Scanner sc = new Scanner(System.in);
        int n = sc.nextInt(); 
        int[] numbers = new int[n];
        for (int i = 0; i < n; i++) {
            numbers[i] = sc.nextInt();
        }
        sc.close();
        ExecutorService executor = Executors.newFixedThreadPool(3);
        List<Future<Integer>> futures = new ArrayList<>();
        for (int i = 0; i < n; i++) {
            int num = numbers[i];
            futures.add(executor.submit(() -> num * num));
        }
        for (Future<Integer> f : futures) {
            System.out.println("Square: " + f.get());
        }
        executor.shutdown();
    }
}
```





## OUTPUT:
<img width="735" height="474" alt="Screenshot 2025-11-20 at 11 58 23 AM" src="https://github.com/user-attachments/assets/254ef549-0778-426d-9a7e-cf5551791ce5" />



## RESULT:
Thus, the Java program using a Thread Pool to compute the square of numbers concurrently was executed successfully.

