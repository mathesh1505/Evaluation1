# Git:

1)What is git

Git is a version control tool and we can be use by our local computer without having the internet connection.

2)What is repository

Repository is the storing area and By using the Repository we can able to store the files. 

3)Use of status command

Status command is used to see what are the files are stagged and unstagged in the local.

4)What is the command to initialize the git

We use git init command to initialize the git.

5)What is the use of push command 

By using the push command we can able to upload the files and changes we made in the local to the remote repository.

6)Difference between fetch and pull

Git fetch only downloads the files from remote to the local and it doesn't merge the files automatically.

Git pull download and merge the files from remote to the local automatically. Gitpull=Gitfetch + Gitmerge.

7)What is the use of git ignore

By using .gitignore we can able to ignore the unwanted files like cache.It will tell what are the files have to be untrack.

8)What is the command for know the commit history

git log is the command we can use for see the commit history.

9)Command for switching the branch

Git checkout is the command used for to switching the branch.

10)What is merge conflict and how to fix it

when two or more users can edit the same file and they want to push that file the merge conflicts will occur.Then the admin will have the notification in remote as merge conflict will occur then the admin have to decide which changes will be there then solve the conflicts and merge the changes into the main repository.  

# Python:

1)Use of python

Python is the high level interpreter language, scalable,
faster and secure.

2)Difference between list and set

List is mutable datatype we can able to change the values in the list and it will have duplicates value and it can be denoted by [].

Set is also a mutable datatype we can change the values in the set and it doesn't allow the duplicate values.

3)Use of break statement

By using the Break statement we can terminate the loop and return the value.

Program:  

input: totalSalesAmount

output: total_sales_amount

input: EmployeeName

output: employee_name

texts="totalSalesAmount","EmployeeName"

for text in texts:

  result=""

  for char in text():
	
    if char.isupper():
    
                  result +="_"+char.lower()
		else:
    
                result +=char
	
  if result.startswith("_):
	
    result=result[1:]
	
  print(result)

list = [1,2,2,3,3,4,5,6,6,6,7]

result=""

for num in list():

  if num not in result:
  
               result.append(num) 

print(result)

# SQL:

1)define DDL

Data Definition Language contains the command like create,drop,truncate and alter.

2)Difference between drop, truncate and delete

Drop vanish the whole table structure.

Truncate removes the value in the table.

Delete removes the particular row or value based on the given condition.

3)Difference between where and having

Where is the conditional command and it is used before the group by statement.

Having clause is also a conditional statement and we can use by after the group by statement.

4)Difference between group by and windows

Group by statement returns the values as group 

Windows functions returns all the values by group 

5)Joins and it's types

Joins can be define by it will combine the two tables by the column. Inner, Left, Right, Full and cross joins are it's types. 

6)Use of union

By using the union we can combine the table by it's row

7)Difference between inner join and union

Inner join combines the two tables by the primary and foreign key and it will only returns the common values by the primary key.

Union combines the two table values by the row and it doesn't take the duplicate values.

8)What is foreign key

Foreign key is the unique key and it connect the two table

emp_id	name	department	salary	joining_date
1	Alice	HR	50000	2022-01-15
2	Bob	IT	60000	2021-03-12
3	Charlie	IT	70000	2020-07-25
4	David	Finance	55000	2022-06-01
5	Eva	HR	65000	2019-12-30
6	Frank	Finance	70000	2020-09-20
7	Grace	IT	60000	2021-11-10

Find duplicate salary

select * from(

select name,department,salary,count(*) over(partition by salary) as duplicate

 from employees ) t

where duplicate>1

Department wise Average salary

select department,avg(salary)

from employees 

group by department
