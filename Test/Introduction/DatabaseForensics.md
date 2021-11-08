# Database Forensics

## Introduction
It is the examination of database related content and its associated metadata.

## Objectives
1. Retrace operations performed by the attacker 
2. Recover deleted data
3. Identify activities related to fraudulent activities
4. Identify attributes that signify an attack

## Database Forensic Analysis

### MSSQL Database Server
#### SQL Server Architecture
1. Data Storage Files
  - Primary Data File (MDF): Contains database schema information
  - Secondary Data File (NDF): Store user information.
  - Log File (LDF): Stores changes made on the database.

  Each data storage file except for LDF contains multiple data pages:
    1. Page Header: Page metadata: page id, page type
    2. Data Rows: Store data
    3. Offset Table: Point to location of data
