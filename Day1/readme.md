# Salesforce Developer Bridge Program - Day 1

## Project Title
**E-Commerce Management System**

## Objective
The objective of today's work was to design and build the data model for an E-Commerce Management System in Salesforce using both standard and custom objects. The work was completed in a Trailhead Playground as part of the Salesforce Developer Bridge Program.

---

# Standard Objects Used

## 1. Account
Represents the Customer.

## 2. Contact
Stores customer contact details.

---

# Custom Objects Created

1. Category
2. Product
3. Order
4. Order Item
5. Payment
6. Shipment

---

# Data Model

## Category
Stores different product categories.

### Fields
- Category Name (Record Name - Text)
- Category Description (Long Text Area)

---

## Product
Stores all products available in the application.

### Fields
- Product ID (Auto Number)
- Product Name (Record Name)
- Price (Currency)
- Stock Quantity (Number)
- Description (Long Text Area)
- Brand (Text)
- Category (Master-Detail Relationship)

---

## Order
Stores customer order information.

### Fields
- Order Number (Auto Number)
- Order Date (Date)
- Total Amount (Currency)
- Status (Picklist)
- Customer (Lookup - Account)

### Status Values
- Pending
- Packed
- Shipped
- Delivered
- Cancelled

---

## Order Item
Stores products included in each order.

### Fields
- Quantity (Number)
- Unit Price (Currency)
- Total Price (Formula)
- Order (Master-Detail Relationship)
- Product (Lookup Relationship)

---

## Payment
Stores payment details for customer orders.

### Fields
- Payment Method (Picklist)
- Payment Status (Picklist)
- Payment Date (Date)
- Transaction ID (Text)
- Order (Lookup Relationship)

### Payment Methods
- UPI
- Credit Card
- Debit Card
- Net Banking
- Cash on Delivery
- Wallet

### Payment Status
- Pending
- Completed
- Failed
- Refunded

---

## Shipment
Stores shipment and delivery details.

### Fields
- Courier Partner (Picklist)
- Tracking Number (Text)
- Delivery Status (Picklist)
- Estimated Delivery Date (Date)
- Order (Lookup Relationship)

### Courier Partners
- Blue Dart
- Delhivery
- DTDC
- Ekart
- Amazon Logistics

### Delivery Status
- Processing
- Out for Delivery
- Delivered
- Returned
- Cancelled

---

# Relationships

- Category → Product (Master-Detail)
- Account → Order (Lookup)
- Order → Order Item (Master-Detail)
- Product → Order Item (Lookup)
- Order → Payment (Lookup)
- Order → Shipment (Lookup)

---

# Work Completed Today

- Understood the business requirements for an E-Commerce Management System.
- Identified standard and custom objects.
- Designed the complete data model.
- Finalized fields for every custom object.
- Planned relationship types (Master-Detail and Lookup).
- Started creating custom objects in the Trailhead Playground.
- Configured Auto Number fields for Product ID and Order Number.
- Created the Product object and added its fields.
- Created the relationship between Category and Product.

---

# Learning Outcomes

- Learned the difference between Standard and Custom Objects.
- Understood when to use Lookup and Master-Detail relationships.
- Learned to create custom fields with appropriate data types.
- Gained experience configuring Auto Number, Currency, Number, Text, Long Text Area, Picklist, and Relationship fields.
- Improved understanding of Salesforce Object Manager and data modeling.

---

# Next Steps

- Complete the remaining custom objects.
- Create all relationship fields.
- Insert sample records.
- Write SOQL queries.
- Develop Apex Trigger and Handler Class.
- Build Lightning Web Component (LWC).
- Test the application and prepare screenshots for submission.

---

## Tools Used

- Salesforce Trailhead Playground
- Salesforce Object Manager
- Salesforce Setup
