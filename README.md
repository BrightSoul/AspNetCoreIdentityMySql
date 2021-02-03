# ASP.NET Core Identity template for MySql

This is a demo ASP.NET Core application for .NET 5 using MySql.

It's basically the starting project you can get by running:
```
dotnet new mvc --auth Individual --use-local-db
```
But it's been updated to use MySql.
 * Referenced the `Pomelo.EntityFrameworkCore.MySql` and `Microsoft.EntityFrameworkCore.Design` NuGet packages;
 * Replaced `UseSqlServer` with `UseMySql` in the [Startup](Startup.cs#L31) class;
 * Removed all migrations and re-generated them by running the command:
   ```
   dotnet ef migrations add InitialMigration
   ```

> **Please note** This project is using an **alpha release** of `Pomelo.EntityFrameworkCore.MySql`. Wait for an updated, stable version of this package before moving to production (or downgrade EFCore and the NuGet package to versions 3.x).

# Getting Started
 1. Create a MySql database;
 2. Update the connection string in the `appsettings.json` file;
 3. Run the commands
    ```
    dotnet tool install --global dotnet-ef
    dotnet ef database update
    ```
 4. Start debugging the application by pressing `F5` in Visual Studio Code and register your first user.