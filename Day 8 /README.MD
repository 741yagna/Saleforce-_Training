# Sprint-09-LWC

# Salesforce E-Commerce Application

A Salesforce Lightning Web Components (LWC) based e-commerce application developed as part of Sprint 09.

The application retrieves product information from Salesforce using Apex and displays the products through reusable Lightning Web Components. It also demonstrates product details, cart management, component communication, and proper handling of different UI states.

---

## 📌 Project Overview

The application follows an e-commerce scenario where products are stored in Salesforce.

Users can:

- View available products
- View product details
- Add products to the cart
- Increase product quantity
- Decrease product quantity
- Remove products from the cart
- Handle products that are unavailable
- Receive appropriate feedback while data is loading or when an error occurs

The project is implemented using a reusable and component-based LWC architecture.

---

# 🎯 Objectives

The main objectives of this sprint are:

- Build reusable Lightning Web Components
- Connect LWC with Apex
- Retrieve Salesforce data using SOQL
- Implement parent-child component communication
- Implement Custom Events
- Build a basic shopping cart
- Handle different UI states
- Separate data retrieval logic using a service layer
- Deploy and test the application using VS Code and Salesforce

---

# 🛒 E-Commerce Scenario

The application uses a Salesforce `Product__c` object to store product information.

### Product Information

| Field | Purpose |
|---|---|
| `Product_Name__c` | Product name |
| `Price__c` | Product price |
| `Stock_Quantity__c` | Available stock |
| `Available__c` | Product availability |

Only products satisfying the following conditions are displayed:

```text
Available__c = true
Stock_Quantity__c > 0


# ARCHITECTURE

                         SALESFORCE
                             │
                             ▼
                       Product__c
                             │
                             ▼
                    ┌─────────────────┐
                    │ ProductService  │
                    │     Apex        │
                    └────────┬────────┘
                             │
                             ▼
                    ┌─────────────────┐
                    │ProductController│
                    │      Apex       │
                    └────────┬────────┘
                             │
                             ▼
                       @wire / LWC
                             │
                             ▼
                    ┌─────────────────┐
                    │   ProductList   │
                    │      LWC        │
                    └────────┬────────┘
                             │
                  ┌──────────┴──────────┐
                  │                     │
                  ▼                     ▼
          ┌──────────────┐       ┌──────────────┐
          │ Product Card │       │ Shopping Cart│
          │     LWC      │       │     Logic    │
          └──────┬───────┘       └──────────────┘
                 │
          ┌──────┴───────┐
          │              │
          ▼              ▼
    View Details     Add to Cart

## DATA FLOW ##

Product__c
     │
     ▼
SOQL Query
     │
     ▼
ProductService.cls
     │
     ▼
ProductController.cls
     │
     ▼
@wire
     │
     ▼
ProductList.js
     │
     ▼
ProductList.html
     │
     ▼
ProductCard
     │
     ├───────────────► View Details
     │
     └───────────────► Add to Cart
