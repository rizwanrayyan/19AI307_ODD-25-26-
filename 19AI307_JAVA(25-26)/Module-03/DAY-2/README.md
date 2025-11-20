# Ex.No:3(b) POLYMORPHISM

## QUESTION:
Write a Java program that calculates the net salary of an employee using method overloading.
Two ways to compute the salary:

Without bonus: net = base + 20% of base

With bonus: net = base + bonus

The program should use method overloading to implement both versions.
## AIM:
To write a Java program that calculates an employee’s net salary using method overloading, based on whether a bonus is provided or not.

## ALGORITHM :
1. Start the program.

2. Create a class Salary containing two overloaded methods:

   - calculate(double base) → compute base + 20% of base.

   - calculate(double base, double bonus) → compute base + bonus.

3. In the main method:

   - Read the base salary from the user.

   - Ask whether the employee has received a bonus.

   - If yes, read the bonus and call the overloaded method with two parameters.

   - If no, call the overloaded method with only the base salary.

4. Display the net salary based on the selected calculation method.

5. End the program.

## PROGRAM:
 ```
/*
Program to implement a Polymorphism using Java
Developed by: RIZWAN T
Register Number: 212222040134
*/
```

## SOURCE CODE:
```
import java.util.Scanner;

public class Salary {

    void calculate(double base) {
        double netSalary = base + (0.20 * base);
        System.out.println("Net Salary (20% allowance): ₹" + netSalary);
    }

    void calculate(double base, double bonus) {
        double netSalary = base + bonus;
        System.out.println("Net Salary with bonus: ₹" + netSalary);
    }

    public static void main(String[] args) {
        Scanner sc = new Scanner(System.in);
        Salary s = new Salary();
        double base = sc.nextDouble();
        sc.nextLine();
        String choice = sc.nextLine();
        if (choice.trim().equalsIgnoreCase("yes")) {
            double bonus = sc.nextDouble();
            s.calculate(base, bonus);
        } else {
            s.calculate(base);
        }
    }
}
```





## OUTPUT:
<img width="718" height="394" alt="Screenshot 2025-11-20 at 11 04 05 AM" src="https://github.com/user-attachments/assets/b82d9cca-9fb4-4d6c-b59f-c7b92e0a415f" />




## RESULT:
Thus, the program to calculate employee salary using method overloading was successfully executed and verified.
















