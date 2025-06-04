# E-Commerce-project
Overview
This is a Java Spring Boot e-commerce application that provides a platform for merchants to sell products and customers to purchase them. The application includes features like user authentication, product management, shopping cart functionality, and payment processing through RazorPay integration.

Project Structure
src/
├── main/
│   ├── java/
│   │   └── com/
│   │       └── jsp/
│   │           └── ecommerce/
│   │               ├── entity/
│   │               │   ├── Customer.java
│   │               │   ├── Merchant.java
│   │               │   ├── Payment.java
│   │               │   └── Product.java
│   │               ├── helper/
│   │               │   └── RazorPayHelper.java
│   │               ├── controller/
│   │               ├── repository/
│   │               ├── service/
│   │               └── dto/
│   └── resources/
│       ├── application.properties
│       ├── static/
│       └── templates/
└── test/

Features:
  1.User Management: Registration and authentication for customers and merchants
  2.Product Management: CRUD operations for products
  3.Order Processing: Shopping cart and order management
  4.Payment Integration: Secure payment processing with RazorPay

Technology Stack:
  1.Java
  2.Spring Boot
  3.Spring Data JPA
  4.Hibernate
  5.RazorPay API
  6.MySQL/PostgreSQL (database)

Entity Details:
  1.Customer: Stores user information with creation timestamp
  2.Merchant: Stores seller information with creation timestamp
  3.Product: Contains product details with update timestamp
  4.Payment: Tracks payment information with creation timestamp

Payment Integration:
The application integrates with RazorPay for payment processing. The RazorPayHelper class handles the creation of payment orders:
    public String createPayment(double amount) {
    // Creates a payment order with RazorPay
    // Returns the order ID for client-side processing
    }

Setup and Installation:
1. Clone the repository:
       git clone https://github.com/yourusername/ecommerce-app.git
2. Configure database settings in application.properties
3. Set up RazorPay API keys in application.properties
4. Build the project
      mvn clean install
5. Run the application
      mvn spring-boot:run
   
API Documentation:
The application exposes RESTful APIs for various operations:
  1.User registration and authentication
  2.Product listing and management
  3.Cart operations
  4.Order processing
  5.Payment handling
