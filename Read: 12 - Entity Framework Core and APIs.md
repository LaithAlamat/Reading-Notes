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

## User Secrets

User secrets is a secure way of storing private user information such as API keys, client secrets, and connection strings. Essentially anything that you don’t want others to know about when using your code base.

We can do this by using the JSON file that we have that act like the .ENV file is javascript.

These secrerts can be accessed by the configuration method that allows us to access them.

## Data Seeding
Data seeding is the process of populating a database with an initial set of data.

There are several ways this can be accomplished in EF Core:

- Model seed data
- Manual migration customization
- Custom initialization logic

### Model Seeding
Seeding data can be associated with an entity type as part of the model configuration. Then EF Core migrations can automatically compute what insert, update or delete operations need to be applied when upgrading the database to a new version of the model.

### Manual migration customization
When a migration is added the changes to the data specified with HasData are transformed to calls to InsertData(), UpdateData(), and DeleteData(). One way of working around some of the limitations of HasData is to manually add these calls or custom operations to the migration instead.

## What is MVC Entity Framework?
It is a data access framework which used to create and test data in the visual studio. It is part of . NET Framework and Visual Studio. The latest package is shipped as Entity Framework NuGet Package.