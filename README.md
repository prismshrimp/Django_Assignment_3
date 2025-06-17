By Wan Nurqistina binti Rosmin

To-Do List Application
A simple and responsive To-Do List web application built with Django and styled with Bootstrap 5. Users can create, view, update, and delete tasks, with a clean interface suitable for desktop and mobile devices.
Project Overview
This Django-based application demonstrates the Model-View-Template (MVT) architecture, using SQLite for data storage and Bootstrap 5 for frontend styling. It’s designed for learning Django fundamentals, including models, views, forms, templates, URLs, and the messaging framework.
Features

Create Tasks: Add tasks with a title, optional description, and completion status.
View Tasks: Display tasks in a responsive card layout with hover effects.
Update Tasks: Edit task details or toggle completion status.
Delete Tasks: Remove tasks with a confirmation prompt.
Responsive UI: Styled with Bootstrap 5 for a modern, mobile-friendly experience.
User Feedback: Success/error messages via Django’s messaging framework.
Admin Panel: Manage tasks through Django’s admin interface.
Database: SQLite for development simplicity.

Prerequisites

Python 3.13.5 (or 3.8+)
pip (Python package manager)
Virtual environment (recommended)
Git (optional for cloning)

Setup Instructions
Follow these steps to run the application locally on Windows:

Clone the Repository (if using Git):
git clone <repository-url>
cd todo_project


Create and Activate a Virtual Environment:
python -m venv venv
venv\Scripts\activate


Install Dependencies:
pip install -r requirements.txt

Ensure requirements.txt includes:
django>=5.0
django-widget-tweaks


Apply Database Migrations:
python manage.py migrate


Create a Superuser (optional, for admin access):
python manage.py createsuperuser


Run the Development Server:
python manage.py runserver


Access the Application:

Open a browser and visit: http://127.0.0.1:8000/
Admin panel: http://127.0.0.1:8000/admin/ (use superuser credentials)


Dependencies

django: Web framework for backend logic.
django-widget-tweaks: Enhances form styling with Bootstrap classes.
Bootstrap 5: Loaded via CDN for responsive UI.

Install dependencies:
pip install django django-widget-tweaks

Usage

Home Page: View all tasks in a card layout with edit/delete options.
Add Task: Click “Add Task” to create a new task.
Edit Task: Click “Edit” to modify a task’s details.
Delete Task: Click “Delete” and confirm to remove a task.
Admin Panel: Manage tasks at /admin/.

Troubleshooting

TemplateSyntaxError: Invalid filter 'add_class':
Ensure django-widget-tweaks is installed: pip show django-widget-tweaks.
Verify widget_tweaks is in INSTALLED_APPS in settings.py.
Add {% load widget_tweaks %} at the top of task_form.html.


Database Issues: Delete db.sqlite3 and todo/migrations/ (except __init__.py), then run:python manage.py makemigrations
python manage.py migrate


Server Not Starting: Ensure virtual environment is active and dependencies are installed.
Bootstrap Not Loading: Check internet connection for CDN or host Bootstrap locally.

Future Enhancements

Add user authentication to restrict tasks per user.
Implement task categories or priorities.
Add filtering for completed/pending tasks.
Deploy to Heroku or another platform.
Visualize task stats with Chart.js.

Contributing
Fork the repository, create a branch, and submit a pull request with your changes.
License
MIT License
