# MIST4610-Group-5-Project-1
# Team Members: 
1. Zhen, Christina - 811674601 - https://github.com/cz67968/MIST4610-Group-5-Project-1
2. Snow, Luke - 811958066 - https://github.com/lrs84323/MIST4610_GroupProject_5
3. Arfath, Rushil - 811460339 - https://github.com/R1Arafath/Group-5-Project-1-Final
4. Khan, Azaan - 811686335 - https://github.com/Azaank09/group-project
5. Fontoura, Gabriel - 811794390 - https://github.com/gof98446/GroupProject5/blob/main/README.md

# Problem Description: 
Our project focuses on creating a database for an online bookstore to efficiently track key business operations, including sales, employee hours, genres, authors, and inventory management. The database is designed to manage book inventory by categorizing books under a one-to-many relationship, where multiple ISBNs can belong to a single category. Sales transactions are recorded through a many-to-many relationship between books and sales, using a weak entity that links sales details with inventory. This structure allows for tracking which books are sold in each transaction. Additionally, employee work hours are managed through another many-to-many relationship between employees and shifts, where each employee can work multiple shifts, and each shift can have multiple employees. By structuring the database in this way, the system provides an organized method for analyzing book sales, tracking employee work schedules, and ensuring efficient inventory management.
# Data Model: 
![image](https://github.com/user-attachments/assets/0ea972b7-c4b5-4603-aed1-3760d04fb12c)

Our team’s data model is designed for an online bookstore, capturing key relationships between sales, inventory, employees, and shifts. The inventory entity tracks books, linking each book to a specific category through a one-to-many relationship, as multiple books can belong to a single category. Sales transactions are recorded through a many-to-many relationship between sales and inventory using the sales details entity, which connects each sale to the books purchased. Since a sale can include multiple books, and a book can appear in multiple sales, this entity ensures proper tracking of transactions. Employee work hours are managed through another many-to-many relationship between employees and shifts, where an employee can work multiple shifts, and a shift can have multiple employees. The shift assignment entity facilitates this relationship by linking employees to specific shifts. The sales entity serves as the foundation of the model, containing key transaction data and connecting to shifts through employee sales records. This data model allows for efficient tracking of inventory, sales trends, and employee scheduling, optimizing bookstore operations.
# Data Dictionary: 
![image](https://github.com/user-attachments/assets/7c2671ee-c530-4922-bbdc-157854272f8f)
![image](https://github.com/user-attachments/assets/094aeadc-79fe-46b9-a02d-d8f1f3eb9127)
![image](https://github.com/user-attachments/assets/12fed416-d2bd-4f37-ba00-c5ccfadae4f6)
![image](https://github.com/user-attachments/assets/a2cc3d2f-5b10-4722-a4db-b6f0f17d87c1)
![image](https://github.com/user-attachments/assets/d991d994-3ba6-4bb0-9104-485ceb5a9d0a)
![image](https://github.com/user-attachments/assets/f02bc27e-2835-4e27-94aa-4747da52d601)
![image](https://github.com/user-attachments/assets/6791fb3c-3551-4586-bed8-679594dd89e9)
# Queries: 
1. Query 1 retrieves employee details, assigned shifts, and pay rates by joining multiple tables to link employees, assignments, and shifts for a comprehensive view.

![image](https://github.com/user-attachments/assets/2aa7443a-ec97-45a3-bb84-1584c172d02b)

Description:
This query retrieves the total number of books sold by each employee, ordering them from highest to lowest sales. This helps evaluate employee performance and identify top sellers.

2. Query 2 displays each book's selling price, purchase cost, and computed profit, helping identify high-margin books that contribute the most to revenue.

   
![image](https://github.com/user-attachments/assets/a72d8090-7c38-47ca-86d9-7e87fe3cd310)

Description:
This query highlights books with higher-than-average profit, helping recognize best-selling, high-margin products to inform purchasing and marketing strategies.

3.Query 3 identifies how much profit each book generates per sale, helping assess which books contribute the most profit.

![image](https://github.com/user-attachments/assets/0d13c720-374c-4507-b5fb-4053fb5af2b5)

Description:
This query highlights the most sold books along with their price and profitability. It supports restocking decisions and provides insight into customer preferences.

4. Query 4 retrieves sales data, including product details, pricing, and quantity sold, using a window function to compute total profit across all sales. It joins sales data with inventory to link product details and transactions.


![image](https://github.com/user-attachments/assets/03b3f3fd-2b19-45d2-8598-cedb4b57e3d9)

Description:
This query calculates the total hours worked by each employee and ranks them from highest to lowest. It helps with payroll processing and identifying employees with the highest workload.

5. Query 5 retrieves book details, including ISBN, title, author, available quantity, genre categorization, and aisle assignment. It joins the inventory table with the category table to link books with their respective categories.


![image](https://github.com/user-attachments/assets/e6b3ceb4-dd46-482e-a7e4-fae8fc547099)

Description:
This query calculates profit per book (ISBN) and the total profit of each sale transaction, supporting financial analysis and revenue tracking.

6. Query 6 provides employee shift details, labor per employee, and total labor cost per shift by calculating payroll based on hours and pay rate, using window functions for total shift labor.

![image](https://github.com/user-attachments/assets/7205f4d4-b9af-4c83-bb38-af7fce816ec1)

Description:
This query provides payroll calculations per employee shift and the total labor cost per shift. It assists in budgeting and staffing decisions.

7. Query 7 calculates the total profit generated over the entire sales period by computing profit per sale and using a window function to sum total profit across all transactions.

![image](https://github.com/user-attachments/assets/a4a013c3-fce2-4299-afe2-8050a6e5c395)

Description:
This query calculates the total profit generated over all sales transactions. It is useful for high-level financial reporting and performance analysis.

8. Query 8 retrieves the employee with the earliest start date, indicating the longest tenure in the company.

![image](https://github.com/user-attachments/assets/3efaea1b-0283-4b99-a61f-f077a5103939)

Description:
This query finds the employee with the longest tenure in the company. It can be used for employee recognition programs or for workforce planning.

9. Query 9 calculates labor cost per employee shift and uses a window function to compute the total labor cost across all shifts over the entire sales period.

![image](https://github.com/user-attachments/assets/223a4fbc-0ecf-4b2e-a7fe-e1caf684df86)

Description:
This query computes the total labor cost for all shifts over the entire sales period. It is useful for financial planning and workforce cost analysis.

10. Query 10 retrieves book inventory details, including ISBN, title, author, available quantity, category name, and aisle location by joining the inventory and category tables.

![image](https://github.com/user-attachments/assets/ba5be8cd-cc2c-4c80-a0e6-01d7d3e33ed3)

Description:
This query retrieves book inventory details, including quantity available and location in the store. It is helpful for stock management and customer assistance.

# Database Information:

![image](https://github.com/user-attachments/assets/55392353-a833-40ed-8fde-53a91ce5f930)




























