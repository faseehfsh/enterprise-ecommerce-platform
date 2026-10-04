# Project Overview
This system will provide customers with a secure platform for discovering products, managing shopping carts, placing orders, and tracking purchases. It will also provide administrators to manage products, inventory, customers, orders, and other aspects of the platform.

The project is intended to demonstrate professional software engineering practices, including modular architecture, secure authentication and authorization, RESTful APIs, database management, automated testing, containerization, monitoring, and scalable system design.

# Objectives
The platform will contain two primary areas:

1. Customer-facing application
2. Administration and management application

The system will support the complete e-commerce lifecycle:

Product Discovery
       ↓
Product Selection
       ↓
Shopping Cart
       ↓
Checkout
       ↓
Payment
       ↓
Order Processing
       ↓
Order Fulfillment
       ↓
Order Tracking

# Functional Requirements

1. User Registration and Authentication

### FR-01 — User Registration

The system shall allow new customers to create an account using required personal information and valid credentials.

### FR-02 — User Login

The system shall allow registered users to authenticate using their email address and password.

### FR-03 — Secure Password Storage

The system shall store user passwords using a secure one-way password hashing algorithm and shall never store passwords in plain text.

### FR-04 — Logout

The system shall allow authenticated users to securely log out of the system.

### FR-05 — Password Recovery

The system shall provide a mechanism for users to recover or reset forgotten passwords.

### FR-06 — Account Verification

The system shall support email/account verification where required.

### FR-07 — Session Management

The system shall manage authenticated user sessions securely.

2. User Profile Management

### FR-08 — View Profile

Users shall be able to view their profile information.

### FR-09 — Update Profile

Users shall be able to update permitted personal information.

### FR-10 — Address Management

Users shall be able to add, edit, remove, and select delivery addresses.

### FR-11 — Account Management

Users shall be able to manage their account settings.

3. Product Catalogue

### FR-12 — Product Listing

The system shall display available products to customers.

### FR-13 — Product Details

The system shall provide detailed information about individual products, including:
- Product name
- Description
- Price
- Images
- Category
- Availability
- Stock information
- Relevant attributes

### FR-14 — Product Categories

The system shall organize products into categories.

### FR-15 — Product Search

Customers shall be able to search for products using keywords.

### FR-16 — Product Filtering

Customers shall be able to filter products based on relevant attributes such as:
- Category
- Price range
- Availability
- Brand
- Product attributes

### FR-17 — Product Sorting

Customers shall be able to sort products according to supported criteria such as price, popularity, or newest products.

### FR-18 — Product Pagination

The system shall support pagination or an equivalent mechanism when displaying large product collections.

4. Shopping Cart

### FR-19 — Add to Cart

Authenticated customers shall be able to add available products to their shopping cart.

### FR-20 — View Cart

Customers shall be able to view the contents of their shopping cart.

### FR-21 — Update Cart Quantity

Customers shall be able to increase or decrease product quantities in their cart.

### FR-22 — Remove Cart Item

Customers shall be able to remove products from their cart.

### FR-23 — Cart Total

The system shall automatically calculate item subtotals and the total cart value.

### FR-24 — Stock Validation

The system shall validate product availability before allowing products to be added to or purchased from the cart.

5. Checkout

### FR-25 — Checkout

Customers shall be able to proceed from their shopping cart to checkout.

### FR-26 — Delivery Information

Customers shall be able to select or provide delivery information during checkout.

### FR-27 — Order Summary

The system shall display a complete order summary before order confirmation.

### FR-28 — Price Calculation

The system shall calculate the final order amount based on applicable:
- Product prices
- Quantities
- Discounts
- Taxes, where applicable
- Delivery charges

### FR-29 — Order Confirmation

The system shall require customers to confirm the order before it is submitted.

6. Payment

### FR-30 — Payment Processing

The system shall integrate with a supported payment provider to process customer payments.

### FR-31 — Payment Status

The system shall maintain the status of each payment.

Supported states may include:
- Pending
- Successful
- Failed
- Refunded

### FR-32 — Payment Failure Handling

The system shall handle failed payments without incorrectly creating a completed order.

### FR-33 — Payment Confirmation

The system shall associate successful payment information with the relevant order.

### FR-34 — Payment Security

The system shall not store sensitive payment credentials such as raw card numbers or CVV values.

7. Order Management

### FR-35 — Create Order

The system shall create an order after successful checkout and payment processing according to the defined business rules.

### FR-36 — Order Number

Each order shall have a unique order identifier.

### FR-37 — Order Details

Customers shall be able to view the details of their orders.

### FR-38 — Order History

Customers shall be able to view their previous orders.

### FR-39 — Order Status

The system shall maintain order statuses.

