# PhastSub Data Purchase System

A PHP-based VTU/Data Subscription platform that enables users to purchase data bundles using their wallet balance.

## Features

- User Login System
- Wallet Balance Management
- Data Plan Selection
- Automated Balance Deduction
- Transaction History Storage
- API Integration for Data Purchase
- MySQL Database Support
- Responsive Interface

## Technologies Used

- PHP
- MySQL
- HTML5
- CSS3
- JavaScript
- SweetAlert2
- cURL API Integration

## Project Structure

```
project/
│
├── assets/
│   ├── header.php
│   ├── footer.php
│   └── scripts/
│
├── db.php
├── buy-data.php
├── login.php
├── dashboard.php
│
└── README.md
```

## Database Tables

### users

| Column | Type |
|----------|----------|
| Id | INT |
| Username | VARCHAR |
| Password | VARCHAR |
| Phone | VARCHAR |
| Balance | DECIMAL |

### data_plan

| Column | Type |
|----------|----------|
| Data_ID | INT |
| Network | VARCHAR |
| Plan_type | VARCHAR |
| Amount | DECIMAL |
| Size | VARCHAR |
| Validity | VARCHAR |

### user_data

| Column | Type |
|----------|----------|
| Id | INT |
| Plan_id | INT |
| Network | VARCHAR |
| Phone | VARCHAR |
| User_phone | VARCHAR |
| Amount | DECIMAL |
| Paid_amount | DECIMAL |
| Username | VARCHAR |
| Time | TIMESTAMP |

## Installation

1. Clone repository

```bash
git clone https://github.com/yourusername/phastsub.git
```

2. Import database

```sql
CREATE DATABASE phastsub;
```

Import all SQL tables.

3. Configure database connection

Edit:

```php
db.php
```

```php
$servername = "localhost";
$username = "root";
$password = "";
$dbname = "phastsub";
```

4. Start server

Using XAMPP:

```bash
http://localhost/phastsub
```

## API Configuration

Locate:

```php
$token = "****APIKEY";
```

Replace with your provider's API token.

## Security Notes

- Use password hashing
- Validate all form inputs
- Protect against SQL Injection
- Use HTTPS in production
- Hide API tokens in environment variables

## License

MIT License

## Author

Developed by Your Name
