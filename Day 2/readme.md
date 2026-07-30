# Salesforce Automation - Validation Rules & Record-Triggered Flow

## 📌 Overview

This project demonstrates Salesforce declarative automation by implementing **Validation Rules** and a **Record-Triggered Flow** for an E-Commerce application. The goal was to automate order processing while maintaining data integrity without writing Apex code.


## 🚀 Features

- Automatic Order Date population
- Email notification on new Order creation
- Data validation using Validation Rules
- Record-Triggered Flow automation
- Real-world E-Commerce business scenario

## 🛠️ Technologies Used

- Salesforce Lightning Platform
- Flow Builder
- Validation Rules
- Object Manager
- Developer Console

## 📂 Implementations

### ✅ Record-Triggered Flow

**Object:** `Order__c`

**Trigger:** Record Created

**Flow Actions:**
- Auto-populate `Order_Date__c`
- Send email notification to the administrator

### ✅ Validation Rules

Implemented the following business validations:

- Prevent future Order Dates
- Total Amount must be greater than zero
- Pending Orders cannot have zero amount
- Customer must be selected
- Maximum Order Amount limit


## 📚 Concepts Learned

- Validation Rules
- Record-Triggered Flow
- Before-Save vs After-Save Flow
- Update Records Element
- Send Email Action
- Salesforce Declarative Automation
- Business Process Automation

## 🎯 Outcome

Successfully automated the Order Management process using Salesforce's declarative tools while enforcing business rules through Validation Rules. This project strengthened my understanding of Salesforce automation and best practices.

