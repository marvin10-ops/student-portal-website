
<!DOCTYPE html>
<html lang="en">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>Student Portal</title>

<style>
@import url('https://fonts.googleapis.com/css2?family=Inter:wght@400;500;600;700;800&display=swap');

* {
    margin: 0;
    padding: 0;
    box-sizing: border-box;
    font-family: 'Inter', sans-serif;
}

body {
    background: #f4f6fb;
    color: #20243a;
}

.container {
    display: flex;
    min-height: 100vh;
}

/* SIDEBAR */
.sidebar {
    width: 250px;
    background: #171c35;
    color: white;
    padding: 30px 20px;
    position: fixed;
    height: 100vh;
}

.logo {
    font-size: 23px;
    font-weight: 800;
    margin-bottom: 45px;
}

.logo span {
    color: #8c83ff;
}

.sidebar h4 {
    color: #858ba9;
    font-size: 11px;
    margin: 25px 10px 12px;
    letter-spacing: 2px;
}

.sidebar a {
    display: block;
    padding: 13px 15px;
    margin: 6px 0;
    color: #c2c7dc;
    text-decoration: none;
    border-radius: 10px;
    cursor: pointer;
    font-size: 14px;
    transition: .3s;
}

.sidebar a:hover,
.sidebar a.active {
    background: #7168ec;
    color: white;
}

/* MAIN */
.main {
    margin-left: 250px;
    padding: 30px 40px;
    width: calc(100% - 250px);
}

.topbar {
    display: flex;
    justify-content: space-between;
    align-items: center;
    margin-bottom: 35px;
}

.topbar h2 {
    font-size: 24px;
}

.topbar p {
    color: #888da3;
    font-size: 13px;
    margin-top: 7px;
}

.profile {
    display: flex;
    align-items: center;
    gap: 12px;
}

.avatar {
    background: #dedaff;
    color: #6258d9;
    width: 43px;
    height: 43px;
    display: grid;
    place-items: center;
    border-radius: 50%;
    font-weight: 700;
}

