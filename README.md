<h1>Apply filters to SQL queries</h1>

<h2>Description</h2>
Our organization is committed to enhancing the security of our system. My responsibility involves guaranteeing the system's safety, scrutinizing potential security concerns, and updating employee computers as required. The subsequent steps offer illustrations of how I employed SQL along with filters to execute security-related operations.
<br />


<h2>Languages and Utilities Used</h2>

- <b>SQL</b> 

<h2>Environments Used </h2>

- <b>Linux</b> 

<h2>Retrieve after hours failed login attempts:</h2>


<p align="center">
Retrieve failed login attempts that occurred after business hours. A potential security incident took place after regular business hours (after 18:00). It is imperative to investigate all unsuccessful login attempts that transpired during this time.Below is the SQL code exemplifying how I crafted a query to isolate these failed login attempts. **The following screenshots all contain old data that has since been updated, and permission has been granted for me to use said screenshots as a proof of concept project:**
<br/>
  
<img src="https://i.imgur.com/cMj7r8p.png" height="80%" width="80%" alt="SQL_Lab"/>
<br />
<br />
The initial segment of the screenshot displays my query, while the subsequent part showcases a section of the output. This particular query is designed to narrow down failed login attempts that occurred post 18:00. The process commenced with a selection of all data from the 'log_in_attempts' table. Subsequently, I employed a WHERE clause coupled with an AND operator to refine the results, exclusively displaying login attempts that took place after 18:00 and were unsuccessful. The first criterion, 'login_time > '18:00',' isolates attempts that occurred after this time. The second criterion, 'success = FALSE,' targets the unsuccessful login attempts:  <br/>

<h2>Retrieve login attempts on specific dates:</h2>


<p align="center">
An unusual event raised suspicion on 2022-05-09. Consequently, any login activity that transpired on either 2022-05-09 or the preceding day requires thorough investigation.
Below is the SQL code exemplifying how I formulated a query to isolate login attempts on these specific dates.**<br/>
  
<img src="https://imgur.com/RPHE9Uc.png" height="80%" width="80%" alt="SQL"/>
<br />
<br />
The initial segment of the screenshot displays my query, while the subsequent part showcases a section of the output. This particular query retrieves all login attempts that took place on either 2022-05-09 or 2022-05-08. To achieve this, I initiated by selecting all data from the 'log_in_attempts' table. I then utilized a WHERE clause coupled with an OR operator to refine the results, exclusively displaying login attempts from either 2022-05-09 or 2022-05-08. The first criterion, 'login_date = '2022-05-09',' focuses on logins from 2022-05-09. The second criterion, 'login_date = '2022-05-08',' targets logins from 2022-05-08.


<h2>Retrieve login attempts outside of Mexico:</h2>


<p align="center">
Upon scrutinizing the organization's login attempt data, it has come to my attention that there may be a concern regarding login attempts originating from outside of Mexico. These attempts warrant thorough investigation.
Below is the SQL code exemplifying how I formulated a query to isolate login attempts that occurred outside the borders of Mexico.
Enter the number of passes: <br/>
 
<img src="https://imgur.com/RXuG4kI.png" height="80%" width="80%" alt="SQL"/>

The initial segment of the screenshot displays my query, while the subsequent part showcases a section of the output. This specific query retrieves all login attempts that took place in countries outside of Mexico. The process commenced with a selection of all data from the 'log_in_attempts' table. Following this, I employed a WHERE clause with the NOT operator to isolate countries other than Mexico. To achieve this, I used the LIKE operator in conjunction with the pattern 'MEX%' because the dataset represents Mexico as either 'MEX' or 'MEXICO'. The percentage sign (%) serves as a wildcard, representing any number of unspecified characters when utilized with LIKE.
<br />
<br />


<h2>Retrieve employees in Marketing:</h2>


<p align="center">
My team wants to update the computers for certain employees in the Marketing department. To do this, I have to get information on which employee machines to update.
The following code demonstrates how I created a SQL query to filter for employee machines from employees in the Marketing department in the East building.<br/>
 
<img src="https://imgur.com/ymhji4D.png" height="80%" width="80%" alt="SQL"/>

The initial segment of the screenshot showcases my query, while the subsequent part presents a portion of the output. This particular query isolates all employees working in the Marketing department located in the East building. The process initiated with a selection of all data from the 'employees' table. Following this, I utilized a WHERE clause with an AND operator to refine the results, specifically targeting employees affiliated with both the Marketing department and the East building. To accomplish this, I employed the LIKE operator along with the pattern 'East%' since the 'office' column in the dataset represents the East building along with a specific office number. The initial criterion, 'department = 'Marketing',' selects employees in the Marketing department. The second criterion, 'office LIKE 'East%',' narrows it down to employees in the East building.
<br />
<br />


<h2>Retrieve employees in Finance or Sales:</h2>


<p align="center">
The computers used by employees in the Finance and Sales departments require an update due to the need for a distinct security enhancement. Consequently, I must gather information exclusively from employees in these two departments. Below is the SQL code illustrating how I constructed a query to isolate employee machines belonging to the Finance or Sales departments<br/>
 
<img src="https://imgur.com/dC1fWwf.png" height="80%" width="80%" alt="SQL"/>

The initial segment of the screenshot displays my query, while the subsequent part showcases a section of the output. This particular query retrieves all employees belonging to either the Finance or Sales departments. The process commenced with a selection of all data from the 'employees' table. Following this, I utilized a WHERE clause with an OR operator to refine the results, inclusively targeting employees from either the Finance or Sales departments. I opted for the OR operator over AND since I aim to include employees from either department. The first criterion, 'department = 'Finance',' selects employees from the Finance department. The second criterion, 'department = 'Sales',' narrows it down to employees from the Sales department.
<br />
<br />


<h2>Retrieve all employees not in IT:</h2>


<p align="center">
My team needs to make one more security update on employees who are not in the Information Technology department. To make the update, I first have to get information on these employees.The following demonstrates how I created a SQL query to filter for employee machines from employees not in the  Information Technology department.<br/>
 
<img src="https://imgur.com/biz54M2.png" height="80%" width="80%" alt="SQL"/>

The initial section of the screenshot presents my query, while the subsequent part displays a segment of the output. This query provides a list of employees who are not affiliated with the Information Technology department. The process began with a selection of all data from the 'employees' table. Following this, I applied a WHERE clause with the NOT operator to specifically target employees outside of this department.
<br />
<br />


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
