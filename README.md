
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
