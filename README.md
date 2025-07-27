# 🔗 URL Shortener Project

## 📖 Overview

This project is a simple and efficient **URL Shortener** application that allows users to convert long URLs into short, shareable ones. It’s built with:

* **Frontend**: HTML, CSS, JavaScript
* **Backend**: Python with Flask
* **Database**: MySQL

---

## 🚀 Features

* 🔗 Shorten long URLs
* 🚀 Redirect from short URL to original URL
* 📊 Track number of clicks for each shortened URL

---

## 🗂️ Project Structure

```
URL-Shortner/
├── static/
│   ├── css/
│   │   └── styles.css
│   └── js/
│       └── scripts.js
│
├── templates/
│   └── index.html
│
├── app.py
└── README.md
```

---

## 🛠️ Prerequisites

* Python 3.x
* MySQL Server
* pip (Python package installer)

---

## ⚙️ Installation & Setup

### Step 1: Clone the Repository

```bash
git clone https://github.com/hiteshsingh01/URL-Shortner.git
cd URL-Shortner
```

### Step 2: Set Up a Virtual Environment

```bash
python -m venv venv
source venv/bin/activate  # On Windows: venv\Scripts\activate
```

### Step 3: Install Required Packages

```bash
pip install flask flask-mysqldb
```

### Step 4: Configure MySQL Database

1. **Start MySQL Server**
2. **Create a Database**

   ```sql
   CREATE DATABASE url_shortener;
   ```
3. **Create Table Schema**

   ```sql
   CREATE TABLE urls (
       id INT AUTO_INCREMENT PRIMARY KEY,
       long_url TEXT NOT NULL,
       short_url VARCHAR(6) NOT NULL,
       clicks INT DEFAULT 0
   );
   ```
4. **Update `app.py` with your MySQL credentials**

   ```python
   app.config['MYSQL_HOST'] = 'localhost'
   app.config['MYSQL_USER'] = 'root'
   app.config['MYSQL_PASSWORD'] = 'your_password'
   app.config['MYSQL_DB'] = 'url_shortener'
   ```

---

### Step 5: Run the App

```bash
python app.py
```

Navigate to: [http://127.0.0.1:5000/](http://127.0.0.1:5000/)

---

## 💡 How to Use

1. **Shorten a URL**:
   Paste any long URL, hit "Shorten URL", and get a short link instantly.

2. **Redirect**:
   Use the generated short URL to automatically redirect to the original long URL.

3. **Track Clicks**:
   Every time a short URL is used, its click count increases in the backend.

---

## 📂 Key Files

* `app.py` – Main Flask backend
* `static/` – CSS and JS files
* `templates/` – HTML templates

---

## 🤝 Contributing

Want to improve or add a feature?
Feel free to **fork** this repository and submit a **pull request**.

---

## 📬 Contact

Created by **Hitesh Singh**
📧 Email: \[Your email here if you'd like to add it]
🔗 LinkedIn: [https://www.linkedin.com/in/hiteshsingh01/](https://www.linkedin.com/in/hiteshsingh01/)

---
