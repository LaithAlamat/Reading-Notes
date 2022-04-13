# Entity Framework Core

Entity Framework (EF) Core is a lightweight, extensible, open source and cross-platform version of the popular Entity Framework data access technology.

EF Core can serve as an object-relational mapper (O/RM), which:

- Enables .NET developers to work with a database using .NET objects.
- Eliminates the need for most of the data-access code that typically needs to be written.
- EF Core supports many database engines, see Database Providers for details.

## The Model
With EF Core, data access is performed using a model. A model is made up of entity classes and a context object that represents a session with the database. The context object allows querying and saving data.

## Querying
Instances of your entity classes are retrieved from the database using Language Integrated Query (LINQ). 

## Saving data
Data is created, deleted, and modified in the database using instances of your entity classes.

## Data Seeding

Data seeding is the process of populating a database with an initial set of data.

There are several ways this can be accomplished in EF Core:

- Model seed data
- Manual migration customization
- Custom initialization logic