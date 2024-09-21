
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>My Portfolio</title>
    <link rel="stylesheet" href="style.css">
</head>
<body>
    <header>
        <nav>
            <ul>
                <li><a href="#home">Home</a></li>
                <li><a href="#about">About Me</a></li>
                <li><a href="#projects">Projects</a></li>
                <li><a href="#contact">Contact</a></li>
            </ul>
        </nav>
    </header>

    <section id="home" class="section">
        <h1>Welcome to My Portfolio</h1>
        <p>This is a place where I showcase my skills and projects.</p>
    </section>

    <section id="about" class="section">
        <h2>About Me</h2>
        <p>Hi, I'm a web developer with a passion for creating dynamic websites.</p>
    </section>

    <section id="projects" class="section">
        <h2>Projects</h2>
        <div id="project-list">
            <!-- Projects will be dynamically loaded here -->
        </div>
    </section>

    <section id="contact" class="section">
        <h2>Contact Me</h2>
        <form id="contactForm">
            <label for="name">Name:</label>
            <input type="text" id="name" name="name" required>
            <label for="email">Email:</label>
            <input type="email" id="email" name="email" required>
            <label for="message">Message:</label>
            <textarea id="message" name="message" required></textarea>
            <button type="submit">Submit</button>
        </form>
    </section>

    <footer>
        <p>&copy; 2024 My Portfolio. All rights reserved.</p>
    </footer>

    <script src="app.js"></script>
</body>
</html>
body {
    font-family: Arial, sans-serif;
    margin: 0;
    padding: 0;
    box-sizing: border-box;
    background-color: #f4f4f4;
}

header {
    background-color: #333;
    color: white;
    padding: 10px 0;
    text-align: center;
}

nav ul {
    list-style: none;
    padding: 0;
}

nav ul li {
    display: inline;
    margin-right: 20px;
}

nav ul li a {
    color: white;
    text-decoration: none;
}

.section {
    padding: 50px;
    margin: 20px;
    background-color: white;
    border-radius: 8px;
    box-shadow: 0 0 10px rgba(0, 0, 0, 0.1);
}

#project-list {
    display: flex;
    flex-wrap: wrap;
}

.project-item {
    background-color: #ddd;
    margin: 10px;
    padding: 20px;
    border-radius: 8px;
    width: calc(33% - 40px);
    box-shadow: 0 0 10px rgba(0, 0, 0, 0.1);
}

footer {
    text-align: center;
    background-color: #333;
    color: white;
    padding: 10px;
    position: fixed;
    bottom: 0;
    width: 100%;
}
// JavaScript to handle dynamic content
const projects = [
    { title: 'Project 1', description: 'Description for project 1' },
    { title: 'Project 2', description: 'Description for project 2' },
    { title: 'Project 3', description: 'Description for project 3' },
];

function loadProjects() {
    const projectList = document.getElementById('project-list');

    projects.forEach((project) => {
        const projectItem = document.createElement('div');
        projectItem.classList.add('project-item');

        const projectTitle = document.createElement('h3');
        projectTitle.innerText = project.title;

        const projectDescription = document.createElement('p');
        projectDescription.innerText = project.description;

        projectItem.appendChild(projectTitle);
        projectItem.appendChild(projectDescription);

        projectList.appendChild(projectItem);
    });
}

// Load projects when the page is ready
document.addEventListener('DOMContentLoaded', loadProjects);

// Contact form submission handler
document.getElementById('contactForm').addEventListener('submit', function(event) {
    event.preventDefault();

    const name = document.getElementById('name').value;
    const email = document.getElementById('email').value;
    const message = document.getElementById('message').value;

    alert(`Thank you, ${name}! We have received your message.`);
    // Here, you can add an AJAX call to send the data to your server or API
});

