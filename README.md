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

# Task 4: Create a star schema using the fact and dimension tables

Based on the previous two tasks, we have now arrived at 3 tables, we can name them as in the table below.

![image](https://github.com/user-attachments/assets/4385d5fb-edc9-4671-af27-5cb3a3365fe3)

When we arrange the above tables in Star Schema style, we get a table strucutre that looks likes the one in the image below.

![image](https://github.com/user-attachments/assets/6cea0e1a-8cf9-4333-a439-3a080e67132b)

The image shows the fact and dimension tables along with the relaionships between them.

# Task 5: Create the schema on the data warehouse

- Step 1: Start the postgresql server.
- Step 2: Create the database on the data warehouse.
- Step 3: Download the schema .sql file.

The commands to create the schema are available in the file below.

[https://cf-courses-data.s3.us.cloud-object-storage.appdomain.cloud/IBM-DB0260EN-SkillsNetwork/labs/Working%20with%20Facts%20and%20Dimension%20Tables/star-schema.sql](https://drive.google.com/file/d/1pzGEQ5DV2EBiEeteqDSHK7G0nHMKUYBP/view?usp=sharing)

- Step 4: Create the schema

Run the command in the script above to create the schema in the under billingDW database.

# Task 6: Practice exercises

In this practice exercise, you will analyze the below csv file, which contains data about the daily sales at different stores of an international fashion retailer.

![image](https://github.com/user-attachments/assets/9109a095-c899-4f89-951f-e48777629b84)

# Exercise 1: Design the schema for the fact table FactSales.

![image](https://github.com/user-attachments/assets/9e9d7210-2b7b-4d3a-91ea-c047e40fdecf)

# Exercise 2: Design the schema for the dimension table DimStore.

![image](https://github.com/user-attachments/assets/55870cdc-948a-4881-ac64-1e9e0d003b1d)

# Exercise 3: Design the schema for the dimension table DimDate.

![image](https://github.com/user-attachments/assets/cf129845-c03c-4868-ad37-ead7e152cc2f)






