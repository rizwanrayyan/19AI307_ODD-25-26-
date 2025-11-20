# Ex.No:3(C) ABSTRACTION

## QUESTION:
Description:
Create abstract class GameScore with method finalScore().
Subclasses:

ArcadeGame: score = baseScore + (level × 100)

PuzzleGame: score = (attempts ≤ 3) ? 1000 - (attempts × 100) : 500


## AIM:
To implement abstraction in Java using an abstract class and subclasses to compute game scores based on game type.

## ALGORITHM :
1. Start the program.

2. Import java.util.*

3. Create an abstract class GameScore with abstract method int finalScore().

4. Create subclass ArcadeGame with attributes baseScore and level.
Implement finalScore() = baseScore + (level × 100).

5. Create subclass PuzzleGame with attribute attempts.
Implement finalScore():

    - If attempts ≤ 3 → score = 1000 - (attempts × 100)

    - Else → score = 500

6. In main(), read the game type.

7. If type is 1 → read baseScore, level → create ArcadeGame object.

8. If type is 2 → read attempts → create PuzzleGame object.

9. Print the final score.

10. End the program.


## PROGRAM:
 ```
/*
Program to implement a Abstraction using Java
Developed by: RIZWAN T
Register Number: 212222040134
*/
```

## SOURCE CODE:
```
import java.util.*;

abstract class GameScore {
    abstract int finalScore();
}

class ArcadeGame extends GameScore {
    int baseScore, level;

    ArcadeGame(int baseScore, int level) {
        this.baseScore = baseScore;
        this.level = level;
    }

    int finalScore() {
        return baseScore + (level * 100);
    }
}

class PuzzleGame extends GameScore {
    int attempts;

    PuzzleGame(int attempts) {
        this.attempts = attempts;
    }

    int finalScore() {
        if (attempts <= 3)
            return 1000 - (attempts * 100);
        else
            return 500;
    }
}

public class Main {
    public static void main(String[] args) {
        Scanner sc = new Scanner(System.in);
        int type = sc.nextInt();
        GameScore game;

        if (type == 1) {
            int base = sc.nextInt();
            int level = sc.nextInt();
            game = new ArcadeGame(base, level);
        } else {
            int attempts = sc.nextInt();
            game = new PuzzleGame(attempts);
        }

        System.out.println(game.finalScore());
        sc.close();
    }
}
```






## OUTPUT:
<img width="703" height="266" alt="Screenshot 2025-11-20 at 10 43 52 AM" src="https://github.com/user-attachments/assets/e6c9ae85-6a0e-4958-a8dc-cb778b607e4b" />



## RESULT:
Thus, the program to implement abstraction using Java for calculating game scores was successfully executed.


