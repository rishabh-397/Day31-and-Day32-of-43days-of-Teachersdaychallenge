# Day31-and-Day32-of-43days-of-Teachersdaychallenge

D. Constructing the Array
time limit per test1 second
memory limit per test256 megabytes
You are given an array a
 of length n
 consisting of zeros. You perform n
 actions with this array: during the i
-th action, the following sequence of operations appears:

Choose the maximum by length subarray (continuous subsegment) consisting only of zeros, among all such segments choose the leftmost one;
Let this segment be [l;r]
. If r−l+1
 is odd (not divisible by 2
) then assign (set) a[l+r2]:=i
 (where i
 is the number of the current action), otherwise (if r−l+1
 is even) assign (set) a[l+r−12]:=i
.
Consider the array a
 of length 5
 (initially a=[0,0,0,0,0]
). Then it changes as follows:

Firstly, we choose the segment [1;5]
 and assign a[3]:=1
, so a
 becomes [0,0,1,0,0]
;
then we choose the segment [1;2]
 and assign a[1]:=2
, so a
 becomes [2,0,1,0,0]
;
then we choose the segment [4;5]
 and assign a[4]:=3
, so a
 becomes [2,0,1,3,0]
;
then we choose the segment [2;2]
 and assign a[2]:=4
, so a
 becomes [2,4,1,3,0]
;
and at last we choose the segment [5;5]
 and assign a[5]:=5
, so a
 becomes [2,4,1,3,5]
.
Your task is to find the array a
 of length n
 after performing all n
 actions. Note that the answer exists and unique.

You have to answer t
 independent test cases.

Input
The first line of the input contains one integer t
 (1≤t≤104
) — the number of test cases. Then t
 test cases follow.

The only line of the test case contains one integer n
 (1≤n≤2⋅105
) — the length of a
.

It is guaranteed that the sum of n
 over all test cases does not exceed 2⋅105
 (∑n≤2⋅105
).

Output
For each test case, print the answer — the array a
 of length n
 after performing n
 actions described in the problem statement. Note that the answer exists and unique.

Example

Input
6
1
2
3
4
5
6

Output
1 
1 2 
2 1 3 
3 1 2 4 
2 4 1 3 5 
3 4 1 5 2 6 


A. Gravity Flip
time limit per test1 second
memory limit per test256 megabytes
Little Chris is bored during his physics lessons (too easy), so he has built a toy box to keep himself occupied. The box is special, since it has the ability to change gravity.

There are n columns of toy cubes in the box arranged in a line. The i-th column contains ai cubes. At first, the gravity in the box is pulling the cubes downwards. When Chris switches the gravity, it begins to pull all the cubes to the right side of the box. The figure shows the initial and final configurations of the cubes in the box: the cubes that have changed their position are highlighted with orange.


Given the initial configuration of the toy cubes in the box, find the amounts of cubes in each of the n columns after the gravity switch!

Input
The first line of input contains an integer n (1 ≤ n ≤ 100), the number of the columns in the box. The next line contains n space-separated integer numbers. The i-th number ai (1 ≤ ai ≤ 100) denotes the number of cubes in the i-th column.

Output
Output n integer numbers separated by spaces, where the i-th number is the amount of cubes in the i-th column after the gravity switch.

Examples

Input
4
3 2 1 2

Output
1 2 2 3 

Input
3
2 3 8

Output
2 3 8 

C. Registration system
time limit per test5 seconds
memory limit per test64 megabytes
A new e-mail service "Berlandesk" is going to be opened in Berland in the near future. The site administration wants to launch their project as soon as possible, that's why they ask you to help. You're suggested to implement the prototype of site registration system. The system should work on the following principle.

Each time a new user wants to register, he sends to the system a request with his name. If such a name does not exist in the system database, it is inserted into the database, and the user gets the response OK, confirming the successful registration. If the name already exists in the system database, the system makes up a new user name, sends it to the user as a prompt and also inserts the prompt into the database. The new name is formed by the following rule. Numbers, starting with 1, are appended one after another to name (name1, name2, ...), among these numbers the least i is found so that namei does not yet exist in the database.

Input
The first line contains number n (1 ≤ n ≤ 105). The following n lines contain the requests to the system. Each request is a non-empty line, and consists of not more than 32 characters, which are all lowercase Latin letters.

Output
Print n lines, which are system responses to the requests: OK in case of successful registration, or a prompt with a new name, if the requested name is already taken.

Examples
Input
4
abacaba
acaba
abacaba
acab

Output
OK
OK
abacaba1
OK

Input
6
first
first
second
second
third
third

Output
OK
first1
OK
second1
OK
third1



