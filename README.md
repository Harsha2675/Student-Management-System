# Student Management System

A Django web application for managing student records with full CRUD (Create, Read, Update, Delete) functionality.

## Features

- ✅ Add new students
- ✅ View all students in a responsive table
- ✅ Edit existing student information
- ✅ Delete students with confirmation
- ✅ Modal dialogs for detailed views
- ✅ Bootstrap responsive design
- ✅ Form validation and error handling

## Installation & Setup

1. **Create virtual environment**
   ```bash
   python -m venv venv
   venv\Scripts\activate
   ```

2. **Install dependencies**
   ```bash
   pip install django
   ```

3. **Run migrations**
   ```bash
   python manage.py makemigrations
   python manage.py migrate
   ```

4. **Start the server**
   ```bash
   python manage.py runserver
   ```

5. **Access the application**
   ```
   http://127.0.0.1:8000/
   ```

## Database Model

```python
class Student(models.Model):
    student_number = IntegerField()
    first_name = CharField(max_length=50)
    last_name = CharField(max_length=50)
    email = EmailField(max_length=100)
    field_of_study = CharField(max_length=50)
    gpa = FloatField()
```

## Core Functionality

### Create (Add Student)
- **URL**: `/students/add/`
- Form validation and success messages

### Read (View Students)
- **URL**: `/students/`
- Responsive table with modal popups

### Update (Edit Student)
- **URL**: `/students/edit/<id>/`
- Pre-populated forms with validation

### Delete (Remove Student)
- **URL**: `/students/delete/<id>/`
- Confirmation modal with error handling

## Technologies Used

- **Backend**: Django 5.2.7, Python 3.10
- **Database**: SQLite3
- **Frontend**: HTML5, CSS3, Bootstrap 5
- **Icons**: Font Awesome 7.0.1

## Project Structure

```
Student/
├── django_project/     # Main project configuration
├── students/          # Django app
│   ├── models.py     # Database models
│   ├── views.py      # Business logic
│   ├── forms.py      # Form definitions
│   ├── urls.py       # URL routing
│   └── templates/    # HTML templates
└── db.sqlite3        # SQLite database
```

## Author

**Harsha Vardhan**

---

*A complete Django web application with modern design and full CRUD functionality.*