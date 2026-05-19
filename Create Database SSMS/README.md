To create a database in Microsoft SQL Server using SQL Server Management Studio:

## Step 1: Open SSMS

1. Launch SSMS.
2. Connect to your SQL Server instance.

   * Server name: `localhost` or `.\SQLEXPRESS`
   * Authentication: Windows Authentication (usually)

![Image](https://images.openai.com/static-rsc-4/G622UOVTfqKkHrBvgf1BuEAepBXf-5fARKsMfuLaa3wHkMmbcuDt7GMlCbMk-99PK04FKH5aFGFs8KJxTPqtqpeYnVyEIL51aDEGQCUA1qE1b5B0edhBEexIJqFo9f6c2kwovVmskIXkwFaAFdQ1tHHy5E0vALBI_UGbZ500bzu4uYhzfja6stcAhPYjp5n1?purpose=fullsize)

![Image](https://images.openai.com/static-rsc-4/FnDSia1JcNhYACvnfEgNxhBRfOYizYKg-wmHdZSVre9SawEhyGoLHdpBjod0LuTxkXwljoqRa54rit-ksys8dL94aEJ5U-le_Xa1_2gHxH25paOe0sPMg0ikxRpPplzysEzw2g1CFXtvoaitcTvnby08CVt1ieGPkU5LhfGalg9zoLzNY6tnzpg-DyvHsJ4f?purpose=fullsize)

![Image](https://images.openai.com/static-rsc-4/vmwnpjS_tzDnTCiiemZeT9rKvSL6tfIx_XiTdoR4KBwucZm6lYw7iTnGwhj1mTDMcE7fDRX0dOJ2N1KKuxC_3TZpJvAVAttJvDTr83jpMIQWgK-n-y-CYHVYkHwsayZ-xUvFpHoqAy80eg7DYmemLASx67Gom7duQE82BTWrjbRwXxpTB4rbJQv4MX7yarSY?purpose=fullsize)

![Image](https://images.openai.com/static-rsc-4/VqrcGrS94xv-qoYTX7SKL2FRaV8AOVhgkla7xoHNL8ULekPbMbvXy4yobufunKqLO3tjpDb0lw9nrwRhEFl6zkUymIEjeX1b5bZ8ZJxaYp_f4YQ4yzlXJoSDP27WY1PRWnrNVwIGtCeLgm8yzqJobBnmsIUoRb-Bleh16u89IStvel4Z5IZF7AYkM6zhh4vc?purpose=fullsize)

---

## Step 2: Create Database using GUI

1. In **Object Explorer**
2. Right-click **Databases**
3. Click **New Database...**
4. Enter database name
   Example: `CollegeDB`
5. Click **OK**

![Image](https://images.openai.com/static-rsc-4/5ZALss9KR0okYVeGYJ3fKYUKl6qcXo8YEFp31TbY5er984k_EYnuR6FXxezv_2RtNblBqZQ1DzosmG4BoASgJpfH1Y7DM9bKkMa8V5lnIllhQuVgIaXqtGdEWJlIcVdstE5cCwPO_xX9Jjc-8STmD5rxQ2AQpMQFKFHA4lDuZ8dfq35803FESqCExPh1LPfN?purpose=fullsize)

![Image](https://images.openai.com/static-rsc-4/6uHNzq7nAyx45HsPfEp3ug6t5-VDd4PlVSdylDLHjcj5aTxjsssN2gHzzHjCp-eM_s68TujVXBfQnIt4L9zJOLQo_rQYPeMXDaaDzCK3k3qOyYDQLVF8OoP_qg0EHxja9qnQpQSHz0XM4A0dwRFTvfO4Y7zq4j54GkrsaOYxSNJ3KgeDBC8KqRQGZQD-7dgi?purpose=fullsize)

![Image](https://images.openai.com/static-rsc-4/cOeOsW5anbDlGqBDAqfdIr31NF8Cu5zRqpBLQ-8wFfy8MHFxUlU8Y7dmP5Oy_3oDOxRXIPhT_DD-LNtxj5Gy5QWO2LcwjDgDIGX5PDeukrpqXN7k2cB0ZCE8CRaYrR090VQAzOQb7lvd4r5Sv8jdqglZsz4ye9J0NZC9oZeAcUG-IipfiXSKujWKctgPPDAP?purpose=fullsize)

![Image](https://images.openai.com/static-rsc-4/jp2530j6BNVQSCyGW64YsuYELwI0k0mfq85zq8qBmHUB7GJ2mxOJxrmvDL_S2T0B4WOSRGYHk_t2hWt7gATKieZe4PKA5xbcb6Pw8TBT5-tRRAqxeqNs6_9aQSwDfkPKb5Q7eGZoe-9vygSKklt6whnn2-E5j2sVxMRukl4ZsOv9WpRqRCL9YCJMcZy60Y8A?purpose=fullsize)

![Image](https://images.openai.com/static-rsc-4/sPYufdXBe5eDjwzm3Ibfs0h-AqHMot1_KTYaXHEWd-dt6iKAKm4PQTk-U6KOmp2mMN-jHtJdvGYR9oCvBtxbvDU7xz5vhwFsg5mFsHhljT3cIUNpX626Xv1QlpehepcILWPY0S8K5NbzSKiAyQu_6B2wdolJPe_iOxPyIei-TyrWegiyLUHVrSgCXSokDLUp?purpose=fullsize)

![Image](https://images.openai.com/static-rsc-4/wqpQ0Me1kfS9VnBLUqpMF-faisPc5gfpleaOSDh-SIyndetdTpTeD3VsimPxrYdpTpctXfmYAEyS8GfWP8XpUO1YkE6u_QPfR-L8UtkyBjoxS4isCRY02E0LVmmkYKXklzujTOKKe0UcK4QKUJHP2JRmm3gBcAVVQhN-XqD0A7rul_kY9kroBXlVfDzmqO2Y?purpose=fullsize)

---

## Step 3: Create Database using SQL Query

Open **New Query** and run:

```sql
CREATE DATABASE CollegeDB;
GO
```

To use the database:

```sql
USE CollegeDB;
GO
```

---

## Step 4: Verify Database

Refresh the **Databases** folder in Object Explorer.

You should see:

```text
Databases
 └── CollegeDB
```

![Image](https://images.openai.com/static-rsc-4/qtf0HAqvgOf11JwixzdjOP7NfEABaIW7BFvznt_1xw3Ku8crymURbEAwFyZcdL9WUnXHnJt_epeoutvdFYqdqZJTPZ7TrcSz7Yf7fNLJIib8e5JP5y2KMnfUnmyFNuPkEYEda2Iyr3skoXq582aqpGRdNLy5nwUiWECc9SUJiLIqQ4yhVc3Tb2kb1_u7KV2O?purpose=fullsize)

![Image](https://images.openai.com/static-rsc-4/BWupU2Iv4rS3F8iF5n0w5Go5dXiEDALs7nXsgY68_V453BNsYu0DW-TxGJSNGZ5nrWb6y3FCKwngUeeg_EsrIPHLwX8ePMg1Y_tH_5Qb2n0vbtxa_mzThydleRUA7hqCGhGBLSLQ1US6ZM3m5VsV2HLwTXML03XW4aXjz6TkDeSFQT3wD3PML2PZkKoGuR26?purpose=fullsize)

![Image](https://images.openai.com/static-rsc-4/mD6cUT3UupmAQnforbeteWCzsUKOo_ojz0AdMBhFZwfs-f750qTzpkFCspaKKUc7smmhc_5HkM-IJ0zAoTxd4JWHzLGY9SIv9_4C9oTlG0XFkNSyPjbNlOYjwkHBL8_n0p-dskdaqwm2zqILzdVMv8ZQJt-cAiIsM8bd7Zejdzu2_BhlzblM9dPYpQ3VYOMQ?purpose=fullsize)

![Image](https://images.openai.com/static-rsc-4/FnDSia1JcNhYACvnfEgNxhBRfOYizYKg-wmHdZSVre9SawEhyGoLHdpBjod0LuTxkXwljoqRa54rit-ksys8dL94aEJ5U-le_Xa1_2gHxH25paOe0sPMg0ikxRpPplzysEzw2g1CFXtvoaitcTvnby08CVt1ieGPkU5LhfGalg9zoLzNY6tnzpg-DyvHsJ4f?purpose=fullsize)

![Image](https://images.openai.com/static-rsc-4/34uRaVsuleGBKIm4mGrtGmhDo8ruC9prHTzz--o-_zinPY34Txxhq5kaQH1wymxYYqG8XcBoAZZMPFZ13Dv0Sgum8iNqRMPvrXba2YnAWyD7ppobQt3UEDYVgo50J3DhLHrZApn9Sq3JTK5Vy9EOoE33f0xIVek_AQ7Dj9yNfLB5Ng9bJqjBz8YfUKJgylzs?purpose=fullsize)

![Image](https://images.openai.com/static-rsc-4/nFdmKw-Zdumwi_W_5uAaCDxbZTLP7P3pzMfseviKQtywX7ieoKFtLmvUVopYXnWqP5XMQgrSNYED5p7Qd-A67Ri-U0yCVavFpvwvEnaUixPh28cxB0tWaDxqvvxmAckvhLT4s8Q8rWbvdpebvtcsgPlLjhwMbcohqkE8_pMKHTU4WrT7K9bCf3-2oqA7uhXE?purpose=fullsize)

---

## Example: Create Table inside Database

```sql
USE CollegeDB;
GO

CREATE TABLE Student (
    Id INT PRIMARY KEY IDENTITY(1,1),
    Name VARCHAR(100),
    Department VARCHAR(100)
);
GO
```

Insert sample data:

```sql
INSERT INTO Student (Name, Department)
VALUES
('Arun', 'Computer Science'),
('Priya', 'Mathematics');
```

View data:

```sql
SELECT * FROM Student;
```

---

## Common SQL Server Database Commands

```sql
-- Show all databases
SELECT name FROM sys.databases;

-- Delete database
DROP DATABASE CollegeDB;

-- Rename database
ALTER DATABASE CollegeDB
MODIFY NAME = NewCollegeDB;
```

---

Official websites:

* [Microsoft SQL Server](https://www.microsoft.com/en-us/sql-server?utm_source=chatgpt.com)
* [SQL Server Management Studio (SSMS) Download](https://learn.microsoft.com/en-us/sql/ssms/download-sql-server-management-studio-ssms?utm_source=chatgpt.com)
