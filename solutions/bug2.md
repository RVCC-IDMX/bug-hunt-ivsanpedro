# Bug 2: The grade that's never excellent

## Trace table

| Step | score | Condition checked | Result |
| ---- | ----- | ----------------- | ------ |
|   1  |   95  |   True            |Grade D |
|      |       |                   |        |
|      |       |                   |        |

## What's wrong
All scores that are above 60 will automatically receive a D. 

## Fixed pseudocode

```pseudo
BEGIN
    DISPLAY "Enter your score (0-100):"
    INPUT score

    IF score >= 90 THEN
        DISPLAY "Grade: A - Excellent"
    ELSEIF score >= 80 THEN
        DISPLAY "Grade: B - Good"
    ELSEIF score >= 70 THEN
        DISPLAY "Grade: C - Satisfactory"
    ELSEIF score >= 60 THEN
        DISPLAY "Grade: D - Passing"
    ELSE
        DISPLAY "Grade: F - Failing"
    ENDIF
END
```

## Reframed explanation

If this bug controlled how music was ranked on the Top 100 Billboard, every song that receives more than 
600,000 streams would immediately be ranked number 100. In a world that 600,000 is the minimum number of streams to get on the Top 100 Billboard ranking. A song with a billion streams will be treated the same as a record with 600,001 streams. 

## Flowchart

Download your fixed flowchart and save it as `flowcharts/bug2-fixed.svg`
