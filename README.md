# HMC-manual
Hackerearth Monthly Contests manual for problem setters

This manual is under writing, not completed yet.

# Propose a problem
[Check this blog](https://codeforces.com/blog/entry/73839) and [this](https://docs.google.com/document/d/1zD2imtOyX4fCFCg_5Yf5Va1Y5KV1494trFgkty_E1wM/edit#heading=h.o69k3hsgdlqi).

# Selection
For every contest, I (Arpa) check your proposals and accept some of them. Also, I'm trying to accept some problems as backup problems. // TODO

# Preparation
## Things to be done
Let the day the email sent be d, 

| S. No. | Task                                                                                                                                                                                                                                                                                                                                                                                                                                                                                               | Deadline    | Assigned to |
|--------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------|-------------|
| 1      | Fill this form to get access to the HMC dashboard.                                                                                                                                                                                                                                                                                                                                                                                                                                                 | d + 1      | Setters     |
| 2      | Finish writing complete statements on the HMC dashboard. Mark the problem as ready for testing.                                                                                                                                                                                                                                                                                                                                                                                                    | d + 1      | Setters     |
| 3      | Do the following for your problem in order: <br>- Generate test cases <br>- Write solutions <br>- Write editorials <br>- Write validator <br>- Write a naive solution (optional)  <br>- After creating a problem in Polygon, share it with me using the "Manage access" tab. My username is "arpa". Give me WRITE access. | d + 4   | Setters     |
| 4      | Grammar verification - I will notify you on this email thread after grammar verification is complete                                                                                                                                                                                                                                                                                                                                                                                               | TBA         | Yash        |
| 5      | Verification of grammar-verified statements - Read your statement - Check for change in meaning if any - Respond in the same email thread to Yash (one email with all the changes) No changes will be made in the last week                                                                                                                                                                                                                                                                            | TBA         | Setters     |
| 6      | Testing of the entire problem                                                                                                                                                                                                                                                                                                                                                                                                                                                                      | d + 7~10 | Arpa        |
| 7      | Transfer test cases, solution, etc. from Polygon/TPS to HMC dashboard                                                                                                                                                                                                                                                                                                                                                                                                                              | d + 4      | Setters     |
| 8      | Problems marked as ready                                                                                                                                                                                                                                                                                                                                                                                                                                                                           | 3 days  before the contest      | Arpa        |
| 9      | Publish a blog post on Codeforces - You can search for some examples. - Volunteer and let me know who is doing this - Search names of authors to find their username on Codeforces.                                                                                                                                                                                                                                                                                                                | TBA         | Setters     |
| 10     | Contest goes live                                                                                                                                                                                                                                                                                                                                                                                                                                                                                  | TBA         | Arpit       |

For test cases, use Polygon or TPS for preparing problems. Don't create test cases locally and upload them to Polygon. It's important. If you don't know about Polygon and TPS, I can help you.
Times are in IST.
Dates are inclusive.
Although there is a gap between when you finish and the contest date, it's not acceptable that you prepare something after the deadline. We need that time for a substitution if needed.
Useful links: HMC, Polygon, Polygon help, Testlib, polygonToHE.
Important note: From August contests, writing a complete validator is necessary for all problems. Take a look at the Testlib guide for more information. Also, don't forget to submit your solution on HMC to get accepted and your validator (it should not get RE on any test case). You need to copy-paste testlib.h above your code when submitting.
After you finished the first task, please notify us (me and +Tripti Padukone) in this thread.
Please note that even if you have access previously, send an acknowledgment email that you'll prepare your problem in the given deadline.
If you are unwilling or you can't prepare the problem in the given time, please notify me today.
Here is the task sheet (check the "DSA" tab). Don't forget to color cells with green when you finish a task. Change your email address to your name in the cells.
Always CC: Tripti and Yash on all emails.

## Maintaining HMC master tracker
After you finished a task, color the corresponding cell with green. Put your problem link in the "Setter link" column. It's something like: https://app.hackerearth.com/setter/problemform/hmc/algorithm-template/43646/.

Sum of scores must be 100.

## Statement format
story, input, output, constraints
samples

Dear setters, to make statements more clear, let's add more than one sample test cases.
* I always recommend you use a parameter t in your problem and give a bunch of test cases in a test file. If you're using this format, simply set a suitable t. Try to give as many sample tests as possible to help contestants get the statement easier. Even generate a little big (n = 10) random test cases to help them.
* Otherwise, write your sample test cases 2, 3, ... in the statement section.

You can preview your problem by clicking on "..." (to the left of "Save changes") and then "View access link".

For problems having multiple answers, we need checker. To write checker, first, read input from stdin, then read user output from stdin. Put assert to give wrong answer, otherwise, to print the score, use stdout.
Don't check "relative scoring". 
Here is an example: [Problem](https://www.hackerearth.com/problem/approximate/fractions-sequence-b183b02a/), [Checker](https://github.com/ar-pa/HMC-manual/blob/main/sample-checker.cpp).

### Checker troubleshoot
If when you submit a solution it keeps turning with no result inside after a minute, there is a problem with your checker. Try fixing compile errors or time limits with the checker.

### Test generation
* Never generate test cases on your machine and upload them.
* Use generator using [testlib](http://codeforces.com/testlib) for generating test cases.
* Don't use multiple-test generator. This type of generator could not be used in stressing.

### Writing generator, validator
Check [Testlib Toturial](codeforces.com/testlib).
