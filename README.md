# 📈 Stock Trading API (Clone) - ASP.NET Core Web API

This project is a clone stock trading API built with ASP.NET Core, using Code First Entity Framework Core, and documented with Swagger UI. It allows users to manage stock listings and their related comments.

## 🚀 Features

- ASP.NET Core Web API with Swagger UI  
- Code First approach using Entity Framework Core  
- SQL Server database integration  
- Basic stock and comment management endpoints  
- RESTful structure for easy frontend integration  

## 🧱 Tech Stack

- .NET 6/7/8 (depending on your version)  
- Entity Framework Core  
- SQL Server  
- Swagger / Swashbuckle  
- Visual Studio or .NET CLI  

## 🗃️ Entity Models

### 📄 Stock.cs  
public class Stock  
{  
    public int Id { get; set; }  
    public string Symbol { get; set; }  
    public string CompanyName { get; set; }  
    public decimal Price { get; set; }  
    public List<Comment> Comments { get; set; }  
}  

### 💬 Comment.cs  
public class Comment  
{  
    public int Id { get; set; }  
    public string Content { get; set; }  
    public int StockId { get; set; }  
    public Stock Stock { get; set; }  
}  

## 📦 How to Run

1. Clone the repository:  
   git clone https://github.com/yourusername/StockCloneAPI.git  
   cd StockCloneAPI  

2. Setup your SQL Server connection string in `appsettings.json`:  
   "ConnectionStrings": {  
     "DefaultConnection": "Server=YOUR_SERVER_NAME;Database=StockDb;Trusted_Connection=True;"  
   }  

3. Add the initial migration and update the database:  
   dotnet ef migrations add InitialCreate  
   dotnet ef database update  

4. Run the project:  
   dotnet run  

5. Open in your browser:  
   https://localhost:<port>/swagger  

## 📘 API Testing via Swagger

Use the integrated Swagger UI to:  
- View all available endpoints  
- Test GET, POST, PUT, and DELETE operations  
- Easily explore your API as it evolves  

## 📂 Folder Structure

/Controllers      → API endpoints  
/Models           → Entity classes (Stock, Comment)  
/Data             → DbContext and configuration  
Program.cs        → App entry and service configuration  

## ✅ To-Do

- Add authentication and user management  
- Implement stock price updates  
- Expand comment features (likes, timestamps)  
- Add pagination and filtering  

## 📄 License

This project is for educational/demo purposes. Feel free to modify and use it as a base for your own apps.
