# Applying-filters-to-SQL-queries

## Objective

In this lab, I apply additional filters to SQL queries to retrieve specific information from a database. I use standard SQL operators to filter data based on particular dates and times. Throughout this process, I execute SQL queries using the MariaDB shell.
This is a Quciklabs-based project hosted on the Google Cloud.

### Skills Learned
[Bullet Points - Remove this afterwards]

- Advanced understanding of SIEM concepts and practical application.
- Proficiency in analyzing and interpreting network logs.
- Ability to generate and recognize attack signatures and patterns.
- Enhanced knowledge of network protocols and security vulnerabilities.
- Development of critical thinking and problem-solving skills in cybersecurity.

### Tools Used
[Bullet Points - Remove this afterwards]

- Security Information and Event Management (SIEM) system for log ingestion and analysis.
- Network analysis tools (such as Wireshark) for capturing and examining network traffic.
- Telemetry generation tools to create realistic network traffic and attack scenarios.

## Scenario
In this project, you’re investigating a recent security incident.

You need to gather information about login attempts for certain dates and times. This will help in resolving a security incident.

You’ll first need to retrieve login events made after a certain date. Second, you’ll narrow the focus of the search to filter logins in a date range. Third, you’ll investigate logins that were made at certain times. 
Finally, filter login attempts based on their event IDs.

## My Procedure 
I structured the procedure into four main tasks, as demonstrated below:

### Task 1. Retrieve login attempts after a certain date 
In this task, I am investigating a recent security incident. To do this, I need to gather information about login attempts made after a certain date.
I carried out this task in two steps: 

1. To retrieve data for login attempts made after '2022-05-09', I completed the SQL query using the greater than operator:

```
SELECT *
FROM login_attempts
WHERE login_time > '2022-05-09';
```
![Z1](https://github.com/godfreyndlovu/Applying-filters-to-SQL-queries/assets/102636518/62bc2f7d-ac0b-4026-b449-8d046554548e)


The number of login attempts made after '2022-05-09' is **125**.

2. Based on my initial query, I now needed to expand the date range to include login attempts made on or after '2022-05-09'. To do this, I completed the SQL query using the greater than or equal to operator:

```
SELECT *
FROM login_attempts
WHERE login_time >= '2022-05-09';
```
![Z2](https://github.com/godfreyndlovu/Applying-filters-to-SQL-queries/assets/102636518/8c28d358-5216-49c0-80b3-526b26d10b86)

The number of login attempts made from 2022-05-09 onward is **165**.


### Task 2. Retrieve login attempts after a certain date 
In this task, I needed to narrow the focus of my search. I needed exclude login attempts made after 2022-05-11. To achieve this, I used the BETWEEN and AND operators to return results between '2022-05-09' and '2022-05-11':

```
SELECT *
FROM login_attempts
WHERE login_time BETWEEN '2022-05-09' AND '2022-05-11';
```
![Z3](https://github.com/godfreyndlovu/Applying-filters-to-SQL-queries/assets/102636518/a5566657-c170-4c30-8f99-f2b184ef4a65)

**123** login attempts were made between 2022-05-09 and 2022-05-11.

### Task 3.  Investigate logins at certain times 
In this task, I needed to investigate logins that occurred at specific times. To begin, I needed to filter the data in the login_attempts table by login time (login_time).

First, our organization's typical work hours begin at 07:00:00. I'd need to retrieve all login attempts made before 07:00:00 to understand more about the users who are logging in outside of these typical hours.

1. I wrote SQL query to retrieve data for login attempts made before '07:00:00'

```
SELECT *
FROM login_attempts
WHERE TIME(login_time) < '07:00:00';
```
![Z4](https://github.com/godfreyndlovu/Applying-filters-to-SQL-queries/assets/102636518/8175fd85-f794-483b-8574-722483d23bc0)

The username in the fifth record returned from this query is **eraab**.

### Task 4. Investigate logins by event ID
In this task, I am investigating a recent security incident. To do this, I need to gather information about login attempts made after a certain date.
I carried out this task in two steps: 






















<h2>Languages and Utilities Used</h2>

- <b>PowerShell</b> 
- <b>Diskpart</b>

<h2>Environments Used </h2>

- <b>Windows 10</b> (21H2)

<h2>Program walk-through:</h2>

<p align="center">
Launch the utility: <br/>
<img src="https://i.imgur.com/62TgaWL.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<br />
Select the disk:  <br/>
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
