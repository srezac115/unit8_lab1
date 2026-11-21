# Lab Reflection: Git Version Control + Debugging (BuggyProgram)

## Student Name
Sky Rezac

## GitHub Repository URL
https://github.com/srezac115/unit8_lab1

---

# Commit 1: Initial Commit

## What did you include in this commit?
- Uploaded the starter version of BuddyProgram.java into the unit8_lab1 repository.

## What was the purpose of this commit?
- To establish a clean baseline of the starter code in version control before making any debugging edits.

---

# Commit 2: Task 1 (getGrade)

## Which tests in Task1Test were failing before your fix?
- Boundary and threshold test cases around the score cutoffs where the starter logic returned the wrong performance category. 

## What was the issue in the code?
- The nested if/else conditions in getGrade used incorrect score thresholds instead of the required boundaries.

## What change did you make to fix it?
- Updated the if condition to score >= 90 returning Exceeds, the inner if condition to score >= 80 returning Meets.

## How did the tests help guide your fix?
- They pointed directly to the boundary values where there were errors so I could verify the logic.

---

# Commit 3: Task 2 (sumEvenNumbers)

## Which tests in Task2Test were failing before your fix?
- Array summation test cases that failed due to a out of bounds index error when iterating through values.

## What was the issue in the code?
- The for loop in sumEvenNumbers used <= instead of <, causing i to reach an invalid index equal to the length of the array.

## What change did you make to fix it?
- Changed the loop condition from <= to < while preserving the null check and even number accumulation.

## How did the tests help guide your fix?
- They confirmed the expected even number sums across array and highlighted the off by one loop bound bug.

---

# Commit 4: Task 3 (sumRange)

## Which tests in Task3Test were failing before your fix?
- Range summation test cases involving inclusive upper bounds and cases where start was greater than end.

## What was the issue in the code?
- The for loop used < instead o f<= and sumRange did not swap start and end when it was larger than end.

## What change did you make to fix it?
- Added if(start>end) using a temp variable so start is never greater than end, and updated the loop condition to i<=end so both bounds are included.

## How did the tests help guide your fix?
- They showed which boundary and ordering cases failed so I could handle inclusive endpoints and reserved ranges cleanly.

---

# Overall Reflection

## Which task was the easiest to fix? Why?
- Task 1 because rhe issue was isolated to adjusting the score threshold values.

## Which task was the most difficult? Why?
- Task 3 because I had to catch both the inclusive upper bound and the reversed bounds case without breaking normal ascending ranges.

## How did Git help you track your progress through the debugging process?
- Each commit recorded a distinct stage of the lab in order, making it clear what was changed and verifying that all five required steps were completed.

## Why is it important to make small, frequent commits when debugging code?
- It isolates each fix so it is easier to see what changes, trace problems back to a specific edit, and keep history organized.

## What did you learn about using JUnit tests to guide debugging?
- Running targeted tests helps pin[oint exact logical and edge case bugs quickly and gives clear confirmation that a fix works as expected.

---

# Commit 5: Final Reflection

## What did you complete or update before making this final commit?
- Completed all 3 method fixes across commits 2-4 and filled out the reflection sections and the info on the top.

## Why is it useful to document your work after completing a programming task?
- It records what bugs existed, how they were solved, and what you learned, making the project easier to review and submit accurately.
