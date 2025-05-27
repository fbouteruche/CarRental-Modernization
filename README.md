# CarRental - Car Rental Management System

## Overview

CarRental is a comprehensive Windows Forms-based car rental management system built with .NET Framework 4.7.2. This application provides a complete solution for managing car rental operations, including vehicle inventory, customer management, employee administration, rental transactions, and partner relationships.

## Acknowledgments

This project is based on the latest .NET Framework version of the original Car Rental Application from [Matrix-Developers/Car-Rental-App](https://github.com/Matrix-Developers/Car-Rental-App). We extend our sincere thanks to the original authors for their excellent work and foundation that made this demonstration possible.

## Purpose

**⚠️ This repository is for demonstration purposes only.** It serves as an example of a modernized .NET Framework application architecture and is not intended for production use.

## Architecture

The application follows a layered architecture pattern with clear separation of concerns:

### Project Structure

- **CarRental.WindowsApp** - Windows Forms presentation layer
- **CarRental.Domain** - Business logic and domain models
- **CarRental.Controllers** - Application controllers and business operations
- **CarRental.SqlServer** - Database project with SQL Server schema
- **CarRental.Tests** - Unit tests for the application components

### Technology Stack

- **.NET Framework 4.7.2**
- **Windows Forms** - Desktop UI framework
- **C#** - Primary programming language
- **SQL Server** - Database management system
- **MSTest** - Unit testing framework
- **PDFsharp** - PDF generation library
- **FluentAssertions** - Testing assertions library

## Functional Features

### Core Modules

1. **Customer Management**
   - Customer registration and profile management
   - Customer search and filtering capabilities
   - Customer rental history tracking

2. **Vehicle Management**
   - Vehicle inventory management
   - Vehicle group categorization
   - Vehicle image management
   - Vehicle availability tracking

3. **Employee Management**
   - Employee registration and authentication
   - Role-based access control
   - Employee performance tracking

4. **Rental Operations**
   - Rental booking and reservation system
   - Rental agreement generation
   - Return processing and validation
   - Rental pricing and calculation

5. **Partner Management**
   - Partner company registration
   - Partner relationship management
   - Service provider coordination

6. **Service Management**
   - Vehicle maintenance tracking
   - Service scheduling and management
   - Service provider relationships

7. **Coupon System**
   - Discount coupon management
   - Promotional offer administration
   - Coupon validation and application

8. **Dashboard & Reporting**
   - Business intelligence dashboard
   - Rental analytics and reporting
   - Financial reporting capabilities

### Additional Features

- **User Authentication & Authorization** - Secure login system with role-based access
- **PDF Report Generation** - Automated report generation using PDFsharp
- **Data Validation** - Comprehensive input validation and error handling
- **Search & Filtering** - Advanced search capabilities across all modules

## Technical Architecture

### Domain-Driven Design

The application implements domain-driven design principles with:

- **Domain Models** - Core business entities and value objects
- **Controllers** - Application service layer handling business operations
- **Shared Components** - Common utilities and database access layers

### Database Design

The SQL Server database includes tables for:
- Customers, Employees, Partners
- Vehicles, Vehicle Groups, Vehicle Images
- Rentals, Services, Coupons
- Rental-Service relationships

### User Interface

The Windows Forms application features:
- Modern, intuitive user interface design
- Responsive form layouts
- Data grid controls with grouping capabilities
- Modal dialogs for data entry and editing

## Getting Started

### Prerequisites

- Visual Studio 2017 or later
- .NET Framework 4.7.2 or higher
- SQL Server (Express or full version)

### Building the Solution

1. Clone the repository
2. Open `src/CarRental.sln` in Visual Studio
3. Restore NuGet packages
4. Build the solution (Ctrl + Shift + B)

### Database Setup

1. Deploy the database schema using the `CarRental.SqlServer` project
2. Configure the connection string in the application configuration

### Running the Application

1. Set `CarRental.WindowsApp` as the startup project
2. Press F5 to run the application
3. Use the login form to access the system

## Testing

The solution includes comprehensive unit tests in the `CarRental.Tests` project:

- Controller tests for business logic validation
- Domain model tests for entity behavior
- Integration tests for data access operations

Run tests using Visual Studio Test Explorer or the command line:
```
dotnet test CarRental.Tests.csproj
```

## Dependencies

### NuGet Packages

- **PDFsharp 1.50.5147** - PDF document generation
- **System.Data.SqlClient 4.9.0** - SQL Server connectivity
- **MSTest.TestFramework 2.2.5** - Unit testing framework
- **FluentAssertions 5.10.3** - Test assertions

### External Libraries

- **DataGridViewGrouper** - Enhanced DataGridView with grouping capabilities

## License

This project is licensed under the terms specified in the LICENSE file.

## Contributing

As this is a demonstration project, contributions are not actively sought. However, feel free to fork the repository for educational purposes.

## Disclaimer

This application is provided as-is for demonstration and educational purposes. It is not recommended for production use without proper security auditing, testing, and compliance verification.
