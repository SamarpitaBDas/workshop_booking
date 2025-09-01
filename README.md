# **Workshop Booking**

> This website is for coordinators to book a workshop(s), they can book a workshop based on instructors posts or can propose a workshop date based on their convenience.


### Set up guidelines
1. Clone this repo.
    > git clone -b fossee-autumn-25-task1 https://github.com/SamarpitaBDas/workshop_booking.git

    >cd workshop_booking

2. Create virtual environment and install the required packages from requirements.txt

    > python -m venv venv
    > source venv/bin/activate   # for Linux/Mac
    > venv\Scripts\activate      # for Windows

    > pip install -r requirements.txt

3. Make Migrations and Migrate
    > python manage.py makemigrations\
    > python manage.py migrate

4. Create Super User
    > python manage.py createsuperuser

5. Start Server
    > python manage.py runserver

6. Goto admin page and login using superuser credentials
    > localhost:8000/admin

6. Configure Admin Panel

    Log in using your superuser credentials.

    Go to Groups → Create a group named instructor and assign all permissions.

    By default, new users are registered as coordinators.

    For instructors, update their profile position to instructor and add them to the instructor group.

7. Local Settings

    Make sure local_settings.py exists and contains required variables (e.g., DB configs, API keys, etc.).

### NOTE:
in case this error occurs
Error: cms_page table not found
Fix:    > Run migrations for the cms app:


### Features
* Statistics
    1. Instructors Only
        * Monthly Workshop Count
        * Instructor/Coordinator Profile stats
        * Upcoming Workshops
        * View/Post comments on Coordinator's Profile
    2. Open to All
        * Workshops taken over Map of India
        * Pie chart based on Total Workshops taken to Type of Workshops.

* Workshop Related Features
    > Instructors can Accept, Reject or Delete workshops based on their preference, also they can postpone a workshop based on coordinators request.

__NOTE__: Check docs/Getting_Started.md for more info.
