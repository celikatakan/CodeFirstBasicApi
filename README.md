# Patika Code First Database Project

## Overview

This project demonstrates how to create a database using the *Code First* approach in *Entity Framework Core. It includes two independent tables: **Movies* and *Games*. These tables are automatically created based on the models defined in the application.

## Requirements

- *Entity Framework Core* is used to implement the Code First approach.
- The following models are created:
  - *Movie* table with fields:
    - Id (int): Primary key, auto-incremented.
    - Title (string): Title of the movie.
    - Genre (string): Genre of the movie (e.g., Action, Comedy, Drama).
    - ReleaseYear (int): The release year of the movie.
  - *Game* table with fields:
    - Id (int): Primary key, auto-incremented.
    - Name (string): Name of the game.
    - Platform (string): Platform the game is played on (e.g., PC, PlayStation, Xbox).
    - Rating (decimal): The rating of the game (between 0 and 10).

## Database Configuration

- *Context Class Name*: PatikaFirstDbContext
- *Database Name*: PatikaCodeFirstDb1
- The database contains two tables:
  - Movies
  - Games

## How to Run the Project

1. *Install Dependencies*: Ensure you have the required dependencies installed, including Entity Framework Core.
2. *Configure the Context*: Define the database context class PatikaFirstDbContext with DbSet properties for Movies and Games.
3. *Migrations*:
   - Run migrations to create the database schema:
     bash
     dotnet ef migrations add InitialCreate
     dotnet ef database update
     
4. *Run the Application*: After the database schema is created, you can run the application to add, update, or retrieve data from the Movies and Games tables.

## Code Sample

Here’s an example of the model classes and DbContext:

```csharp
public class Movie
{
    public int Id { get; set; }
    public string Title { get; set; }
    public string Genre { get; set; }
    public int ReleaseYear { get; set; }
}

public class Game
{
    public int Id { get; set; }
    public string Name { get; set; }
    public string Platform { get; set; }
    public decimal Rating { get; set; }
}

public class PatikaFirstDbContext : DbContext
{
    public DbSet<Movie> Movies { get; set; }
    public DbSet<Game> Games { get; set; }

    protected override void OnConfiguring(DbContextOptionsBuilder optionsBuilder)
    {
        optionsBuilder.UseSqlServer("Server=(localdb)\\mssqllocaldb;Database=PatikaCodeFirstDb1;Trusted_Connection=True;");
    }
}
