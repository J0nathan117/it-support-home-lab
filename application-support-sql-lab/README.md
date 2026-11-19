# SQL Application Support Lab

> **Home-lab technical project.** All customers, products, records, errors, and support cases are simulated for learning and portfolio purposes.

## Goal

Built and troubleshot a small SQL Server database that represents an application-support environment. This lab practices Tier II-style work: investigating data issues, making approved corrections, verifying results, and documenting access controls.

## Environment

- Microsoft SQL Server Express
- SQL Server Management Studio (SSMS)
- Database: `ApplicationSupportLab`
- Local Windows home-lab environment

## What I built

| Table | Purpose |
| --- | --- |
| `Customers` | Customer and contact records |
| `Products` | Supported retail/POS products and prices |
| `Quotes` | Customer quote status records |
| `Orders` | Customer orders, totals, and linked products |

## Support scenarios completed

1. Created the database, tables, keys, and relationships.
2. Used `SELECT`, `WHERE`, `ORDER BY`, `GROUP BY`, and `JOIN` queries to review application data.
3. Corrected a customer email address and verified the change.
4. Simulated a duplicate customer import, detected it with `GROUP BY` and `HAVING`, removed only the test record, and verified cleanup.
5. Found an order total that did not match its linked product price, corrected the record, and verified that no mismatches remained.
6. Created a `SupportReadOnly` account with read-only access. Verified it could view customer data and that an `UPDATE` attempt was denied.
7. Simulated a failed SQL connection using an incorrect server instance name, identified the instance-not-found error, and reconnected to the correct instance.

## Skills demonstrated

- SQL Server administration fundamentals
- Relational database design and table relationships
- T-SQL: `CREATE`, `SELECT`, `INSERT`, `UPDATE`, `DELETE`, `JOIN`, `WHERE`, `GROUP BY`, and `HAVING`
- Data-quality troubleshooting and validation
- Read-only database permissions
- SQL connection troubleshooting
- Change verification and support documentation

## Screenshot evidence

The `screenshots` folder contains evidence for connection setup, database creation, table creation, query results, customer-record correction, duplicate detection and cleanup, order-total mismatch detection and resolution, read-only permissions, and connection troubleshooting.

## Important note

In a real workplace, database changes require approval, data preservation, and change-control procedures. All changes in this project were completed only in a simulated home-lab database.
