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

<p align="center">
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
 

<img src="https://i.imgur.com/tcTyMUE.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<br />
Enter the number of passes: <br/>
<img src="https://i.imgur.com/nCIbXbg.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<br />
Confirm your selection:  <br/>
<img src="https://i.imgur.com/cdFHBiU.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<br />
Wait for process to complete (may take some time):  <br/>
<img src="https://i.imgur.com/JL945Ga.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<br />
Sanitization complete:  <br/>
<img src="https://i.imgur.com/K71yaM2.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<br />
Observe the wiped disk:  <br/>
<img src="https://i.imgur.com/AeZkvFQ.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>

<!--
 ```diff
- text in red
+ text in green
! text in orange
# text in gray
@@ text in purple (and bold)@@
```
--!>
