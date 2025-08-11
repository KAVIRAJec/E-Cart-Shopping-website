# 🛒 ChienVHShop Migration Project

![Sample Image](https://raw.githubusercontent.com/KAVIRAJec/E-Cart-Shopping-website/refs/heads/main/Images/Screenshot%202025-08-11%20at%209.34.31%E2%80%AFAM.png)

## Overview
This project is a migration of an ASP.NET MVC e-commerce application to a modern .NET Core Web API architecture. It features a clean separation of concerns, PostgreSQL database, Swagger API documentation, and robust business logic.

---

## 🖥️ Frontend (FR)

- **Technology:** Angular
- **Role:** Consumes RESTful APIs from the backend
- **Features:**
  - Product listing, filtering, and search
  - Shopping cart management
  - Checkout and payment (PayPal integration)
  - Order history and tracking
  - User authentication and profile
  - News and content display
  - Contact form
- **How it works:**
  - Makes HTTP requests to `/api/*` endpoints
  - Handles authentication via JWT tokens
  - Displays data using modern UI components

---

## ⚙️ Backend (BE)

- **Technology:** ASP.NET Core Web API
- **Architecture:**
  - **Models:** Entity classes representing DB tables
  - **DTOs:** Data Transfer Objects for API communication
  - **Repositories:** Data access logic (EF Core, PostgreSQL)
  - **Services:** Business logic, validation, and orchestration
  - **Controllers:** API endpoints for all features
  - **Mappers:** Custom mapping between Models and DTOs
- **Key Features:**
  - Soft delete (IsActive field)
  - Pagination and filtering
  - Secure authentication (JWT)
  - PayPal payment integration
  - Export/report endpoints (PDF, Excel, CSV)
  - Swagger for API testing

---

## 🗂️ Project Structure

```
DotnetCoreMigration/
├── Controllers/
├── DTOs/
├── Interfaces/
├── Mappers/
├── Models/
├── Repositories/
├── Services/
├── Data/
├── Properties/
├── Program.cs
├── appsettings.json
└── README.md
```

---

## 🚀 How to Run

1. **Clone the repository**
2. **Configure PostgreSQL connection** in `appsettings.json`
3. **Run database migrations**
4. **Start the API**
5. **Open Swagger UI** at `/swagger` for API testing

---

## 📚 API Endpoints (Sample)

- `GET /api/products` - List products
- `GET /api/categories` - List categories
- `POST /api/cart/add` - Add to cart
- `POST /api/cart/checkout` - Checkout
- `POST /api/payments/paypal/create` - PayPal payment
- `GET /api/orders` - List orders
- `GET /api/news` - List news
- `POST /api/contact` - Contact form

---

## 🏗️ Migration Highlights

- All legacy MVC logic refactored into services and repositories
- Models updated for soft delete and relationships
- DTOs for clean API responses
- PostgreSQL replaces SQL Server
- Swagger for easy API exploration

---

## 📦 Packages Used
- Entity Framework Core
- Npgsql (PostgreSQL)
- Swashbuckle (Swagger)
- PayPal SDK
- AutoMapper

---

## 💡 Contributing
Pull requests and suggestions are welcome! Please open issues for bugs or feature requests.

---

## 📄 License
MIT
