# SQL Subqueries Example

An example of the use of subqueries in SQL.  
In this code, I try to solve a problem that's given by Claude in a prompt I wrote.

## Context

I have a database of AAPL's stock prices between 2016-09-08 and 2021-09-07 (`YYYY-MM-DD`).

During my introduction to SQL, I discovered "subqueries". So, I asked Claude to give me exercises on subqueries, applied to my database.  
One exercise was:
> Keep the rows where the volume is higher than the average volume on the whole period (i.e. the average volume between 2016 and 2021).

After completing the exercise, I thought that one might only want the rows where the volume is higher than the average that same year, not across the whole period.

This code shows 4 different ways to approach this question:
- The 2 first approaches use **uncorrelated subqueries**.
- The 2 last approaches use **correlated subqueries**.



### Note: How did I reason ?
I didn't understand correlated subqueries at first glance; it took me time to get a better grasp of them.
What I did, in order to solve this problem, was to:
1. **Create the code on a smaller alternative database.**

   The problem can be viewed in many ways.
   I viewed it in a more generalised way, which was to only keep the rows where their value in a given column is greater than the average value for that same year.
   So I tried to solve this problem on an alternative database with 10 observations, with the following columns: id, name, age, email, year.
   Applied to this alternative database, the problem was to keep the rows where the age of the person is greater than the average age for their year.

   The reason lies in the control, visualization and verification of the results: since this alternative database has few rows, it's easier to verify the results.


2. **Adapt the code to the real database.**

   Once I fetched the right correlated subquery that worked on the smaller alternative database, I adapted it to the real database.
