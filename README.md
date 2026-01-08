# FixMyCampus - Campus Issue Reporting System

FixMyCampus is a comprehensive web application designed to streamline the reporting and tracking of campus infrastructure issues. It empowers students to report problems (like electricity, water, internet) and allows administrators to manage and resolve them efficiently.



## Features

- **User Authentication**: Secure Login/Signup using Roll Number authentication.
- **Issue Reporting**: Students can report issues with type, description, and location.
- **Issue Tracking**: Real-time status updates (Pending, In Progress, Resolved).
- **Dashboard**:
  - **Student**: View personal report history and status.
  - **Admin**: Overview of all issues, statistics, and graphs.
- **Admin Panel**:
  - Manage Issues (Update status, Delete).
  - User Management (Ban/Unban users).
  - Audit Logs (Track admin actions).
- **Responsive Design**: Mobile-friendly interface.

## Technical Stack

- **Backend**: Django 5.x.x (Python)
- **Database**: SQLite3 (Default Django DB)
- **Frontend**: HTML5, CSS3, and JavaScript 
- **Styling**: `styles.css`, `index.css`

## Directory Structure

```
/FixMyCampus-1
|   manage.py              # Django CLI utility
|   requirements.txt       # Python dependencies
|   README.md              # Project documentation
|   db.sqlite3             # SQLite Database
|   
+---FixMyCampus            # Project Configuration
|       asgi.py
|       settings.py        # Main settings
|       urls.py            # Root URL routing
|       wsgi.py
|       
+---core                   # Main Application (App)
|   |   admin.py
|   |   apps.py
|   |   models.py          # Database Models (User, Issue, AuditLog)
|   |   urls.py            # App-specific URLs
|   |   views.py           # Logic/Controllers
|   |   ...
|           
+---static                 # Static Assets
|   +---css
|   \---js
|           
\---templates              # HTML Templates
    |   base.html
    |   ...
    +---admin              # Admin templates
    \---layouts
```

## Installation & Setup

1. **Clone the repository:**
   ```bash
   git clone https://github.com/Mehta-g1/Django_FixMyCampus.git
   cd Django_FixMyCampus
   ```

2. **Create and Activate a Virtual Environment (Recommended):**
   ```bash
   python -m venv .venv
   # Windows
   .venv\Scripts\activate
   # Mac/Linux
   source .venv/bin/activate
   ```

3. **Install Dependencies:**
   ```bash
   pip install -r requirements.txt
   ```

4. **Apply Database Migrations:**
   Initialize the SQLite database.
   ```bash
   python manage.py makemigrations
   python manage.py migrate
   ```

5. **Create an Admin User:**
   To access the Admin Dashboard, you need a user with staff privileges.
   ```bash
   python manage.py createsuperuser
   ```
   Follow the prompts to set the `Roll No` (acts as username), email, and password.

6. **Run the Server:**
   ```bash
   python manage.py runserver
   ```
   Access the app at `http://127.0.0.1:8000/`.

## Usage

### Student (Regular User)
- **Sign Up**: Create a new account using your Roll Number.
- **Login**: Access the dashboard to report issues or view status.

### Administrator
- **Custom Admin Panel**:
  - Go to `http://127.0.0.1:8000/admin/login/`
  - Login with the credentials created via `createsuperuser`.
- **Django Admin Interface**:
  - Go to `http://127.0.0.1:8000/admin_django/` for raw database access.

## License

This project is licensed under the MIT License.
