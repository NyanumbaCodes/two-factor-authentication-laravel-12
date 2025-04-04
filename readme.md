# Laravel 12 Two-Factor Authentication (2FA)

## 📌 Introduction
This repository demonstrates how to implement **Two-Factor Authentication (2FA) in Laravel 12** using **pragmarx/google2fa-laravel**. Two-Factor Authentication adds an extra layer of security to your application, requiring users to verify their identity with an authentication code.

## 🎯 Features
- **User Authentication**
- **Enabling & Verifying 2FA using Google2FA**
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

### 6️⃣ Install and Configure Google2FA
Install the `pragmarx/google2fa-laravel` package:
```bash
composer require pragmarx/google2fa-laravel
```
Publish the config file:
```bash
php artisan vendor:publish --provider="PragmaRX\Google2FALaravel\ServiceProvider"
```

### 7️⃣ Implement Two-Factor Authentication
Ensure your application handles the necessary logic for:
- **Generating QR codes for Google Authenticator**
- **Verifying user-entered OTPs**
- **Providing recovery codes**
- **Allowing users to disable 2FA if needed**

### 8️⃣ Start Development Server
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

## 🏆 Challenge for Developers
In this implementation, recovery codes are generated when a user enables Two-Factor Authentication. Your challenge is to extend this system by allowing users to log in using a recovery code when they don't have access to their authenticator app.

### Steps to Implement:
- Create a form where users can enter a recovery code instead of an OTP.
- Validate the entered recovery code against stored ones.
- If valid, allow login and regenerate a new set of recovery codes.
- Ensure used recovery codes cannot be reused.

Let us know if you implement this! 🚀

## 🛠 Technologies Used
- Laravel 12
- Pragmarx Google2FA-Laravel
- Tailwind CSS (for UI)
- Google Authenticator / Authy (for 2FA verification)

## 📝 License
This project is open-source and available under the [MIT License](LICENSE).

---
📢 **Follow for more Laravel content!** 🚀
