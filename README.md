# real-time-currency-exchanger-using-java
Here’s a `README.md` template for your `CurrencyConverter2` project that you can use when uploading to GitHub:

```markdown
# Currency Converter 2

## Overview
**CurrencyConverter2** is a real-time currency exchange calculator that allows users to convert between various global currencies. The application includes fees for foreign transactions and currency conversions, and it stores the conversion data in a MySQL database. It is built using Java Swing for the user interface, with live data fetched from the Exchange Rate API.

## Features
- Converts between numerous currencies (over 100 available).
- Calculates and displays foreign transaction fees (2%) and currency conversion fees (1%).
- Displays a final amount after deducting fees.
- Stores each conversion transaction into a MySQL database with detailed information about the original amount, converted amount, and fees.

## Requirements
- Java JDK 8 or higher
- MySQL database server
- Internet connection for fetching real-time exchange rates from [Exchange Rate API](https://www.exchangerate-api.com/)

## Technologies Used
- Java Swing for the GUI
- MySQL for storing conversion data
- REST API integration using `HttpURLConnection` for fetching exchange rates
- JDBC for database connectivity

## Setup Instructions

### 1. Clone the Repository
```bash
git clone https://github.com/omraje2424/CurrencyConverter2.git
```

### 2. Database Setup
Create a MySQL database and a table for storing conversion data:
```sql
CREATE DATABASE currency_converter1;

USE currency_converter1;

CREATE TABLE conversions1 (
  id INT AUTO_INCREMENT PRIMARY KEY,
  amount DOUBLE NOT NULL,
  from_currency VARCHAR(10) NOT NULL,
  to_currency VARCHAR(10) NOT NULL,
  converted_amount DOUBLE NOT NULL,
  foreign_transaction_fee DOUBLE NOT NULL,
  conversion_fee DOUBLE NOT NULL,
  total_fees DOUBLE NOT NULL,
  final_amount DOUBLE NOT NULL,
  conversion_date TIMESTAMP DEFAULT CURRENT_TIMESTAMP
);
```

### 3. Update Database Configuration
In the `CurrencyConverter2` class, update the following credentials for your MySQL database:
```java
String url = "jdbc:mysql://localhost:3306/currency_converter1";
String user = "root";
String password = "Morya@123";  // Replace with your MySQL password
```

### 4. Run the Application
Compile and run the Java program from your IDE or using the command line:
```bash
javac CurrencyConverter2.java
java CurrencyConverter2
```

## How to Use
1. Enter the amount you want to convert.
2. Select the source currency ("From Currency") and the target currency ("To Currency").
3. Click the **Convert** button.
4. The application will display the converted amount, along with the fees and the final amount after deductions.
5. Conversion data will be stored in the MySQL database.

## Example Screenshot
![image](https://github.com/user-attachments/assets/a8b15b12-d8d7-4736-9588-e1b48306db7d)

![image](https://github.com/user-attachments/assets/4d1687bd-3e97-48f0-9346-72c0c977b5ec)

![image](https://github.com/user-attachments/assets/1aaf3c34-4c1a-4ce9-b2d9-e05688ed71bc)

![image](https://github.com/user-attachments/assets/57570f34-4b55-4ebc-8b7e-37a84bee9497)

![image](https://github.com/user-attachments/assets/9208d0fb-21a2-4504-bae1-b1267f3c1072)

![image](https://github.com/user-attachments/assets/4469bc86-57f8-4ea5-88a7-e1f0a21cedbf)






## Future Improvements
- Add a currency chart to display historical exchange rates.
- Allow saving favorite currency pairs for quicker conversions.
- Implement error handling for API requests and database operations.



---

### Contributing
Pull requests are welcome. For major changes, please open an issue first to discuss what you would like to change.

For any inquiries or suggestions, feel free to contact me at your-omrajeshinde2424@gmail.com
```

