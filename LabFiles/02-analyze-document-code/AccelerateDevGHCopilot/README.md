# Library App

## Description

Library App is a .NET 9 console application for managing library patrons and book loans. It supports patron searches, membership renewals, loan extensions, and loan returns.

Data is loaded from and saved to JSON files. The application uses dependency injection and separates domain entities, services, repository interfaces, JSON repositories, and console presentation.

## Project Structure

- `src/`
  - `Library.ApplicationCore/`
    - `Entities/`
    - `Enums/`
    - `Interfaces/`
    - `Services/`
  - `Library.Infrastructure/`
    - `Data/`
  - `Library.Console/`
    - `Json/`
    - `Program.cs`
    - `ConsoleApp.cs`
- `tests/`
  - `UnitTests/`

## Key Classes and Interfaces

- `ConsoleApp`
  - Console-based user interface and application workflow.
- `PatronService`
  - Handles membership renewal rules.
- `LoanService`
  - Handles loan extension and return rules.
- `IPatronRepository`
  - Defines patron search, retrieval, and update operations.
- `ILoanRepository`
  - Defines loan retrieval and update operations.
- `JsonData`
  - Loads and saves JSON data and populates entity relationships.
- `JsonPatronRepository`
  - JSON implementation of `IPatronRepository`.
- `JsonLoanRepository`
  - JSON implementation of `ILoanRepository`.
- `Author`, `Book`, `BookItem`, `Patron`, and `Loan`
  - Core domain entities.

## Usage

Run the console application:

```powershell
dotnet run --project .\src\Library.Console\Library.Console.csproj

