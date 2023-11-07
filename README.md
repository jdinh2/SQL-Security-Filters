<p align="center">
  <img src="https://upload.wikimedia.org/wikipedia/commons/8/87/Sql_data_base_with_logo.png" alt="SQL Logo" width="400" height="200" />
</p>

> **Disclaimer**: This documentation pertains to a **fictional** company and is part of a lab exercise in the Google Cybersecurity Program. All the data and scenarios presented here are purely fictitious and for educational purposes only.

My organization is striving for enhanced security. I'm at the forefront of this endeavor, ensuring system safety, delving into potential security concerns, and orchestrating necessary updates for employee computers. Below are examples showcasing how I utilized SQL filters for security-specific tasks.

## **1. Retrieve After-Hours Failed Login Attempts**

Following a security incident that took place post-business hours (after 18:00), it became imperative to scrutinize all failed login attempts during this timeframe.

![](https://i.gyazo.com/418ce739a3d46528d3cc27858e48913c.png)

**Description:** This query sifts through the `log_in_attempts` table to find failed login attempts after 18:00. It employs the `WHERE` clause in tandem with the `AND` operator, filtering out successful logins and those occurring before 18:00.

---

## **2. Retrieve Login Attempts on Specific Dates**

Given the suspicious activities detected on 2022-05-09, I needed to investigate login attempts from this date as well as the preceding day.

![](https://i.gyazo.com/952cffe7cc564e8fbf5c6f983715094e.png)

**Description:** This query focuses on the `log_in_attempts` table to discern logins from 2022-05-09 or 2022-05-08, making use of the `WHERE` clause with the `OR` operator.

---

## **3. Retrieve Login Attempts Outside of Mexico**

Post data investigation, there was an emerging concern regarding login attempts originating outside of Mexico.

![](https://i.gyazo.com/2b01354a0fcfba2d2bca46bd26de4ebc.png)

**Description:** This query, rooted in the `log_in_attempts` table, filters out logins from Mexico, employing the `LIKE` operator to match variations representing Mexico.

---

## **4. Retrieve Employees in Marketing**

For an IT upgrade, I needed details of employees affiliated with the Marketing department, specifically from the East building.

![](https://i.gyazo.com/e8537b3571c29916ae45aee796f7bccb.png)

**Description:** The query pulls data from the `employees` table, utilizing the `WHERE` clause and the `AND` operator to specify the Marketing department in the East building.

---

## **5. Retrieve Employees in Finance or Sales**

Employees in the Finance and Sales sectors required a distinctive security upgrade.

![](https://i.gyazo.com/2fafe0862371988edc89d3bdd78ccdc3.png)

**Description:** Here, the query is anchored in the `employees` table and uses the `OR` operator within the `WHERE` clause to pinpoint employees from either the Finance or Sales department.

---

## **6. Retrieve All Employees not in IT**

To effectuate a security upgrade, I needed to identify employees outside the Information Technology department.

![](https://i.gyazo.com/88428f349039cb199d65e02d1357ca31.png)

**Description:** This query taps into the `employees` table, leveraging the `WHERE` clause combined with the `NOT` operator to exclude IT department employees.

---

# **Summary**

Through strategic SQL filtering, I extracted pivotal data concerning login attempts and employee computer systems from `log_in_attempts` and `employees` tables. This involved the integration of `AND`, `OR`, and `NOT` operators, supplemented by `LIKE` and the `%` wildcard for pattern recognition.
