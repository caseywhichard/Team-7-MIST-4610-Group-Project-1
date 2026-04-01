# Team 7-MIST 4610 Group Project 1
## Team Name:
21479 Group 7
## Group Members:
  1. Casey Whichard
  2. Ally McVay - https://github.com/allymcvay/CoffeeShop 
  3. Sydney Pratt - https://github.com/scp31975/Jiterry-Joe-s-
  4. Mino Guzman - https://github.com/Mino-Guzman/JitteryJoes
## Problem Description
The problem we have been tasked to solve is to design a data model and build a database that represents the relationships in operations of a global, multi‑location coffee chain. For this company, the Store serves as the central entity, since it is the physical center that connects customers to the products the coffee shop offers. The database also models the menu items and merchandise offered, suppliers of inventory, customer loyalty programs, and orders customers make. Using this data model, we generated realistic sample data that aligns with these entities and their relationships. By doing this, we are creating a database that allows us to perform relevant SQL queries that provide meaningful business insights that managers would be interested in, including company sales revenue, customer trends, and inventory levels.

## Data Model
As mentioned above, our model is based on the structure of a global coffee chain. The Store is the central entity that represents each physical coffee shop location. Each store hires many employees, so we established a one‑to‑many relationship between the Store and Employees entities. Also, several pieces of inventory and equipment are assigned to one store, so there is a one‑to‑many relationship with the Store and Inventory and with the Store and Equipment entities as well. Finally, one store can take many orders from customers, so we created a one-to-many relationship between the Store and Order entities. 

What drives this business is sales, so customers interact with the business through order purchases. These purchases can consist of orders of food, drinks, and merchandise. We concluded that one customer can place many orders, so we created a one‑to‑many relationship between the Customers and Order entities. Orders can consist of merchandise as well, so using the same idea that one customer can purchase several pieces of merchandise, we placed a one-to-many relationship between the Customers and Merchandise entities. Finally, customers typically participate in the loyalty program to earn points with the hopes of getting deals on future purchases. Each customer can only have one loyalty account attached to their name, so this is modeled as a one‑to‑one relationship between the Customers and Loyalty entities.

Customers can make several payments on order purchases, since they can return to the store whenever they would like.So, we established a one-to-many relationship between the Customers and Payment entities. We also assume that each order only consists of one payment, so we created a one-to-one relationship between the Order and Payment entities. 

The company requires supplies on hand that go into inventory. In order to generate supplies, the company requires a supplier or suppliers to supply these items. Each supplier can ship several supplier items, which led us to establish a one-to-many relationship between the Suppliers and SupplierItem entities.

Overall, the data model, as shown below, successfully captures the relationships between the activities that take place in a global coffee chain. It provides a detailed understanding on the customer orders, inventory and equipment levels, the payment process, and hiring distributions. 

<img width="1282" height="1294" alt="image" src="https://github.com/user-attachments/assets/e211dfa2-dd6d-4671-a325-3721a2485ceb" />

