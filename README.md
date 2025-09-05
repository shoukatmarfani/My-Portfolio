# My-Portfolio
"Personal portfolio showcasing my skills, projects, and professional journey as a developer."
<!DOCTYPE html>
<html lang="en">

<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Shoukat’s Portfolio</title>
    <link rel="stylesheet" href="style.css">
    <link href="https://fonts.googleapis.com/css2?family=Poppins:wght@400;600&display=swap" rel="stylesheet">
</head>

<body>
    <!-- Header Section -->
    <header>
        <h1 class="typing">Welcome to My Portfolio</h1>
        <p>Frontend Developer | Data Entry Specialist | Web Enthusiast</p>
    </header>

    <!-- Navigation -->
    <nav>
        <a href="#about">About</a>
        <a href="#skills">Skills</a>
        <a href="#projects">Projects</a>
        <a href="#contact">Contact</a>
        <button onclick="toggleDarkMode()">🌙 Dark Mode</button>

    </nav>

    <!-- About Section -->
    <section id="about">
        <h2>About Me</h2>
        <div class="card fade-in">
            <p>
                Hello! My name is <strong>Shoukat Ali</strong>. Through this website, I showcase my skills and projects.
                This portfolio reflects my journey and growth as a developer 🚀.
            </p>
        </div>
    </section>

    </section>

    <!-- Skills Section -->
    <section id="skills">
        <h2>My Skills</h2>
        <div class="card fade-in">
            <ul>
                <li> HTML5, CSS3, JavaScript</li>
                <li> Responsive Web Design</li>
                <li> Data Entry & Data Management</li>
                <li> Google Sheets Automation</li>
                <li> Problem Solving & Continuous Learning</li>
            </ul>
        </div>
    </section>

    <!-- Projects Section -->
    <section id="projects">
        <h2>My Projects</h2>
        <div class="card fade-in">
            <h3>Portfolio Website</h3>
            <p>A personal website built to showcase my skills, projects, and growth journey.</p>
            <button onclick="showMessage()">View Demo</button>
        </div>
        <div class="card fade-in">
            <h3>Data Management Dashboard</h3>
            <p>A project integrating Google Sheets and web tools to manage data efficiently.</p>
        </div>
        <div class="card fade-in">
            <h3>Simple Web Apps</h3>
            <p>Small JavaScript-based applications to practice coding and problem-solving.</p>
        </div>
    </section>

    <!-- Contact Section -->
    <section id="contact">
        <h2>Contact Me</h2>
        <div class="card fade-in">
            <p>📧 Email:shoukatmarfani@gmail.com</p>
            <p>🔗 LinkedIn: <a href="#">www.linkedin.com/in/shoukat-marfani</a></p>
        </div>
    </section>

    <!-- Footer -->
    <footer>
        <p>© 2025 Shoukat’s Portfolio Website | Built with HTML, CSS & JavaScript</p>
        <div class="social-icons">
            <a href="www.linkedin.com/in/shoukat-marfani" target="_blank">🔗 LinkedIn</a> |
            <a href="https://github.com/shoukatmarfani" target="_blank">💻 GitHub</a> |
            <a href="shoukatmarfani@gmail.com">📧 Email</a>
        </div>
        <div class="card fade-in">
            <img src="project1.png" alt="Portfolio Project" class="project-img">
            <h3>Portfolio Website</h3>
            <p>A personal website built to showcase my skills, projects, and growth journey.</p>
            <button onclick="showMessage()">View Demo</button>
        </div>


    </footer>

    <!-- JavaScript -->
    <script src="script.js"></script>
    // Show alert message
function showMessage() {
  alert("🚀 Thanks for checking out my Portfolio Project!");
}

// Fade-in effect on scroll
const faders = document.querySelectorAll('.fade-in');

const appearOptions = {
  threshold: 0.2,
  rootMargin: "0px 0px -50px 0px"
};

const appearOnScroll = new IntersectionObserver(function(entries, appearOnScroll) {
  entries.forEach(entry => {
    if (!entry.isIntersecting) return;
    entry.target.classList.add("appear");
    appearOnScroll.unobserve(entry.target);
  });
}, appearOptions);

