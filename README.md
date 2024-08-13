# Symfony ER Diagram Generation

This guide provides instructions on how to generate an Entity-Relationship (ER) diagram for a Symfony project using Doctrine ORM.

## Prerequisites

Before you start, ensure that you have the following installed:

- Symfony (with Doctrine ORM)
- Composer
- A working Symfony project with Doctrine entities

## Step 1: Install Required Packages

First, ensure that Doctrine ORM and Doctrine Migrations are installed in your Symfony project.

```bash
composer require symfony/orm-pack
composer require doctrine/doctrine-migrations-bundle
```

Next, install the `jkniest/doctrine-erd` package, which is used to generate the ER diagram.

```bash
composer require --dev jkniest/doctrine-erd
```

## Step 2: Generate the ER Diagram

Once the required packages are installed, you can generate the ER diagram by running the following command:

```bash
php bin/console doctrine:generate:erd
```

This command will generate an ER diagram, usually saved as a `.png` file in the root directory of your project or in the specified output directory.

## Step 3: Customize the ER Diagram (Optional)

If you prefer to customize the ER diagram or need a more detailed visualization, consider using one of the following tools:

### MySQL Workbench

1. Export your database schema using Doctrine.
2. Import the schema into MySQL Workbench.
3. Use the reverse-engineer feature to generate the ER diagram.

### dbdiagram.io

1. Export your database schema SQL file.
2. Import the file into [dbdiagram.io](https://dbdiagram.io) to generate the ER diagram.

### DBeaver

1. Export your database schema.
2. Use DBeaver to reverse-engineer the schema and generate an ER diagram.

## Conclusion

You can easily generate an ER diagram for your Symfony project using the `jkniest/doctrine-erd` package. For more customization, consider using database design tools like MySQL Workbench, dbdiagram.io, or DBeaver.
