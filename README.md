# Online Learning Platform (Django + Angular)

## Project Description

A web application for creating and taking online courses. The platform allows users to register as either a Student or a Teacher.

* **Students** can browse the list of available courses, view their details, enroll in courses, view the list of courses they are enrolled in, and unenroll from courses.
* **Teachers** can create new courses, and edit and delete the courses they have created.
* **Administrator** (via Django Admin) can manage all aspects of the platform (users, courses, categories, enrollments).

The project is divided into two parts:
* **Backend:** Implemented with Django and Django REST Framework, providing a REST API.
* **Frontend:** Implemented with Angular (using Standalone Components API), interacting with the Backend via the API.

## Team members
**Bagauova Danara - 23B031233**
**Ibadullaev Assylzhan - 23B030359**

## Key Features

* User registration with role selection (Student/Teacher).
* User authentication using JWT (Access + Refresh tokens).
* Viewing the list of all courses.
* Viewing detailed information about a course.
* Student enrollment in a course.
* Student unenrollment from a course.
* Student view of their enrolled courses ("My Courses").
* Course creation by a teacher.
* Course editing by a teacher (only their own courses).
* Course deletion by a teacher (only their own courses).
* Frontend route protection (Route Guards) based on login status and role.
* Automatic attachment of JWT token to API requests (HTTP Interceptor).
* Management via Django Admin.

## Technologies Used

**Backend:**
* Python 3.x
* Django
* Django REST Framework
* djangorestframework-simplejwt (for JWT)
* django-cors-headers (for CORS)
* SQLite (default database)
* pytils, pytranslit (for slug generation)

**Frontend:**
* TypeScript
* Angular (Standalone Components API)
* Angular CLI
* RxJS
* Bootstrap 5 (for styling)
* ngx-toastr (for notifications)
* jwt-decode (for JWT decoding)

## Setup and Installation

### Prerequisites:
* Git
* Python 3.8+ and Pip
* Node.js (LTS version recommended) and npm
* Angular CLI (`npm install -g @angular/cli`)

### Setup Steps:

1.  **Clone the repository:**
    ```bash
    git clone <https://github.com/ddananna/WebProjectl>
    cd <online_learning_platform>
    ```

2.  **Backend Setup (`back` folder):**
    * Navigate to the backend directory: `cd back`
    * Create and activate a virtual environment:
        ```bash
        # Windows
        python -m venv venv
        .\venv\Scripts\activate
        # macOS / Linux
        python3 -m venv venv
        source venv/bin/activate
        ```
    * Install Python dependencies:
        ```bash
        pip install -r requirements.txt
        ```
    * Apply database migrations:
        ```bash
        python manage.py migrate
        ```
    * (Optional) Create a superuser for admin access:
        ```bash
        python manage.py createsuperuser
        ```

3.  **Frontend Setup (`front` folder):**
    * Navigate to the frontend directory: `cd ../front` (if you were in `back`)
    * Install Node.js dependencies:
        ```bash
        npm install
        ```

### Running the Application:

1.  **Run the Backend Server:**
    * Navigate to the `back` directory.
    * Activate the virtual environment (if not already active).
    * Start the server:
        ```bash
        python manage.py runserver
        ```
    * By default, the backend will be available at `http://127.0.0.1:8000/`.

2.  **Run the Frontend Server:**
    * Open a **new terminal**.
    * Navigate to the `front` directory.
    * Start the Angular development server:
        ```bash
        ng serve -o
        ```
    * The application will automatically open in your default browser at `http://localhost:4200/`.

## Django Admin Access

The Django admin panel is available at `http://127.0.0.1:8000/admin/` (use the superuser login/password).
