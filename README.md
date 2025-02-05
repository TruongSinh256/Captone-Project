# Base Project

This is the base project. Follow the instructions below to set up the project.

## Setup

1. Navigate to the project directory:

```bash
dotnet ef migrations add InitialCreate --output-dir Migrations
dotnet build
dotnet ef database update
dotnet run -- seed
dotnet run
```

# Database Migration Checklist

- [ ] If you want to check the list of migrations in the project, use `dotnet ef migrations list`
- [ ] Create a new migration file with `dotnet ef migrations add <MigrationName>`
- [ ] If you need to change a column, create a new migration with `dotnet ef migrations add <MigrationName>` and manually update the `Up` method in the migration file to reflect the column change
- [ ] Review the generated migration file and the changes to the database schema
- [ ] Apply the migration to the database with `dotnet ef database update`
- [ ] If you need to rollback to a previous migration, use `dotnet ef database update <PreviousMigrationName>` or `dotnet ef database update 0` to rollback all migrations
- [ ] Test the application to ensure the new database schema works correctly
- [ ] Commit the migration file to version control

# For gitignore

- [ ] git rm -rf --cached .
- [ ] git add .

# For MailCatcher
- [ ] [text](https://rubyinstaller.org/downloads/)
- [ ] run ruby -v
- [ ] run gem install mailcatcher
- [ ] run mailcatcher