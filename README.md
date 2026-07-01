# 🎉 EMS — Event Management System

A production-ready **Django Event Management System** that helps organizations create, manage, and analyze events efficiently. The application provides secure role-based access, event registration, analytics, email notifications, and profile management.

---

## ✨ Features

| Feature | Description |
|---------|-------------|
| 🔐 Role-Based Access Control | Admin, Event Manager and Attendee roles |
| 📅 Event Management | Create, edit, publish, unpublish and delete events |
| 🎟 Event Registration | Register for events with duplicate registration prevention |
| ⏳ Waitlist Management | Automatic waitlist promotion when seats become available |
| 📊 Analytics Dashboard | Interactive Pie, Line, Bar and Gauge charts |
| 📧 Email Notifications | Email confirmation using Django Signals |
| 👤 User Profile | Avatar upload, bio and profile management |
| 📁 CSV Export | Export events and registrations |
| 📱 Responsive Design | Bootstrap 5 with mobile-friendly UI |

---

# 🚀 Tech Stack

- Python 3
- Django
- SQLite
- Bootstrap 5
- HTML5
- CSS3
- JavaScript
- Google Charts
- Django Signals

---

# 👥 User Roles

## 👨‍💼 Admin

- Manage all users
- Manage all events
- Delete any event
- View analytics
- Export CSV
- Manage user roles

## 👨‍💻 Event Manager

- Create events
- Edit own events
- Delete own events
- View own registrations
- View analytics

## 🙋 Attendee

- Register for events
- Cancel registration
- View registered events
- Manage profile

---

# 📊 RBAC Summary

| Action | Admin | Manager | Attendee |
|---------|:----:|:------:|:--------:|
| Create Event | ✅ | ✅ | ❌ |
| Edit Event | ✅ | Own | ❌ |
| Delete Event | ✅ | Own | ❌ |
| Register Event | ❌ | ❌ | ✅ |
| Analytics | ✅ | ✅ | ❌ |
| Export CSV | ✅ | ❌ | ❌ |

---

# 📂 Project Structure

```text
SmartEventManagement/
├── config/
├── ems/
├── media/
├── manage.py
├── requirements.txt
├── README.md
```

---

# 🗄 Database Models

## User
- Username
- Email
- Password

## Profile
- Avatar
- Bio
- Phone
- Role

## Event
- Title
- Description
- Category
- Venue
- Date
- Banner
- Total Seats
- Status

## Registration
- User
- Event
- Registration ID
- Status

---

# 🌐 URL Overview

| URL | Description |
|------|-------------|
| / | Home |
| /login | Login |
| /register | Register |
| /dashboard | Dashboard |
| /events | Event List |
| /events/create | Create Event |
| /analytics | Analytics |
| /profile | Profile |
| /admin | Django Admin |

---

# ⚙ Installation

```bash
git clone https://github.com/bhupendrakushwaha0108/SmartEventManagement.git
cd SmartEventManagement

python3 -m venv venv
source venv/bin/activate

pip install -r requirements.txt

python manage.py migrate

python manage.py createsuperuser

python manage.py runserver
```

Open:

```
http://127.0.0.1:8000/
```

---

# 📧 Email Configuration

```python
EMAIL_BACKEND = "django.core.mail.backends.smtp.EmailBackend"
EMAIL_HOST = "smtp.gmail.com"
EMAIL_PORT = 587
EMAIL_USE_TLS = True
EMAIL_HOST_USER = "your-email@gmail.com"
EMAIL_HOST_PASSWORD = "your-app-password"
DEFAULT_FROM_EMAIL = EMAIL_HOST_USER
```

---

# 🧪 Testing Checklist

- User Registration
- Login & Logout
- Create Event
- Edit Event
- Delete Event
- Register for Event
- Waitlist Promotion
- Analytics Charts
- CSV Export
- Email Notification
- Role Permissions

---

# 🔒 Production Checklist

- DEBUG=False
- Secure SECRET_KEY
- PostgreSQL
- HTTPS
- ALLOWED_HOSTS
- Collect Static Files

---

# 🚀 Future Improvements

- REST API
- JWT Authentication
- Docker Support
- Redis Cache
- Celery
- Payment Gateway
- QR Code Attendance
- Event Scanner

---

# 🤝 Contributing

Contributions are welcome. Fork the repository and submit a pull request.

---

# 📜 License

This project is created for educational and portfolio purposes.

---

# 👨‍💻 Author

**Bhupendra Kushwaha**

Python Full Stack Developer

GitHub: https://github.com/bhupendrakushwaha0108

⭐ If you found this project useful, consider giving it a star.