Example statuses include:
- PENDING
- CONFIRMED
- PROCESSING
- SHIPPED
- DELIVERED
- CANCELLED

### FR-40 — Order Tracking

Customers shall be able to view the current status of their orders.

### FR-41 — Order Cancellation

Customers shall be able to request or perform order cancellation where permitted by the business rules.

### FR-42 — Order Notifications

The system shall notify customers about important order status changes.

8. Inventory Management

### FR-43 — Stock Management

The system shall maintain the available stock quantity for each applicable product.

### FR-44 — Stock Update

Authorized administrators shall be able to update inventory quantities.

### FR-45 — Inventory Reservation

The system shall prevent the same inventory from being incorrectly allocated to multiple orders.

### FR-46 — Out-of-Stock Handling

The system shall prevent customers from purchasing unavailable products.

### FR-47 — Low Stock Monitoring

The system shall identify products whose stock falls below a configurable threshold.

9. Product Management

### FR-48 — Create Product

Authorized administrators shall be able to create products.

### FR-49 — Update Product

Authorized administrators shall be able to update product information.

### FR-50 — Delete/Deactivate Product

Authorized administrators shall be able to remove or deactivate products according to business rules.

### FR-51 — Product Image Management

Authorized administrators shall be able to manage product images.

### FR-52 — Product Category Management

Authorized administrators shall be able to create, update, and manage product categories.

10. Administration

### FR-53 — Admin Authentication

Administrators shall authenticate through a secure authentication mechanism.

### FR-54 — Role-Based Authorization

The system shall restrict administrative functionality according to the authenticated user's role and permissions.

### FR-55 — Admin Dashboard

The system shall provide administrators with a dashboard containing relevant business information.

The dashboard may include:
- Total orders
- Revenue
- Product count
- Customer count
- Low-stock products
- Pending orders

### FR-56 — Customer Management

Authorized administrators shall be able to view and manage customer accounts according to their permissions.

### FR-57 — Order Management

Authorized administrators shall be able to view and manage customer orders.

### FR-58 — Inventory Management

Authorized administrators shall be able to manage product inventory.



# Non-functional Requirement

1. Security
NFR-01 — Authentication Security

The system shall use secure authentication mechanisms for customer and administrative accounts.

NFR-02 — Password Security

Passwords shall be securely hashed using an industry-standard password hashing algorithm.

NFR-03 — Authorization

The system shall enforce role-based access control for protected resources.

NFR-04 — Data Protection

Sensitive user information shall be protected from unauthorized access.

NFR-05 — Secure Communication

Communication between clients and servers shall use HTTPS in production environments.

NFR-06 — Input Validation

The system shall validate and sanitize user-provided input to reduce security risks such as injection attacks.

NFR-07 — API Security

Protected APIs shall require appropriate authentication and authorization.

NFR-08 — Secret Management

Sensitive configuration values such as database credentials, API keys, and authentication secrets shall not be committed to source control.

NFR-09 — Payment Security

The application shall follow the security requirements of the selected payment provider and shall avoid storing sensitive payment credentials.

2. Performance
NFR-10 — API Response Time

Under normal operating conditions, commonly used API requests should respond within an acceptable target latency.

NFR-11 — Page Load Performance

Customer-facing pages should load efficiently and avoid unnecessary network requests.

NFR-12 — Database Performance

Database queries shall be designed and indexed appropriately to support expected application workloads.

NFR-13 — Search Performance

Product search and filtering should provide results within an acceptable response time under normal system load.

3. Scalability
NFR-14 — Horizontal Scalability

The application architecture should support running multiple backend instances when required.

NFR-15 — Database Scalability

The database design shall support growth in products, customers, orders, and transactional data.

NFR-16 — Stateless Backend

Where practical, backend services should remain stateless to facilitate horizontal scaling.

NFR-17 — Large Catalogue Support

The system shall be capable of handling a growing product catalogue without significant degradation in usability.

4. Availability and Reliability
NFR-18 — Availability

The production system should target high availability and minimize unnecessary downtime.

NFR-19 — Fault Handling

The system shall handle expected application and infrastructure failures gracefully.

NFR-20 — Transaction Integrity

Critical operations such as order creation, payment processing, and inventory updates shall maintain data consistency.

NFR-21 — Data Recovery

The system shall support database backup and recovery procedures.

NFR-22 — Failure Recovery

The system should recover from recoverable failures without corrupting transactional data.

5. Maintainability
NFR-23 — Modular Architecture

The application shall use a modular architecture that separates major business responsibilities.

NFR-24 — Separation of Concerns

The system shall separate presentation, business logic, data access, and infrastructure concerns.

NFR-25 — Code Quality

The source code shall follow consistent coding conventions and established best practices for the selected technologies.

NFR-26 — Documentation

Important APIs, architectural decisions, setup procedures, and development processes shall be documented.

