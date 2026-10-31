# RIDEFORGE — Project Requirements

## 1. Project Overview
Build a professional motorcycle accessories shop website with an admin panel and an internal billing application.

## 2. Business Problem
Describe how the shop currently displays products, manages inventory and prepares customer bills. Identify the problems the software should solve.

## 3. Project Users
- Public customer
- Shop administrator
- Billing staff (confirm whether this is a separate role)

## 4. Functional Requirements
### Customer Website
- Browse products and categories
- Search, filter and sort products
- View product details
- Find shop location and contact information

### Admin Panel
- Secure login
- Add, edit and manage products
- Manage prices, descriptions, images and stock

### Billing Application
- Search and select products
- Enter quantities
- Calculate subtotal, tax and discount
- Generate and print invoices
- Save finalized bills
- Update inventory according to confirmed business rules

## 5. Non-Functional Requirements
- Responsive user interface
- Secure authentication and authorization
- Reliable calculations and inventory updates
- Maintainable code
- Appropriate performance and error handling
- Backups and production logging

## 6. Out of Scope for Phase 1
- Customer login
- Online shopping cart and checkout
- Online payment gateway

## 7. Open Questions for the Client
- What are the required tax and invoice fields?
- Should stock decrease when a bill is finalized?
- How should cancelled bills and returns affect stock?
- Are discounts permitted? Who can authorize them?
- Are there different admin and billing staff permissions?
- What are the shop's actual name, address, hours and contact details?

## 8. Acceptance Criteria
Define how we will test each feature and decide whether it meets the client's requirements.

## 9. Functional Requirements

| ID | Requirement | Priority |
|---|---|---|
| FR-01 | Customers can browse the product catalogue. | Must |
| FR-02 | Customers can search and filter products. | Must |
| FR-03 | Customers can view product details. | Must |
| FR-04 | Administrators can securely sign in. | Must |
| FR-05 | Authorized administrators can create, edit and manage products. | Must |
| FR-06 | Billing staff can search for products and enter quantities. | Must |
| FR-07 | The system calculates invoice totals using confirmed tax and discount rules. | Must |
| FR-08 | The system saves finalized bills and supports invoice printing. | Must |
| FR-09 | Finalized bills update stock according to approved rules. | Must |
| FR-10 | Customers can view the shop's contact details and directions. | Must |

## 10. Non-Functional Requirements

| ID | Requirement | Acceptance Method |
|---|---|---|
| NFR-01 | The interface supports agreed mobile, tablet and desktop sizes. | Responsive UI testing |
| NFR-02 | Admin operations require server-side authorization. | API security tests |
| NFR-03 | Invoice calculations use precise monetary values and approved rounding rules. | Unit tests |
| NFR-04 | Finalizing a bill and updating stock are handled consistently. | Integration and concurrency tests |
| NFR-05 | Secrets are stored in environment configuration, not committed to Git. | Repository and configuration review |
| NFR-06 | Production errors are logged without exposing passwords or sensitive data. | Logging and security tests |
| NFR-07 | Performance targets are agreed upon and measured under a defined workload. | Performance testing |

## 11. Business Rules Requiring Client Confirmation

- Tax registration details and invoice fields
- Tax rates, inclusive/exclusive pricing and rounding
- Invoice numbering format
- Discounts and who can approve them
- Stock deduction and restoration rules
- Returns, cancellations and correction records
- Roles and permissions for administrators and billing staff
- Whether product variants such as helmet size or colour require separate stock records
