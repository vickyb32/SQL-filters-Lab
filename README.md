<h1>SQL-Filters-Lab</h1>

<h2>Description/Scenario</h2>
<br /> My organization is working to make their system more secure. It is my job to ensure the system
is safe, investigate all potential security issues, and update employee computers as needed.
The following steps provide examples of how I used SQL with filters to perform
security-related tasks.


<h2>Retrieve after hours failed login attempts:</h2>
<br /> There was a potential security incident that occurred after business hours (after 18:00). All after
hours login attempts that failed need to be investigated.
The following code demonstrates how I created a SQL query to filter for failed login attempts
that occurred after business hours.


 <br/>
<img src="https://i.imgur.com/Bc1bfjX.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br /> The first part of the screenshot is my query, and the second part is a portion of the output.
This query filters for failed login attempts that occurred after 18:00. First, I started by selecting
all data from the log_in_attempts table. Then, I used a WHERE clause with an AND operator
to filter my results to output only login attempts that occurred after 18:00 and were
unsuccessful. The first condition is login_time > '18:00', which filters for the login
attempts that occurred after 18:00. The second condition is success = FALSE, which filters
for the failed login attempts.
<br />
<h2>Retrieve login attempts on specific dates:</h2>
 
<br />A suspicious event occurred on 2022-05-09. Any login activity that happened on 2022-05-09
or on the day before needs to be investigated. The following code demonstrates how I created a SQL query to filter for login attempts that
occurred on specific dates.
<img src="https://i.imgur.com/hTeXMb5.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br /> The first part of the screenshot is my query, and the second part is a portion of the output.
This query returns all login attempts that occurred on 2022-05-09 or 2022-05-08. First, I
started by selecting all data from the log_in_attempts table. Then, I used a WHERE clause
with an OR operator to filter my results to output only login attempts that occurred on either
2022-05-09 or 2022-05-08. The first condition is login_date = '2022-05-09', which
filters for logins on 2022-05-09. The second condition is login_date = '2022-05-08',
which filters for logins on 2022-05-08.
<br />

<h2>Retrieve login attempts outside of Mexico:</h2>

After investigating the organization’s data on login attempts, I believe there is an issue with the
login attempts that occurred outside of Mexico. These login attempts should be investigated.
The following code demonstrates how I created a SQL query to filter for login attempts that
occurred outside of Mexico.: <br/>
<img src="https://i.imgur.com/henLRQB.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br /> The first part of the screenshot is my query, and the second part is a portion of the output.
This query returns all login attempts that occurred in countries other than Mexico. First, I
started by selecting all data from the log_in_attempts table. Then, I used a WHERE clause
with NOT to filter for countries other than Mexico. I used LIKE with MEX% as the pattern to
match because the dataset represents Mexico as MEX and MEXICO. The percentage sign (%)
represents any number of unspecified characters when used with LIKE.
<br />

<h2>Retrieve employees in Marketing:</h2>

<br /> My team wants to update the computers for certain employees in the Marketing department.
To do this, I have to get information on which employee machines to update.
The following code demonstrates how I created a SQL query to filter for employee machines
from employees in the Marketing department in the East building.
:  <br/>
<img src="https://i.imgur.com/M79Y2nn.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />The first part of the screenshot is my query, and the second part is a portion of the output.
This query returns all employees in the Marketing department in the East building. First, I
started by selecting all data from the employees table. Then, I used a WHERE clause with AND
to filter for employees who work in the Marketing department and in the East building. I used
LIKE with East% as the pattern to match because the data in the office column represents
the East building with the specific office number. The first condition is the department =
'Marketing' portion, which filters for employees in the Marketing department. The second
condition is the office LIKE 'East%' portion, which filters for employees in the East
building.
<br />


<h2>Retrieve employees in Finance or Sales:</h2>
The machines for employees in the Finance and Sales departments also need to be updated.
Since a different security update is needed, I have to get information on employees only from
these two departments.
The following code demonstrates how I created a SQL query to filter for employee machines
from employees in the Finance or Sales departments.:  <br/>
<img src="https://i.imgur.com/AWVQaqe.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />The first part of the screenshot is my query, and the second part is a portion of the output.
This query returns all employees in the Finance and Sales departments. First, I started by
selecting all data from the employees table. Then, I used a WHERE clause with OR to filter for
employees who are in the Finance and Sales departments. I used the OR operator instead of
AND because I want all employees who are in either department. The first condition is
department = 'Finance', which filters for employees from the Finance department. The
second condition is department = 'Sales', which filters for employees from the Sales
department.
<br />

<h2>Retrieve all employees not in IT:</h2>

My team needs to make one more security update on employees who are not in the
Information Technology department. To make the update, I first have to get information on
these employees.
The following demonstrates how I created a SQL query to filter for employee machines from
employees not in the Information Technology department.  <br/>
<img src="https://i.imgur.com/xdaLh9u.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />The first part of the screenshot is my query, and the second part is a portion of the output. The
query returns all employees not in the Information Technology department. First, I started by
selecting all data from the employees table. Then, I used a WHERE clause with NOT to filter for
employees not in this department.
<br />

<h2>Summary:</h2>

I applied filters to SQL queries to get specific information on login attempts and employee
machines. I used two different tables, log_in_attempts and employees. I used the AND,
OR, and NOT operators to filter for the specific information needed for each task. I also used
LIKE and the percentage sign (%) wildcard to filter for patterns. <br/>


<!--
 ```diff
- text in red
+ text in green
! text in orange
# text in gray
@@ text in purple (and bold)@@
```
--!>
