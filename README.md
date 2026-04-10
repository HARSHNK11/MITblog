# 📝 MIT-Blog

MIT-Blog is an academic blogging platform built with Django, designed to streamline knowledge sharing within institutions. It features a structured moderation system where students can submit posts for faculty review, ensuring quality content is published. With role-based access control, clean UI, and a status-driven post lifecycle, MIT-Blog provides a secure and organized environment for academic content collaboration.

---

## ⚙️ System Highlights
- Auto profile creation using Django signals
- Pagination for performance optimization
- Responsive UI with Bootstrap 5
- WhiteNoise for static file handling

---

## 🛠️ Tech Stack

- **Frontend:** HTML5, CSS, Bootstrap 5
- **Backend:** Python 3.13, Django 6.0
- **Database:** SQLite3 (Development)
- **Authentication:** Django Auth System
- **Media Handling:** Pillow
- **Static Files:** WhiteNoise

---

## 📂 Project Structure

```
blog/
│── models.py
│── views.py
│── urls.py
│── forms.py
│── signals.py
│── context_processors.py
│── templates/
│── static/
```

---

## ⚡ Installation & Setup

```bash
# Clone repository
git clone https://github.com/your-username/mit-blog.git
cd mit-blog

# Create virtual environment
python -m venv venv

# Activate (Windows)
venv\Scripts\activate

# Activate (Mac/Linux)
source venv/bin/activate

# Install dependencies
pip install -r requirements.txt

# Apply migrations
python manage.py migrate

# Run server
python manage.py runserver
```

## 🔑 Core Functional Flow

1. User registers (Student / Faculty)
2. Profile is auto-created using signals
3. Student submits a post → marked as **PENDING**
4. Faculty reviews:
   - ✅ Approve → becomes public
   - ❌ Reject → hidden
5. Users can upvote and comment on approved posts

---

## 📊 Key Design Decisions

- Slug-based URLs for better readability and SEO
- Centralized role handling via `_get_role()` helper
- Signal-based profile management (decoupled logic)
- Status-driven post lifecycle
- Clean separation of concerns (Models → Views → Templates)

---

## 🧪 Testing

Manual integration testing performed. Verified:
- Authentication workflows
- Role-based access control
- Moderation system
- Comment threading
- Upvote toggle functionality

---

## 🔮 Future Enhancements

- Markdown / Rich text editor (CKEditor or TinyMCE)
- PostgreSQL migration for scalability
- Email & in-app notifications
- AJAX-based interactions
- REST API integration (Django REST Framework)
- Syntax highlighting for code blocks

---

## 👨‍💻 Contributors

- Harsha N K
- Barri Harshith
- Mohan Sravanth Varma Rudraraju

---

## 📜 License

This project is developed for academic purposes and can be extended for production use with enhancements.

---

## 💡 Conclusion

MIT-Blog demonstrates a scalable Django-based architecture for academic content sharing, combining structured moderation, role-based access control, and a clean UI to improve knowledge accessibility within institutions.
