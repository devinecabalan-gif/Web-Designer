# Web-Designer
<html lang="en">
<head>
  <meta charset="UTF-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1.0" />
  <title>Dave Cabalan - Web Designer</title>
  <style>
    /* ---------- GLOBAL STYLES ---------- */
    * {
      box-sizing: border-box;
      margin: 0;
      padding: 0;
      font-family: 'Poppins', sans-serif;
    }

    body {
      background-color: #f4f4f9;
      color: #333;
      line-height: 1.6;
    }

    header {
      background-color: #1f1f1f;
      color: #fff;
      padding: 20px 0;
      text-align: center;
    }

    header h1 {
      margin-bottom: 5px;
      font-size: 2em;
    }

    nav ul {
      list-style: none;
      display: flex;
      justify-content: center;
      gap: 20px;
      margin-top: 10px;
    }

    nav a {
      color: #fff;
      text-decoration: none;
      font-weight: bold;
      transition: 0.3s;
    }

    nav a:hover {
      color: #ff6f61;
    }

    /* ---------- HERO SECTION ---------- */
    .hero {
      background: linear-gradient(rgba(0, 0, 0, 0.6), rgba(0, 0, 0, 0.6)),
                  url('https://images.unsplash.com/photo-1517248135467-4c7edcad34c4?auto=format&fit=crop&w=1920&q=80');
      background-size: cover;
      background-position: center;
      color: white;
      height: 70vh;
      display: flex;
      flex-direction: column;
      justify-content: center;
      align-items: center;
      text-align: center;
    }

    .hero h2 {
      font-size: 2.5em;
      margin-bottom: 10px;
    }

    .hero p {
      font-size: 1.2em;
      max-width: 600px;
    }

    .hero a {
      background-color: #ff6f61;
      color: white;
      padding: 12px 25px;
      border-radius: 5px;
      text-decoration: none;
      margin-top: 20px;
      display: inline-block;
      transition: 0.3s;
    }

    .hero a:hover {
      background-color: #e65b50;
      transform: scale(1.05);
    }

    /* ---------- ABOUT SECTION ---------- */
    .about {
      padding: 60px 20px;
      text-align: center;
      background-color: #fff;
    }

    .about h2 {
      font-size: 2em;
      margin-bottom: 20px;
      color: #1f1f1f;
    }

    .about p {
      max-width: 800px;
      margin: 0 auto;
      font-size: 1.1em;
    }

    /* ---------- PROJECTS SECTION ---------- */
    .projects {
      background-color: #fafafa;
      padding: 60px 20px;
      text-align: center;
    }

    .projects h2 {
      margin-bottom: 40px;
      color: #1f1f1f;
    }

    .project-grid {
      display: flex;
      flex-wrap: wrap;
      justify-content: center;
      gap: 30px;
    }

    .project-card {
      background: white;
      width: 300px;
      border-radius: 8px;
      box-shadow: 0 2px 10px rgba(0,0,0,0.1);
      overflow: hidden;
      transition: transform 0.3s ease;
      cursor: pointer;
    }

    .project-card:hover {
      transform: translateY(-5px);
    }

    .project-card img {
      width: 100%;
      height: 200px;
      object-fit: cover;
    }

    .project-card h3 {
      margin: 15px;
    }

    .project-card p {
      margin: 0 15px 20px;
      font-size: 0.95em;
      color: #555;
    }

    /* ---------- CONTACT SECTION ---------- */
    .contact {
      padding: 60px 20px;
      background-color: #1f1f1f;
      color: white;
      text-align: center;
    }

    .contact h2 {
      margin-bottom: 20px;
    }

    .contact p {
      font-size: 1.1em;
      margin-bottom: 10px;
    }

    footer {
      background-color: #111;
      color: white;
      text-align: center;
      padding: 15px;
      font-size: 0.9em;
    }

    /* ---------- MODAL STYLES ---------- */
    .modal {
      display: none;
      position: fixed;
      z-index: 10;
      left: 0;
      top: 0;
      width: 100%;
      height: 100%;
      overflow: auto;
      background-color: rgba(0, 0, 0, 0.6);
      animation: fadeInBg 0.4s ease;
    }

    @keyframes fadeInBg {
      from { opacity: 0; }
      to { opacity: 1; }
    }

    .modal-content {
      background-color: #fff;
      margin: 10% auto;
      padding: 30px;
      border-radius: 10px;
      width: 80%;
      max-width: 550px;
      text-align: center;
      box-shadow: 0 2px 10px rgba(0,0,0,0.3);
      transform: translateY(-20px);
      animation: slideUp 0.4s ease forwards;
    }

    @keyframes slideUp {
      from { opacity: 0; transform: translateY(50px); }
      to { opacity: 1; transform: translateY(0); }
    }

    .modal-content h2 {
      color: #ff6f61;
      margin-bottom: 15px;
    }

    .modal-content p {
      margin-bottom: 10px;
      color: #444;
    }

    .modal-content a.btn {
      display: inline-block;
      margin-top: 10px;
      background-color: #ff6f61;
      color: white;
      padding: 10px 20px;
      border-radius: 5px;
      text-decoration: none;
      transition: 0.3s;
    }

    .modal-content a.btn:hover {
      background-color: #e65b50;
      transform: scale(1.05);
    }

    .close {
      color: #333;
      float: right;
      font-size: 24px;
      font-weight: bold;
      cursor: pointer;
    }

    .close:hover {
      color: #ff6f61;
    }

    @media (max-width: 768px) {
      .project-grid {
        flex-direction: column;
        align-items: center;
      }
    }
  </style>
