Download Link: https://assignmentchef.com/product/solved-eecs484-homework-2-write-sql-queries-given-a-schema
<br>
<h1>Part 1</h1>

<strong>Part 1:</strong> You are asked to write SQL queries given a schema. We will not be providing you with a database for this question. It is advised that you think of some way to be able to check if your queries really work the way they should. Please submit this part in separate files specified in each of the problem.

<strong>Part 2:</strong> This part requires you to look at the database associated with a sql file called <strong><em>booktown.sql</em></strong>​ ​. This file should be attached along with this document on canvas. You will need your Oracle account to load and see the database. Please answer question 5 in the file named <strong><em>booktownqueries_problems.sql</em></strong>​ ​<em>.</em> Question 6 is to be answered in a pdf file called ​<strong><em>hw2q6.pdf</em></strong>​. Please neatly write the relational algebra and relational calculus questions and scan them with a high quality scanner (either a good phone or a scanner found in the library). Alternatively, you can write them using an equation writing software (e.g. LaTeX).

Write some queries for the given relational schema. You are given the following relations (primary keys are underlined):

Student (<u>​</u><strong><u>sid</u></strong><u>​</u>, name, major) : student ID, name, and majors of students

Project (<u>​</u><strong><u>pid</u></strong><u>​</u>, ptitle) : project ID and title of projects

Course (<u>​</u><strong><u>cid</u></strong><u>​</u>, title) : course ID and title of courses

Member (<u>​</u><strong><u>pid</u></strong>, <u>​ </u><strong><u>sid</u></strong><u>​         </u>)<u>​</u> : Relationship. Student sid is a member of project pid Enrolled (<u>​</u><strong><u>sid</u></strong><u>​</u>, <u>​</u><strong><u>cid</u></strong><u>​</u>) : Relationship. Student sid is enrolled in course cid.

<strong><em>Please submit the answers to these questions in </em></strong><u>​</u><strong><em><u>separate</u></em></strong><strong><em> <u>files</u></em></strong><strong><em> as shown. The files </em></strong><strong><em>should execute within sqlplus</em></strong><strong><em> and should only answer the query (no need to create tables). </em></strong>

<strong>Question 1 </strong>

Find the student IDs of all students who are enrolled in (‘EECS484’ and ‘EECS485’) or enrolled in (‘EECS482’ and ‘EECS486’) or enrolled in ‘EECS281’. For example, student A will be the output if student A is enrolled in (‘EECS484’ and ‘EECS485’) or (‘EECS482’ and ‘EECS486’) or (‘EECS281’). ​<em>Note that ‘EECS482’ is a course title. </em>

<em>Correct solutions that use views, nested queries will only receive 50% of the grade. </em>​(This query can be done without views, nested queries)

FIle: q1.sql

<strong>Question 2</strong>

Find the student IDs of all students who have a project partner who is enrolled in either ‘EECS482’ or ‘EECS483’ and either ‘EECS484’ or ‘EECS485’ and ‘EECS280’. For example, student A will be the output if students A and B are project partners and B is enrolled in (‘EECS482’ or ‘EECS483’) and (‘EECS484’ or ‘EECS485’) and (‘EECS280’).

<em>Correct solutions that use views, nested queries, or set operation like intersections, minus, or unions will receive only 50% credit.</em> (This query can be done without views, nested queries, intersections, minus, or unions)

FIle: q2.sql

<strong>Question 3 :</strong>

We would like to know the <strong>CS</strong>​<strong> majors</strong> who are taking non-heavy CS-based courses. We define non-heavy CS-based courses as courses where more than 100 non-CS majors are enrolled. Return all the student IDs (sid) and names of these CS students. The result of the query should be output in decreasing order by name.

<em>You may use views or nested queries for this part. </em>

File: q3.sql

<strong>Question 4 :                </strong>

The school is interested in seeing the possible combinations of students who take a course together but are not project partners. Define a VIEW called <strong>StudentPairs</strong>​ that contains all student ID pairs (sid1, sid2) with the following property: The students who are enrolled in a common course but are not members of the same project. List each pair of students only once. For example, if you list (1, 2), do not list (2, 1). Student IDs can be assumed to be integers. <em>You may use views or nested queries for this part. Correct solutions that use extra tables than needed will receive only 50% credit.  </em>

<em>Hint: This one is actually quite subtle and tricky! Try not to lose potential student pairs when joining your tables! </em>

FIle: q4.sql     <strong> </strong>

<h1>Part 2</h1>

We have provided you a sample database in ​<strong>booktown.sql</strong>.​ Please look through the beginning of this file to understand the schema. Feel free to add more sample data to test your answers. However, don’t change the schema! We <em>will</em>​ ​be testing your answers using the schema that we have given you.

To build the database in SQLPlus, log into CAEN and navigate to the directory where booktown.sql is located at. Run sqlplus as in Project 1 to connect to Oracle and load booktown.sql:

<strong>SQL&gt; </strong>​START booktown.sql

<strong>Question 5 </strong>

<ul>

 <li>Please provide queries to the questions listed in <strong>sql</strong>​ .​  – There should be 8 questions in total in this file.</li>

 <li>Your queries should work for any database with the schema provided in ​<strong>sql</strong>​, ​<em>not</em> just with the same data we have given you.</li>

 <li>​If you ever make intermediate view, make sure you ​<strong><em>drop</em></strong>​ them at the end of that question.</li>

</ul>

<strong>Clarifications:  </strong>

For problem 3 in question 5, ​<em>List titles, publication, author’s id, author’s last name, and author’s first name of all books by authors who have published a book after 1999-10-01 but before 2001-10-01</em>​. Here <strong><em>who have published a book</em></strong>​ ​we mean ​<strong>at least one book</strong>​ rather than exactly one book.

<strong>IMPORTANT:</strong> Ensure that once you are done, the entire ​<strong>booktownqueries_problems.sql</strong> can run completely without errors by:

<strong>SQL&gt; </strong>​START booktownqueries_problems.sql

<strong>Question 6 : </strong>

Write Relational algebra expressions for your solutions to Q5.1, Q5.2, Q5.3 and Q5.4 (in booktownqueries_problems.sql). Write Relational calculus expressions for Q5.1, Q5.2 and Q5.3 (in booktownqueries_problems.sql).

These do not involve aggregation and should be doable with relational algebra.


