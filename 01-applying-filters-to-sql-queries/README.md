\# Applying Filters to SQL Queries



\## Project Description

As part of an organizational effort to strengthen system security, I used SQL to

investigate potential security issues: analyzing login activity for suspicious

patterns and identifying employee devices that required a security update. The

work uses two tables in a MariaDB database — `log\_in\_attempts` and `employees`

(schemas documented in `docs/Table\_formats.pdf`).



\## Tasks and Queries



\*\*1. After-hours failed login attempts\*\*

Investigated a potential security incident by isolating failed logins after 18:00.

```sql

SELECT \* FROM log\_in\_attempts

WHERE login\_time > '18:00' AND success = FALSE;

```

Combined two conditions with `AND` to narrow results to failed attempts outside

business hours.



\*\*2. Login attempts on specific dates\*\*

A suspicious event on 2022-05-09 required reviewing activity from that date and

the day before.

```sql

SELECT \* FROM log\_in\_attempts

WHERE login\_date = '2022-05-09' OR login\_date = '2022-05-08';

```

Used `OR` to pull both dates in a single query.



\*\*3. Login attempts outside Mexico\*\*

```sql

SELECT \* FROM log\_in\_attempts

WHERE NOT country LIKE 'MEX%';

```

Used `NOT` with `LIKE` and the `%` wildcard to exclude both `MEX` and `MEXICO`

formats present in the dataset — a single pattern match handled the inconsistency.



\*\*4. Employees in

