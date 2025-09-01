# **Workshop Booking**

> This website is for coordinators to book a workshop(s). They can book a workshop based on instructor posts or propose a workshop date based on their convenience.

---

## 🔹 Set up guidelines

1. **Clone this repo**

   ```bash
   git clone -b fossee-autumn-25-task1 https://github.com/SamarpitaBDas/workshop_booking.git
   cd workshop_booking
   ```

2. **Create virtual environment and install requirements**

   ```bash
   python -m venv venv
   source venv/bin/activate   # Linux/Mac
   venv\Scripts\activate      # Windows

   pip install -r requirements.txt
   ```

3. **Make Migrations and Migrate**

   ```bash
   python manage.py makemigrations
   python manage.py migrate
   ```

4. **Create Super User**

   ```bash
   python manage.py createsuperuser
   ```

5. **Start Server**

   ```bash
   python manage.py runserver
   ```

   Go to: [http://localhost:8000/admin](http://localhost:8000/admin)

6. **Configure Admin Panel**

   * Log in using your superuser credentials.
   * Go to **Groups** → Create a group named `instructor` and assign all permissions.
   * By default, when a user registers, they are assigned as **coordinator**.
   * To make an instructor, update their profile position to `instructor` and add them to the instructor group.

7. **Local Settings**
   Make sure `local_settings.py` exists and contains the required variables (DB configs, API keys, etc.).

---

### ⚠️ Note (Important)

If the following error occurs:

```
Error: cms_page table not found
```

**Fix:** Run migrations for the `cms` app:

```bash
python manage.py makemigrations cms
python manage.py migrate cms
```

---

## 🔹 Task Documentation

The objective was to **improve the look and feel of the website** while maintaining its existing functionality.

### Issues in the previous version

* [ ] Static tables replaced with responsive UI components
* [ ] Improved UI/UX for mobile devices (responsiveness)
* [ ] Applied consistent **Bootstrap-based styling**
* [ ] Fixed inconsistent spacing across elements
* [ ] Added a **dark theme** for better readability

---

## 🔹 Homepage ( `/workshop/status` )

### Improvements I Made

* Removed static tables → replaced them with **cards** for a cleaner layout.
* Added a **dark theme** for a modern look and reduced eye strain.
* Optimized spacing and alignment for better visual hierarchy.
* Ensured responsiveness → smooth experience across desktop and mobile.

### Earlier Version

* Minimal design with plain static tables.
* Not optimized for mobile screens.

**Screenshots (Before):**
![alt text](https://i.postimg.cc/PfMtjZMq/Screenshot-2025-08-29-220922.png)
![alt text](https://i.postimg.cc/FsshsRPV/Screenshot-2025-08-30-192726.png)

---

### Current Version

**Desktop View:**
![alt text](https://i.postimg.cc/SxH4rGmg/Screenshot-2025-08-30-221515.png)

**Mobile View:**
![alt text](https://i.postimg.cc/MKPqcSN2/Screenshot-2025-08-30-221525.png)

---

## 🔹 Workshop Statistics Page

* Added a filter button for the mobile layout.
* Switched the table layout with **cards** (because tables were overflowing on mobile).

### Previous Version

*(screenshots not available)*

### Current Version

![alt text](https://i.postimg.cc/Y0M2jLKt/Screenshot-2025-08-31-150939.png)
![alt text](https://i.postimg.cc/6qcWZ6tn/Screenshot-2025-08-31-150947.png)

---

## 🔹 Features

* **Statistics**

  1. **Instructors Only**

     * Monthly Workshop Count
     * Instructor/Coordinator Profile stats
     * Upcoming Workshops
     * View/Post comments on Coordinator's Profile
  2. **Open to All**

     * Workshops taken over Map of India
     * Pie chart of Total Workshops taken vs Type of Workshops

* **Workshop Related Features**

  * Instructors can Accept, Reject, Delete workshops
  * Postpone a workshop based on coordinator’s request

---

📌 For more info: check [`docs/Getting_Started.md`](docs/Getting_Started.md)
