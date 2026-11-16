# Project 3 · Fifty students


## Demo video (required)

Paste a link to a short video of you running this assignment (tool + code + run).
Work without a working video link is incomplete.

**Your demo:** _add your link here_

**Week 12 · Project 3**  
**Theme:** Project 2’s report, on fifty random scores  
**Type:** Cumulative mini project (replaces the lab and the homework this week)

## Functions Explained

**countGrades:**  This function uses references and a for loop to compare values within the array and count how many of each value within that array meet the criteria for each letter grade. The references store the count as real numbers in main, not a copy and, the function does not print.

**officeHours:**  This function uses a pointer that points to the variable failingCount which counts the lines printed for each students score that is under 60 (F). The nullptr in this function skips writing to that count if it is null.

**average:**  This function returns a double because grades often have decimals. To do this you multiply the sum by a variable that is a double, in this case we use one so the value doesnt changebut the variable type does.

**My Run:**  
[0] 37

[1] 24

[2] 53

[3] 78

[4] 22

[5] 43

[6] 3

[7] 73

[8] 2

[9] 52

[10] 19

[11] 23

[12] 11

[13] 30

[14] 35

[15] 70

[16] 87

[17] 40

[18] 47

[19] 40

[20] 43

[21] 35

[22] 36

[23] 56

[24] 57

[25] 0

[26] 19

[27] 35

[28] 7

[29] 95

[30] 60

[31] 96

[32] 19

[33] 13

[34] 26

[35] 41

[36] 56

[37] 29

[38] 67

[39] 59

[40] 33

[41] 38

[42] 34

[43] 45

[44] 68

[45] 69

[46] 67

[47] 55

[48] 10

[49] 66

A: 2

B: 1

C: 3

D: 6

Failing: 38

Average: 42.46

Student at index [0] needs to come in for office hours! 

Student at index [1] needs to come in for office hours! 

Student at index [4] needs to come in for office hours! 

Student at index [5] needs to come in for office hours!

Student at index [6] needs to come in for office hours!

Student at index [8] needs to come in for office hours! 

Student at index [10] needs to come in for office hours!

Student at index [11] needs to come in for office hours! 

Student at index [12] needs to come in for office hours! 

Student at index [13] needs to come in for office hours! 

Student at index [14] needs to come in for office hours! 

Student at index [17] needs to come in for office hours! 

Student at index [18] needs to come in for office hours! 

Student at index [19] needs to come in for office hours! 

Student at index [20] needs to come in for office hours! 

Student at index [21] needs to come in for office hours! 

Student at index [22] needs to come in for office hours! 

Student at index [25] needs to come in for office hours! 

Student at index [26] needs to come in for office hours! 

Student at index [27] needs to come in for office hours! 

Student at index [28] needs to come in for office hours! 

Student at index [32] needs to come in for office hours! 

Student at index [33] needs to come in for office hours!

Student at index [34] needs to come in for office hours!

Student at index [35] needs to come in for office hours! 

Student at index [37] needs to come in for office hours! 

Student at index [40] needs to come in for office hours! 

Student at index [41] needs to come in for office hours! 

Student at index [42] needs to come in for office hours!

Student at index [43] needs to come in for office hours!

Student at index [48] needs to come in for office hours!

Office hours: 31


## What to ship
One array of fifty scores. Each score is one student. The starter fills the array with `rand`, the same way Project 2 did. You count the letter grades, print who needs office hours, and report the average. Functions do that work. `main` fills the array, calls the functions, and prints the report.

The numbers change every time the program runs. Do not type scores or names into the file.

## The functions
Use these signatures. The parameter list is the lesson.

```cpp
void countGrades(const int scores[], int n,
                 int& a, int& b, int& c, int& d, int& failing);
double average(const int scores[], int n);
void officeHours(const int scores[], int n, int* failingCount);
```

`countGrades` walks with `for`. It writes the five counts through the references and does not print.

- A is 90 and up
- B is 80 to 89
- C is 70 to 79
- D is 60 to 69
- Failing is below 60

A score of 60 is a D. It does not get an office-hours line. The five counts add up to 50.

`average` returns the mean as a `double`: `sum * 1.0 / n`. It does not print. If `n` is 0, return 0.

`officeHours` walks with `while`. For each score under 60 it prints:

```text
Student at index i needs to come to office hours.
```

`failingCount` is a pointer. When it is not `nullptr`, write how many of those lines you printed through `*failingCount`. When it is `nullptr`, still print the lines, and do not write through the pointer.

`n` is an ordinary copy. Pass `n` with the array. Do not use `sizeof` to discover the length. Put `const` on the array, because these functions only read it.

## Requirements
1. Leave `srand` and the fill loop alone. Every score comes from `rand() % 100`, a value from 0 through 99. Do not type scores or names into the source.
2. Print each index and its score, in order, before the totals.
3. `countGrades` writes A, B, C, D, and failing through `int&`. The five numbers add up to 50. The function does not print.
4. `average` returns the mean and does not print. `main` prints that returned value.
5. `officeHours` prints one line per score under 60, and writes the line count through `int*` when the pointer is not `nullptr`.
6. `main` calls the three functions. The `Failing` count and `Office hours` are the same number.
7. In the README, write a short explanation in your own words. Name the three functions. Say what the references change in `main`, what the pointer writes, what a `nullptr` skips, and why `average` returns a `double`. Under that paragraph, paste the run you actually got.

## Sample shape
This shows the shape of the report. Your fifty scores are random, so these numbers will not appear.

```text
[0] 91
[1] 58
...
A: 6
B: 9
C: 12
D: 8
Failing: 15
Average: 64.2
Student at index 1 needs to come to office hours.
...
Office hours: 15
```

`Failing` and `Office hours` match. The five counts add up to 50.

## Starter
`assignment-starter.cpp`. The fill, the printing, and the three calls are already wired. Fill in the function bodies. `lab-starter.cpp` is the same file.

## Deliverables
1. Course-visible GitHub repo
2. README — the short explanation, plus the run you got
3. Short demo video: the fifty scores, the five counts, and the office-hours lines, then what the references, the pointer, and the return each did
4. Canvas links

## Scope
No classes, `new` / `delete`, file I/O, or a menu. Strings and structs are week 13. This project does not need them.

## Integrity
- AI = tutor, not ghostwriter
- Fake ownership → zero
- Due: Monday night (not Sunday)
- Discussions (every week): first post Friday, replies Sunday
- Late: course policy (−10%/day unless stated otherwise)

## Rubric (100)

| Criterion | Pts |
|-----------|----:|
| Code submitted that does the work | 50 |
| Video explanation | 50 |
