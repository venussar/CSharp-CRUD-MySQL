# 🖥️ MySQL Desktop CRUD Application (C# / Windows Forms)

This repository contains a desktop application developed in **C# (Windows Forms)** that implements a full **CRUD (Create, Read, Update, Delete)** system for managing customer records in a **MySQL** database.

---

## ✨ Features

* **Create (Guardar):** Insert new customer records (ID, Nombre, Apellido) into the `clientes` table.
* **Read (Listar):** Display all records from the database in a `DataGridView`.
* **Update (Actualizar):** Modify the name and last name of an existing customer record based on the ID.
* **Delete (Eliminar):** Remove a customer record based on the ID.
* **Connection Test:** Button to verify successful connection to the MySQL database.
* **Reporting:** Functionality to generate a simple Excel report using the `SpreadsheetLight` library.

---

## 🛠️ Technologies Used

| Category | Technology | Purpose |
| :--- | :--- | :--- |
| **Frontend/App** | **C#** | Main language for the application logic. |
| **UI Framework** | **Windows Forms** | Desktop user interface. |
| **Database** | **MySQL** | Backend data storage. |
| **Driver** | **MySql.Data.MySqlClient** | Official MySQL ADO.NET Data Provider for database connectivity. |
| **Reporting** | **SpreadsheetLight** | Library used for creating and manipulating Excel files (.xlsx). |

---

## 🚀 Getting Started

Follow these steps to set up and run the application.

### 1. Prerequisites

You must have the following installed and configured:

* **Visual Studio** (Recommended: 2019 or newer)
* **MySQL Server** (and MySQL Workbench or equivalent for initial DB setup).
* **MySQL Connector/NET** (Required for the `MySql.Data` dependency).

### 2. Database Setup

1.  **Create the Database:** Create a new database named `BASE_DATOS` on your local MySQL server.
2.  **Create the Table:** Execute the following SQL query to create the `clientes` table:
    ```sql
    CREATE TABLE clientes (
        ID INT PRIMARY KEY,
        Nombre VARCHAR(100),
        Apellido VARCHAR(100)
    );
    ```

### 3. Connection Configuration

The application uses a hardcoded connection string. **For development purposes**, ensure your connection string matches your local setup:

```csharp
string CadenaConexion = "Server=localhost;User=root;Password=;Port=3306;Database=BASE_DATOS";
