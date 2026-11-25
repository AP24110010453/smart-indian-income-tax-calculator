# Smart Indian Income Tax Calculator

A Java 17 Swing desktop application for registering taxpayers, estimating tax under India’s old and new tax regimes, comparing results, and exporting PDF or CSV summaries. This project was submitted for Advanced Java Programming (CSE 309) at SRM University–AP.

## Features

- Manage and search taxpayer records
- Estimate tax for supported ordinary slab income under both regimes
- Compare regime results and save calculation history
- Export tax summaries as PDF or CSV
- Validate PAN format, email, mobile number, age, and nonnegative inputs

## Technology

- Java 17, Swing, and FlatLaf
- Maven
- MySQL 8 with JDBC
- OpenPDF and JUnit 5

## Requirements

- JDK 17 or later
- MySQL 8.x

## Setup and run

1. Initialize the database from the project folder:

   ```powershell
   Get-Content -Raw database/schema.sql | mysql -u root -p
   ```

2. Set your MySQL connection values in PowerShell:

   ```powershell
   $env:DB_URL = 'jdbc:mysql://localhost:3306/smart_income_tax_db?serverTimezone=Asia/Kolkata'
   $env:DB_USER = 'root'
   $env:DB_PASSWORD = 'your-MySQL-password'
   ```

3. Run tests and launch the application:

   ```powershell
   .\mvnw.cmd test
   .\mvnw.cmd exec:java
   ```

The Maven Wrapper downloads Maven the first time it runs. Taxpayer storage and calculation history require MySQL to be running with the schema initialized.

## Project files

- [Project report](REPORTJAVA.pdf)
- [Demo video](javavideo.mp4)
- [Clean source archive](Smart%20Indian%20Income%20Tax%20Calculator-clean.zip)

## Scope notes

The application provides educational estimates, not tax-filing advice. The current calculator supports ordinary slab income for Tax Year 2026–27 and does not handle capital gains or taxable income above ₹50 lakh. Deduction eligibility is simplified; check current official guidance before relying on an estimate.
