 SHEIN Database Project
 -------------------------

This project is aimed at creating a robust database for SHEIN, an online retail platform that offers products such as shoes, clothes, bags, and accessories for both men and women, as well as a children's and home section. The purpose of this database is to enhance data management and improve support for SHEIN's retail operations, including order tracking, product management, and customer interactions.

## Project Overview

### Project Name: SHEIN Database
### Course: IT222 - Database Principles (2nd Semester 1444 H)
### Instructor: Dr. Luluh Aldhubayi
### TA: Abeer Aldrees

 Team Members
 -----------------
- Najla Alajaleen (ID: 442202197)
- Hadeel Alsaleh (ID: 441201424)
- Noura Alaskar (ID: 442202216)
- Taif Alrubeaan (ID: 442202301)
- Shahad Aldhawyan (ID: 442204761)

 Project Description
-------------------------
SHEIN is a well-known e-commerce platform that deals with a variety of fashion products and accessories. This project focuses on building a comprehensive database to support SHEIN’s operations, with a particular focus on the following:

- Customers: Manage customer data including names, contact information, and order history.
- Products: Maintain a catalog of products such as shoes, clothes, and accessories, including product details like name, price, and color.
- Orders: Store and manage orders placed by customers, including tracking order status and shipment details.
- Categories: Organize products into categories such as men’s, women’s, and children’s sections.
- Shipping: Manage shipping company details and link orders with the corresponding shipping companies.

 Database Structure
-----------------------
The project implements an enhanced entity-relationship (EER) model to design and structure the database. The following entities and their relationships are part of the system:

Key Entities:
--------------------
- Customer: Stores customer details like name, email, phone number, and address.
- Product: Represents the items available for sale, including attributes such as product number, name, price, color, and state (available/unavailable).
- Order: Records customer orders with details like order ID, date, total price, quantity, and tracking information.
- Category: Represents the categories products belong to (e.g., men’s clothes, women’s clothes).
- ShippingCompany: Contains details of companies responsible for shipping orders.
  
Relationships:
-------------------
- Place: Links customers to the orders they place.
- Has: Represents the products contained in each order.
- Shipped: Links orders with the shipping companies that handle the delivery.
- Belongs: Associates products with their respective categories.

Functional Requirements
------------------------
### Data Entry
- Enter customer’s email and name.

### Data Updates/Deletion
- Update customer information.
- Update order information (e.g., add or delete products).
- Update shipping information.

### Queries
- Search products by price range.
- Search for products by name, color, or product number.
- Display order tracking state.
- List all orders for a particular customer.
- Display products by category (e.g., women’s clothes).
- Display all customer details.

 Database Schema
--------------------

### Tables and Attributes:
- Customer (Email, Fname, Lname, Password, PhoneNo, Address)
- Product (ProductNo, PName, Price, PState, PColor)
- Order (OrderID, OrderDate, Quantity, Email)
- ShippingCompany (ShippingID, CompanyName)
- Category (Cname, Photo)
- Belongs (ProductNo, Cname)
- Shipped (OrderID, ShippingID, TrackingNo, State)

## Example Data Queries

- Search for products in a price range:
   SELECT * FROM Product WHERE Price BETWEEN 50 AND 100;
  
- List all orders for a specific customer:
   SELECT * FROM Order WHERE Email = 'customer_email@example.com';
  
- Display women's clothes:
   SELECT * FROM Product JOIN Belongs ON Product.ProductNo = Belongs.ProductNo WHERE Belongs.Cname = 'Women';
  

