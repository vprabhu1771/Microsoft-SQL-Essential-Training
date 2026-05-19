#  Connect SQL Server with Command Prompt | SQLcmd

```
https://www.youtube.com/watch?v=Ag-y_mNSef8
```

This error means `sqlcmd` cannot find or connect to your SQL Server instance.

Most common causes:

* SQL Server service is not running
* Wrong server/instance name
* TCP/IP or Named Pipes disabled
* SQL Server Browser service stopped
* Using wrong authentication

---

# 1. Check SQL Server Service

Open:

* `Win + R`
* Type:

```cmd
services.msc
```

Look for services like:

* `SQL Server (MSSQLSERVER)`
* `SQL Server (SQLEXPRESS)`
* `SQL Server (MSSQLLocalDB)`

Make sure status is **Running**.

---

# 2. Find Your SQL Server Instance Name

Open:

* Start Menu
* Search: **SQL Server Configuration Manager**

Go to:

```text
SQL Server Services
```

You may see:

| Service                  | Instance Name    |
| ------------------------ | ---------------- |
| SQL Server (MSSQLSERVER) | Default Instance |
| SQL Server (SQLEXPRESS)  | SQLEXPRESS       |
| SQL Server (SQL2025)     | SQL2025          |

---

# 3. Connect Using Correct sqlcmd Syntax

## Default Instance

```cmd
sqlcmd -S localhost
```

OR

```cmd
sqlcmd -S .
```

---

## Named Instance (Example SQLEXPRESS)

```cmd
sqlcmd -S localhost\SQLEXPRESS
```

OR

```cmd
sqlcmd -S .\SQLEXPRESS
```

---

# 4. For Windows Authentication

Use:

```cmd
sqlcmd -S .\SQLEXPRESS -E
```

`-E` means Windows Authentication.

---

# 5. Test Available SQL Instances

Run:

```cmd
sqlcmd -L
```

This lists SQL Server instances on your PC/network.

Example output:

```text
Servers:
    DESKTOP-ABC\SQLEXPRESS
```

Then connect:

```cmd
sqlcmd -S DESKTOP-ABC\SQLEXPRESS -E
```

---

# 6. Enable TCP/IP and Named Pipes

Open:

## SQL Server Configuration Manager

Go to:

```text
SQL Server Network Configuration
→ Protocols for SQLEXPRESS
```

Enable:

* TCP/IP
* Named Pipes

Restart SQL Server service afterward.

---

# 7. Start SQL Server Browser Service

In SQL Server Configuration Manager:

```text
SQL Server Services
```

Start:

```text
SQL Server Browser
```

---

# 8. LocalDB Connection

If using LocalDB:

List instances:

```cmd
sqllocaldb info
```

Example:

```text
MSSQLLocalDB
```

Connect:

```cmd
sqlcmd -S "(localdb)\MSSQLLocalDB"
```

---

# 9. Verify sqlcmd Installed

Run:

```cmd
sqlcmd -?
```

If not recognized, install:

* [Microsoft SQL Server Command Line Utilities](https://learn.microsoft.com/sql/tools/sqlcmd/sqlcmd-install?utm_source=chatgpt.com)

---

# 10. Successful Connection Example

If connected successfully:

```cmd
sqlcmd -S .\SQLEXPRESS -E
```

You will see:

```text
1>
```

Test query:

```sql
SELECT @@VERSION;
GO
```

Exit:

```sql
QUIT
```

---

# Common Working Commands

## SQL Server Express

```cmd
sqlcmd -S .\SQLEXPRESS -E
```

## LocalDB

```cmd
sqlcmd -S "(localdb)\MSSQLLocalDB"
```

## Full SQL Server

```cmd
sqlcmd -S localhost -E
```

---

# If Still Not Working

Send:

1. Output of:

```cmd
sqlcmd -L
```

2. Output of:

```cmd
sqllocaldb info
```

3. Screenshot of:

```text
SQL Server Configuration Manager → SQL Server Services
```

4. Which SQL Server version you installed:

* Express
* Developer
* LocalDB
* 2022 / 2025 etc.
