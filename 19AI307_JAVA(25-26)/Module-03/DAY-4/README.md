# Ex.No:3(D)    INTERFACE 

## QUESTION:
Each judge uses different criteria to score fighters. Based on points, the judge will declare “WIN”, “LOSE” or “DRAW”.

LenientJudge: WIN if diff ≥ 5, DRAW if < 5

StrictJudge: WIN if diff ≥ 10, DRAW if < 10

## AIM:
To write a Java program that implements an interface to evaluate fight results using LenientJudge and StrictJudge rules.

## ALGORITHM :
1. Start the program.

2. Import the necessary package java.util.

3. Create an interface Judge with a method String declareResult(int p1, int p2).

4. Implement LenientJudge class using Judge interface and apply rules:

    - WIN if difference ≥ 5

    - else DRAW

5. Implement StrictJudge class using Judge interface and apply rules:

    - WIN if difference ≥ 10

    - else DRAW

6. Read player1Score, player2Score, and judgeType from the user.

7. Create appropriate judge object based on judgeType.

8. Call declareResult() and display WIN / LOSE / DRAW.

9. End the program.




## PROGRAM:
 ```
/*
Program to implement a Interface using Java
Developed by: RIZWAN T
Register Number: 212222040134
*/
```

## SOURCE CODE:
```
import java.util.*;

abstract class Judge {
    abstract String decideResult(int player1, int player2);
}

class LenientJudge extends Judge {
    String decideResult(int player1, int player2) {
        int diff = player1 - player2;
        if (diff >= 5)
            return "WIN";
        else if (diff < 0)
            return "LOSE";
        else
            return "DRAW";
    }
}

class StrictJudge extends Judge {
    String decideResult(int player1, int player2) {
        int diff = player1 - player2;
        if (diff >= 10)
            return "WIN";
        else if (diff < 0)
            return "LOSE";
        else
            return "DRAW";
    }
}

public class Main {
    public static void main(String[] args) {
        Scanner sc = new Scanner(System.in);
        int player1 = sc.nextInt();
        int player2 = sc.nextInt();
        int judgeType = sc.nextInt();

        Judge judge;
        if (judgeType == 1)
            judge = new LenientJudge();
        else
            judge = new StrictJudge();

        System.out.println(judge.decideResult(player1, player2));
        sc.close();
    }
}
```






## OUTPUT:
<img width="690" height="332" alt="Screenshot 2025-11-20 at 10 49 39 AM" src="https://github.com/user-attachments/assets/ee04426d-4237-4dfd-aacf-92b0d3ff239d" />



## RESULT:
Thus, the program to implement a Judge scoring system using Interface in Java was executed successfully.


