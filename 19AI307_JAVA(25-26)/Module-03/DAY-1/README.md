# Ex.No:3(A) INHERITANCE AND AGGREGATION

## QUESTION:
A fuel station sells two types of fuels: Petrol and Diesel.
Create a base class Fuel with attributes fuelId, customerName, litersPurchased, and pricePerLiter.
The Petrol class applies a 3% discount, and the Diesel class applies a 5% discount.

Write a program that accepts three fuel purchase records, computes the total price after discount, and displays all details.



## AIM:
To implement inheritance in Java using a base class Fuel and subclasses Petrol and Diesel, and to process three fuel transactions with discount calculations.

## ALGORITHM :
1. Start the program.

2. Import necessary packages (Scanner, DecimalFormat).

3. Create a base class Fuel with:

   - Instance variables

   - Constructor

   - Method getDiscountRate()

   - Method calculateTotalPrice()

   - Method display()

4. Create subclass Petrol overriding getDiscountRate() to return 3.

5. Create subclass Diesel overriding getDiscountRate() to return 5.

6. In main:

   - Loop exactly 3 times

   - Read fuelType, fuelId, customerName, litersPurchased, pricePerLiter

   - Based on fuel type, create appropriate object

   - Call display()

7. End program.




## PROGRAM:
 ```
/*
Program to implement a Inheritance and Aggregation using Java
Developed by: RIZWAN T
Register Number: 212222040134
*/
```

## SOURCE CODE:
```
import java.util.Scanner;
import java.text.DecimalFormat;

class Fuel {
    String fuelId, customerName;
    double litersPurchased, pricePerLiter;

    Fuel(String fuelId, String customerName, double litersPurchased, double pricePerLiter) {
        this.fuelId = fuelId;
        this.customerName = customerName;
        this.litersPurchased = litersPurchased;
        this.pricePerLiter = pricePerLiter;
    }

    double getDiscountRate() {
        return 0;
    }

    double calculateTotalPrice() {
        double total = litersPurchased * pricePerLiter;
        double discountAmount = total * getDiscountRate() / 100;
        return total - discountAmount;
    }

    void display() {
        DecimalFormat df = new DecimalFormat("0.00");
        System.out.println("Fuel ID: " + fuelId);
        System.out.println("Customer Name: " + customerName);
        System.out.println("Fuel Type: General");
        System.out.println("Liters Purchased: " + litersPurchased);
        System.out.println("Price per Liter: " + pricePerLiter);
        System.out.println("Discount: " + (int)getDiscountRate() + "%");
        System.out.println("Total Price: " + df.format(calculateTotalPrice()));
    }
}

class Petrol extends Fuel {
    Petrol(String fuelId, String customerName, double litersPurchased, double pricePerLiter) {
        super(fuelId, customerName, litersPurchased, pricePerLiter);
    }

    @Override
    double getDiscountRate() {
        return 3.0;
    }

    @Override
    void display() {
        DecimalFormat df = new DecimalFormat("0.00");
        System.out.println("Fuel ID: " + fuelId);
        System.out.println("Customer Name: " + customerName);
        System.out.println("Fuel Type: Petrol");
        System.out.println("Liters Purchased: " + litersPurchased);
        System.out.println("Price per Liter: " + pricePerLiter);
        System.out.println("Discount: " + (int)getDiscountRate() + "%");
        System.out.println("Total Price: " + df.format(calculateTotalPrice()));
    }
}

class Diesel extends Fuel {
    Diesel(String fuelId, String customerName, double litersPurchased, double pricePerLiter) {
        super(fuelId, customerName, litersPurchased, pricePerLiter);
    }

    @Override
    double getDiscountRate() {
        return 5.0; 
    }

    @Override
    void display() {
        DecimalFormat df = new DecimalFormat("0.00");
        System.out.println("Fuel ID: " + fuelId);
        System.out.println("Customer Name: " + customerName);
        System.out.println("Fuel Type: Diesel");
        System.out.println("Liters Purchased: " + litersPurchased);
        System.out.println("Price per Liter: " + pricePerLiter);
        System.out.println("Discount: " + (int)getDiscountRate() + "%");
        System.out.println("Total Price: " + df.format(calculateTotalPrice()));
    }
}

public class FuelStation {
    public static void main(String[] args) {
        Scanner sc = new Scanner(System.in);

        // Read until input ends (EOF)
        while (sc.hasNextLine()) {
            String type = sc.nextLine().trim();
            if (type.isEmpty()) break; // stop if blank line

            String fuelId = sc.nextLine().trim();
            String customerName = sc.nextLine().trim();
            double liters = sc.nextDouble();
            double price = sc.nextDouble();
            if (sc.hasNextLine()) sc.nextLine(); 

            Fuel fuel;
            if (type.equalsIgnoreCase("Petrol")) {
                fuel = new Petrol(fuelId, customerName, liters, price);
            } else if (type.equalsIgnoreCase("Diesel")) {
                fuel = new Diesel(fuelId, customerName, liters, price);
            } else {
                fuel = new Fuel(fuelId, customerName, liters, price);
            }

            fuel.display();
        }

        sc.close();
    }
}
```





## OUTPUT:
<img width="723" height="640" alt="Screenshot 2025-11-20 at 10 13 59 AM" src="https://github.com/user-attachments/assets/fd2d462f-f708-4244-8f9a-3d073a034af0" />




## RESULT:
The program successfully demonstrates inheritance, method overriding, and discount calculation for Petrol and Diesel purchases for exactly three records.




