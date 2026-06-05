# ✍️ Laravel Microblogging Platform

A full-stack microblogging web application built with **PHP**, **Laravel**, **MySQL**, and **Eloquent ORM** — inspired by platforms like Twitter/X. Create, edit, and share short-form posts with a secure and intuitive interface.

---

## 📌 Features

- **User Authentication** — Secure registration, login, logout, and session management via Laravel Breeze
- **Authorization** — Role-based access so users can only edit/delete their own posts
- **Post Management** — Full CRUD: create, read, update, and delete blog posts
- **Eloquent ORM** — Clean, expressive database interactions with a normalized schema
- **Blade Templating** — Dynamic, reusable frontend views using Laravel's Blade engine
- **Normalized Database** — Well-structured MySQL schema supporting dynamic content at scale

---

## 🛠️ Tech Stack

| Layer        | Technology            |
|--------------|-----------------------|
| Language     | PHP                   |
| Framework    | Laravel               |
| Database     | MySQL                 |
| ORM          | Eloquent ORM          |
| Auth         | Laravel Breeze        |
| Templating   | Blade                 |

---

## 🚀 Getting Started

### Prerequisites

- PHP >= 8.1
- Composer
- MySQL
- Node.js & NPM (for frontend assets)

### Installation

```bash
# Clone the repository
git clone https://github.com/your-username/laravel-microblogging-platform.git
cd laravel-microblogging-platform

# Install PHP dependencies
composer install

# Install frontend dependencies
npm install && npm run dev

# Copy and configure environment
cp .env.example .env
php artisan key:generate

# Configure your .env file
# DB_DATABASE, DB_USERNAME, DB_PASSWORD

# Run migrations
php artisan migrate

# Start the development server
php artisan serve
```

Then visit `http://localhost:8000` in your browser.

---

## 🌐 Application Routes

| Method | Route                  | Description                   |
|--------|------------------------|-------------------------------|
| GET    | `/`                    | Home feed — all posts         |
| GET    | `/register`            | User registration page        |
| GET    | `/login`               | User login page               |
| GET    | `/posts/create`        | Create a new post             |
| POST   | `/posts`               | Store a new post              |
| GET    | `/posts/{id}`          | View a single post            |
| GET    | `/posts/{id}/edit`     | Edit post (owner only)        |
| PUT    | `/posts/{id}`          | Update post (owner only)      |
| DELETE | `/posts/{id}`          | Delete post (owner only)      |
| GET    | `/profile`             | View user profile & posts     |

---

## 🗄️ Database Schema

```
users
  - id, name, email, password, timestamps

posts
  - id, user_id (FK), title, body, timestamps
```

---

## 📁 Project Structure

```
├── app/
│   ├── Http/
│   │   ├── Controllers/       # PostController, ProfileController
│   │   └── Middleware/        # Auth middleware
│   └── Models/                # User, Post (Eloquent models)
├── resources/
│   └── views/                 # Blade templates
│       ├── posts/             # Post CRUD views
│       ├── auth/              # Login/Register views
│       └── layouts/           # Shared layout templates
├── routes/
│   └── web.php                # Web routes
└── database/
    └── migrations/            # DB schema
```

---

## 📸 Screenshots

> _Add screenshots here to showcase the UI_

---

## 📄 License

This project is open-source and available under the [MIT License](LICENSE).