</head>
<body>
  <header>
    <h1>Dave Cabalan</h1>
    <p>Web Designer & Developer</p>
    <nav>
      <ul>
        <li><a href="#hero">Home</a></li>
        <li><a href="#about">About</a></li>
        <li><a href="#projects">Projects</a></li>
        <li><a href="#contact">Contact</a></li>
      </ul>
    </nav>
  </header>

  <section class="hero" id="hero">
    <h2>Creating Modern & Responsive Websites</h2>
    <p>Crafting digital experiences with creativity, precision, and passion for clean design.</p>
    <a href="#projects">View My Work</a>
  </section>

  <section class="about" id="about">
    <h2>About Me</h2>
    <p>Hello! I'm Dave Cabalan, a passionate web designer and developer with a love for crafting user-friendly websites. My focus is on creating elegant and functional designs that look great on all devices.</p>
  </section>

  <section class="projects" id="projects">
    <h2>My Projects</h2>
    <div class="project-grid">
      <div class="project-card" onclick="openModal('modal1')">
        <img src="https://images.unsplash.com/photo-1522202176988-66273c2fd55f" alt="Project 1">
        <h3>Portfolio Website</h3>
        <p>A responsive and elegant portfolio showcasing my design work.</p>
      </div>
      <div class="project-card" onclick="openModal('modal2')">
        <img src="https://images.unsplash.com/photo-1498050108023-c5249f4df085" alt="Project 2">
        <h3>Business Landing Page</h3>
        <p>A sleek, professional site for a modern tech startup.</p>
      </div>
      <div class="project-card" onclick="openModal('modal3')">
        <img src="https://images.unsplash.com/photo-1556761175-5973dc0f32e7" alt="Project 3">
        <h3>Coffee Shop Site</h3>
        <p>A cozy, warm website design for a local coffee brand.</p>
      </div>
    </div>
  </section>

  <!-- MODALS -->
  <div id="modal1" class="modal">
    <div class="modal-content">
      <span class="close" onclick="closeModal('modal1')">&times;</span>
      <h2>Portfolio Website</h2>
      <p>This portfolio is designed to showcase creativity and functionality with a sleek, mobile-friendly interface.</p>
      <p><strong>Tech Used:</strong> HTML, CSS, JavaScript</p>
      <a href="https://example.com/portfolio" target="_blank" class="btn">View Live Demo</a>
    </div>
  </div>

  <div id="modal2" class="modal">
    <div class="modal-content">
      <span class="close" onclick="closeModal('modal2')">&times;</span>
      <h2>Business Landing Page</h2>
      <p>A modern, conversion-focused landing page featuring smooth animations and CTA sections for a startup.</p>
      <p><strong>Tech Used:</strong> HTML, CSS, Bootstrap</p>
      <a href="https://example.com/business" target="_blank" class="btn">View Live Demo</a>
    </div>
  </div>

  <div id="modal3" class="modal">
    <div class="modal-content">
      <span class="close" onclick="closeModal('modal3')">&times;</span>
      <h2>Coffee Shop Site</h2>
      <p>A warm and welcoming website for a local café, featuring an interactive menu and reservation system.</p>
      <p><strong>Tech Used:</strong> HTML, CSS, JavaScript</p>
      <a href="https://example.com/coffee" target="_blank" class="btn">View Live Demo</a>
    </div>
  </div>

  <section class="contact" id="contact">
    <h2>Contact Me</h2>
    <p>📧 davecabalan14@gmail.com</p>
    <p>📱 09955727665</p>
    <p>🌍 Based in Kitcharao, Agusan Del Norte, Philippines</p>
  </section>

  <footer>
    <p>© 2025 Dave Cabalan. All Rights Reserved.</p>
  </footer>

  <script>
    function openModal(id) {
      document.getElementById(id).style.display = "block";
    }
    function closeModal(id) {
      document.getElementById(id).style.display = "none";
    }
    window.onclick = function(event) {
      document.querySelectorAll('.modal').forEach(modal => {
        if (event.target === modal) {
          modal.style.display = 'none';
        }
      });
    };
  </script>
</body>
</html>

