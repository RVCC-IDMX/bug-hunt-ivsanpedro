# Bug 3: The infinite greeting

## Trace table

| Step | usersGreeted | usersGreeted < 3 | Action |
| ---- | ------------ | ---------------- | ------ |
|   1  |       0      |        True      |Display |
|   2  |       0      |        True      |Display |
|   3  |       0      |        True      |Display |
|   4  |       0      |        True      |Display |

## What's wrong
The loop will run infinitely because usersGreeted never changes within the loop. 

## Fixed pseudocode

```pseudo
BEGIN
    SET usersGreeted TO 0

    WHILE usersGreeted < 3 DO
        DISPLAY "What is your name?"
        INPUT userName
        DISPLAY "Hello, " + userName + "!"
        SET usersGreeted TO usersGreeted + 1
    END WHILE

    DISPLAY "All users have been greeted!"
END
```

## Warning for future students

Write a 3-4 sentence warning that would help a future student avoid this type of bug. What should they always check before saying their loop is finished?

How many times will the loop run? Before running the loop, I suggest checking if there is a base case that will stop the loop from executing infinitely. Ask yourself how many guests the program is supposed to greet.

For fun, you may choose the voice of your warning: HAP, Grace, Prof. Teeters, or a character of your choosing. Feel free to have an AI assistant help with this.

**Voice chosen: Prof. Teeters**

**Used AI assistant (yes/no): no**

## Flowchart

Download your fixed flowchart and save it as `flowcharts/bug3-fixed.svg`
