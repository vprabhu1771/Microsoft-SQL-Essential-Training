This error occurs in Microsoft SQL Server because there are active connections using the database.

Use this query to force disconnect all users and drop the database:

```sql
USE master;
GO

ALTER DATABASE ShopDB
SET SINGLE_USER
WITH ROLLBACK IMMEDIATE;
GO

DROP DATABASE ShopDB;
GO
```

### Explanation

* `SET SINGLE_USER` → allows only one connection.
* `WITH ROLLBACK IMMEDIATE` → disconnects all active users/sessions immediately.
* `DROP DATABASE` → removes the database.

If you only want to close your own query window:

1. Open a new query window.
2. Run the above script from the new window.
3. Ensure the current database dropdown is not `ShopDB` (set it to `master`).

You can also check active sessions using:

```sql
EXEC sp_who2;
```

Or specifically for the database:

```sql
SELECT 
    session_id,
    login_name,
    host_name,
    program_name
FROM sys.dm_exec_sessions
WHERE database_id = DB_ID('ShopDB');
```
