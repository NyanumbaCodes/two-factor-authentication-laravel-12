# Laravel 12 Two-Factor Authentication (2FA)

## 📌 Introduction
This repository demonstrates how to implement **Two-Factor Authentication (2FA) in Laravel 12** using **Laravel Fortify**. Two-Factor Authentication adds an extra layer of security to your application, requiring users to verify their identity with an authentication code.

## 🎯 Features
- **User Authentication with Fortify**
- **Enabling & Verifying 2FA**
- **Generating and Using Recovery Codes**
- **Integration with TOTP Apps (Google Authenticator, Authy, etc.)**

## 🚀 Installation
Follow these steps to set up the project:

### 1️⃣ Clone the Repository
```bash
git clone https://github.com/yourusername/laravel-12-2fa.git
cd laravel-12-2fa
```

### 2️⃣ Install Dependencies
```bash
composer install
npm install && npm run build
```

### 3️⃣ Set Up Environment File
Copy the `.env.example` file and update database credentials:
```bash
cp .env.example .env
```
Edit `.env` and configure your **database settings**:
```ini
DB_DATABASE=your_database_name
DB_USERNAME=your_database_user
DB_PASSWORD=your_database_password
```

### 4️⃣ Generate Application Key
```bash
php artisan key:generate
```

### 5️⃣ Run Migrations & Seed Database
```bash
php artisan migrate --seed
```

### 6️⃣ Configure Laravel Fortify
Fortify is already installed and set up in this project. Ensure the `config/fortify.php` file contains the necessary configurations for **two-factor authentication**.

### 7️⃣ Start Development Server
```bash
php artisan serve
```
Access the app at `http://127.0.0.1:8000`

## 🔐 How to Use 2FA
1. **Login to your account**
2. **Navigate to the 2FA settings page**
3. **Enable Two-Factor Authentication** (QR code & recovery codes are generated)
4. **Scan the QR code** using Google Authenticator/Authy
5. **Enter the generated OTP code** to verify
6. **Save your recovery codes** for backup

## 🛠 Technologies Used
- Laravel 12
- Laravel Fortify
- Tailwind CSS (for UI)
- Google Authenticator / Authy (for 2FA verification)

## 📝 License
This project is open-source and available under the [MIT License](LICENSE).

---
📢 **Follow for more Laravel content!** 🚀
