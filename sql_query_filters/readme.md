# SQL Query Filtering for Security Tasks


## Overview
This project demonstrates my ability to apply SQL queries with filters to investigate security events and manage employee systems. The activity covers retrieving login attempts and filtering employee records to perform security updates.

## Objectives
- Investigate after-hours failed login attempts.
- Examine suspicious login events on specific dates.
- Identify login attempts originating outside Mexico.
- Retrieve employees in specific departments for system updates.
- Apply SQL filters using AND, OR, NOT, and LIKE operators with wildcards.

## Queries
1. **Failed login attempts after hours**
   - Filtered login attempts where `login_time > '18:00'` AND `success = FALSE`.
2. **Login attempts on specific dates**
   - Filtered login attempts using `login_date = '2022-05-09' OR login_date = '2022-05-08'`.
3. **Login attempts outside Mexico**
   - Filtered using `NOT LIKE 'MEX%'` to capture non-Mexico logins.
4. **Employees in Marketing department**
   - Filtered using `department = 'Marketing' AND office LIKE 'East%'`.
5. **Employees in Finance or Sales**
   - Filtered using `department = 'Finance' OR department = 'Sales'`.
6. **Employees not in IT**
   - Filtered using `NOT department = 'Information Technology'`.

## Skills Applied
- SQL query construction
- Logical operators (AND, OR, NOT)
- Pattern matching with LIKE and wildcards (%)
- Data filtering for cybersecurity monitoring and asset management
- Investigating potential security incidents


