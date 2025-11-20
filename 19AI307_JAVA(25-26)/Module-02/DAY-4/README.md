# Ex.No:2(D) VARIABLE SCOPE AND CONSTRUCTOR

## QUESTION:
Create a class with a private constructor and a static factory method that returns an object of the class. Read name and ID from the user and display employee details.

## AIM:
To write a Java program that demonstrates the use of a private constructor and a static factory method for object creation.

## ALGORITHM :
1. Start the program.

2. Import java.util.Scanner.

3. Create a class Employee with:

    - Private instance variables name and id.

    - A private constructor to initialize these variables.

    - A static factory method createEmployee(String name, String id) that returns a new object.

4. Create a public method display() to print details.

5. In the main method:

     - Read name and ID from the user.

     - Call the static factory method to create an object.

     - Display the details.

6. Stop the program.



## PROGRAM:
 ```
/*
Program to implement a Variable scope and Constructor using Java
Developed by: RIZWAN T
Register Number: 212222040134
*/
```

## SOURCE CODE:
```
import java.util.*;
class Employee{
    private String name;
    private int id;
    private Employee(String name,int id){
        this.name=name;
        this.id=id;
    }
    public static Employee createem(String name,int id){
        return new Employee(name,id);
    }
    public void display(){
        System.out.println("Employee Details:");
        System.out.println("Name: "+name);
        System.out.println("ID  : "+id);
    }
}
class prog{
    public static void main(String[] args){
        Scanner sc=new Scanner(System.in);
        String name=sc.nextLine();
        int id=sc.nextInt();
        Employee emp=Employee.createem(name,id);
        emp.display();
    }
}
```






## OUTPUT:
<img width="634" height="377" alt="Screenshot 2025-11-20 at 9 59 51 AM" src="https://github.com/user-attachments/assets/de1c231e-6917-4782-8f04-0a1baa7bbe66" />



## RESULT:
Thus, the Java program using a private constructor and static factory method was executed successfully.



