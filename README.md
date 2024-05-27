# 🏦 JDBC Banking System Project


## Overview
This project implements a console-based banking system using Java and JDBC (Java Database Connectivity) technology. Users can perform various banking operations such as user registration, account creation, fund transfers, balance inquiries, and more.
## Features
1. **User Registration & Login**
   - **Create**: Users can register with their full name, email, and password.
   - **Read**: Registered users can log in using their email and password credentials.
   - **Update**: Users can update their profile information such as full name, email, or password.
   - **Delete**: Users can request to delete their account, which may involve marking the account as inactive or anonymizing personal information.

2. **Account Creation**
   - **Create**: Registered users can open new bank accounts by providing their full name, initial balance, and security PIN.

3. **Debit and Credit Transactions**
   - **Update**: Account holders can perform debit and credit transactions by specifying the amount and security PIN. The balance is updated accordingly.

4. **Money Transfer Between Accounts**
   - **Update**: Users can transfer money between their accounts or to other accounts by providing the recipient's account number, amount, and security PIN.

5. **Balance Inquiry**
   - **Read**: Account holders can check their account balance by entering their security PIN.

6. **Robust Security Measures**
   - The system ensures security by verifying the user's security PIN before allowing transactions or inquiries.


## Technologies Used
- **Java**: The core programming language used for implementing the banking system's logic.
- **JDBC (Java Database Connectivity)**: Used to interact with the MySQL database, including executing SQL queries and managing database connections.
- **MySQL**: Chosen database system for storing user and account information, providing persistence for the banking system data.

## Database Tables
1. **"accounts"**
    **Fields**:
     - `account_number` (Primary Key): Unique identifier for each account.
     - `full_name`: Full name of the account holder.
     - `email`: Email address associated with the account.
     - `balance`: Current balance in the account.
     - `security_pin`: Security PIN for account authentication.

2. **"user"**
    **Fields**:
     - `full_name`: Full name of the user.
     - `email` (Primary Key): Unique email address serving as the user's identifier.
     - `password`: Password for user authentication.

     Tables screenshort
   ![Screenshot 2024-04-22 005831](https://github.com/shreyabhuwania/Java_Banking_System/assets/95756422/66e8fa88-2e52-46c0-91ae-be6dab13cbb9)

## Usage
1. Clone the repository.
```bash
git clone https://github.com/YourUsername/YourBankingSystemRepo.git
```
2. Configure the database connection in the project files.
   ```
    1.Open the project files.
    2.Locate the database configuration section.
    3.Update the database URL, username, and password to match your MySQL database configuration.
    ```
3. Compile and run the project to start the banking system.
 ```
 cd banking_system
javac *.java  # Compile all Java files
java BankingApp  # Run the main class
```
4. Interact with the System:
    ```
    Welcome to the Banking System!

    'Menu:
    1. Register
    2. Login
    3. Exit

    Please enter your choice:

    Enter the corresponding number to select the desired operation and follow the on-screen instructions.
    ```



## Future Improvements

- **Transaction History Tracking**: Implement a feature to record transaction history for each account, allowing users to view their past transactions.
- **Account Locking Mechanism**: Enhance security by implementing an account locking mechanism after multiple failed login attempts.
- **Multi-factor Authentication (MFA)**: Integrate multi-factor authentication options such as SMS-based OTP (One-Time Password) or biometric authentication for added security.
- **Improved Error Handling**: Enhance error handling mechanisms to provide informative error messages to users in case of failures or invalid inputs.
- **User Interface Enhancement**: Develop a graphical user interface (GUI) to provide a more intuitive and user-friendly experience for customers.
