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
>Our model is based on the structure of a multi‑location coffee chain. The Store entity represents each physical coffee shop location. Each store employs multiple workers, which is why we established a one‑to‑many relationship between the Store and Employees entities. Stores also manage their own equipment and inventory, so the Equipment and Inventory tables each have a one‑to‑many relationship with Store as well.
>
>Customers interact with the business primarily through orders. Because a customer can place many orders, we created a one‑to‑many relationship between Customers and Order. Customers typically also participate in the loyalty program, which is represented by the Loyalty entity. Since each customer can only have one loyalty account, this is modeled as a one‑to‑one relationship between Customers and Loyalty.
>
>Each order can have multiple items, and each menu item can appear in many different orders. To represent this many‑to‑many relationships, we created the OrderItem associative entity, which links Order and MenuItem. OrderItem also stores the quantity and unit price for each item purchased.
>
>Inventory is replenished through shipments from suppliers. The SupplierItem entity represents items shipped by suppliers, and the Inventory table references these shipments to track which supplier deliveries contributed to current stock levels. Because a supplier can ship many items, but each shipment record corresponds to a single supplier, this is modeled as a one‑to‑many relationship between Suppliers and SupplierItem.
>
>Payments are recorded in the Payment entity, which stores the payment method, amount, and date. Each order has exactly one payment associated with it, so we modeled a one‑to‑one relationship between Order and Payment. Payment also references the customer who made the purchase, allowing the business to analyze spending behavior.
>
>Finally, the Merchandise entity represents retail items sold in stores, such as mugs or apparel. Merchandise is tied to specific store locations, so we included a one‑to‑many relationship between Store and Merchandise.
>
>Overall, this data model captures the complete operational flow of the global coffee chain—from customers placing orders, to inventory being supplied, to payments being processed—while maintaining a clear relational structure that supports meaningful business insights.
<img width="1282" height="1294" alt="image" src="https://github.com/user-attachments/assets/e211dfa2-dd6d-4671-a325-3721a2485ceb" />

## Data Dictionary
## Queries:
## Assumptions
- LoyaltyID is stored redundantly to preserve the customer’s loyalty tier at the time of the order/payment, since loyalty status can change over time.
