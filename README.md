# SQL_Stored_Procedure_Application_Project
Instead of sending multiple SQL statements from the client to the server, I encapsulate them in a stored procedure on the server and send one statement from the client end to execute them. 

Benefits: Stored procedures can be useful if you have an SQL query that you write and execute over and over again. You can save it as a stored procedure, and then just call it to execute it directly in the database server. In stored procedures, you can also pass parameters so that a stored procedure can act based on the passed parameter values.

Project case study: I business dealing on pet sales wants to automate the price update of pets on based on the present health status of the pet(good, bad, worse), they could not keep determining this price manually as that would take a lot of time with their database hosted on the cloud(IBM Db2). The task is-How can this business automate the price update of a particular pet given its health status? That is the question this project aims to answer. I created a stored procedure routine named UPDATE_SALEPRICE with parameters Animal_ID and Animal_Health.
- This UPDATE_SALEPRICE routine contains SQL queries to update the sale price of the animals in the PETSALE table depending on their health conditions, BAD or WORSE.
- This procedure routine takes animal ID and health condition as parameters which will be used to update the sale price of animal in the PETSALE table by an amount depending on their health condition. Suppose:
- For animal with ID XX having BAD health condition, the sale price will be reduced further by 25%.
- For animal with ID YY having WORSE health condition, the sale price will be reduced further by 50%.
- For animal with ID ZZ having other health condition, the sale price won't change.
