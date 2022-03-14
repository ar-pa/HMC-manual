# HMC-manual
Hackerearth Monthly Contests manual for problem setters

# Propose a problem
[Check this blog](https://codeforces.com/blog/entry/73839) and [this](https://docs.google.com/document/d/1zD2imtOyX4fCFCg_5Yf5Va1Y5KV1494trFgkty_E1wM/edit#heading=h.o69k3hsgdlqi).
Also, [here](https://help.hackerearth.com/hc/en-us/articles/900002483366-HMCs-rate-card-programming-questions-only-) is the rate card.

# Selection
For every contest, I (Arpa) check your proposals and accept some of them. Also, I'm trying to accept some problems as backup problems.

No one can prepare a full contest for us. Each contest is shared between at least two problem setters. This is a new rule on HackerEarth to motivate problem setters.

# Preparation
## Things to be done
Let the day the email sent be d, 

| S. No. | Task                                                                                                                                                                                                                                                                                                                                                                                                                                                                                               | Deadline    | Assigned to |
|--------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------|-------------|
| 1      | Fill [this](https://docs.google.com/forms/d/e/1FAIpQLSf8Eem1KImiKWqqm6Hh3uZ7tLFi0m7dlaOUKXYtDx_mV7AJ7A/viewform) form to get access to the HMC dashboard.                                                                                                                                                                                                                                                                                                                                                                                                                                                 | d + 1      | Setters     |
| 2      | Finish writing complete statements on the HMC dashboard. Mark the problem as ready for testing.                                                                                                                                                                                                                                                                                                                                                                                                    | d + 1      | Setters     |
| 3      | Do the following for your problem in order: <br>- Generate test cases <br>- Write solutions <br>- Write editorials <br>- Write validator <br>- Write a naive solution (optional)  <br>- After creating a problem in Polygon, share it with me using the "Manage access" tab. My username is "arpa". Give me WRITE access. <br> Don't miss to commit the changes. | d + 4   | Setters     |
| 4      | Transfer test cases, solution, etc. from Polygon/TPS to HMC dashboard                                                                                                                                                                                                                                                                                                                                                                                                                              | d + 4      | Setters     |
| 5      | Testing of the entire problem                                                                                                                                                                                                                                                                                                                                                                                                                                                                      | d + 7~10 | Arpa        |
| 6      | Problems marked as ready                                                                                                                                                                                                                                                                                                                                                                                                                                                                           | a week before the contest      | Arpa        |
| 7      | Publish a blog post on Codeforces <br> - You can search for some examples. <br>  - Volunteer and let me know who is doing this  <br> - Search names of authors to find their username on Codeforces.                                                                                                                                                                                                                                                                                                                | a week before the contest         | Setters     |
| 8     | Contest goes live                                                                                                                                                                                                                                                                                                                                                                                                                                                                                  | See below         | Arpit       |

* Although there is a gap between when you finish and the contest date, it's not acceptable that you prepare something after the deadline. We need that time for a substitution if needed.
* After you finished the first task, please notify us (me and +Tripti Padukone) in the mail thread.
* Please note that even if you have access previously, send an acknowledgment email that you'll prepare your problem in the given deadline.
* If you are unwilling or you can't prepare the problem in the given time, please notify me today.
* Always CC: Tripti and Problem_setting@hackerearth.com on all emails.
* [Here](https://docs.google.com/spreadsheets/d/1zvzCMbm4zSU6HRuudU2bOoXTzkvYL5AALGXx4ObBfow/edit#gid=1287111182) is the task sheet (check the tab for corresponding contest, e.g. if you received the email "September Easy '21", check the Easy tab). Don't forget to color cells with green when you finish a task. Write your name in the corresponding cells.
* You can find your problem statement in the sheet by hovering mouse on the problem.
## Useful links
* [Polygon](https://polygon.codeforces.com/), the platform that we prepare the problem and test cases at the first.
* [Polygon help](https://polygon.codeforces.com/static/polygon.rtf).
* [Testlib](https://codeforces.com/testlib), the library to be used for generators and validators (and maybe checkers).
* [polygonToHE](https://github.com/ar-pa/polygonToHE), it helps you to transfer your test cases from Polygon to HMC.
* [HMC](https://app.hackerearth.com/setter/)

## Maintaining HMC master tracker
After you finished a task, color the corresponding cell with green. Put your problem link in the "Setter link" column. It's something like: https://app.hackerearth.com/setter/problemform/hmc/algorithm-template/43646/.

Sum of scores must be 100.

## Statement format
Order: story, Input format, Output format, Constraints, Samples.

Use our formula writer, it's better than using LaTeX. Don't write something like  "3\*sqrt(x)", use formula writer to make it beautiful.

[A good example](https://www.hackerearth.com/practice/algorithms/graphs/depth-first-search/practice-problems/approximate/tennis-tournament-75939265/).

Use proper English. For example "no more than once" doesn't mean "zero or one time" in normal English. Note that Codeforces is not proper way to learn English (while I learnt English from it). So if you want to say "no more than once", write "zero or one time". Otherwise grammar verification team changes it to "exactly once".

To write in latex format, single dollar sing is not enough, use two, like: `$$x$$`, although native formula writer is preferred. 

To make statements more clear, let's add more than one sample test cases.
* I always recommend you use a parameter t in your problem and give a bunch of test cases in a test file. If you're using this format, simply set a suitable t. Try to give as many sample tests as possible to help contestants get the statement easier. Even generate a little big (n = 10) random test cases to help them.
* Otherwise, write your sample test cases 2, 3, ... in the statement section.

Always have at least one non-obvious sample test case. Sample test cases should help participants better understand the statement. Don't write something to bail out yourself. 

Do not use uppercase varable names like `N`, use lowercase: `n`.

You can preview your problem by clicking on "..." (to the left of "Save changes") and then "View access link".


## Checker
For problems having multiple answers, we need checker. To write checker, first, read input from stdin, then read user output from stdin. Put assert to give wrong answer, otherwise, to print the score, use stdout.
Don't check "relative scoring". 
Here is an example: [Problem](https://www.hackerearth.com/problem/approximate/fractions-sequence-b183b02a/), [Checker](https://github.com/ar-pa/HMC-manual/blob/main/sample-checker.cpp).

If when you submit a solution it keeps turning with no result inside after a minute, there is a problem with your checker. Try fixing compile errors or time limits with the checker.

Sometimes the problem is with the judge. Leave the problem and submit your solution several hours later, when judge is free.

## Test generation
* For test cases, use Polygon for preparing problems. If you don't know about Polygon, I can help you.
* There are no restrictions on the number of test cases. Go ahead and make good enough test cases. Sometimes it's reachable with five test cases, sometimes with a hundred.
* Never generate test cases on your machine and upload them.
* Use generator using [testlib](http://codeforces.com/testlib) for generating test cases.
* Don't use multiple-test generator. This type of generator could not be used in stressing.
* When writing a generator, use argv to have some parameters (like n, q, etc). Refer to testlib repository for examples. Then you can add stress (in Polygon) and test solutions easily.
* You can move test cases from Polygon to HMC using [PolygonToHE](https://github.com/ar-pa/polygonToHE).
* We don't prefer problems with subtasks. A wrong solution must get zero score (and for sure a correct solution must get 100). So you can set test scores as you want. Anyway, dividing score to test cases equally is always a good strategy.
* Sometimes we face the state that judges go forever and don't come back with response. In such a case, remove **all** of the test cases and add just one very small test case. Check if judge is still broken. If it fixed, add your test cases again. If problem repeated, it's maybe because of huge input/output.

## Writing generator, validator
Check [Testlib Toturial](codeforces.com/testlib). For examples, check [Testlib Github Repository](https://github.com/MikeMirzayanov/testlib).
Writing a complete validator is necessary for all problems. Take a look at the Testlib guide for more information. Also, don't forget to submit your solution on HMC to get accepted and your validator (it should not get RE on any test case). You need to copy-paste testlib.h above your code when submitting.

## Editorial
We want the editorials written like [this](https://docs.google.com/document/d/17HCQbvIAAliqHB3920QkjaIjLcinSw9_-K83dx6LEJU/edit) and well written like the sample.

About editorials for easy problems: The coder how didn't solved the problem and switched to the editorial, is not strong as you are. Write a editorial that he can understand. Editorial for easier problem should be more detailed than harder ones. You should even point out to implementation in different languages. 

## Contest date
We have three contests per month, Easy, DSA and Circuits. Almost always Easy is held on the first Saturday, DSA is held on the second Saturday, and, Circuits is held on the third Saturday.

## Other points
For raising invoice, please checkout the sheet again, because it's possible that after testing, I update the problem difficulty.
