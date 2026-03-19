# LMS Platform

A comprehensive Learning Management System built with Laravel, featuring live video conferencing, SMS notifications, multi-gateway payments, and a full REST API for mobile and third-party integrations.

## Features

- **Course Management** -- Create, organize, and sell courses with bundles, chapters, quizzes, assignments, and certificates
- **Live Classes** -- Real-time video conferencing via Agora and BigBlueButton integrations
- **SMS Notifications** -- Twilio-powered SMS alerts for enrollment confirmations, reminders, and updates
- **REST API** -- Fully documented API layer for mobile apps and external service integrations
- **Multi-Payment Gateways** -- Stripe, PayPal, Razorpay, JazzCash, Paytm, Instamojo, M-Pesa, Flutterwave, Authorize.Net, iyzico, Robokassa, and more
- **Multilingual Support** -- Built-in translation system with Arabic language support
- **Affiliate & Cashback System** -- Affiliate codes and configurable cashback rules
- **Blog & CMS** -- Integrated blog with categories, advertising banners, and customizable pages
- **User Roles** -- Admin panel, instructor dashboard, and student portal with role-based access control
- **Social Authentication** -- Login via Google, Facebook, and other OAuth providers
- **Media Management** -- Image processing with Intervention, audio/video metadata extraction with getID3, and AWS S3 / MinIO storage
- **Consultation & Appointments** -- Instructor consultation booking system
- **Forum & Noticeboard** -- Course-level discussion forums and announcement boards

## Tech Stack

- **Backend:** PHP 7.2+, Laravel 7
- **Frontend:** Blade templates, Laravel Mix, Webpack
- **Database:** MySQL
- **Real-Time:** Agora SDK, BigBlueButton
- **SMS:** Twilio
- **Payments:** Stripe, PayPal, Razorpay, JazzCash, Paytm, Instamojo, M-Pesa, Flutterwave, and others
- **Storage:** Local, AWS S3, MinIO
- **Authentication:** Laravel Socialite (Google, Facebook), Laravel UI

## Prerequisites

- PHP >= 7.2.5
- Composer
- MySQL 5.7+
- Node.js & npm

## Setup

1. **Clone the repository**
   ```bash
   git clone https://github.com/mhmalvi/LMS-original.git
   cd LMS-original
   ```

2. **Install dependencies**
   ```bash
   composer install
   npm install
   ```

3. **Configure environment**
   ```bash
   cp .env.example .env
   php artisan key:generate
   ```

4. **Update `.env`** with your database credentials, Agora keys, Twilio credentials, and payment gateway API keys.

5. **Run migrations and seeders**
   ```bash
   php artisan migrate --seed
   ```

6. **Build frontend assets**
   ```bash
   npm run dev
   ```

7. **Start the development server**
   ```bash
   php artisan serve
   ```

The application will be available at `http://localhost:8000`.

## Project Structure

```
app/
  Http/Controllers/
    Admin/       # Admin panel controllers
    Api/         # REST API controllers
    Panel/       # Instructor panel controllers
    Web/         # Public-facing controllers
  Models/        # Eloquent models
routes/
  admin.php      # Admin routes
  api.php        # API routes
  panel.php      # Instructor panel routes
  web.php        # Public web routes
resources/       # Blade views, lang files, and frontend assets
```

## License

MIT
