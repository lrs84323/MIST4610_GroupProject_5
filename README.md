# MIST4610-Group-5-Project-1
# Team Members: 
1. Zhen, Christina - 811674601 - https://github.com/cz67968/MIST4610-Group-5-Project-1
2. Snow, Luke -
3. Arfath, Rushil -
4. Khan, Azaan -
5. Fontoura, Gabriel -

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














