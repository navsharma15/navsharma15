</div>

        <div class="about-content">
            <h2>🚀 What I'm Up To</h2>
            <ul class="about-list">
                <li>🔭 Building <strong>LOOPI</strong> - A modern web experience</li>
                <li>🌱 Learning <strong>Backend Development & AI/ML</strong></li>
                <li>👯 Open to collaborate on <strong>Cloud Native Projects</strong></li>
                <li>💬 Ask me about <strong>UI/UX, React, Java, Python</strong></li>
                <li>⚡ Fun fact: I enjoy blending creativity with logic!</li>
            </ul>
        </div>
    </div>

    <!-- Skills Section -->
    <div class="skills-section">
        <h2>🛠️ Tech Stack</h2>
        <div class="skills-grid">
            <div class="skill-card">
                <h3>Frontend & Design</h3>
                <div class="skill-icons">
                    <div class="skill-icon" title="HTML5">🌐</div>
                    <div class="skill-icon" title="CSS3">🎨</div>
                    <div class="skill-icon" title="JavaScript">⚡</div>
                    <div class="skill-icon" title="React">⚛️</div>
                    <div class="skill-icon" title="Figma">🎭</div>
                </div>
            </div>

            <div class="skill-card">
                <h3>Backend & Databases</h3>
                <div class="skill-icons">
                    <div class="skill-icon" title="Node.js">🟢</div>
                    <div class="skill-icon" title="PHP">🐘</div>
                    <div class="skill-icon" title="MySQL">🗄️</div>
                </div>
            </div>

            <div class="skill-card">
                <h3>Programming Languages</h3>
                <div class="skill-icons">
                    <div class="skill-icon" title="Java">☕</div>
                    <div class="skill-icon" title="Python">🐍</div>
                    <div class="skill-icon" title="C">©️</div>
                </div>
            </div>

            <div class="skill-card">
                <h3>Tools & Platforms</h3>
                <div class="skill-icons">
                    <div class="skill-icon" title="Git">📦</div>
                    <div class="skill-icon" title="Linux">🐧</div>
                    <div class="skill-icon" title="GitHub">🐙</div>
                </div>
            </div>
        </div>
    </div>

    <!-- Stats Section -->
    <div class="stats-section">
        <h2>📊 GitHub Analytics</h2>
        <div class="stats-grid">
            <div class="stat-card">
                <h3>50+</h3>
                <p>Projects Completed</p>
            </div>
            <div class="stat-card">
                <h3>1000+</h3>
                <p>Commits This Year</p>
            </div>
            <div class="stat-card">
                <h3>5+</h3>
                <p>Languages Mastered</p>
            </div>
        </div>
    </div>

    <!-- Contact Section -->
    <div class="contact-section">
        <h2>🎯 Let's Connect & Collaborate!</h2>
        <p>
            I'm always excited to connect with fellow developers and designers.<br>
            Whether you want to discuss a project, share ideas, or just say hi,<br>
            feel free to reach out!
        </p>
        <div class="social-links">
            <a href="https://linkedin.com/in/nav-sharma" target="_blank" class="social-btn">
                Let's Connect on LinkedIn
            </a>
            <a href="mailto:navdhruv12@gmail.com" class="social-btn">
                Email Me
            </a>
        </div>
    </div>

    <!-- Footer -->
    <footer>
        <p>&copy; 2026 Nav Sharma. Crafted with 💜 and code.</p>
        <p style="margin-top: 10px; opacity: 0.7;">
            "Code is like humor. When you have to explain it, it's bad." – Cory House
        </p>
    </footer>
</div>

<script>
    // Typing Animation
    const texts = [
        "UI/UX Designer",
        "Frontend Developer",
        "ReactJS Specialist",
        "Problem Solver",
        "Creative Thinker"
    ];
    
    let textIndex = 0;
    let charIndex = 0;
    let isDeleting = false;
    const typingElement = document.getElementById('typingText');
    
    function type() {
        const currentText = texts[textIndex];
        
        if (isDeleting) {
            typingElement.textContent = currentText.substring(0, charIndex - 1);
            charIndex--;
        } else {
            typingElement.textContent = currentText.substring(0, charIndex + 1);
            charIndex++;
        }
        
        if (!isDeleting && charIndex === currentText.length) {
            setTimeout(() => isDeleting = true, 2000);
        } else if (isDeleting && charIndex === 0) {
            isDeleting = false;
            textIndex = (textIndex + 1) % texts.length;
        }
        
        const speed = isDeleting ? 50 : 100;
        setTimeout(type, speed);
    }
    
    type();

    // Smooth scroll animation for cards
    const observer = new IntersectionObserver((entries) => {
        entries.forEach(entry => {
            if (entry.isIntersecting) {
                entry.target.style.opacity = '1';
                entry.target.style.transform = 'translateY(0)';
            }
        });
    });

    document.querySelectorAll('.skill-card, .stat-card').forEach(card => {
        card.style.opacity = '0';
        card.style.transform = 'translateY(30px)';
        card.style.transition = 'all 0.6s ease';
        observer.observe(card);
    });
</script>