/* WELCOME */
.welcome {
    background: linear-gradient(120deg, #7168ec, #a18af9);
    border-radius: 20px;
    padding: 35px;
    color: white;
    margin-bottom: 30px;
}

.welcome h1 {
    font-size: 27px;
    margin-bottom: 10px;
}

.welcome p {
    opacity: .85;
    font-size: 14px;
}

/* CARDS */
.stats {
    display: grid;
    grid-template-columns: repeat(4, 1fr);
    gap: 18px;
    margin-bottom: 30px;
}

.card {
    background: white;
    padding: 23px;
    border-radius: 17px;
    box-shadow: 0 5px 20px #20243a08;
}

.card small {
    color: #9296a9;
    font-size: 12px;
}

.card h2 {
    font-size: 28px;
    margin: 12px 0 5px;
}

.card p {
    font-size: 11px;
    color: #777d92;
}

.icon {
    font-size: 23px;
}

/* CONTENT */
.content {
    display: grid;
    grid-template-columns: 1.5fr 1fr;
    gap: 20px;
}

.section {
    background: white;
    border-radius: 17px;
    padding: 25px;
    margin-bottom: 20px;
}

.section h3 {
    margin-bottom: 20px;
    font-size: 17px;
}

.subject {
    display: flex;
    justify-content: space-between;
    margin-bottom: 17px;
    font-size: 13px;
}

.progress {
    background: #eeeefa;
    height: 8px;
    border-radius: 20px;
    margin-top: 9px;
}

.bar {
    height: 8px;
    background: #796ef0;
    border-radius: 20px;
}

.announcement {
    padding: 13px 0;
    border-bottom: 1px solid #eee;
    font-size: 13px;
}

.announcement:last-child {
    border: none;
}

.announcement small {
    color: #969bad;
    display: block;
    margin-top: 6px;
}

.schedule {
    display: flex;
    gap: 14px;
    align-items: center;
    margin-bottom: 17px;
    font-size: 13px;
}

.time {
    background: #efedff;
    color: #6d63e5;
    padding: 12px;
    border-radius: 10px;
    font-weight: 700;
}

/* PAGES */
.page {
    display: none;
}

.page.active {
    display: block;
}

table {
    width: 100%;
    border-collapse: collapse;
    font-size: 13px;
}

th, td {
    padding: 15px 10px;
    text-align: left;
    border-bottom: 1px solid #eee;
}

th {
    color: #888da3;
}

.badge {
    background: #e8f8ef;
    color: #22995c;
    padding: 6px 10px;
    border-radius: 20px;
    font-size: 11px;
}

button {
    background: #7168ec;
    color: white;
    border: none;
    padding: 11px 18px;
    border-radius: 9px;
    cursor: pointer;
}

button:hover {
    background: #5b51d2;
}

@media(max-width: 900px) {
    .stats { grid-template-columns: repeat(2, 1fr); }
    .content { grid-template-columns: 1fr; }
}

@media(max-width: 600px) {
    .sidebar {
        width: 75px;
        padding: 20px 8px;
    }

    .logo { font-size: 13px; text-align: center; }
    .sidebar h4 { display: none; }
    .sidebar a {
        font-size: 0;
        text-align: center;
        padding: 15px 5px;
    }

    .sidebar a::first-letter {
        font-size: 19px;
    }

    .main {
        margin-left: 75px;
        width: calc(100% - 75px);
        padding: 20px 12px;
    }

    .stats { grid-template-columns: 1fr 1fr; gap: 10px; }
    .card { padding: 15px; }
    .topbar h2 { font-size: 18px; }
    .welcome { padding: 22px; }
    .welcome h1 { font-size: 21px; }
    table { font-size: 11px; }
}
</style>
</head>

<body>
<div class="container">

<!-- SIDEBAR -->
<aside class="sidebar">
    <div class="logo">STUDENT<span>HUB.</span></div>

    <h4>MENU</h4>
    <a class="active" onclick="showPage('dashboard',this)">🏠 Dashboard</a>
    <a onclick="showPage('grades',this)">📊 My Grades</a>
    <a onclick="showPage('attendance',this)">📅 Attendance</a>
    <a onclick="showPage('schedule',this)">📚 Class Schedule</a>

    <h4>ACCOUNT</h4>
    <a onclick="showPage('profile',this)">👤 My Profile</a>
    <a onclick="logout()">🚪 Logout</a>
</aside>

<!-- MAIN -->
<main class="main">

<div class="topbar">
    <div>
        <h2 id="pageTitle">Dashboard</h2>
        <p>Welcome back! Here's your academic overview.</p>
    </div>
    <div class="profile">
        <div>
            <strong>Alex Santos</strong>
            <p>BS Information Technology</p>
        </div>
        <div class="avatar">AS</div>
    </div>
</div>

<!-- DASHBOARD -->
<div id="dashboard" class="page active">

    <div class="welcome">
        <h1>Hello, Alex! 👋</h1>
        <p>Welcome to your student portal. Keep learning and achieving your goals!</p>
    </div>

    <div class="stats">
        <div class="card">
            <div class="icon">📚</div>
            <small>Enrolled Subjects</small>
            <h2>6</h2>
            <p>This semester</p>
        </div>

        <div class="card">
            <div class="icon">⭐</div>
            <small>General Average</small>
            <h2>92.5</h2>
            <p>Excellent performance</p>
        </div>

        <div class="card">
            <div class="icon">📅</div>
            <small>Attendance</small>
            <h2>95%</h2>
            <p>Overall attendance</p>
        </div>

        <div class="card">
            <div class="icon">📝</div>
            <small>Pending Tasks</small>
            <h2>3</h2>
            <p>Activities to complete</p>
        </div>
    </div>

    <div class="content">
        <div class="section">
            <h3>📈 Academic Performance</h3>

            <div class="subject">
                <div style="width:100%">
                    <div style="display:flex;justify-content:space-between">
                        <span>Web Development</span><b>95%</b>
                    </div>
                    <div class="progress"><div class="bar" style="width:95%"></div></div>
                </div>
            </div>

            <div class="subject">
                <div style="width:100%">
                    <div style="display:flex;justify-content:space-between">
                        <span>Database Management</span><b>90%</b>
                    </div>
                    <div class="progress"><div class="bar" style="width:90%"></div></div>
                </div>
            </div>

            <div class="subject">
                <div style="width:100%">
                    <div style="display:flex;justify-content:space-between">
                        <span>Programming</span><b>92%</b>
                    </div>
                    <div class="progress"><div class="bar" style="width:92%"></div></div>
                </div>
            </div>

            <div class="subject">
                <div style="width:100%">
                    <div style="display:flex;justify-content:space-between">
                        <span>Networking</span><b>88%</b>
                    </div>
                    <div class="progress"><div class="bar" style="width:88%"></div></div>
                </div>
            </div>
        </div>

        <div class="section">
            <h3>📢 Announcements</h3>

            <div class="announcement">
                <b>Enrollment Reminder</b>
                <small>Check your enrollment status.</small>
            </div>

            <div class="announcement">
                <b>Midterm Examination</b>
                <small>Prepare for your upcoming exams.</small>
            </div>

            <div class="announcement">
                <b>School Event</b>
                <small>Join the upcoming campus activities.</small>
            </div>
        </div>
    </div>

    <div class="section">
        <h3>🕒 Today's Classes</h3>
        <div class="schedule">
            <div class="time">8:00 AM</div>
            <div><b>Web Development</b><p>Room 301</p></div>
        </div>
        <div class="schedule">
            <div class="time">10:00 AM</div>
            <div><b>Database Management</b><p>Room 204</p></div>
        </div>
        <div class="schedule">
            <div class="time">1:00 PM</div>
            <div><b>Programming</b><p>Computer Laboratory</p></div>
        </div>
    </div>
</div>

<!-- GRADES -->
<div id="grades" class="page">
    <div class="section">
        <h3>📊 My Grades</h3>
        <table>
            <tr><th>Subject</th><th>Grade</th><th>Status</th></tr>
            <tr><td>Web Development</td><td>95</td><td><span class="badge">Passed</span></td></tr>
            <tr><td>Programming</td><td>92</td><td><span class="badge">Passed</span></td></tr>
            <tr><td>Database Management</td><td>90</td><td><span class="badge">Passed</span></td></tr>
            <tr><td>Networking</td><td>88</td><td><span class="badge">Passed</span></td></tr>
            <tr><td>Mathematics</td><td>94</td><td><span class="badge">Passed</span></td></tr>
            <tr><td>Purposive Communication</td><td>96</td><td><span class="badge">Passed</span></td></tr>
        </table>
    </div>
</div>

<!-- ATTENDANCE -->
<div id="attendance" class="page">
    <div class="section">
        <h3>📅 Attendance Record</h3>
        <table>
            <tr><th>Date</th><th>Subject</th><th>Status</th></tr>
            <tr><td>Nov 24</td><td>Web Development</td><td><span class="badge">Present</span></td></tr>
            <tr><td>Nov 23</td><td>Programming</td><td><span class="badge">Present</span></td></tr>
            <tr><td>Nov 22</td><td>Networking</td><td><span class="badge">Present</span></td></tr>
            <tr><td>Nov 21</td><td>Mathematics</td><td><span class="badge">Present</span></td></tr>
        </table>
    </div>
</div>

<!-- SCHEDULE -->
<div id="schedule" class="page">
    <div class="section">
        <h3>📚 Weekly Class Schedule</h3>
        <table>
            <tr><th>Day</th><th>Time</th><th>Subject</th><th>Room</th></tr>
            <tr><td>Monday</td><td>8:00 AM</td><td>Web Development</td><td>301</td></tr>
            <tr><td>Tuesday</td><td>10:00 AM</td><td>Programming</td><td>Lab 1</td></tr>
            <tr><td>Wednesday</td><td>1:00 PM</td><td>Networking</td><td>204</td></tr>
            <tr><td>Thursday</td><td>8:00 AM</td><td>Database</td><td>302</td></tr>
            <tr><td>Friday</td><td>9:00 AM</td><td>Mathematics</td><td>205</td></tr>
        </table>
    </div>
</div>

<!-- PROFILE -->
<div id="profile" class="page">
    <div class="section">
        <h3>👤 Student Profile</h3>
        <div class="avatar" style="width:80px;height:80px;font-size:25px;margin-bottom:20px">AS</div>
        <p><b>Full Name:</b> Alex Santos</p><br>
        <p><b>Student ID:</b> 2026-00123</p><br>
        <p><b>Course:</b> BS Information Technology</p><br>
        <p><b>Year Level:</b> 2nd Year</p><br>
        <p><b>Email:</b> alex@student.edu</p><br>
        <p><b>School Year:</b> 2026-2027</p>
    </div>
</div>

</main>
</div>

<script>
function showPage(page, element) {
    document.querySelectorAll('.page').forEach(p => {
        p.classList.remove('active');
    });

    document.getElementById(page).classList.add('active');

    document.querySelectorAll('.sidebar a').forEach(a => {
        a.classList.remove('active');
    });

    element.classList.add('active');

    const titles = {
        dashboard: 'Dashboard',
        grades: 'My Grades',
        attendance: 'Attendance',
        schedule: 'Class Schedule',
        profile: 'My Profile'
    };

    document.getElementById('pageTitle').innerText = titles[page];
}

function logout() {
    if(confirm('Are you sure you want to logout?')) {
        alert('You have been logged out!');
    }
}
</script>

</body>
</html>
