# Script-Controlled ACL – Restrict Record Access Based on Field Value

## 📌 Project Overview

This project demonstrates a Script-Controlled Access Control List (ACL) in ServiceNow.

The ACL restricts record access based on a specific field value. The system checks the field value and dynamically decides whether the user is allowed to access the record.

## 🎯 Objective

- Implement a Script-Controlled ACL in ServiceNow.
- Restrict record access based on field values.
- Dynamically validate user access using JavaScript.
- Prevent unauthorized access to records.
- Test the ACL using a ServiceNow user.

## 🛠️ Technologies Used

- ServiceNow
- Access Control List (ACL)
- JavaScript
- ServiceNow Scripting
- sys_user table

## 👤 Test User

The project uses the following ServiceNow user for testing:

| Field | Value |
|---|---|
| User ID | EEE User |
| First Name | EEE |
| Last Name | User |
| Identity Type | Human |
| Active | True |
| Email | eeeuser@gmail.com |
| Locked Out | False |

The uploaded ServiceNow User Details report confirms that **EEE User** is active and is a Human identity. :contentReference[oaicite:0]{index=0}

## 🔐 User Role and Group

The user has an active:

`snc_required_script_writer_permission`

role and is a member of:

`Conditional Script Writer`

These details are present in the ServiceNow User Details report. :contentReference[oaicite:1]{index=1}

## ⚙️ How It Works

```text
User requests a record
        ↓
ServiceNow checks ACL
        ↓
ACL Script executes
        ↓
Required field value is checked
        ↓
Condition satisfied?
      /       \
    YES        NO
     ↓          ↓
  ALLOW       DENY
  ACCESS      ACCESS
