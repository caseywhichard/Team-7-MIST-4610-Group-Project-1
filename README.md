# Team 7-MIST 4610 Group Project 1
## Team Name:
Group 7
## Group Members:
  1. Casey Whichard
  2. Ally McVay - https://github.com/allymcvay/JitteryJoes
  3. Sydney Pratt - https://github.com/scp31975/Jiterry-Joe-s-
  4. Mino Guzman 
## Problem Description
The goal of this project is to design and build a relational database that represents the core operations of a global, multi‑location coffee chain. The Store serves as the central entity, which connects customers, employees, equipment, inventory, and orders. The database models how each store manages menu items, merchandise, suppliers, loyalty programs, and customer orders. We aim to accurately represent these relationships, generate realistic sample data, and populate each entity accordingly. Once built, the database will support functional SQL queries that provide meaningful business insights into company sales, inventory levels, customer behavior, and overall store performance.

## Data Model
Our model is based on the structure of a multi‑location coffee chain. The Store entity represents each physical coffee shop location. Each store employs multiple workers, which is why we established a one‑to‑many relationship between the Store and Employees entities. Stores also manage their own equipment and inventory, so the Equipment and Inventory tables each have a one‑to‑many relationship with Store as well.

Customers interact with the business primarily through orders. Because a customer can place many orders, we created a one‑to‑many relationship between Customers and Order. Customers typically also participate in the loyalty program, which is represented by the Loyalty entity. Since each customer can only have one loyalty account, this is modeled as a one‑to‑one relationship between Customers and Loyalty.

Each order can have multiple items, and each menu item can appear in many different orders. To represent this many‑to‑many relationships, we created the OrderItem associative entity, which links Order and MenuItem. OrderItem also stores the quantity and unit price for each item purchased.

Inventory is replenished through shipments from suppliers. The SupplierItem entity represents items shipped by suppliers, and the Inventory table references these shipments to track which supplier deliveries contributed to current stock levels. Because a supplier can ship many items, but each shipment record corresponds to a single supplier, this is modeled as a one‑to‑many relationship between Suppliers and SupplierItem.

Payments are recorded in the Payment entity, which stores the payment method, amount, and date. Each order has exactly one payment associated with it, so we modeled a one‑to‑one relationship between Order and Payment. Payment also references the customer who made the purchase, allowing the business to analyze spending behavior.

Finally, the Merchandise entity represents retail items sold in stores, such as mugs or apparel. Merchandise is tied to specific store locations, so we included a one‑to‑many relationship between Store and Merchandise.

Overall, this data model captures the complete operational flow of the global coffee chain—from customers placing orders, to inventory being supplied, to payments being processed—while maintaining a clear relational structure that supports meaningful business insights.
<img width="1282" height="1294" alt="image" src="https://github.com/user-attachments/assets/e211dfa2-dd6d-4671-a325-3721a2485ceb" />

## Data Dictionary
!<img width="456" height="456" alt="Screenshot 2026-03-31 at 2 25 55 PM" src="https://github.com/user-attachments/assets/463f99cc-354d-4487-bb20-a8dac6a2afd1" />

!<img width="451" height="456" alt="Screenshot 2026-03-31 at 2 26 05 PM" src="https://github.com/user-attachments/assets/f21ece02-3687-449c-bb1d-eb7347bb4c97" />

!<img width="451" height="409" alt="Screenshot 2026-03-31 at 2 26 16 PM" src="https://github.com/user-attachments/assets/97caa528-8771-4ad9-b277-bc652a9f7bdc" />

!<img width="451" height="458" alt="Screenshot 2026-03-31 at 2 26 25 PM" src="https://github.com/user-attachments/assets/e7748a6d-ee96-47a7-a2d4-dfa0d2818fa4" />

!<img width="465" height="432" alt="Screenshot 2026-03-31 at 2 26 34 PM" src="https://github.com/user-attachments/assets/fd65dc39-b19c-42b7-98ac-d3761286117b" />

!<img width="454" height="294" alt="Screenshot 2026-03-31 at 2 26 42 PM" src="https://github.com/user-attachments/assets/3182d553-bac2-46b8-bbd0-8f448864d17b" />

!<img width="458" height="436" alt="Screenshot 2026-03-31 at 2 26 52 PM" src="https://github.com/user-attachments/assets/d08ca955-ec0a-44de-803c-32bc53218628" />

!<img width="465" height="458" alt="Screenshot 2026-03-31 at 2 27 03 PM" src="https://github.com/user-attachments/assets/bc2e3b12-c84c-49df-8f43-27b8d3c5ee8c" />

!<img width="464" height="532" alt="Screenshot 2026-03-31 at 2 27 16 PM" src="https://github.com/user-attachments/assets/27d375bc-78b9-4f3a-8cf1-326b07f4a92d" />

!<img width="454" height="528" alt="Screenshot 2026-03-31 at 2 27 26 PM" src="https://github.com/user-attachments/assets/a6181e58-69e5-458e-9f73-2a0c2e96bc35" />

!<img width="455" height="255" alt="Screenshot 2026-03-31 at 2 27 34 PM" src="https://github.com/user-attachments/assets/039b47f9-a3fb-4693-a1b3-10d3fa7e260b" />

!<img width="453" height="366" alt="Screenshot 2026-03-31 at 2 27 47 PM" src="https://github.com/user-attachments/assets/b79c0bdd-0119-48a4-88ab-b13dc9ac2133" />

!<img width="452" height="322" alt="Screenshot 2026-03-31 at 2 27 59 PM" src="https://github.com/user-attachments/assets/bfc9539f-c1df-4927-8a1b-b26e6c05726f" />

## Queries:
## Assumptions
- LoyaltyID is stored redundantly to preserve the customer’s loyalty tier at the time of the order/payment, since loyalty status can change over time.
