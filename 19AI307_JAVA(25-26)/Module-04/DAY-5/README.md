# Ex.No:4(D) DESIGN PATTERN  ---- BEHAVIOUR PATTERN

## QUESTION:
Create an Article class where changes to the content are saved as mementos.
Let the user view and restore any saved version.

## AIM:
To implement the Memento Design Pattern in Java by saving and restoring states (versions) of an Article object.

## ALGORITHM :
1. Start the program.

2. Import the necessary package java.util.

3. Create a Memento class to store the article state.

4. Create an Article class that can save its content into a memento and restore it.

5. Create a Caretaker class that stores multiple mementos (versions).

6. In main(),

    - Read the number of versions.

    - Read each content and save it as a memento.

    - Read the index to restore.

    - Display the restored version.

7. End the program.
## PROGRAM:
 ```
/*
Program to implement a Behaviour Pattern using Java
Developed by: RIZWAN T
Register Number: 212222040134
*/
```

## SOURCE CODE:
```
import java.util.*;
class Article {
    private String content;
    public void setContent(String content) {
        this.content = content;
    }
    public String getContent() {
        return content;
    }
    public ArticleMemento save() {
        return new ArticleMemento(content);
    }
    public void restore(ArticleMemento memento) {
        this.content = memento.getContent();
    }
}
class ArticleMemento {
    private final String content;

    public ArticleMemento(String content) {
        this.content = content;
    }
    public String getContent() {
        return content;
    }
}
class ArticleHistory {
    private List<ArticleMemento> versions = new ArrayList<>();
    public void saveVersion(Article article) {
        versions.add(article.save());
    }
    public ArticleMemento getVersion(int index) {
        if (index >= 0 && index < versions.size()) {
            return versions.get(index);
        }
        return null;
    }
}
public class ArticleManager {
    public static void main(String[] args) {
        Scanner sc = new Scanner(System.in);
        Article article = new Article();
        ArticleHistory history = new ArticleHistory();
        int n = Integer.parseInt(sc.nextLine());
        for (int i = 0; i < n; i++) {
            String content = sc.nextLine();
            article.setContent(content);
            history.saveVersion(article);
        }
        int restoreIndex = Integer.parseInt(sc.nextLine());
        ArticleMemento m = history.getVersion(restoreIndex);
        if (m != null) {
            article.restore(m);
            System.out.println(article.getContent());
        } else {
            System.out.println("Invalid version");
        }
        sc.close();
    }
}
```






## OUTPUT:
<img width="714" height="529" alt="Screenshot 2025-11-20 at 11 34 34 AM" src="https://github.com/user-attachments/assets/4b55b190-d36f-40f7-a810-ca916fce72af" />



## RESULT:
Thus, the Java program using the Memento Behavioural Pattern was executed successfully, allowing saving and restoring of article versions.

