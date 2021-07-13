# Implementing a Data Warehouse
[![NPM](https://img.shields.io/npm/l/react)](https://github.com/pand-eX/DataWarehouseOracle/blob/main/LICENSE) 

# About the project

Data Warehouse is a database, used to store information related to the activities of an organization in a consolidated manner. It enables the analysis of large volumes of data, which are collected from an OLTP (Online Transaction Processing) transactional system. DW is organized to support the company's strategic decision-making and we will use Virtual Machine with the Linux OS (Operating System) with Oracle integrated for the implementation of this project. 



## Why?

because this project is part of my personal portfolio, so I'll be happy if you could provide me with any feedback on the project, code, structure or anything you can report that could make me a better data engineer!

Email-me: henricao_7@yahoo.com.br

Connect with me at [LinkedIn](https://www.linkedin.com/in/henrique-castro-484269203//).


## Understanding the customer's need!


A XYZ Inc. based in São Paulo-SP, it is one of the largest companies in Brazil in the segment of direct-to-consumer electronics sales. The company has several stores throughout the state of São Paulo, in addition to Rio de Janeiro, Minas Gerais, Pernambuco, Bahia, Goiás and Santa Catarina. In its seventh year of operation, the company has managed to maintain good profit margins, with annual revenue growth of around 8.2%. The CEO has decided that it is time to expand operations and needs to better understand the current scenario of the company. After extensive research, the CEO and board of directors decided that a Business Intelligence solution, with metrics and KPIs related to the company's business would be useful to understand errors / successes in management so far and help in defining the growth strategy for the coming years. The BIAVANTE project was then created, with the objective of providing a corporate Business Intelligence solution. The company's IT department already has BI solution software licenses for reporting, a software package purchased from a vendor. Licenses had never been used and the directors determined that the software be used as a way to reduce cost, since the package had already been paid for. However, the company has no experience in Data Warehouses and has hired you to offer the necessary advice in the construction of the solution. You will be responsible for creating the Data Warehouse and ETL interfaces. First-level administration and support will be the responsibility of the company's IT team. At their first meeting, several directors explained in general terms how the company's operation works and recorded this in minutes. Below is the outcome of this meeting 
A XYZ Inc. is a company that sells electronics, especially computer equipment in general. The company works with aggressive margins and although the investment in Marketing is small, it is constant. There are several stores throughout Brazil and approximately 930 employees. Each store has a stock of various electronic products, such as desktops, notebooks, tablets and smartphones, which are the main products of the company, but several other products are sold, such as TVs, sound systems, peripherals, among others. There are approximately 250 products, distributed in 15 categories. A warehouse located in Barueri-SP, maintains products that arrive via import or from factories in São Paulo and Minas Gerais, where they are cataloged, receive an RFID seal and are then dispatched to stores throughout Brazil. Each product has a unique SKU code, as well as details that are stored in the product registration system, such as product name, brand, dimensions and other technical specifications. Whenever a sale is registered at a point of sale, one of 23 stores throughout Brazil, sellers are instructed to create a register about the customer and request an authorization for the customer to receive future promotions and marketing campaigns. Name, telephone number, address and email are mandatory in the registration, but other information may be requested, especially in the case of term sales, such as current employment, income, residence time and number of children. The company also has a registration of each store, which today is in Excel spreadsheet. There are the name of each store (a kind of nickname that helps identify each store), the address, the region, city and state. Each store has a code. This worksheet periodically updates the company's sales system, since each recorded sales is associated with a store. All stores sell all products, but stores maintain different inventories, as a way to reduce logistics costs, that is, not dispatch many products to stores that have a lower volume of sales, which could require possible further movement of products to stores with higher volume. Each store has a carefully registered ZIP Code, as the company often implements logistics optimization algorithms using graph analysis. They compared a new system recently, after they heard that the system, which is based on Artificial Intelligence, could reduce fuel costs by up to 25% by optimizing delivery truck routes! In each store, employees serve customers in the showroom, where products are displayed and also on the phone. Each store has some vendors, cleaning staff and supervisor, working in 2 shifts. The company intends to start selling online, but there is still no forecast. All employees are registered in the company's internal system, with registration number, personal data and specialty. A sale is always made by a seller, because the company pays commission for the sales made and the registration of the person responsible for the sale is tied to each sale made. The value and quantity of each sale are present in the company's daily reports, which are used for different decisions during the week. But these reports are manual, typically created in Excel, and often present errors. Each regional director needs to know the sales by region, to track the performance of your store and compare with the other regions. The company makes many sales of products as a single package or combo, but that are different products. For example, a desktop can be sold along with a monitor, keyboard, and mouse. Although it is a package, products have different SKUs, different values, and contribute differently when a discount is granted. The company calculates the percentage of each product in a package sale or combos. Directors believe that some product categories may not be profitable and would like to confirm this information with the new BI system. This information will also be useful for defining expansion strategies and which new product categories should be considered.

## Starting the Project!

- So let's implement a process that some companies pay thousands of dollars to implement and so I will try to show the step by step. 
I will take as a basis that you have already implemented Oracle in the LINUX OS (Redhat), if I did this process the project would be gigantic and take the focus of the creation of DW.
 As I am doing a personal project I will only have a Database that is Oracle, but it will serve 3 different purpose we will have a schema for data source, a schema for Staging Area and a schema for the DW itself. Let's start running the system for data source. Remembering that in a DW project you do not need to create the source that will be the RCP database system, CRM system, an Excel spreadsheet, a txt file or any other source. What I'm doing here is just to simulate the environment so you can see how the whole process works from start to finish.

- All Script will be in order for a better understanding of the project. Here will be more the part to understand what is being done and also the dw creation timeline!!! Let's go!


- Now that we understand the customer's need to stay focused on it!!! Objectivity and Simplicity are an Art so let's practice!
I'll try to be objective by keeping things simple by not inventing unnecessary things just to increase the design to make things more interesting or seem wiser than I am really is although that's not the rule in many situations. I'm going to stay focused on the client.
To start the project we need to study the process of implementing a Business Intelligence solution because the Data Warehouse is a component of a BI solution

![1](https://github.com/pand-eX/DataWarehouseOracle/blob/main/assets/img/1.png)
 
 The BI implementation process has 5 main ones: 
![2](https://github.com/pand-eX/DataWarehouseOracle/blob/main/assets/img/2.png)
 

![3](https://github.com/pand-eX/DataWarehouseOracle/blob/main/assets/img/3.png)
![4](https://github.com/pand-eX/DataWarehouseOracle/blob/main/assets/img/4.png)

In the Understanding of Customer Needs part, you need to have a meeting with Directors and Managers in the Knowledge Capture sessions where we will list:

What's the point?
- Who benefits from this Project?
- What are the current problems?
- Who will be the sponsor of the project?
What budget is available?
- What resources are available?
- What are the current reports 
and also in this stage internal meetings with different key actors. Document analysis. Query the processes and methods used in the company. Process mapping.


In the Requirements Gathering the meeting are with analysts with some people who are the team leaders those Professional who has the knowledge of the business area itself we list some of these tasks:


- Meetings with functional professionals.

- List of main requirements.

- Accept and agree between key stakeholders.

- Acceptance criteria.

- Details on the final operation of the solution

- Final remascans of the project.

- Os requerimentos devem ser Smart(specific, Measurable, Attainable, Relevant e Time-Based)

- Feedback sessions.




In Architecture it takes people from the IT area to build the solution that is technically feasible in it we will list a few steps:


- Internal meetings with IT staff.

- Identify data sources.

- Identify computational resources.

- Legacy systems.

- Integrations and Interfaces

- Suppliers that impact the project.

- How data is stored
 
- Design da solução de ETL(Extract, Transform and Load)

- Modeling (Logic, Dimensional and Physics)


-Project Objective:
This project is part of XYZ Inc's BIAVANTE project, aiming to implement a Data WareHouse to support BI, analysis and decision-making solutions.

- The Project includes the delivery of two products:


 -Data Warehouse
 
 -ETL interfaces for integration with data sources.
 

## Attention !!!

- In these requirements gathering processes and Project Deliveries such as Buusiness Case, Customer Functional Specification is not the responsibility of the Data Engineer but wanted to show the beginning of the project to have a direction and understanding of how a project to implement a Data Warehouse starts from here we will focus on the part that is the responsibility of a Data Engineer!!!



## Data Warehouse Architecture


![5](https://github.com/pand-eX/DataWarehouseOracle/blob/main/assets/img/5.png)

The Staging Area is an intermediate area used for data processing during ETL before going to DW. Basically the data that enters the DW already needs to be integrated and validated tracts so a separate area to do this.

## Logical Model and Dimensional Model

![6](https://github.com/pand-eX/DataWarehouseOracle/blob/main/assets/img/6.png)

The basic logic model for every dw implementation project is required to understand the entire segment and need of the company.


![7](https://github.com/pand-eX/DataWarehouseOracle/blob/main/assets/img/7.png)

A tip> the more complete your dimensional model will be easier to create your physical model so pay a lot of attention to this step. 
- Star Squema is a more consolidated model and a slightly more standardized model 
- First there in the logical model we did not have the DIMENSION TIME the time it records the date of sale eventually the year, month by week the day, but this is a sales information here in the Dimensional model I need to control the time in a slightly more detailed way up because in the customer specifications it became clear that he wants the report per day so I already know that my level of Granularity is until day then I need to extract from the date the information of year, month, week and day.
- Another feature that draws attention and not having the Dimension Employees is because we do not have? A valuable tip!!! Start the small Data Warehouse and then you will increment your DW. As you the company and the project team learn you can incorporate more and more dimensions you can modify the dimensions by adding more attributes by modifying your Star Squema model to Snow Flake the Data Warehouse is a living structure because it reflects the business of the company if the business changes the business has new requirements it is normal that it also grow. Returning to the question of the dimension Employees is because it does not have this need to create this now I need the Customer Dimension because the sale is made by the customer, Product Dimension because the sale and made from the product, I need the dimension of the Locale because the managers and directors want sales reports by regions and I need a Dimension Time to record each of the moments that the sale is made.
Let's understand the need of the Keys project and the differences between Surrogate Key x Natural Key very important concept when working with Data Warehouse. It is critical because the keys that will determine key relationships are nothing more than primary keys, foreign keys, and surrogate key it is important for you to understand how these keys will be implemented because all the relationships you do in your model all you extract information from DW is made the relationships between those keys therefore if this is not well implemented of course it will generate problems up front
- Let's start at ID_CLIENTE there in the Logical Model we created the Client Entity we put there the ID_CLIENTE and called with Primary Key because there in the Transactional database there in the data source my customer registration table she has a column that uniquely identifies each client this column and called the primary key only when you work with Data Warehouse I really want to create another field that helps with relationships only with the Dimensional model that other field is called Surrogate Key which is also called artificial key the Surrogate Key does not exist in nor else it only exists in the Data Warehouse will be a column that will auto increment so you enter the first record will be the number 1 in surrogate key the second number 2 and etc... If you analyze a dimension table you will see a Surrogate key and also a key that is Natural Key is no longer the Primary Key and why do we do it? Why now it helps to know where the record comes from what exactly was that record there in the data source I have some advantages in keeping this information, however to create the relationships between the tables in my Dimensional model we have created an artificial primary key that is called Surrogate Key /\ Our Key Project says that in our DW we will not use the primary key of the source as the primary key the primary key of the data source will turn into a Natural key or Business Key and there in our DW will be created a Surrogate Key an artificial key. 
- Another important question is whether you look at the table Fato_VENDA look who comes to fact table exactly the columns of the Surrogate Keys 
- Remember and understand Normalized Data x Denormalized Data > remembering that you have the purpose of DW that is query and you lose performance with Normalized data and why you want to denormalize. The purpose of DW is to consult
- Naming patterns > dimension name, column name, eventually documentation is important that you have some kind of Pattern. Usually companies already have a document talking about these Standards you as a Consultant need to check with the business if there is some kind of pattern being adopted if there is no you create and use your own pattern, but it is important that there is some pattern. (SK > Surrogate Key /\ NK> Natural Key /\ NM> name /\ DESC> description /\ BY>Binary /\ NR>Number /\ FLAG> Holiday)
- One of the dimensions of your Dimensional model is quite special which is TIME and will be in any DW that will always be there to support exactly one of the main questions you ask for the Data Warehouse i.e. when that sale occurred, when that "situation" occurred we want our Data Warehouse to answer several questions one of them is exactly related to the time. The time dimension is not loaded along with the ETL process, that is, you don't have to keep constantly updating your time dimension because in fact it is a virtually static structure is a dimension that will rarely change. Some features when you build this dimension, see that in the first we have a Surrogate Key or is it a unique ID for each of the entries and a Column with date type Date and what date is this? Is each of the dates representing each of the working period dates of that DW which is the year of the DW who responds is the client 1 year? Two years? Three years? 20 years? The client will define what period of data he wants to analyze so assuming he wants four years I will have entry dates for those 4 years so I can create the crosses. 
- Fill in all documentation of all columns whenever you are creating your Dimensional model.
- Physical Model it understands the creation of the Tables the definition of storage whether or not I will use or partitioning, that is, if I will have a table distributed in more than one physical file still in the physical model we also define how will the indexing we have to create some index project and all this occurs in physical modeling  



 - That's our goal we want to create a dimensional model there in DW I have the data source including already extract ing this data to Staging Area but the data is in raw format is uncleaned they require a transformation process to manipulate this data that is the ETL process 
ETL is as Raul seixas said > is a walking metamorphosis is always in the process of change. We need to have the skills necessary to recognize both the technical analysis and also the issues involved in the business rules.

- /\ The 1 table we're going to load is from the Time dimension because the time dimension data doesn't come in the ETL or usually doesn't come. Creating a specific operation to load the Time Dimension remembering that it will hardly change or will change very little in the lifetime of your DW we do not need to include this in the ETL but I REPEAT depending on the Project there is not a single rule there is not only one standard will always depend on the project in most cases the dimension Time it varies very little so we can generate the data that will be loaded within this TABLE, what data are these? Data for date in a given period 

So in staging area we'll prepare the data and then load into dw.
- We will not use the ETL process for Time dimension that we will do manually at the time we will create the DW.
In Staging Area we will work the Customer, Locale and Product dimension we will collect the data from the source to verify that we need some kind of transformation if I have to clean up the data and I'm already preparing the data for later loading. Also, we're going to prepare a sales table I'm not going to prepare the fact ok table I'll prepare the Sales table because by what we learned from our project the sales data they are spread over more than one Table so I'll group this data I'll rearrange put into a single single table structure and also already prepare for later load in the TABLE FACT , basically let's prepare data 4 tables. 3 dimensions and for fact table and time dimension we will do in DW.
 
 
 ## PROJECT END /\ Now it's continuous improvements!!! 


- Now with DW ready we need to make improvements to our DW
- Purposely left there in the data source of the transactional database in the source user a hierarchy category that was not well implemented


![8](https://github.com/pand-eX/DataWarehouseOracle/blob/main/assets/img/8.png)

You can see repeating the categories and this cannot happen in the Transactional database at source because the data needs to be NORMALIZED.... The data is not normalized there in the DW but in the SOURCE in the transactional database needs to be normalized.

## Implementing Hierarchy in database source

We will implement the Hierarchy correctly and we will have to change the entire ETL process until we reload our FACT TABLE
First let's understand the hierarchy level

![9](https://github.com/pand-eX/DataWarehouseOracle/blob/main/assets/img/9.png)

It is category according to what the company sells or provides product or Service, below this category we have the category daughter, personal and business /\ notebooks for personal use and for use of service company. And I will then have each product associated to the lowest level of my Hierarchy the product name Notebook MSI is a grain, that is, it is the lowest level of Granularity we can have levels of the size we want depends on what the company implements. 
Sales are not associated with Category, what you sell is the product what we have here is the Hierarchy so we can categorize these products because then I want to issue a report which were the categories that sold the most. Which categories sold the most by region. Which categories sold the most by customer type and etc...
Product does not enter the Category table because we have a table only for product after I need to enter the product table and update the category.
- We have just implemented our Category Hierarchy see that we have 1 column with All Ids 2 Column with all categories without repetition and the respective Ids of the Parent Category

![10](https://github.com/pand-eX/DataWarehouseOracle/blob/main/assets/img/10.png)

Now as i said the above let's update the Product table. We changed the ID_CATEGORIA and this no longer reflects on the product table, we can only do this because we disabled constraints which is the constraint that maintains referential integrity so we disable constraints, command > 
ALTER TABLE TB_PRODUTO MODIFY CONSTRAINT TB_PRODUTO_FK1 DISABLE; We use this command before performing the entire process up. So I can modify the Category table but if now I do not update the Product table will become all wrong./\ MODIFIED NOW ACTIVE TO DO THE QUERY command >
CHANGE TB_PRODUTO CHANGE THE MODIFICATION RESTRICTION TB_PRODUTO_FK1 ENABLE;
IT IS IMPORTANT TO REMEMBER TO TURN CONSTRAINTS ON AND OFF THIS IS A PROCESS THAT WE DO A LOT DURING THE ETL PROCESS ESPECIALLY BEFORE LOADING THE DATA NORMALLY YOU DISABLE THE INDICES AND CONSTRAINT AS THERE OF YOUR DW PERFORMS THE LOAD AFTER ACTIVE AGAIN IF YOU DO NOT ACTIVATE IT WILL HAVE PROBLEM AFTER IN REFERENTIAL INTEGRITY.

## Improving VIEW performance

- We can have several views in our database, we can create a view for example with a business rule i.e. I include a clause WERE this view could have sales only from 2018 /\ 2019 etc... We can create a Vision for each month of the year we can create a view for category for example and then I'll create the views and then I feed there for example when I have using a BI tool instead of the BI tool using query makes a direct query in VIEW is a good practice is much safer because if I then need to change the query I change the query within the view but my BI system will be pointing to VIEW I don't need to change anything in the system I just change the view in the database. 
- There's only a small issue here when we use a VIEW in practice what the database does is run the QUERY this here is good for the human it doesn't need to know the QUERY is simple to give a select on view but internally the database knows that this is a VIEW and runs the query of course and this has a cost in the database we will visualize what that cost is. (EXPLAIN PLAN FOR QUERY DOWN)


![11](https://github.com/pand-eX/DataWarehouseOracle/blob/main/assets/img/11.png)


How did the database optimizer run this query? As follows! He made the Select Statement /\ ORDER BY /\ used the HASH for the BY group and join and made a FULL ACESS TABLE i.e. he did not even use an index.
- Of course in my example this makes no difference because we have few lines but if instead of 7 lines I had 7 million lines this here would make all the difference the query would get very slow to create a VIEW is a good alternative but does not solve much of the problem of performance because I'm still running the query the same way. So to solve this I created a Materialized VIEWs where I'm going to store in the database the result of running query. What I want is basically every time I run the VIEW I don't want to run query what I want is to look at the data already stored in DW that QUERY that is part of that VIEW we'll run there and write the records to a database when I call the view again I'll be with another execution plan much faster 
Notice that he made a FULL ACESS only on a table that was the one that we created the materialized View if you see the difference of the execution plan there from our Query he did the TABLE SCAN on 3 different tables now no I sweep only a single runtime table is infinitely smaller and I can considerablely optimize the performance of the database it is also useful when you want to connect in remote database for example you have a DW on a Server in the Unit of São Paulo and the analyst are in Rio de Janeiro how will you traffic the data?  I can create a Materialized View that she will consult from Rio to São Paulo, she goes to São Paulo consults the database brings the data of course this will take a while I can create the Materialized View at night and the next day the analysts from Rio de Janeiro go to work they will consult the data locally from Rio de Janeiro because we create the materializad in the river do not need to stay spending bandwidth to perform consultation between Rio and São Paulo I create a Data Base Link between the two banks I create a materialized views in Rio pointing to the data of São Paulo I do this process the night the next day the analysts are happy of life working with High Performance. What if I happen to enter more data in the fact table? For sure the materialized View will get outdated because I ran the Query only once. For this we can make a Refrash of the Materialized View command >
EXEC DBMS_MVIEW.refresh(‘mv_vendas_2018’);
-Sunday the DBA of Rio creates the View Materialized during Monday so working normally, consulting the local data when it is on Monday night the DBA of Rio schedule this REFRESH so it will update the view materialized the night with the new data that was loaded in the fact table on Tuesday morning analysts continue working with the happy materialized view of life with High Performance. A professional environment


![12](https://github.com/pand-eX/DataWarehouseOracle/blob/main/assets/img/12.png)



## One important thing is to define refresh's strategy




![13](https://github.com/pand-eX/DataWarehouseOracle/blob/main/assets/img/13.png)


Some companies delete all DW and refresh with the new data you update the ENTIRE DW (Depends on several factors including the size of the DW)
-Other companies update the DW, i.e. only applies the changes since the last load (depending on the size of the DW is an approach)
-And you can find way to detect the changes that occurred in the source system between one load and another and apply only these changes this will greatly reduce your update window.

![14](https://github.com/pand-eX/DataWarehouseOracle/blob/main/assets/img/14.png)


![15](https://github.com/pand-eX/DataWarehouseOracle/blob/main/assets/img/15.png)

Depending on the database we can use Golden Gate technology.
In my case of oracle database we can use the Archive Logs it has a concept of Data Guard you can create a kind of copy database and all the database logs the logs (is that contains all the DML commands that are applied in all tables are the Logs of the database you can picks up the archives that exactly is the results of these Logs move this to another database and apply the archives which is basically apply the DML applications, that other database looks like it's a copy) you can apply a similar solution in DW and we have the Golden gate concept that is to work with Streaming data you can configure golden gate to look at its source whatever it is other than the Relational Bank capture only the changes and apply to your Destination system.

![16](https://github.com/pand-eX/DataWarehouseOracle/blob/main/assets/img/16.png)


Here we can make several partitions for each month and when you update the data you can update by partition do not need to update the entire DW this considerably reduces the volume of data and speeds up the load time and you can use this option and then if necessary could clean the data by partition assuming that a company wanted for example update the data from June I can clean only the partitions of the data from june and load only on that partition. If the partition that are physical files have on Disk different the fact of loading a partition would not affect the query performance of the data on another partition i.e. choose the best strategy according to what the company has at its disposal remembering that Oracle Particion which is the functionality of oracle for partitioning has a separate license.

![17](https://github.com/pand-eX/DataWarehouseOracle/blob/main/assets/img/17.png)


No caso de uma empresa ter o nível de granularidade de 5 anos e passa 6 anos precisamos fazer uma estratégia para essa demanda. O que as empresas fazem é criar uma cópia da dimensão, mantendo apenas uma cópia daquele ano que não está no período de 5 anos então você tem no DW apenas os 5 anos, mas se necessário os dados históricos estão ali em mãos em disposição você cria uma cópia da Dimensão e pronto e inclusive você pode utilizar essa cópia em relatórios mesmo você pode criar os relatórios lá na ferramenta de BI apontando para essa dimensão de históricos. 

![18](https://github.com/pand-eX/DataWarehouseOracle/blob/main/assets/img/18.png)


In case a company has the level of granularity of 5 years and passes 6 years we need to make a strategy for this demand. What companies do is create a copy of the dimension, keeping only a copy of that year that is not in the period of 5 years so you have in DW only 5 years, but if necessary the historical data is there in hand you create a copy of the Dimension and ready and even you can use that copy in reports even you can create the reports there in the BI tool pointing for this dimension of hishistóricos.

![19](https://github.com/pand-eX/DataWarehouseOracle/blob/main/assets/img/19.png)


# 10 Common errors to avoid in Data Warehouse Projects.

![20](https://github.com/pand-eX/DataWarehouseOracle/blob/main/assets/img/20.png)
