<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>My Portfolio</title>
  <link rel="stylesheet" href="styles.css">
</head>
<body>
  <header>
    <h1>Liliana Jimenez</h1>
    <nav>
      <ul>
        <li><a href="#about">About Me</a></li>
        <li><a href="#resume">Resume</a></li>
        <li><a href="#work">Samples of Work</a></li>
      </ul>
    </nav>
  </header>

  <section id="about">
    <h2>About Me</h2>
    <p>Bilingual IT Business Analyst and Project Manager with over 6 years of experience in healthcare technology, process optimization, QA, and stakeholder communications. Passionate about improving systems and creating user-centered solutions.</p>
  </section>

  <section id="resume">
    <h2>Resume</h2>
    <p><strong>Current Role:</strong> IT Business Analyst at Family Health Centers of San Diego</p>
    <p><strong>Skills:</strong> Project Management, DevOps knowledge, SQL, QA Testing, Customer Relations, Bilingual (English/Spanish), Fast Learner, Detail Oriented</p>
    <p><strong>Education:</strong> MA & BA in Spanish, San Diego State University</p>
    <p><strong>Certifications:</strong> Product Management, Project Management, SQL</p>
    <p><strong>Experience:</strong></p>
    <ul>
      <li>Led software implementations, QA, and stakeholder training.</li>
      <li>Managed SQL reporting, requirement gathering, and support services.</li>
      <li>Developed training materials, test plans, and process workflows.</li>
    </ul>
  </section>

<section id="work">
  <h2>📁 Samples of Work</h2>

  <div class="tab-container">
    <div class="tabs">
      <button class="tab-button active" data-tab="roadmap">📌 Roadmap</button>
      <button class="tab-button" data-tab="personas">👤 User Personas</button>
      <button class="tab-button" data-tab="prd">📄 Product Requirement Document</button>
      <button class="tab-button" data-tab="wireframe">🖼️ Wireframe Sample</button>
    </div>

    <div class="tab-content active" id="roadmap">
      <iframe 
        src="https://docs.google.com/document/d/e/2PACX-1vTPn5U66HwfeSZQn9PjbtD4FvnSh3MmD9fa9FakD37P-wlKdP-DuqkA5-KvnfQsu7B9cAS7kN6bcAsh/pub?embedded=true"
        width="100%" 
        height="600" 
        style="border: none;" 
        title="Netflix Roadmap">
      </iframe>
    </div>

    <div class="tab-content" id="personas">
      <iframe 
        src="https://docs.google.com/document/d/e/2PACX-1vRmB0JWZISW6kvpZTHglDbGY1ty82JMaXExlLuSijmSA3AmrIkv65RI85bLF6lNFivqSqOttjh4Oz9Z/pub?embedded=true" 
        width="100%" 
        height="600" 
        style="border: none;" 
        title="Netflix User Personas">
      </iframe>
    </div>

    <div class="tab-content" id="prd">
      <iframe 
        src="https://docs.google.com/document/d/e/2PACX-1vSpyxU9IeJKqNup4zkmbcjisPejpnSJuQNQcqGKTZIsibue0sLKqXCG0OId4DWQ-fo4vidFPqdrQmzH/pub?embedded=true" 
        width="100%" 
        height="600" 
        style="border: none;" 
        title="Netflix PRD">
      </iframe>
    </div>

  <div class="tab-content" id="wireframe">
  <h3>🖼️ Wireframe Sample</h3>
  <p>Click below to view the Netflix wireframe created using Balsamiq:</p>
  <a href="https://balsamiq.cloud/s878st3/p6whak5" target="_blank" rel="noopener noreferrer">
    🔗 View Netflix Wireframe
  </a>
</div>

body {
  font-family: Arial, sans-serif;
  margin: 0;
  padding: 0;
  background: #f9f9f9;
  color: #333;
}

header {
  background-color: #006699;
  color: white;
  padding: 1rem;
  text-align: center;
}

nav ul {
  list-style: none;
  padding: 0;
}

nav ul li {
  display: inline;
  margin: 0 1rem;
}

nav ul li a {
  color: white;
  text-decoration: none;
}

section {
  padding: 2rem;
}

h2 {
  color: #006699;
}

footer {
  text-align: center;
  background: #ddd;
  padding: 1rem;
  margin-top: 2rem;
}
  
  .tab-container {
  margin-top: 2rem;
}

.tabs {
  display: flex;
  flex-wrap: wrap;
  margin-bottom: 1rem;
}

.tab-button {
  padding: 10px 20px;
  border: none;
  background-color: #eee;
  cursor: pointer;
  margin-right: 10px;
  border-radius: 5px;
  transition: background 0.3s;
}

.tab-button.active {
  background-color: #006699;
  color: white;
}

.tab-content {
  display: none;
}

.tab-content.active {
  display: block;
}
// Simple log to test JS
console.log("Portfolio loaded.");
const tabButtons = document.querySelectorAll('.tab-button');
const tabContents = document.querySelectorAll('.tab-content');

tabButtons.forEach(button => {
  button.addEventListener('click', () => {
    // Remove active from all buttons and contents
    tabButtons.forEach(btn => btn.classList.remove('active'));
    tabContents.forEach(tab => tab.classList.remove('active'));

    // Activate the clicked button and corresponding tab
    button.classList.add('active');
    document.getElementById(button.dataset.tab).classList.add('active');
  });
});
