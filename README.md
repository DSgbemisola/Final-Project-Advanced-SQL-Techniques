# Hands-on-Project-Working-with-Facts-and-Dimension-Tables

This project outlines the process of designing a data warehouse for a cloud service provider. 
It focuses on using billing data provided in a CSV file to create a star schema, including the design of fact and dimension tables. 
This schema will support complex queries related to billing, such as average billing per customer, billing by country, industry, 
and category, as well as trends over time.

# Objectives
The objectives of this project were to:

1. Study the schema of the given csv file
2. Design the fact tables
3. Design the dimension tables
4. Create a star schema using the fact and dimension tables

# Software Used in this Lab

PgAdmin 4 (PostgreSQL 15)

# Task 1: Study the schema of the given csv file

The aim of this project is to design a data warehouse for a cloud service provider.

The cloud service provider has given us their billing data in the csv file (cloud-billing-dataset.csv). This file contains the billing data for the past decade.

Here are the field wise details of the billing data.

![image](https://github.com/user-attachments/assets/1cc89937-84c9-4d43-ac45-acb40cf99517)

We need to design a data warehouse that can support the queries listed below:

average billing per customer
billing by country
top 10 customers
top 10 countries
billing by industry
billing by category
billing by year
billing by month
billing by quarter
average billing per industry per month
average billing per industry per quarter
average billing per country per quarter
average billing per country per industry per quarter

Here are five rows picked at random from the csv file.

![image](https://github.com/user-attachments/assets/c18df32b-66e5-4ec2-9a2b-1c8edcfc980e)

# Task 2: Design the fact tables

The fact in this data is the bill which is generated monthly.

The fields customerid and billedamount are the important fields in the fact table.

We also need a way to identify the additional customer information, other than the id, and date information. 

So we need fields that refer to the customer and date information in other tables.

The final fact table for the bill would look like this:

![image](https://github.com/user-attachments/assets/5acc399e-1c40-4431-8442-21a56e090bbb)

# Task 3: Design the dimension tables
There are two dimensions to our fact(monthly bill).

  - Customer information
  - Date information

Let us organize all the fields that give information about the customer into a dimension table.

![image](https://github.com/user-attachments/assets/7c51e5a8-ba9e-4bbe-907f-a8ffc55b5381)

Let us organize or derive all the fields that give information about the date of the bill.

![image](https://github.com/user-attachments/assets/7da89f53-0ecc-436e-99f8-88db556f6831)


