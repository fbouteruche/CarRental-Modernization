# CarRental Project - Copilot Instructions

## Project Overview
- **Type**: Car Rental Management System
- **UI Framework**: Windows Forms (.NET Framework 4.7.2)
- **Architecture**: Layered architecture with Domain-Driven Design

## Project Structure
```
src/
├── CarRental.WindowsApp/        # Windows Forms UI layer
├── CarRental.Domain/            # Business entities and models
├── CarRental.Controllers/       # Business logic controllers
├── CarRental.SqlServer/         # Database project
└── CarRental.Tests/            # Unit tests
```

## Technology Stack
- **.NET Framework 4.7.2**
- **Windows Forms** - Desktop UI
- **SQL Server** - Database
- **MSTest** - Testing framework
- **PDFsharp** - PDF generation
- **FluentAssertions** - Test assertions

## Key Modules
- **Customer Management** - Customer CRUD operations
- **Vehicle Management** - Vehicle inventory and images
- **Employee Management** - Staff and authentication
- **Rental Operations** - Booking, agreements, returns
- **Partner Management** - External partnerships
- **Service Management** - Vehicle maintenance
- **Coupon System** - Discounts and promotions
- **Dashboard** - Reporting and analytics

## Coding Conventions
- **Namespace Pattern**: `CarRental.{ProjectName}.{Module}`
- **Controller Pattern**: `{Entity}Controller` in Controllers project
- **Domain Models**: Located in `CarRental.Domain/{Entity}/`
- **UI Forms**: Located in `CarRental.WindowsApp/Features/{Module}/`
- **Database**: SQL Server with stored procedures

## Important Files
- **Entry Point**: `CarRental.WindowsApp/Program.cs`
- **Main Form**: `CarRental.WindowsApp/MainForm.cs`
- **Solution**: `src/CarRental.sln`
- **Database Connection**: Check `App.config` files for connection strings

## Dependencies
- PDFsharp for report generation
- DataGridViewGrouper for enhanced grids
- System.Data.SqlClient for database connectivity

## Testing
- Unit tests in `CarRental.Tests/`
- Test structure mirrors main project modules
- Use FluentAssertions for readable assertions

## UI Guidelines
- Windows Forms with modal dialogs
- DataGridView for data display
- Form naming: `{Entity}Form`, `{Entity}EditForm`
- Login-based authentication system

## Build Requirements
- **Always ensure changes build successfully** - All code changes must compile without errors
- **Zero warnings tolerance** - Address all compiler warnings before completing changes
- **Validate after edits** - Test build after making modifications to verify compilation
- **Maintain project references** - Ensure all project dependencies remain intact