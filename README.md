# Car Rental System

A Java Swing application for managing a car rental business. This system allows for car inventory management, customer management, and rental operations.

## Features

- **User Authentication**: Secure login system with role-based access control
- **Car Management**: Add, edit, and delete cars in the inventory
- **Customer Management**: Manage customer information and history
- **Rental Operations**: Create, edit, complete, and cancel rental transactions
- **Dashboard**: Overview of key business metrics

## Requirements

- Java Development Kit (JDK) 8 or higher
- MySQL Database Server 5.7 or higher
- MySQL Connector/J (JDBC driver)

## Setup Instructions

### 1. Database Setup

1. Install MySQL if not already installed
2. Create a new database:
   ```sql
   CREATE DATABASE car_rental_system;
   ```
3. Run the SQL script in `database/car_rental_db.sql` to create the tables and sample data:
   ```
   mysql -u root -p car_rental_system < database/car_rental_db.sql
   ```

### 2. JDBC Driver Setup

1. Download the MySQL Connector/J JDBC driver from the [MySQL website](https://dev.mysql.com/downloads/connector/j/)
2. Place the JAR file in the `lib` directory of the project

### 3. Configure Database Connection

1. Open `src/main/java/com/carrentalsystem/util/DatabaseConnection.java`
2. Update the database connection parameters if needed:
   ```java
   private static final String URL = "jdbc:mysql://localhost:3306/car_rental_system";
   private static final String USER = "root";
   private static final String PASSWORD = "your_password"; // Update this
   ```

## Running the Application

1. Compile the project:
   ```
   javac -cp "lib/*" -d bin src/main/java/com/carrentalsystem/**/*.java
   ```
2. Run the application:
   ```
   java -cp "bin;lib/*" com.carrentalsystem.ui.LoginScreen
   ```

## Default Login Credentials

- **Admin User**:
  - Username: admin
  - Password: admin123

- **Staff User**:
  - Username: staff
  - Password: staff123

## Project Structure

- `src/main/java/com/carrentalsystem/model/` - Model classes
- `src/main/java/com/carrentalsystem/dao/` - Data Access Objects
- `src/main/java/com/carrentalsystem/ui/` - User Interface components
- `src/main/java/com/carrentalsystem/util/` - Utility classes
- `database/` - Database scripts
- `lib/` - External libraries

## Screenshots

(Add screenshots of your application here)

## License

This project is licensed under the MIT License - see the LICENSE file for details.

