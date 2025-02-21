# IntelliSpot System

## Overview
The **IntelliSpot System** is a vehicle registration and detection platform designed to identify license plate numbers and verify registration with the **CarPlateDS** system. The system helps students and auxiliary police officers check registration statuses, impose fines on unregistered vehicles, and facilitate payments for registration and fines.

## Features
- **License Plate Detection:** Uses a CNN-based model for automatic plate recognition.
- **Vehicle Registration:** Students can register and renew their vehicle registration.
- **Compound Management:** Auxiliary police can issue fines to unregistered vehicles.
- **Online Payment Integration:** Supports **FPX payment gateway** for fee and fine transactions.
- **User Dashboard:** Separate dashboards for students and police officers.
- **Profile Management:** Users can update personal information and check registration status.

## System Requirements
- **Backend:** PHP (Laravel) with MySQL
- **Frontend:** HTML, CSS, JavaScript
- **Database:** MySQL (via XAMPP)
- **Web Server:** Apache (via XAMPP)

## Installation Guide
### Prerequisites
Ensure the following are installed:
- XAMPP (Apache, MySQL, PHP, and phpMyAdmin)
- Composer (PHP dependency manager)

### Steps to Install
1. **Download and Install XAMPP**
   - Download XAMPP from [Apache Friends](https://www.apachefriends.org/index.html).
   - Install and start **Apache** and **MySQL** from the XAMPP Control Panel.

2. **Clone the repository**
   ```sh
   git clone https://github.com/your-repo/intellispot.git
   cd intellispot
   ```

3. **Move the project folder to XAMPP's htdocs**
   - Copy the `intellispot` folder to `C:\xampp\htdocs\`.

4. **Set up the database**
   - Open phpMyAdmin by visiting `http://localhost/phpmyadmin/`.
   - Create a new database, e.g., `intellispot_db`.
   - Import the database schema:
     ```sh
     mysql -u root -p intellispot_db < database/schema.sql
     ```

5. **Configure Laravel environment**
   - Copy the `.env.example` file and rename it to `.env`.
   - Update the database credentials:
     ```env
     DB_CONNECTION=mysql
     DB_HOST=127.0.0.1
     DB_PORT=3306
     DB_DATABASE=intellispot_db
     DB_USERNAME=root
     DB_PASSWORD=
     ```
   - Run Laravel migrations:
     ```sh
     php artisan migrate
     ```

6. **Install PHP dependencies**
   ```sh
   composer install
   ```

7. **Start the Laravel application**
   ```sh
   php artisan serve
   ```
   The application will be available at `http://127.0.0.1:8000`.

## Usage Guide
- **Students:**
  - Log in using university credentials.
  - Register or renew vehicle plate.
  - Pay for registration and compound fines.
  - View and update personal details.
- **Police Officers:**
  - Log in using provided credentials.
  - Scan vehicle plate numbers and verify registration.
  - Issue compound fines for unregistered vehicles.
  - View and manage issued fines.

