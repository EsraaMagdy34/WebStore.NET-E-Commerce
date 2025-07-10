# WebStore.NET E-Commerce

A full-featured e-commerce web application built with ASP.NET Core MVC, featuring a modern shopping experience with comprehensive admin management capabilities.

## Features

### Customer Features
- **Home Page** with featured products and categories
- **Product Catalog** with category-based browsing
- **Product Details** with comprehensive product information
- **Shopping Cart** with add/remove/update functionality
- **Order Management** (checkout, history, cancellation)
- **User Profile** management with shipping information
- **Authentication** (login/register) with ASP.NET Identity
- **Responsive Design** with Bootstrap 5.3

### Admin Features
- **Admin Dashboard** with key metrics and analytics
- **Product Management** (create, edit, delete products)
- **Category Management** (organize product categories)
- **Order Management** (view, update order status)
- **User Management** through ASP.NET Identity
- **Revenue Tracking** and inventory alerts

### Technical Features
- **Role-based Authorization** (Customer/Admin)
- **Entity Framework Core** with SQL Server
- **Security** with data validation and CSRF protection
- **Session Management** for guest cart functionality
- **Cart Merging** when guests login
- **Modern UI** with custom CSS and Bootstrap
- **Performance** optimized with async/await patterns

## Technology Stack

- **Framework**: ASP.NET Core 8.0 MVC
- **Database**: SQL Server with Entity Framework Core
- **Authentication**: ASP.NET Core Identity
- **Frontend**: Bootstrap 5.3, jQuery, Custom CSS
- **Validation**: jQuery Validation & Unobtrusive Validation
- **Session**: ASP.NET Core Session for guest cart
- **Logging**: Built-in ASP.NET Core logging

## Project Structure

```
Ecommerce/
├── Controllers/           # MVC Controllers
│   ├── HomeController.cs
│   ├── ProductController.cs
│   ├── CartController.cs
│   ├── OrderController.cs
│   └── ProfileController.cs
├── Models/               # Data Models
│   ├── User.cs
│   ├── Product.cs
│   ├── Category.cs
│   ├── Cart.cs
│   ├── Order.cs
│   └── Review.cs
├── ViewModels/           # View Models
│   ├── ProductViewModel.cs
│   ├── CartViewModel.cs
│   ├── OrderViewModel.cs
│   ├── ProfileViewModel.cs
│   └── HomeViewModel.cs
├── Views/                # Razor Views
│   ├── Home/
│   ├── Product/
│   ├── Cart/
│   ├── Order/
│   ├── Profile/
│   └── Shared/
├── Areas/                # Admin Area
│   └── Admin/
│       └── Pages/        # Razor Pages for Admin
│           ├── Dashboard.cshtml
│           ├── Products/
│           └── Orders/
├── Data/                 # Data Context
│   └── ApplicationDbContext.cs
└── Program.cs            # Application entry point
```

## Getting Started

### Prerequisites
- .NET 8.0 SDK
- SQL Server (LocalDB or Full)
- Visual Studio 2022 or VS Code

### Installation

1. **Clone the repository**
   ```bash
   git clone https://github.com/EsraaMagdy34/WebStore.NET-E-Commerce.git
   cd WebStore.NET-E-Commerce
   ```

2. **Update connection string**
   
   Edit the connection string in `appsettings.json` (if available) or the default connection string in `Program.cs`:
   ```json
   {
     "ConnectionStrings": {
       "DefaultConnection": "Server=(localdb)\\mssqllocaldb;Database=EcommerceDb;Trusted_Connection=true;MultipleActiveResultSets=true"
     }
   }
   ```

3. **Run the application**
   ```bash
   cd Ecommerce
   dotnet restore
   dotnet run
   ```

4. **Database Setup**
   
   The application automatically applies migrations and seeds initial data on startup, including:
   - Admin and regular user accounts
   - Product categories (Electronics, Clothing, Books)
   - Sample products with images
   - Demo cart and order data

### Default Accounts

**Admin Account:**
- Email: `admin@example.com`
- Password: `Admin123!`

**Regular User:**
- Email: `john@example.com`
- Password: `Password123!`

## Database Schema

### Core Entities
- **User**: Extended Identity user with shipping information
- **Product**: Product catalog with pricing, inventory, and images
- **Category**: Product categorization
- **Cart/CartItem**: Shopping cart functionality
- **Order/OrderItem**: Order processing and history
- **Review**: Product reviews (structure ready)

### Key Relationships
- Products belong to Categories
- Users have multiple Orders
- Orders contain multiple OrderItems
- Users have Carts with CartItems
- Products can have multiple Reviews

## User Interface

The application features a modern, responsive design with:
- Clean Bootstrap 5 styling
- Custom CSS for enhanced visual appeal
- Product cards with hover effects
- Responsive navigation with role-based menus
- Professional admin dashboard
- Mobile-friendly layout

## Security Features

- **Authentication**: ASP.NET Core Identity integration
- **Authorization**: Role-based access control
- **CSRF Protection**: Anti-forgery tokens on forms
- **Data Validation**: Model validation and client-side validation
- **Secure Sessions**: HttpOnly and secure cookies
- **Password Policies**: Strong password requirements

## Key Features Deep Dive

### Shopping Cart
- Persistent cart for logged-in users
- Session-based cart for guests
- Automatic cart merging on login
- Real-time quantity updates
- Stock validation

### Order Processing
- Comprehensive checkout process
- Multiple payment method support
- Order status tracking
- Order history and management
- Admin order management

### Admin Dashboard
- Revenue and order analytics
- Low stock alerts
- Recent orders overview
- Product and category management
- Order status updates

## Contributing

1. Fork the repository
2. Create your feature branch (`git checkout -b feature/AmazingFeature`)
3. Commit your changes (`git commit -m 'Add some AmazingFeature'`)
4. Push to the branch (`git push origin feature/AmazingFeature`)
5. Open a Pull Request

##  Acknowledgments

- ASP.NET Core team for the excellent framework
- Bootstrap team for the responsive UI framework
- jQuery team for client-side functionality
- Entity Framework team for the ORM

## Support

If you encounter any issues or have questions, please create an issue in the GitHub repository.
