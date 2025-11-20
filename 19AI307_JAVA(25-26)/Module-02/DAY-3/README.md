# Ex.No:2(C) ACCESS SPECIFIERS

## QUESTION:
Write a Java program to create a class called BankAccount with private instance variables accountNumber and balance. Provide public getter and setter methods to access and modify these variables.


## AIM:
To write a Java program that demonstrates encapsulation by using private variables and providing public getter and setter methods to access and modify them.

## ALGORITHM :
1. Start the program.

2. Import the java.util package.

3. Create a class BankAccount with two private instance variables:

   - accountNumber

   - balance

4. Create public getter and setter methods for each variable.

5. In the main method:

   - Create a BankAccount object.

   - Read account number and balance from the user.

   - Store them using setter methods.

   - Retrieve and display them using getter methods.

6. Stop the program.



## PROGRAM:
 ```
/*
Program to implement a Access Specifiers using Java
Developed by: RIZWAN T
Register Number: 212222040134
*/
```

## SOURCE CODE:
```
import java.util.*;
class BankAccount{
    private String accountNumber;
    private double balance;
public String getAccountNumber(){
    return accountNumber;
}
public void setAccountNumber(String accountNumber){
    this.accountNumber=accountNumber;
}
public double getBalance(){
    return balance;
}
public void setBalance(double balance){
    this.balance=balance;
}
}
public class Main{
    public static void main(String[] args){
        Scanner sc=new Scanner(System.in);
        BankAccount account=new BankAccount();
        String acc=sc.nextLine();
        account.setAccountNumber(acc);
        double bal=sc.nextDouble();
        account.setBalance(bal);
        
        System.out.println("Account Number: "+account.getAccountNumber());
        System.out.print("Balance: "+account.getBalance());
    }
}
```





## OUTPUT:
<img width="629" height="361" alt="Screenshot 2025-11-20 at 9 54 40 AM" src="https://github.com/user-attachments/assets/ba0711ab-5c1a-444d-8b44-506ece0dc63c" />



## RESULT:
Thus, the program to implement encapsulation using private variables and public getter/setter methods in Java was executed successfully.


