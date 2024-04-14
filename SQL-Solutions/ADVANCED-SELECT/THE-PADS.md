> ### Generate the following two result sets:
>
> - ####  Query an alphabetically ordered list of all names in OCCUPATIONS, immediately followed by the first letter of each profession as a parenthetical (i.e.: enclosed in parentheses). For example: AnActorName(A), ADoctorName(D), AProfessorName(P), and ASingerName(S).
> - #### Query the number of ocurrences of each occupation in OCCUPATIONS. Sort the occurrences in ascending order, and output them in the following format:
> > **There are a total of [occupation_count] [occupation]s.**
>
> #### ***Note: There will be at least two entries in the table for each type of occupation.***
**Input Format**<br>

---
![1443816414-2a465532e7-1](https://github.com/Niket-mishra/Hackerrank-solutions/assets/157272356/ea7e41c1-23fa-4aa3-8d3c-ce383694c73c)
---
Occupation will only contain one of the following values: **Doctor, Professor, Singer or Actor.**
___
![1443816608-0b4d01d157-2](https://github.com/Niket-mishra/Hackerrank-solutions/assets/157272356/086a27de-62be-42eb-ac02-379c57e61096)
---
#### Sample Output -
___
> Ashely(P)
> 
>
> Christeen(P)
>
> Jane(A)
>
> Jenny(D)
>
> Julia(A)
>
> Ketty(P)
>
> Maria(A)
>
> Meera(S)
>
> Priya(S)
>
> Samantha(D)
>
> There are a total of 2 doctors.
>
> There are a total of 2 singers.
>
> There are a total of 3 actors.
>
> There are a total of 3 professors.
>

#### Solution -

```
SELECT CONCAT(name, '(', LEFT(occupation, 1), ')') AS full_info
FROM OCCUPATIONS
ORDER BY name;
SELECT CONCAT('There are a total of ', COUNT(occupation), ' ', LOWER(occupation), 's.') AS result
FROM OCCUPATIONS
GROUP BY occupation
ORDER BY COUNT(occupation), occupation;

```
