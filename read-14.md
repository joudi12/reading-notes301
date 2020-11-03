# summery
## Introduction to Database Normalization
![img](https://www.calebcurry.com/wp-content/uploads/2018/08/db-design-blogs-12.jpg)
#### Database normalization is a process used to organize a database into tables and columns.  The main idea with this is that a table should be about a specific topic and only supporting topics included. 
#### By limiting a table to one purpose you reduce the number of duplicate data contained within your database. This eliminates some issues stemming from database modifications.
#### Reasons for Database Normalization:
1.  to minimize duplicate data,
2. to minimize or avoid data modification issues
3. to simplify queries. 

### I think once you understand the issues, you better appreciate normalization. Consider the following table:
![img2](https://www.essentialsql.com/wp-content/uploads/2014/06/Intro-Table-Not-Normalized.png)
##### The first thing to notice is this table serves many purposes including that As a DBA this raises a red flag.  In general I like to see tables that have one purpose.  Having the table serve many purposes introduces many of the challenges
##### also you have to Notice that for each SalesPerson we have listed both the SalesOffice and OfficeNumber. There are duplicate salesperson data. Duplicated information presents two problems:

1. It increases storage and decrease performance.
2. It becomes more difficult to maintain data changes.
### in this situation  Database normalization fixes them. through  three modification anomalies that can occur
1. Insert Anomaly
2. Update Anomaly
3. Search and Sort Issues
## Definition of Database Normalization
#### There are three common forms of database normalization
##### The forms are progressive, meaning that to qualify for 3rd normal form a table must first satisfy the rules for 2nd normal form, and 2nd normal form must adhere to those for 1st normal form. Before we discuss the various forms and rules in detail, let’s summarize the various forms:
- First Normal Form – The information is stored in a relational table with each column containing atomic values. There are no repeating groups of columns.
- Second Normal Form – The table is in first normal form and all the columns depend on the table’s primary key.
- Third Normal Form – the table is in second normal form and all of its columns are not transitively dependent on the primary key
###### If the rules don’t make too much sense, don’t worry. I’ve linked to article to help you understand them. For now it’s important to understand there are three rules for database normalization that upon each other.  Some people make database normalization seem complicated.
### that is it for today i wish you understand and have a good day 
