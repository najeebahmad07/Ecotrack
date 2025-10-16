# 🌍 EcoTrack – Track Daily Eco Habits & Reduce Your Carbon Footprint

EcoTrack is a free, open-source web application designed to help users **track daily eco-friendly activities**, reduce their **carbon footprint**, and adopt sustainable habits. 🌱  

Built with ❤️ using **PHP, MySQL, JavaScript, HTML, and CSS**, EcoTrack provides a **personalized Green Score**, visualizes weekly reports, and includes a leaderboard to motivate eco-conscious living.

Whether you are a student, developer, environmentalist, or tech enthusiast, EcoTrack helps you **log water, electricity, and transportation usage**, see the impact of your actions, and take steps toward a greener planet.

---

## 🌟 Why EcoTrack?

- Track your **daily eco activities** easily and visually  
- Calculate a **personalized Green Score** automatically  
- Generate **weekly sustainability reports**  
- Compare your eco-efforts with friends using a **leaderboard system**  
- Stay motivated with a **clean and modern dashboard**  
- Open-source and fully **customizable for developers**  

**Keywords for SEO:** eco tracker, carbon footprint tracker, sustainability, PHP MySQL JS web app, green score, eco-friendly habits.

---

## ✨ Key Features

1. 📊 **Daily Eco Tracker**  
   Log water usage (liters), electricity consumption (kWh), and transportation (km) daily.  

2. 🧠 **Smart Green Score System**  
   EcoTrack calculates a **Green Score** based on your daily usage:

 3. 📅 **Weekly Reports & Charts**  
Generate weekly insights and visualize your eco-efforts over time.  

4. 🏆 **Leaderboard**  
Compete with friends or other users to see who is the most eco-conscious.  

5. ☁️ **Responsive & Modern UI**  
Works perfectly on desktops, tablets, and mobile devices.  

6. 🔐 **Secure Data Storage**  
All activity logs are safely stored in a **MySQL database** via **PHP backend**.  

7. 🧮 **Lightweight & Efficient**  
Pure PHP & JS — no heavy frameworks required.  

8. 🌿 **Open Source & Customizable**  
Fork, contribute, and improve EcoTrack for your own sustainability projects.  

---

## 🛠️ Tech Stack

| Layer | Technologies |
|:------|:-------------|
| Frontend | HTML5, CSS3, Bootstrap, JavaScript |
| Backend | Core PHP |
| Database | MySQL |
| Charts/Visualization | Chart.js (optional) |
| Hosting | Any PHP-supported host (Hostinger, XAMPP, InfinityFree) |

---

## 🚀 Installation Guide

Follow these steps to set up EcoTrack locally or on a server.

### 1️⃣ Clone the Repository
```bash
git clone https://github.com/najeebahmad07/EcoTrack.git

2️⃣ Import the Database

1. Open phpMyAdmin.


2. Create a new database called ecotrack.


3. Import the SQL file:

database/ecotrack.sql

3️⃣ Configure Database Connection

Edit includes/db.php:

$servername = "localhost";
$username = "root";
$password = "";
$database = "ecotrack";

$conn = new mysqli($servername, $username, $password, $database);
if ($conn->connect_error) {
    die("Connection failed: " . $conn->connect_error);
}

4️⃣ Run the Project

Place the EcoTrack folder in your server directory (e.g., htdocs/EcoTrack for XAMPP)

Open in your browser:


http://localhost/EcoTrack

🎉 EcoTrack is ready for logging your eco-habits!


---

📁 Project Structure

EcoTrack/
│
├── index.php                     # Home page with overview
├── log_activity.php              # Daily eco activity logging form
├── dashboard.php                 # User dashboard with charts
├── leaderboard.php               # Compare Green Scores
│
├── includes/
│   ├── db.php                    # Database connection
│   ├── header.php                # Page header
│   └── footer.php                # Page footer
│
├── assets/
│   ├── css/
│   │   └── style.css             # Custom CSS styles
│   ├── js/
│   │   └── main.js               # JavaScript for charts and interactivity
│   └── images/
│       └── logo.png              # App logo
│
└── database/
    └── ecotrack.sql              # SQL tables and initial data


---

💡 How EcoTrack Works

1. User Logs Data
Input your daily water usage, electricity, and transportation.


2. Score Calculation

Green Score = 100 - (water + electricity + transport)

Higher score = lower environmental impact.


3. Data Storage
Logs are inserted into the MySQL table logs using PHP.


4. Dashboard Visualization
Charts show weekly usage trends and scores.


5. Leaderboard
Users can compare scores, fostering friendly competition.


6. Eco Insights
Provides tips and visual feedback to help reduce usage.




---

📄 Sample PHP Code for Logging

<?php
if ($_SERVER['REQUEST_METHOD'] == 'POST') {
    $water = $_POST['water'];
    $electricity = $_POST['electricity'];
    $transport = $_POST['transport'];
    $date = date('Y-m-d');

    $score = 100 - ($water + $electricity + $transport);
    if ($score < 0) $score = 0;

    $sql = "INSERT INTO logs (water, electricity, transport, score, log_date)
            VALUES ('$water', '$electricity', '$transport', '$score', '$date')";
    $conn->query($sql);
}
?>


---

🗄️ Database Schema

Database Name: ecotrack

Table: logs

Column	Type	Description

id	INT (AI PK)	Primary key
water	FLOAT	Daily water usage (liters)
electricity	FLOAT	Daily electricity (kWh)
transport	FLOAT	Daily transport distance (km)
score	INT	Calculated Green Score
log_date	DATE	Date of the entry



---

Optional Users Table (for multi-user support)

Column	Type	Description

id	INT (AI PK)	Primary key
username	VARCHAR(50)	User’s name
email	VARCHAR(100)	User email
password	VARCHAR(255)	Hashed password
created_at	TIMESTAMP	Account creation date



---

📊 Dashboard Visualization

Display weekly usage charts for water, electricity, and transport

Show line graphs or bar charts using JavaScript (Chart.js)

Display Green Score trend

Leaderboard sorted by highest score



---

🌱 SEO Keywords

Include keywords naturally throughout the README for discoverability:

Eco tracker web app

Carbon footprint tracker

Sustainability dashboard

Green score calculator

Daily eco habits tracker

PHP MySQL JavaScript web application

Open-source eco-friendly project



---

🤝 Contributing

We welcome contributions! 🌿

1. Fork the repository


2. Create a new branch (feature-new)


3. Commit your changes


4. Push to your forked repository


5. Open a Pull Request




---

🧩 Best Practices for Contributors

Write clean and commented code

Test changes before committing

Follow existing folder structure

Avoid breaking existing functionality

Add screenshots or examples if you add UI changes



---

📸 Screenshots

(Add screenshots here for GitHub showcase)

assets/images/demo-dashboard.png
assets/images/eco-log-form.png


---

📜 License

This project is licensed under MIT License.
Use, modify, and distribute freely with credit to the author.


---

💚 Developed By

👨‍💻 Najeeb Ahmad (@najeebahmad07)
📧 Email: njbdev07@gmail.com
🌐 Portfolio: https://linktr.ee/najeebahmad07
📱 Contact: +91 7992292086


---

🌟 Star this repository if you like EcoTrack!

Let’s make eco-friendly living easier and more data-driven. Every small action counts. 🌍💚
