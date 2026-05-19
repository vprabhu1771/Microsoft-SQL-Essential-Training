Here’s a complete **Microsoft SQL Server Category Table CRUD** example using pure SQL.

## 1. Create Database

```sql
CREATE DATABASE ShopDB;
GO

USE ShopDB;
GO
```

---

## 2. Create Category Table

```sql
CREATE TABLE Category (
    Id INT PRIMARY KEY IDENTITY(1,1),
    CategoryName NVARCHAR(100) NOT NULL,
    Description NVARCHAR(255),
    CreatedDate DATETIME DEFAULT GETDATE()
);
```

---

# CRUD Operations

---

# 3. INSERT (Create)

## Insert Single Record

```sql
INSERT INTO Category (CategoryName, Description)
VALUES ('Electronics', 'Electronic Products');
```

## Insert Multiple Records

```sql
INSERT INTO Category (CategoryName, Description)
VALUES
('Books', 'All Book Categories'),
('Clothing', 'Mens and Womens Wear'),
('Groceries', 'Daily Essentials');
```

---

# 4. SELECT (Read)

## Get All Categories

```sql
SELECT * FROM Category;
```

## Get Category By Id

```sql
SELECT * 
FROM Category
WHERE Id = 1;
```

## Search Category

```sql
SELECT *
FROM Category
WHERE CategoryName LIKE '%Book%';
```

---

# 5. UPDATE

## Update Category By Id

```sql
UPDATE Category
SET 
    CategoryName = 'Mobile Electronics',
    Description = 'Mobiles and Accessories'
WHERE Id = 1;
```

---

# 6. DELETE

## Delete Category By Id

```sql
DELETE FROM Category
WHERE Id = 1;
```

---

# 7. DROP TABLE

```sql
DROP TABLE Category;
```

---

# 8. Full Example Data Output

| Id | CategoryName | Description          | CreatedDate |
| -- | ------------ | -------------------- | ----------- |
| 1  | Electronics  | Electronic Products  | 2026-05-19  |
| 2  | Books        | All Book Categories  | 2026-05-19  |
| 3  | Clothing     | Mens and Womens Wear | 2026-05-19  |

---

# 9. Stored Procedure CRUD

## Insert Procedure

```sql
CREATE PROCEDURE sp_InsertCategory
(
    @CategoryName NVARCHAR(100),
    @Description NVARCHAR(255)
)
AS
BEGIN
    INSERT INTO Category(CategoryName, Description)
    VALUES(@CategoryName, @Description);
END
```

### Execute

```sql
EXEC sp_InsertCategory 
    @CategoryName = 'Furniture',
    @Description = 'Home Furniture';
```

---

## Select Procedure

```sql
CREATE PROCEDURE sp_GetCategories
AS
BEGIN
    SELECT * FROM Category;
END
```

### Execute

```sql
EXEC sp_GetCategories;
```

---

## Update Procedure

```sql
CREATE PROCEDURE sp_UpdateCategory
(
    @Id INT,
    @CategoryName NVARCHAR(100),
    @Description NVARCHAR(255)
)
AS
BEGIN
    UPDATE Category
    SET
        CategoryName = @CategoryName,
        Description = @Description
    WHERE Id = @Id;
END
```

---

## Delete Procedure

```sql
CREATE PROCEDURE sp_DeleteCategory
(
    @Id INT
)
AS
BEGIN
    DELETE FROM Category
    WHERE Id = @Id;
END
```

---

# 10. Useful Queries

## Count Categories

```sql
SELECT COUNT(*) AS TotalCategories
FROM Category;
```

## Sort Categories

```sql
SELECT *
FROM Category
ORDER BY CategoryName ASC;
```

## Pagination

```sql
SELECT *
FROM Category
ORDER BY Id
OFFSET 0 ROWS
FETCH NEXT 5 ROWS ONLY;
```