## Data Dictionary
<p align="center">
<img width="456" height="456" alt="Screenshot 2026-03-31 at 2 25 55 PM" src="https://github.com/user-attachments/assets/463f99cc-354d-4487-bb20-a8dac6a2afd1" />
<br><br>
<img width="451" height="456" alt="Screenshot 2026-03-31 at 2 26 05 PM" src="https://github.com/user-attachments/assets/f21ece02-3687-449c-bb1d-eb7347bb4c97" />
<br><br>
<img width="451" height="409" alt="Screenshot 2026-03-31 at 2 26 16 PM" src="https://github.com/user-attachments/assets/97caa528-8771-4ad9-b277-bc652a9f7bdc" />
<br><br>
<img width="451" height="458" alt="Screenshot 2026-03-31 at 2 26 25 PM" src="https://github.com/user-attachments/assets/e7748a6d-ee96-47a7-a2d4-dfa0d2818fa4" />
<br><br>
<img width="465" height="432" alt="Screenshot 2026-03-31 at 2 26 34 PM" src="https://github.com/user-attachments/assets/fd65dc39-b19c-42b7-98ac-d3761286117b" />
<br><br>
<img width="454" height="294" alt="Screenshot 2026-03-31 at 2 26 42 PM" src="https://github.com/user-attachments/assets/3182d553-bac2-46b8-bbd0-8f448864d17b" />
<br><br>
<img width="458" height="436" alt="Screenshot 2026-03-31 at 2 26 52 PM" src="https://github.com/user-attachments/assets/d08ca955-ec0a-44de-803c-32bc53218628" />
<br><br>
<img width="465" height="458" alt="Screenshot 2026-03-31 at 2 27 03 PM" src="https://github.com/user-attachments/assets/bc2e3b12-c84c-49df-8f43-27b8d3c5ee8c" />
<br><br>
<img width="464" height="532" alt="Screenshot 2026-03-31 at 2 27 16 PM" src="https://github.com/user-attachments/assets/27d375bc-78b9-4f3a-8cf1-326b07f4a92d" />
<br><br>
<img width="454" height="528" alt="Screenshot 2026-03-31 at 2 27 26 PM" src="https://github.com/user-attachments/assets/a6181e58-69e5-458e-9f73-2a0c2e96bc35" />
<br><br>
<img width="455" height="255" alt="Screenshot 2026-03-31 at 2 27 34 PM" src="https://github.com/user-attachments/assets/039b47f9-a3fb-4693-a1b3-10d3fa7e260b" />
<br><br>
<img width="453" height="366" alt="Screenshot 2026-03-31 at 2 27 47 PM" src="https://github.com/user-attachments/assets/b79c0bdd-0119-48a4-88ab-b13dc9ac2133" />
<br><br>
<img width="452" height="322" alt="Screenshot 2026-03-31 at 2 27 59 PM" src="https://github.com/user-attachments/assets/bfc9539f-c1df-4927-8a1b-b26e6c05726f" />
</p>

## Queries:
<p align="center">
<img width="624" height="376" alt="Screenshot 2026-03-31 at 9 18 34 PM" src="https://github.com/user-attachments/assets/b4920fdf-30e2-44ec-9507-6841e27951d3" />
  </p>

### 1. List all seasonal cafe managers
<p align="center">
<img width="622" height="406" alt="Screenshot 2026-03-31 at 9 19 30 PM" src="https://github.com/user-attachments/assets/33d94761-b998-499a-a76b-e654f3c85ecc" />
  </p>
This query allows leadership to quickly identify which café managers are employed on a seasonal basis. Seasonal managers typically work only during peak periods, such as the academic year or high‑traffic months. Knowing exactly who these managers are helps the organization anticipate staffing gaps when the season ends. This ensures that stores relying on seasonal leadership receive the necessary support, training, or replacement coverage ahead of time. By isolating seasonal managers, the café can better plan for continuity, maintain service quality, and allocate resources to locations that may need additional managerial oversight once seasonal staff depart.

### 2. Show all items on the menu that have never been ordered
<p align="center">
<img width="626" height="424" alt="Screenshot 2026-03-31 at 9 24 15 PM" src="https://github.com/user-attachments/assets/947f7a60-e060-4036-ab96-b232a0fb469a" />
  </p>
This query helps managers identify which menu items have never been purchased. Items with zero orders may signal low visibility, poor appeal, or unnecessary complexity on the menu. By isolating these products, managers can decide whether to promote them, adjust pricing, or remove them to reduce waste and streamline inventory.

### 3. Show all orders and their status
<p align="center">
<img width="621" height="484" alt="Screenshot 2026-03-31 at 9 25 40 PM" src="https://github.com/user-attachments/assets/9e4f5de5-2106-4231-8b30-41ad9a21483a" />
  </p>
This query pulls information from the SupplierItem and Suppliers tables to show what items have been shipped, when they were shipped, and the status of the supplier. It provides visibility into the supply chain and helps track incoming inventory.

### 4. Revenue by payment type 
<p align="center">
<img width="621" height="403" alt="Screenshot 2026-03-31 at 9 26 39 PM" src="https://github.com/user-attachments/assets/3e217331-7a7e-4c6c-ae8d-7ba570847c0d" />
  </p>
