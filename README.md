# Team 7-MIST 4610 Group Project 1
## Team Name:
Group 7
## Group Members:
  1. Casey Whichard
  2. Ally McVay - https://github.com/allymcvay/JitteryJoes
  3. Sydney Pratt - https://github.com/scp31975/Jiterry-Joe-s-
  4. Mino Guzman 
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

## Assumptions
- LoyaltyID is stored redundantly to preserve the customer’s loyalty tier at the time of the order/payment, since loyalty status can change over time.
