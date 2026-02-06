# Bug 1: The counter that counts wrong

## Trace table

| Step | counter | counter < 5 | Action |
| ---- | ------- | ----------- | ------ |
|   1  |    1    |    True     | 1+1    |
|   2  |    2    |    True     | 2+1    |
|   3  |    3    |    True     | 3+1    |
|   4  |    4    |    True     | 4+1    |
|   5  |    5    |   False     |No display|
|      |         |             |        |

## What's wrong
The counter only goes up to 4 because the while loop only executes if the counter is less than 5. Once the counter hits 5, the last number that is displayed is 4.

## Fixed pseudocode

```pseudo
BEGIN
    SET counter TO 1

    WHILE counter < 6 DO
        DISPLAY "Count: " + counter
        SET counter TO counter + 1
    END WHILE

    DISPLAY "Done counting to 5!"
END
```

## Real-world consequences

If this bug existed in a hopsital, there could be a complication with doses; the patient would be a dose short of their medication. 

## Flowchart

Download your fixed flowchart and save it as `flowcharts/bug1-fixed.svg`
