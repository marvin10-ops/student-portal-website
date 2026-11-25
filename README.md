
<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <meta name="description" content="Student Portal Dashboard">
  <title>EduConnect | Student Portal</title>
  <link rel="stylesheet" href="style.css">
  <link rel="preconnect" href="https://fonts.googleapis.com">
  <link rel="preconnect" href="https://fonts.gstatic.com" crossorigin>
  <link href="https://fonts.googleapis.com/css2?family=Inter:wght@400;500;600;700;800&display=swap" rel="stylesheet">
</head>
<body>
  <div class="app">
    <aside class="sidebar" id="sidebar">
      <div class="brand">
        <div class="brand-icon">E</div>
        <span>EduConnect</span>
      </div>

      <div class="nav-label">MAIN MENU</div>
      <nav>
        <button class="nav-link active" data-page="dashboard">⌂ <span>Dashboard</span></button>
        <button class="nav-link" data-page="schedule">▦ <span>Class Schedule</span></button>
        <button class="nav-link" data-page="grades">▤ <span>My Grades</span></button>
        <button class="nav-link" data-page="announcements">♢ <span>Announcements</span></button>
        <button class="nav-link" data-page="profile">◉ <span>My Profile</span></button>
      </nav>

      <div class="sidebar-bottom">
        <div class="help-card">
          <div class="help-icon">✦</div>
          <strong>Need help?</strong>
          <p>Contact the student support team for assistance.</p>
          <a href="mailto:support@example.com">Get Support →</a>
        </div>
        <div class="sidebar-user">
          <div class="avatar">JD</div>
          <div><strong>Jamie Davis</strong><small>Student Account</small></div>
        </div>
      </div>
    </aside>

    <main class="main">
      <header class="topbar">
        <button class="menu-toggle" id="menuToggle" aria-label="Toggle menu">☰</button>
        <div class="breadcrumb">Student Portal <span>/</span> <b id="breadcrumb">Dashboard</b></div>
        <div class="top-actions">
          <span class="semester">● Second Semester 2026</span>
          <button class="notification" id="notificationBtn" aria-label="Notifications">♧<i></i></button>
          <div class="avatar small">JD</div>
        </div>
      </header>

      <section class="content">
        <!-- DASHBOARD -->
        <section class="page active" id="dashboard">
          <div class="welcome">
            <div>
              <p class="eyebrow">TUESDAY, NOVEMBER 25, 2026</p>
              <h1>Welcome back, Jamie! 👋</h1>
              <p class="muted">Here's what's happening with your academics today.</p>
            </div>
            <div class="welcome-art">🎓</div>
          </div>

          <div class="stats-grid">
            <article class="stat-card">
              <div class="stat-icon purple">▦</div>
              <p>Enrolled Subjects</p>
              <h2>6</h2>
              <small>For this semester</small>
            </article>
            <article class="stat-card">
              <div class="stat-icon blue">◷</div>
              <p>Classes This Week</p>
              <h2>18</h2>
              <small>Across 5 school days</small>
            </article>
            <article class="stat-card">
              <div class="stat-icon green">★</div>
              <p>General Average</p>
              <h2>92.5%</h2>
              <small class="positive">↑ Excellent performance</small>
            </article>
            <article class="stat-card">
              <div class="stat-icon orange">♧</div>
              <p>Announcements</p>
              <h2>3</h2>
              <small>Latest school updates</small>
            </article>
          </div>

          <div class="dashboard-grid">
            <article class="panel">
              <div class="panel-heading">
                <div><h3>Today's Schedule</h3><p class="muted">Your upcoming classes</p></div>
                <button class="text-button" data-goto="schedule">View all →</button>
              </div>
              <div class="class-list">
                <div class="class-item">
                  <div class="time">08:00<br><small>09:30 AM</small></div>
                  <div class="class-color purple-line"></div>
                  <div class="class-info"><strong>Web Development</strong><small>Room 301 · Prof. Anderson</small></div>
                  <span class="class-tag">Lecture</span>
                </div>
                <div class="class-item">
                  <div class="time">10:00<br><small>11:30 AM</small></div>
                  <div class="class-color blue-line"></div>
                  <div class="class-info"><strong>Database Management</strong><small>Computer Lab 2 · Prof. Smith</small></div>
                  <span class="class-tag">Laboratory</span>
                </div>
                <div class="class-item">
                  <div class="time">01:00<br><small>02:30 PM</small></div>
                  <div class="class-color green-line"></div>
                  <div class="class-info"><strong>Human-Computer Interaction</strong><small>Room 205 · Prof. Wilson</small></div>
                  <span class="class-tag">Lecture</span>
                </div>
              </div>
            </article>

            <article class="panel">
              <div class="panel-heading">
                <div><h3>Recent Announcements</h3><p class="muted">Stay updated with campus news</p></div>
                <button class="text-button" data-goto="announcements">See all →</button>
              </div>
              <div class="announcement-mini">
                <div class="announcement-icon purple">📢</div>
                <div><strong>Final Examination Schedule</strong><p>Final exam schedules are now available.</p><small>November 24, 2026</small></div>
              </div>
              <div class="announcement-mini">
                <div class="announcement-icon orange">📅</div>
                <div><strong>Campus Technology Week</strong><p>Join us for exciting campus activities!</p><small>November 22, 2026</small></div>
              </div>
              <div class="announcement-mini">
                <div class="announcement-icon green">✓</div>
                <div><strong>Enrollment Reminder</strong><p>Check your enrollment information.</p><small>November 20, 2026</small></div>
              </div>
            </article>
          </div>

          <article class="panel performance">
            <div class="panel-heading">
              <div><h3>Academic Performance</h3><p class="muted">Your latest subject grades</p></div>
              <button class="text-button" data-goto="grades">View grades →</button>
            </div>
            <div id="dashboardGrades"></div>
          </article>
        </section>

        <!-- SCHEDULE -->
        <section class="page" id="schedule">
          <div class="page-heading"><p class="eyebrow">ACADEMICS</p><h1>Class Schedule</h1><p class="muted">Your weekly academic timetable.</p></div>
          <article class="panel">
            <div class="panel-heading"><div><h3>Second Semester</h3><p class="muted">Academic Year 2026–2027</p></div><span class="semester">Weekly Schedule</span></div>
            <div class="table-wrap">
              <table>
                <thead><tr><th>Subject</th><th>Day</th><th>Time</th><th>Room</th><th>Instructor</th></tr></thead>
                <tbody id="scheduleRows"></tbody>
              </table>
            </div>
          </article>
        </section>

        <!-- GRADES -->
        <section class="page" id="grades">
          <div class="page-heading"><p class="eyebrow">ACADEMICS</p><h1>My Grades</h1><p class="muted">Track your academic progress this semester.</p></div>
          <div class="grade-summary">
            <article class="stat-card"><p>General Average</p><h2>92.5%</h2><small class="positive">Excellent</small></article>
            <article class="stat-card"><p>Subjects Completed</p><h2>6</h2><small>Current semester</small></article>
            <article class="stat-card"><p>Academic Standing</p><h2 class="standing">Good</h2><small>Keep it up!</small></article>
          </div>
          <article class="panel">
            <div class="panel-heading"><div><h3>Subject Grade Breakdown</h3><p class="muted">Fictional academic records</p></div></div>
            <div class="table-wrap"><table>
              <thead><tr><th>Subject</th><th>Code</th><th>Grade</th><th>Remarks</th></tr></thead>
              <tbody id="gradeRows"></tbody>
            </table></div>
          </article>
        </section>

        <!-- ANNOUNCEMENTS -->
        <section class="page" id="announcements">
          <div class="page-heading"><p class="eyebrow">CAMPUS NEWS</p><h1>Announcements</h1><p class="muted">Important updates and information from your school.</p></div>
          <div class="announcement-grid" id="announcementCards"></div>
        </section>

        <!-- PROFILE -->
        <section class="page" id="profile">
          <div class="page-heading"><p class="eyebrow">ACCOUNT</p><h1>My Profile</h1><p class="muted">View your student information.</p></div>
          <article class="panel profile-card">
            <div class="profile-banner"></div>
            <div class="profile-avatar">JD</div>
            <div class="profile-intro"><h2>Jamie Davis</h2><p class="muted">BS Information Technology · 3rd Year</p><span class="profile-status">● Active Student</span></div>
            <div class="profile-details">
              <div><small>Student ID</small><strong>2026-00125</strong></div>
              <div><small>Email Address</small><strong>jamie.davis@example.com</strong></div>
              <div><small>Department</small><strong>College of Information Technology</strong></div>
              <div><small>Year Level</small><strong>Third Year</strong></div>
              <div><small>Academic Year</small><strong>2026–2027</strong></div>
              <div><small>Enrollment Status</small><strong>Regular</strong></div>
            </div>
          </article>
        </section>
      </section>
      <footer>© 2026 EduConnect Student Portal. For demonstration purposes only.</footer>
    </main>
  </div>
  <div class="toast" id="toast" role="status"></div>
  <script src="script.js"></script>
</body>
</html>
