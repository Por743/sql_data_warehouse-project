/*
========================================================
Create Database and Schemas
========================================================
Script Purpose:
  This script creates a new database named 'DataWarehouse' after checking if it already exists.
  If the database exists, it is dropped and recreated. Additionally, the script sets up two schemas
  within the database: 'bronze' and 'silver'.

WARNING:
  Running this script will drop the entrie 'DataWarehouse' database if it exists.
  All data in the database will be permanently deleted. Proceed with caution
  abd ensure you have proper backups before running this script.
*/



USE master;
Go

IF EXISTS (select 1 from sys.databases where name = 'DataWarehouse')
BEGIN
  ALTER DATABASE DataWarehouse SET SINGLE_USER WITH ROLLBACK IMMEDIATE;
  DROP DATABASE DataWarehouse;
END;
GO

CREATE DATABASE DataWarehouse;
GO

USE DataWarehouse;
GO

CREATE SCHEMA bronze;
GO

CREATE SCHEMA silver;
