Team Health Check Application

A comprehensive web-based application for conducting and visualizing software team health checks using the Spotify Health Check methodology. The application provides advanced analytics, secure authentication, and interactive reporting tools for technical teams.
Features

    Role-Based User Management: Five distinct user roles with appropriate permissions
    Department & Team Structure: Hierarchical organization with departments and teams
    Health Check Templates: Customizable templates based on Spotify's Health Check model
    Anonymous Voting: Team members can submit anonymous responses
    Advanced Analytics: Interactive charts and visualizations of team health metrics
    Historical Tracking: Track team health trends over time
    Comparative Analysis: Compare health metrics across teams and departments
    Responsive Design: Works on desktop and mobile devices

Tech Stack

    Backend: Django 5.2
    Database: SQLite (local database)
    Frontend: Bootstrap 5, JavaScript, Chart.js
    Authentication: Custom user model with role-based permissions
    Static Files: WhiteNoise for static file serving
    Deployment: Replit environment compatible

Installation Instructions
Prerequisites

    Python 3.11+
    Git

Local Setup (macOS/Linux)

    Clone the repository

git clone <your-repository-url>
cd health-check-application

    Create and activate a virtual environment

python -m venv venv
source venv/bin/activate

    Install dependencies

pip install -r requirements.txt

    Set up environment variables

# Set Django secret key
export SESSION_SECRET="your-secret-key-for-django"

    Run database migrations

python manage.py migrate

    Create superuser

python manage.py createsuperuser

    Generate test data

python generate_complete_data.py

    Collect static files

python manage.py collectstatic

    Run the development server

python manage.py runserver

    Access the application

    Open your browser and navigate to http://127.0.0.1:8000
    Access admin panel at http://127.0.0.1:8000/admin/

Local Setup (Windows)

    Clone the repository

git clone <your-repository-url>
cd health-check-application

    Create and activate a virtual environment

python -m venv venv
venv\Scripts\activate

    Install dependencies

pip install -r requirements.txt

    Set up environment variables

# Set Django secret key
set SESSION_SECRET=your-secret-key-for-django

    Run database migrations

python manage.py migrate

    Create superuser

python manage.py createsuperuser

    Generate test data

python generate_complete_data.py

    Collect static files

python manage.py collectstatic

    Run the development server

python manage.py runserver

    Access the application

    Open your browser and navigate to http://127.0.0.1:8000
    Access admin panel at http://127.0.0.1:8000/admin/

Default Login Credentials

After running the data generation script, you can log in with these credentials:

    Administrator:
        Username: admin
        Password: admin123

    Team Leader:
        Username: teamlead1
        Password: password123

    Engineer:
        Username: engineer1
        Password: password123

Application Structure

    accounts: User authentication and profile management
    departments: Department management
    teams: Team and team member management
    health_checks: Health check templates, sessions, and responses
    analytics: Data visualization and analytics dashboard

Database Schema

The application uses SQLite (a local file-based database) with the following key models:

    User (custom user model with role-based permissions)
    Department (organizational unit)
    Team (belongs to a department)
    TeamMember (links users to teams)
    HealthCheckCategory, HealthCheckQuestion (question framework)
    HealthCheck (templates), HealthCheckSession (instances)
    HealthCheckResponse (user responses to questions)

Role-Based Access

    Engineers: Participate in health checks for their teams
    Team Leaders: Create and manage health checks for their teams
    Department Leaders: View all teams and health checks in their department
    Senior Managers: View all departments, teams, and health checks
    Administrators: Full access to all system features

Project Documentation

For comprehensive documentation of the project architecture, code structure, and functionality, see the project_documentation.txt file.
