# Customer Case Management System

This is a web-based case management system built using **ASP.NET Core Web API**. It allows companies to manage customer support cases submitted via various communication channels like Email, WhatsApp, Live Chat, and Phone. The API supports full CRUD (Create, Read, Update, Delete) functionality for managing customer queries.

## 🛠️ Technologies Used

- ASP.NET Core Web API
- Entity Framework Core
- SQL Server
- Swagger (OpenAPI) for API testing
- Visual Studio / Visual Studio Code

---

## 🚀 Features

- Create new customer support cases
- Retrieve all or specific cases
- Update case details and status
- Delete resolved or invalid cases
- Handles input from multiple channels

---

## 📁 Project Structure

- `Models/CustomerCase.cs` - Data model
- `Data/ApiContext.cs` - Database context
- `Controllers/CustomerCasesController.cs` - API endpoints
- `appsettings.json` - Configuration file for database connection
- `Migrations/` - EF Core migration files

---

## ⚙️ Getting Started

### Prerequisites

- [.NET 6 SDK or later](https://dotnet.microsoft.com/download)
- SQL Server or SQL Server Express
- Visual Studio / VS Code

### Step-by-Step Setup

1. **Clone the Repository**
   ```bash
   git clone https://github.com/yourusername/CustomerCaseManagement.git
   cd CustomerCaseManagement

2. **Configure the Database Edit appsettings.json:**
   ```json
   "ConnectionStrings": {
   "DefaultConnection": "Server=MSI\\A2006;Database=CaseManagementDB;Trusted_Connection=True;TrustServerCertificate=True;"
   }

3. **Apply Migrations and Create the Database In the Package Manager Console (PMC):**
   ```powershell
   Update-Database

4. **Run the Application**
   ```bash
    dotnet run


5. **Access Swagger Open your browser and go to:**
    ```bash
    https://localhost:5001/swagger

  ---
  ## 🔄 API Endpoints
    Method | Endpoint | Description
    GET | /api/CustomerCases | Get all customer cases
    GET | /api/CustomerCases/{id} | Get a case by ID
    POST | /api/CustomerCases | Create a new customer case
    PUT | /api/CustomerCases/{id} | Update an existing case
    DELETE | /api/CustomerCases/{id} | Delete a case


  ---
  ## 🧪 Example JSON Payload

      "customerName": "Jane Doe",
      "contact": "jane.doe@email.com",
      "query": "How do I reset my password?",
      "channel": "Email",
      "status": "Pending"
  

---
  ##❗ Troubleshooting
  - If database tables are missing:
    - Ensure your SQL Server is running
    - Confirm your connection string is correct
    - Run Update-Database again

  - If ID errors occur when inserting:
    - Do not manually set the Id field for auto-generated IDs

---
 ##📜 License
 
  This project is licensed under the MIT License. Feel free to use and modify it.
