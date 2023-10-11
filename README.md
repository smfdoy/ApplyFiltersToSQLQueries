<h1>Apply filters to SQL queries</h1>

 ### 

<h2>Project Description</h2>
Working to make their system more secure. It is my job to ensure the system is safe, investigate all potential security issues, and update employee computers as needed. The following steps provide examples of how I used SQL with filters to perform security-related tasks.<br />


<h2>Languages and Utilities Used</h2>

- <b>SQL</b>
- <b>Bash</b>

<h2>Project Walk-Through:</h2>

<p align="center">
<b>Retrieve after hours failed login attempts</b>
<br/> There was a potential security incident that occurred after business hours (after 18:00). All after hours login attempts that failed need to be investigated. <br/>
<br/> The following code demonstrates how I created a SQL query to filter for failed login attempts that occurred after business hours.<br/>
<br/> <img src="https://i.imgur.com/M5AY2BN.png" height="80%" width="80%" alt=/>
<br/> The first part of the screenshot is my query, and the second part is a portion of the output. This query filters for failed login attempts that occurred after 18:00. First, I started by selecting all data from the <i>log_in_attempts</i> table. Then, I used a <i>WHERE</i> clause with an <i>AND</i> operator to filter my results to output only login attempts that occurred after 18:00 and were unsuccessful. The first condition is <i>login_time > '18:00'</i>, which filters for the login attempts that occurred after 18:00. The second condition is <i>success = FALSE</i>, which filters for the failed login attempts. <br/>
<br/>
<b>Retrieve login attempts on specific dates</b> <br/>
A suspicious event occurred on 2022-05-09. Any login activity that happened on 2022-05-09 or on the day before needs to be investigated.<br/>
<br/>
The following code demonstrates how I created a SQL query to filter for login attempts that occurred on specific dates.<br/>
<br/> <img src="https://i.imgur.com/XAry2uh.png" height="80%" width="80%" alt=/>
<br />The first part of the screenshot is my query, and the second part is a portion of the output. This query returns all login attempts that occurred on 2022-05-09 or 2022-05-08. First, I started by selecting all data from the <i>log_in_attempts</i> table. Then, I used a <i>WHERE</i> clause with an <i>OR</i> operator to filter my results to output only login attempts that occurred on either 2022-05-09 or 2022-05-08. The first condition is <i>login_date = '2022-05-09'</i>, which filters for logins on 2022-05-09. The second condition is <i>login_date = '2022-05-08'</i>, which filters for logins on 2022-05-08.<br/>
<br />
<p align="center">
<b> Retrieve login attempts outside of Mexico</b> <br/>
After investigating the organization’s data on login attempts, I believe there is an issue with the login attempts that occurred outside of Mexico. These login attempts should be investigated.<br/>
 <br/>
The following code demonstrates how I created a SQL query to filter for login attempts that occurred outside of Mexico. <br />
<br />
<img src="https://i.imgur.com/5Y3Jr7v.png" height="80%" width="80%"alt=/><br />
The first part of the screenshot is my query, and the second part is a portion of the output. This query returns all login attempts that occurred in countries other than Mexico. First, I started by selecting all data from the <i>log_in_attempts</i> table. Then, I used a <i>WHERE</i> clause with <i>NOT</i> to filter for countries other than Mexico. I used <i>LIKE</i> with <i>MEX%</i> as the pattern to match because the dataset represents Mexico as <i>MEX</i> and <i>MEXICO</i>. The percentage sign (%) represents any number of unspecified characters when used with <i>LIKE</i>. <br/>
<br/>
<b>Retrieve employees in Marketing</b>  
 <br/>
My team wants to update the computers for certain employees in the Marketing department. To do this, I have to get information on which employee machines to update.<br/>
<br/>
The following code demonstrates how I created a SQL query to filter for employee machines from employees in the Marketing department in the East building.
<br/>
<br/>
<img src="https://i.imgur.com/wj0GQjg.png" height="80%" width="80%" alt=/>
<br />
 The first part of the screenshot is my query, and the second part is a portion of the output. This query returns all employees in the Marketing department in the East building. First, I started by selecting all data from the <i>employees</i> table. Then, I used a <i>WHERE</i> clause with <i>AND</i> to filter for employees who work in the Marketing department and in the East building. I used <i>LIKE</i> with <i>East%</i> as the pattern to match because the data in the office column represents the East building with the specific office number. The first condition is the <i>department ='Marketing'</i> portion, which filters for employees in the Marketing department. The second condition is the <i>office LIKE 'East%'</i> portion, which filters for employees in the East building.
 <br />
 <br />
<b>Retrieve employees in Finance or Sales</b>  
<br/>
 The machines for employees in the Finance and Sales departments also need to be updated. Since a different security update is needed, I have to get information on employees only from these two departments.<br/>
<br/>
The following code demonstrates how I created a SQL query to filter for employee machines from employees in the Finance or Sales departments.<br/>
<br/>
<img src="https://i.imgur.com/4yp1tU8.png" height="80%" width="80%" alt=/>
<br />
The first part of the screenshot is my query, and the second part is a portion of the output. This query returns all employees in the Finance and Sales departments. First, I started by selecting all data from the <i>employees</i> table. Then, I used a <i>WHERE</i> clause with <i>OR</i> to filter for employees who are in the Finance and Sales departments. I used the <i>OR</i> operator instead of <i>AND</i> because I want all employees who are in either department. The first condition is <i>department = 'Finance'</i>, which filters for employees from the Finance department. The second condition is <i>department = 'Sales'</i>, which filters for employees from the Sales department.
 <br />
 <br />
<b>Retrieve all employees not in IT</b>  
<br/>
My team needs to make one more security update on employees who are not in the Information Technology department. To make the update, I first have to get information on these employees.<br/>
<br/>
The following demonstrates how I created a SQL query to filter for employee machines from employees not in the  Information Technology department.<br/>
<br/>
<img src="https://i.imgur.com/2Q04Rvv.png" height="80%" width="80%" alt=/>
<br />
The first part of the screenshot is my query, and the second part is a portion of the output. The query returns all employees not in the Information Technology department. First, I started by selecting all data from the <i>employees</i> table. Then, I used a <i>WHERE</i> clause with <i>NOT</i> to filter for employees not in this department.<br/>
 <br/>
 <b>Summary:</b>  <br/>
I applied filters to SQL queries to get specific information on login attempts and employee machines. I used two different tables, <i>log_in_attempts</i> and <i>employees</i>. I used the <i>AND</i>, <i>OR</i>, and <i>NOT</i> operators to filter for the specific information needed for each task. I also used <i>LIKE</i> and the percentage sign (%) wildcard to filter for patterns.<br />
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
