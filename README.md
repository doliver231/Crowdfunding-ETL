# Crowdfunding-ETL

## Objective

Independent Funding is a crowdfunding platform for funding independent projects or ventures.

Independent Funding has been growing, so now it needs to move all their accessible data from one large Excel file onto a PostgreSQL database. This way, the analytics team will be able to perform analysis and create reports for company stakeholders as well as individuals who donate to projects. The following need to be met:

* Extract and transform the data from the large Excel file into four separate CSV files

* Create a PostgreSQL database and tables by using an ERD

* Load the CSV files into the database

* Perform SQL queries to generate reports for stakeholders

## Resources

### Data Source: 

[crowdfunding.xlsx](https://github.com/doliver231/Crowdfunding-ETL/blob/main/crowdfunding.xlsx), 
[backer_info.csv](https://github.com/doliver231/Crowdfunding-ETL/blob/main/backer_info.csv)

### Software:

* PostgreSQL
* pgAdmin 4
* Quick Database Diagrams (Quick DBD)
* Python 3.7.6
* Jupyter Notebook

## Analysis

This project consists of four technical analysis deliverables:

* Deliverable 1: Extract Data
* Deliverable 2: Transform and Clean Data
* Deliverable 3: Create an ERD and Table Schema, and Load Data
* Deliverable 4: SQL Analysis

### Deliverable 1 : Extracting the Data

Using knowledge of Python, Pandas, and the extract and transform phases of ETL, the raw data needs to be extracted and added to a DataFrame for the transform phase. Using regular expressions (regex), the following DataFrame was created:

![Deliverable 1](https://github.com/doliver231/Crowdfunding-ETL/blob/main/Images/Deliverable1_backersDF.png)

### Deliverable 2 : Transforming and Cleaning the Data

Using knowledge of Python, Pandas, and data cleaning strategies, the data needs to be transformed via formatting, splitting, converting data types, and restructuring to create a DataFrame that can be loaded into a postgreSQL database as a CSV file. The following transformed DataFrame was created:

![Deliverable 2](https://github.com/doliver231/Crowdfunding-ETL/blob/main/Images/Deliverable2_backersDF_usingRegex.png)

### Deliverable 3 : Creating an ERD, Table Schema, and Loading the Data

An ERD was created showcasing all five tables and their respective columns. A backers table, with its primary and foreign keys, was also included, based on the summary information about the backers.csv dataset. 

![Deliverable 3 - ERD](https://github.com/doliver231/Crowdfunding-ETL/blob/main/crowdfunding_db_relationships.png)

The updated database schema was exported as a PostgreSQL file and used to create the backers table in the "crowdfunding_db" database. Finally, pgAdmin was used to upload the backers.csv file into the backers table.

![Deliverable 3](https://github.com/doliver231/Crowdfunding-ETL/blob/main/Images/Deliverable3_backers_table.png)


### Deliverable 4 : BONUS SQL Analysis

To retrieve the number of backer_counts in descending order for each “cf_id” for all the "live" campaigns using the "campaign" table:

![Deliverable 4](https://github.com/doliver231/Crowdfunding-ETL/blob/main/Images/Deliverable4_backerscount1.png)

To retrieve the number of backer_counts in descending order for each “cf_id” for all the "live" campaigns using the "backers" table:

![Deliverable 4](https://github.com/doliver231/Crowdfunding-ETL/blob/main/Images/Deliverable4_backerscount2.png)

In order to send an email to each contact of every live campaign to inform them of how much of the goal remains, the following table was created:

![Deliverable 4](https://github.com/doliver231/Crowdfunding-ETL/blob/main/Images/Deliverable4_contactgoals.png)

In order to send an email to each backer to let them know how much of the goal remains for each live campaign that they’ve pledged, the following table was created:

![Deliverable 4](https://github.com/doliver231/Crowdfunding-ETL/blob/main/Images/Deliverable4_backergoals.png)
