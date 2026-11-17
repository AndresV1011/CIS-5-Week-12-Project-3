# Project 3 · Fifty students


## Demo video (required)

Paste a link to a short video of you running this assignment (tool + code + run).
Work without a working video link is incomplete.

**Your demo:** https://drive.google.com/file/d/1J-rbG2icrdT-ui48q9NXFH5B1P83y139/view?usp=sharing

**Week 12 · Project 3**  
**Theme:** Project 2’s report, on fifty random scores  
**Type:** Cumulative mini project (replaces the lab and the homework this week)

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

The three functions are countGrades, average, and officeHours. The references change the A-failing counts in main. The pointer writes the number of students who need office hours. Nullptr skips writing through the pointer when it's empty, and the average returns a double so the result can include decimal places.

Here is my run:
[0] 3
[1] 66
[2] 80
[3] 50
[4] 23
[5] 12
[6] 46
[7] 67
[8] 53
[9] 61
[10] 49
[11] 67
[12] 19
[13] 21
[14] 60
[15] 95
[16] 91
[17] 24
[18] 54
[19] 84
[20] 3
[21] 11
[22] 16
[23] 15
[24] 55
[25] 64
[26] 9
[27] 34
[28] 80
[29] 98
[30] 35
[31] 42
[32] 53
[33] 29
[34] 76
[35] 51
[36] 95
[37] 84
[38] 45
[39] 17
[40] 57
[41] 63
[42] 90
[43] 33
[44] 93
[45] 99
[46] 62
[47] 67
[48] 4
[49] 96
A: 8
B: 4
C: 1
D: 9
Failing: 28
Average: 52.02
Student at index 0 needs to come to office hours.
Student at index 3 needs to come to office hours.
Student at index 4 needs to come to office hours.
Student at index 5 needs to come to office hours.
Student at index 6 needs to come to office hours.
Student at index 8 needs to come to office hours.
Student at index 10 needs to come to office hours.
Student at index 12 needs to come to office hours.
Student at index 13 needs to come to office hours.
Student at index 17 needs to come to office hours.
Student at index 18 needs to come to office hours.
Student at index 20 needs to come to office hours.
Student at index 21 needs to come to office hours.
Student at index 22 needs to come to office hours.
Student at index 23 needs to come to office hours.
Student at index 24 needs to come to office hours.
Student at index 26 needs to come to office hours.
Student at index 27 needs to come to office hours.
Student at index 30 needs to come to office hours.
Student at index 31 needs to come to office hours.
Student at index 32 needs to come to office hours.
Student at index 33 needs to come to office hours.
Student at index 35 needs to come to office hours.
Student at index 38 needs to come to office hours.
Student at index 39 needs to come to office hours.
Student at index 40 needs to come to office hours.
Student at index 43 needs to come to office hours.
Student at index 48 needs to come to office hours.
Office hours: 28

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
