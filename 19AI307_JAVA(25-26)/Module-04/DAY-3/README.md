# Ex.No:4(C)  COMPOSITION IN JAVA

## QUESTION:
Implement a system where a Library contains multiple Book objects.
A Book is created inside the Library, and cannot exist independently — demonstrating Composition.

## AIM:
To implement Composition in Java by creating Book objects inside a Library class such that the lifetime of Book objects completely depends on the Library.

## ALGORITHM :
1. Start the program.

2. Import java.util.*.

3. Create a Book class with title and author.

4. Create a Library class that:

     - Contains an ArrayList of Books

     - Has a method addBook(title, author)

     - Prints all stored books

5. In the main() method:

     - Read number of books

     - For each book, read title and author

     - Add them to the Library

     - Print all books

  6. Stop the program.	





## PROGRAM:
 ```
/*
Program to implement a Composition Concepts in Java
Developed by: RIZWAN T
Register Number: 212222040134
*/
```

## SOURCE CODE:
```
import java.util.*;

class Library {
    private List<Book> books = new ArrayList<>();

    class Book {
        private String title;
        private String author;

        Book(String title, String author) {
            this.title = title;
            this.author = author;
        }

        public String toString() {
            return "- " + title + " by " + author;
        }
    }

    public void addBook(String title, String author) {
        books.add(new Book(title, author));
    }

    public void displayBooks() {
        System.out.println("Books in Library:");
        for (Book b : books) {
            System.out.println(b);
        }
    }
}

public class Main {
    public static void main(String[] args) {
        Scanner sc = new Scanner(System.in);
        Library library = new Library();

        int n = sc.nextInt();
        sc.nextLine(); // consume newline

        for (int i = 0; i < n; i++) {
            String title = sc.nextLine();
            String author = sc.nextLine();
            library.addBook(title, author);
        }

        library.displayBooks();
    }
}
```







## OUTPUT:
<img width="738" height="500" alt="Screenshot 2025-11-20 at 11 20 50 AM" src="https://github.com/user-attachments/assets/9d085a95-904e-4d8d-9d1f-492ce7ba33bf" />



## RESULT:
Thus, composition was successfully implemented by ensuring Book objects are created inside the Library and cannot exist independently.


