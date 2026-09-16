An example of the use of subqueries in SQL
In this code, I try to solve a problem that's given by Claude in a prompt I wrote.
The context is the following : 
    I have a database of AAPL's stock prices between 2016-09-08 and 2021-09-07 (YYY-MM-DD).
    During my introduction to SQL, I discovered "subqueries". So, I asked Claude to give me exercises on subqueries, applied to my database.
    One exercise was : keep the rows where the volume is higher than the average volume on the whole period (i.e the average volume between 2016 and 2021).

    After completing the exercise, I thought that one might only want the rows where the volume is higher than the average that same year, not across the whole period.
    This code shows 4 different ways to approch this question.
    The 2 first approches use uncorrelated subqueries, while the 2 last approches use correlated subqueries.
