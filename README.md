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

The objective was to **improve the look and user experience of the website** while maintaining its existing functionality.

### Issues in the previous version

* [X] Static tables replaced with responsive UI components
* [X] Improved UI/UX for mobile devices (responsiveness)

## major Changes that were made and their screenshots

---


## 🔹 Workshop Statistics Page

* in the mobile version of the statistics page i noticed that the **filter selection** table doesn't look right also it made the entire page messy so i added an additional **button** which when pressed can be used to apply the filters
* changed the ui for the cards in order to give it a modern look and make it more readable to the user.

### Previous Version
**Desktop Version**
![alt text](https://i.postimg.cc/Wz4CvqNd/Screenshot-2025-09-04-195955.png)
**Mobile Version**
![alt text](https://i.postimg.cc/XJ4tsDtc/Screenshot-2025-09-04-200027.png)

### Current Version

**Desktop View**
![!\[alt text\](https://i.postimg.cc/Y0M2jLKt/Screenshot-2025-08-31-150939.png)](https://i.postimg.cc/52m0PDRn/Screenshot-2025-09-04-194154.png)

**Mobile View**
![alt text](https://i.postimg.cc/k5X5Lfr9/Screenshot-2025-09-04-194148.png)
![alt text](https://i.postimg.cc/FFfY9WYH/Screenshot-2025-09-04-194307.png)

---

## 🔹 Homepage ( `/workshop/status` )

### Improvements I Made
* Optimized spacing and alignment for better visual hierarchy.
* changed the way the tables and the cards appeared in smaller screens in order to ensure readability.

### Earlier Version

**Screenshots (Before):**
![alt text](https://i.postimg.cc/PfMtjZMq/Screenshot-2025-08-29-220922.png)
![alt text](https://i.postimg.cc/FsshsRPV/Screenshot-2025-08-30-192726.png)

### Current Version

**Desktop View:**
![!\[alt text\](https://i.postimg.cc/SxH4rGmg/Screenshot-2025-08-30-221515.png)](https://i.postimg.cc/261SSy8K/Screenshot-2025-09-04-193402.png)

**Mobile View:**
![!\[alt text\](https://i.postimg.cc/MKPqcSN2/Screenshot-2025-08-30-221525.png)](https://i.postimg.cc/YSnS7YkF/Screenshot-2025-09-04-193432.png)

## Login and logout screens
* there were no major updates in the login and logout screens though their appearances were slightly changed in order to match the other pages

### Current Version

**Desktop View**
![alt text](https://i.postimg.cc/T3x1JTCK/Screenshot-2025-09-04-194220.png)

**Mobile View**
![alt text](https://i.postimg.cc/ZKp0NWFk/Screenshot-2025-09-04-194237.png)
![alt text](https://i.postimg.cc/J79GtNXc/Screenshot-2025-09-04-194248.png)

NOTE: the navbar was changed to match the theme though no significant ui updates were made on it.

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