NFR-27 — Configuration Management

Environment-specific configuration shall be separated from application source code.

6. Testability
NFR-28 — Automated Testing

The system shall include automated tests for important application functionality.

NFR-29 — Unit Testing

Core business logic shall be covered by unit tests.

NFR-30 — Integration Testing

Important interactions between application components shall be tested through integration tests.

NFR-31 — API Testing

Critical API endpoints shall have automated tests.

NFR-32 — Regression Testing

Automated tests shall help prevent previously implemented functionality from breaking during future development.

7. Usability
NFR-33 — Responsive Interface

The customer-facing application shall provide a usable interface across supported desktop, tablet, and mobile screen sizes.

NFR-34 — Consistent UI

The application shall maintain consistent navigation, terminology, layouts, and interaction patterns.

NFR-35 — Error Feedback

The system shall provide understandable feedback when user operations fail.

NFR-36 — Accessibility

The user interface should follow appropriate web accessibility practices.

8. Observability and Monitoring
NFR-37 — Application Logging

The backend shall maintain structured logs for important application events and errors.

NFR-38 — Error Monitoring

The system should provide mechanisms for identifying and investigating application errors.

NFR-39 — Health Checks

Backend services shall provide health-check mechanisms for monitoring service availability.

NFR-40 — Operational Metrics

The system should expose relevant operational metrics such as request rates, response times, error rates, and resource utilization.

9. Deployment
NFR-41 — Containerization

The application should support containerized deployment using Docker.

NFR-42 — Environment Separation

The system should support separate development, testing, and production environments.

NFR-43 — CI/CD

The project should use a CI/CD pipeline to automate appropriate stages of building, testing, and deployment.

NFR-44 — Deployment Configuration

Deployment configuration shall be version-controlled where appropriate, excluding sensitive credentials.

10. Data Integrity and Consistency
NFR-45 — Referential Integrity

The database shall maintain appropriate relationships and referential integrity between related entities.

NFR-46 — Transaction Management

Critical multi-step database operations shall use appropriate transaction management.

NFR-47 — Duplicate Prevention

The system shall prevent duplicate records or duplicate processing where business rules require uniqueness.

NFR-48 — Concurrency Handling

The system shall handle concurrent operations appropriately, particularly for inventory and order processing.

11. Privacy
NFR-49 — Personal Data Protection

The system shall protect customer personal information from unauthorized access or disclosure.

NFR-50 — Data Minimization

The system should collect only personal information necessary for providing the required functionality.

NFR-51 — Data Access Control

Access to personal information shall be restricted according to user roles and business requirements.

NFR-52 — Sensitive Data Handling

Sensitive data shall not be unnecessarily exposed through API responses, logs, error messages, or client-side storage.


# Future Features

10. More User Roles
The system shall support multiple user and administrative roles where required.
Eg. Seller role,
SUPER_ADMIN	role with elevated administrative privileges

11. Promotions and Discounts
FR-60 — Discount Management

Authorized administrators shall be able to create and manage discounts.

FR-61 — Discount Application

The system shall apply valid discounts to eligible orders.

FR-62 — Discount Validation

The system shall validate discount conditions before applying a discount.

FR-63 — Discount Expiration

The system shall prevent expired discounts from being used.

12. Notifications
FR-64 — Customer Notifications

The system shall provide notifications for important customer events.

Examples include:
Account verification
Password reset
Order confirmation
Payment confirmation
Order status changes

FR-65 — Email Notifications

The system shall support email notifications for configured events.

13. Reviews and Ratings
FR-66 — Product Reviews

Authenticated customers shall be able to submit reviews for eligible products.

FR-67 — Product Ratings

Customers shall be able to provide ratings for eligible products.

FR-68 — Review Management

Authorized administrators shall be able to moderate reviews according to defined business rules.

14. Audit and Administration History
FR-69 — Audit Logging

The system shall record important administrative actions.

Examples include:
Product creation
Product modification
Product deletion/deactivation
Inventory changes
Order status changes
User account changes
FR-70 — Audit Log Access

Authorized administrators shall be able to view relevant audit records.

15. Reporting
FR-71 — Sales Reporting

The system shall provide authorized administrators with sales information.

FR-72 — Order Reporting

The system shall provide information about order volumes and statuses.

FR-73 — Inventory Reporting

The system shall provide information about inventory levels and low-stock products.

## More advanced future features:
Product recommendations
AI-powered product search
Personalized recommendations
Wishlist functionality
Coupon campaigns
Loyalty/reward system
Multiple payment providers
Multiple currencies
Multi-language support
Advanced analytics
Customer support/chat functionality
Event-driven order processing
Distributed caching
Search engine integration
Advanced fraud detection
Microservices decomposition where justified by system requirements