faders.forEach(fader => {
  appearOnScroll.observe(fader);
});
function toggleDarkMode() {
  document.body.classList.toggle("dark-mode");
}
/* Global Styles */
body {
  font-family: 'Poppins', sans-serif;
  margin: 0;
  padding: 0;
  background: #f8f9ff;
  color: #333;
}

/* Header */
header {
  background: linear-gradient(135deg, #ff512f, #dd2476);
  color: white;
  text-align: center;
  padding: 3rem 1rem;
}

header h1 {
  margin: 0;
  font-size: 3rem;
  font-weight: 600;
}

header p {
  margin-top: 0.5rem;
  font-size: 1.2rem;
}

/* Navigation */
nav {
  background: #222;
  padding: 1rem;
  text-align: center;
}

nav a {
  color: #fff;
  margin: 0 15px;
  text-decoration: none;
  font-weight: 500;
  transition: color 0.3s ease;
}

nav a:hover {
  color: #ffcc00;
}

/* Sections */
section {
  padding: 3rem 2rem;
  max-width: 1100px;
  margin: auto;
}

section h2 {
  text-align: center;
  font-size: 2rem;
  margin-bottom: 2rem;
  color: #dd2476;
}

/* Cards */
.card {
  background: white;
  padding: 1.5rem;
  margin-bottom: 1.5rem;
  border-radius: 12px;
  box-shadow: 0 6px 15px rgba(0,0,0,0.1);
  transition: transform 0.3s ease, box-shadow 0.3s ease;
}

.card:hover {
  transform: translateY(-5px);
  box-shadow: 0 10px 20px rgba(0,0,0,0.15);
}

/* Skills List */
ul {
  list-style: none;
  padding: 0;
}

ul li {
  background: #ffeef5;
  margin: 8px 0;
  padding: 10px;
  border-radius: 6px;
}

/* Buttons */
button {
  background: linear-gradient(135deg, #2575fc, #6a11cb);
  color: white;
  border: none;
  padding: 10px 20px;
  border-radius: 6px;
  cursor: pointer;
  transition: background 0.3s ease;
}

button:hover {
  background: linear-gradient(135deg, #6a11cb, #2575fc);
}

/* Footer */
footer {
  background: #222;
  color: white;
  text-align: center;
  padding: 1rem;
  margin-top: 2rem;
}

/* Animations */
.fade-in {
  opacity: 0;
  transform: translateY(20px);
  animation: fadeInUp 1s ease forwards;
}

@keyframes fadeInUp {
  to {
    opacity: 1;
    transform: translateY(0);
  }
}

/* Typing Effect */
.typing {
  border-right: 3px solid #fff;
  white-space: nowrap;
  overflow: hidden;
  width: 0;
  animation: typing 4s steps(30, end) forwards, blink 0.8s infinite;
}

@keyframes typing {
  from { width: 0; }
  to { width: 100%; }
}

@keyframes blink {
  50% { border-color: transparent; }
}
header {
  background: linear-gradient(270deg, #ff512f, #dd2476, #2575fc, #6a11cb);
  background-size: 800% 800%;
  animation: gradientBG 15s ease infinite;
  color: white;
  text-align: center;
  padding: 3rem 1rem;
}

@keyframes gradientBG {
  0% {background-position: 0% 50%;}
  50% {background-position: 100% 50%;}
  100% {background-position: 0% 50%;}
}
.social-icons a {
  color: #ffcc00;
  margin: 0 10px;
  text-decoration: none;
  font-weight: 600;
}

.social-icons a:hover {
  color: #fff;
}
.project-img {
  width: 100%;
  border-radius: 10px;
  margin-bottom: 10px;
}
.dark-mode {
  background: #121212;
  color: #f1f1f1;
}

.dark-mode .card {
  background: #1e1e1e;
  color: #fff;
}

.dark-mode nav {
  background: #000;
}

</body>

</html>