This query shows how much revenue comes from each card type, helping managers understand which cards customers use most. This makes it easier to plan for reliable payment processing, manage card‑related fees, and ensure the café’s systems support the most common payment methods efficiently.

### 5. Average order value by store
<p align="center">
<img width="624" height="425" alt="Screenshot 2026-03-31 at 9 27 30 PM" src="https://github.com/user-attachments/assets/116050d2-280e-49f0-9169-1a3083e2de9c" />
  </p>
This query calculates the average order value for each store and pairs it with key performance metrics such as total orders received and total revenue generated. By comparing stores based on their average order value, managers can quickly identify which locations are driving higher‑value transactions. Sorting the results in descending order makes it easier to prioritize high‑performing stores and recognize those that may need additional support, pricing adjustments, or promotional strategies to improve their average order size.

### 6. Most popular menu items by the total quantity sold 
<p align="center">
<img width="622" height="398" alt="Screenshot 2026-03-31 at 9 28 20 PM" src="https://github.com/user-attachments/assets/ae569539-0fd2-4a62-a735-518bcbf50c86" />
  </p>
This query ranks the popularity of each item based on the item’s total quantity sold. The query ranked each menu item by the number of units sold across all orders, while also calculating the total revenue generated from each item. The information provided became a useful way to identify bestsellers and top revenue-driving items.

### 7. Stores with above average revenue 
<p align="center">
<img width="622" height="435" alt="Screenshot 2026-03-31 at 9 29 09 PM" src="https://github.com/user-attachments/assets/e6892cc4-0eb4-4284-b8f7-1a575f61242f" />
  </p>
This query identifies which stores generate more revenue than the overall average across all locations. By first calculating each store’s total revenue and then using a subquery to determine the average of those totals, managers can clearly see which stores are outperforming expectations. Highlighting above‑average stores helps leadership recognize strong performers, allocate resources effectively, and understand which operational practices may be contributing to higher revenue.

### 8. Stores with low inventory that need to reorder 
<p align="center">
<img width="623" height="426" alt="Screenshot 2026-03-31 at 9 30 11 PM" src="https://github.com/user-attachments/assets/9624bb24-b57b-442e-9f47-cb298ab3c525" />
  </p>
This query identifies any item at a store whose current quantity has dropped below its designated reorder level. It also calculates how many additional units are needed to reach that threshold again. By sorting the results from most urgent to least urgent, managers can quickly see which stores and items require immediate restocking. This helps prevent stockouts, supports smoother operations, and ensures that high‑demand products remain available to customers.

### 9. Show the customer who has spend the most money
<p align="center">
<img width="627" height="433" alt="Screenshot 2026-03-31 at 9 30 52 PM" src="https://github.com/user-attachments/assets/2a2c2e83-850b-46f3-932e-d6af8313b562" />
  </p>
This query identifies the customer with the highest total spending across all their orders. The subquery calculates each customer’s total amount spent, finds the maximum value, and then matches that amount back to the specific customer’s name and ID. This helps managers quickly recognize top‑spending customers, understand purchasing behavior, and potentially target these high‑value customers for loyalty rewards or personalized promotions.

### 10. Which menu items generate an above average amount of revenue 
<p align="center">
<img width="619" height="455" alt="Screenshot 2026-03-31 at 9 32 45 PM" src="https://github.com/user-attachments/assets/6ef849a0-941d-4e29-8988-1102a05751c7" />
  </p>
This query identifies which menu items generate more revenue than the average item on the menu. Like the store‑level version, it calculates each item’s total revenue and compares it to the overall average, returning only the strongest performers. This helps managers quickly see which products drive the most sales, guiding decisions about promotion, pricing, and menu placement to maximize revenue.

## Databased Information
MySQL server: al_Group_21479_G7

## Assumptions
- LoyaltyID is stored redundantly to preserve the customer’s loyalty tier at the time of the order/payment, since loyalty status can change over time.
