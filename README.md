<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>K S Sreeniranjan | AI & Robotics</title>
    
    <link href="https://unpkg.com/aos@2.3.1/dist/aos.css" rel="stylesheet">
    <script src="https://unpkg.com/typewriter-effect@latest/dist/core.js"></script>
    <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.0.0/css/all.min.css">

    <style>
        :root {
            --primary: #00f2ff; /* Cyber Blue */
            --secondary: #7000ff; /* Robotics Purple */
            --bg: #030712;
            --card-bg: rgba(17, 24, 39, 0.9);
            --text: #f3f4f6;
        }

        * { box-sizing: border-box; scroll-behavior: smooth; }
        body { background-color: var(--bg); color: var(--text); font-family: 'Inter', sans-serif; margin: 0; overflow-x: hidden; }

        /* Tech Background Canvas */
        #canvas-bg { position: fixed; top: 0; left: 0; width: 100%; height: 100%; z-index: -1; opacity: 0.4; }

        nav { position: fixed; width: 100%; padding: 20px; background: rgba(3, 7, 18, 0.9); backdrop-filter: blur(12px); z-index: 1000; border-bottom: 1px solid rgba(255,255,255,0.1); }
        .nav-content { max-width: 1100px; margin: auto; display: flex; justify-content: space-between; align-items: center; }
        .nav-links a { color: white; text-decoration: none; margin-left: 25px; font-size: 0.8rem; font-weight: 600; letter-spacing: 1px; transition: 0.3s; }
        .nav-links a:hover { color: var(--primary); }

        .container { max-width: 1100px; margin: auto; padding: 0 20px; }

        /* Hero Section */
        .hero { height: 100vh; display: flex; flex-direction: column; justify-content: center; align-items: center; text-align: center; }
        .hero h1 { font-size: clamp(2.5rem, 8vw, 4.5rem); margin: 0; font-weight: 800; background: linear-gradient(to right, #fff, var(--primary)); -webkit-background-clip: text; -webkit-text-fill-color: transparent; }
        .typewriter { font-family: 'Fira Code', monospace; color: var(--primary); font-size: 1.4rem; margin-top: 15px; min-height: 1.6em; }

        section { padding: 100px 0; }
        h2 { font-size: 2rem; margin-bottom: 50px; display: flex; align-items: center; gap: 15px; }
        h2::after { content: ""; flex: 1; height: 1px; background: linear-gradient(to right, var(--primary), transparent); }

        /* Project Display */
        .project-card {
            background: var(--card-bg);
            border-radius: 20px;
            border: 1px solid rgba(0, 242, 255, 0.2);
            overflow: hidden;
            display: grid;
            grid-template-columns: 1fr 1fr;
            transition: 0.4s;
        }
        .project-card:hover { box-shadow: 0 0 30px rgba(0, 242, 255, 0.15); border-color: var(--primary); }
        .project-img { width: 100%; height: 100%; object-fit: cover; background: #1f2937; }
        .project-content { padding: 40px; }

        /* Skills Grid */
        .skills-grid { display: grid; grid-template-columns: repeat(auto-fit, minmax(300px, 1fr)); gap: 30px; }
        .skill-bar { height: 8px; background: #1f2937; border-radius: 10px; margin: 10px 0 25px; overflow: hidden; }
        .progress { height: 100%; background: linear-gradient(90deg, var(--primary), var(--secondary)); width: 0; transition: 2s ease-out; }

        /* Certification Cards */
        .cert-grid { display: grid; grid-template-columns: repeat(auto-fit, minmax(260px, 1fr)); gap: 20px; }
        .cert-card {
            background: var(--card-bg);
            padding: 25px;
            border-radius: 15px;
            border: 1px solid rgba(255,255,255,0.05);
            transition: 0.3s;
        }
        .cert-card:hover { border-color: var(--primary); transform: translateY(-5px); }
        .provider { color: var(--primary); font-size: 0.7rem; font-weight: bold; text-transform: uppercase; letter-spacing: 1px; }

        footer { text-align: center; padding: 40px 0; border-top: 1px solid rgba(255,255,255,0.05); opacity: 0.6; font-size: 0.8rem; }

        @media (max-width: 768px) { .project-card { grid-template-columns: 1fr; } }
    </style>
</head>
<body>

    <canvas id="canvas-bg"></canvas>

    <nav>
        <div class="nav-content">
            <div style="font-weight: 800; color: var(--primary); letter-spacing: 2px;">SREENIRANJAN.</div>
            <div class="nav-links">
                <a href="#about">ABOUT</a>
                <a href="#projects">PROJECTS</a>
                <a href="#skills">SKILLS</a>
                <a href="#certs">CERTIFICATES</a>
            </div>
        </div>
    </nav>

    <section class="hero">
        <div data-aos="zoom-in">
            <p style="letter-spacing: 4px; font-size: 0.8rem; color: var(--primary); font-weight: bold;">B.TECH COMPUTER SCIENCE • YEAR II</p>
            <h1>K S Sreeniranjan</h1>
            <div id="typewriter" class="typewriter"></div>
            <p style="max-width: 600px; color: #9ca3af; margin-top: 20px; line-height: 1.6;">
                Nehru College of Engineering and Research Centre. <br>
                Exploring the intersection of Computer Vision and Autonomous Robotics.
            </p>
        </div>
    </section>

    <div class="container">
        
        <section id="about" data-aos="fade-up">
            <h2>The Vision</h2>
            <p style="font-size: 1.2rem; color: #d1d5db; line-height: 1.8;">
                I am focused on building <strong>Artificial Intelligence</strong> solutions that interact with the physical world through <strong>Robotics</strong>. 
                Currently strengthening my foundation in Advanced Data Structures and Generative AI to create smarter, more efficient automated systems.
            </p>
        </section>

        <section id="projects">
            <h2 data-aos="fade-right">Flagship Project</h2>
            <div class="project-card" data-aos="fade-up">
                <div class="project-content">
                    <span style="color: var(--primary); font-weight: bold; font-size: 0.8rem;">NSITE 2025</span>
                    <h3 style="font-size: 1.8rem; margin: 15px 0;">AI Outfit Analysis Tool</h3>
                    <p style="color: #9ca3af; line-height: 1.6;">A computer vision-based tool that analyzes fashion aesthetics. It uses deep learning models to recognize clothing patterns and provide style recommendations based on analyzed visual data.</p>
                    <div style="margin-top: 25px; display: flex; gap: 10px; flex-wrap: wrap;">
                        <span style="border: 1px solid #374151; padding: 5px 12px; border-radius: 4px; font-size: 0.75rem;">Python</span>
                        <span style="border: 1px solid #374151; padding: 5px 12px; border-radius: 4px; font-size: 0.75rem;">OpenCV</span>
                        <span style="border: 1px solid #374151; padding: 5px 12px; border-radius: 4px; font-size: 0.75rem;">Machine Learning</span>
                    </div>
                </div>
                <img src="https://via.placeholder.com/600x400/030712/00f2ff?text=AI+Outfit+Analysis" alt="Project Image" class="project-img">
            </div>
        </section>

        <section id="skills">
            <h2 data-aos="fade-right">Technical Arsenal</h2>
            <div class="skills-grid">
                <div>
                    <div style="display: flex; justify-content: space-between;"><span>Python & ML</span><span>90%</span></div>
                    <div class="skill-bar"><div class="progress" style="width: 90%"></div></div>
                    
                    <div style="display: flex; justify-content: space-between;"><span>Java & Data Structures</span><span>85%</span></div>
                    <div class="skill-bar"><div class="progress" style="width: 85%"></div></div>
                </div>
                <div>
                    <div style="display: flex; justify-content: space-between;"><span>C (Robotics/Logic)</span><span>80%</span></div>
                    <div class="skill-bar"><div class="progress" style="width: 80%"></div></div>
                    
                    <div style="display: flex; justify-content: space-between;"><span>Web (HTML/CSS/JS)</span><span>95%</span></div>
                    <div class="skill-bar"><div class="progress" style="width: 95%"></div></div>
                </div>
            </div>
        </section>

        <section id="certs">
            <h2 data-aos="fade-right">Certifications</h2>
            <div class="cert-grid">
                <div class="cert-card" data-aos="fade-up">
                    <div class="provider">Coursera</div>
                    <h4 style="margin: 10px 0;">AWS Cloud Essentials</h4>
                    <p style="font-size: 0.8rem; color: #9ca3af;">Cloud Architecture & Services</p>
                </div>
                <div class="cert-card" data-aos="fade-up" data-aos-delay="100">
                    <div class="provider">Infosys Springboard</div>
                    <h4 style="margin: 10px 0;">Power BI</h4>
                    <p style="font-size: 0.8rem; color: #9ca3af;">Data Visualization & Analytics</p>
                </div>
                <div class="cert-card" data-aos="fade-up" data-aos-delay="200">
                    <div class="provider">Infosys Springboard</div>
                    <h4 style="margin: 10px 0;">Advanced DS: Binary Trees</h4>
                    <p style="font-size: 0.8rem; color: #9ca3af;">Complex Java Algorithms</p>
                </div>
                <div class="cert-card" data-aos="fade-up" data-aos-delay="300">
                    <div class="provider">Infosys Springboard</div>
                    <h4 style="margin: 10px 0;">Generative AI Foundations</h4>
                    <p style="font-size: 0.8rem; color: #9ca3af;">LLMs & Prompt Engineering</p>
                </div>
            </div>
        </section>

    </div>

    <footer>
        <p>&copy; 2025 K S Sreeniranjan. Created with passion for Robotics.</p>
        <div style="margin-top: 10px;">
            <a href="https://www.linkedin.com/in/k-s-sreeniranjan-72025a32a?utm_source=share&utm_campaign=share_via&utm_content=profile&utm_medium=android_app" style="color: white; margin: 0 10px; text-decoration: none;"><i class="fab fa-linkedin"></i></a>
            <a href="https://github.com/sreeniranjan10ks-max" style="color: white; margin: 0 10px; text-decoration: none;"><i class="fab fa-github"></i></a>
        </div>
    </footer>

    <script src="https://unpkg.com/aos@2.3.1/dist/aos.js"></script>
    <script>
        AOS.init({ duration: 1000, once: true });

        new Typewriter('#typewriter', {
            strings: ['AI & ML Enthusiast', 'Robotics Innovator', 'AWS Cloud Learner', 'Java Developer'],
            autoStart: true,
            loop: true,
            delay: 50
        });

        // Background Particles Effect
        const canvas = document.getElementById('canvas-bg');
        const ctx = canvas.getContext('2d');
        canvas.width = window.innerWidth;
        canvas.height = window.innerHeight;
        let particles = [];
        class Particle {
            constructor() {
                this.x = Math.random() * canvas.width;
                this.y = Math.random() * canvas.height;
                this.size = Math.random() * 2;
                this.speedX = Math.random() * 0.4 - 0.2;
                this.speedY = Math.random() * 0.4 - 0.2;
            }
            update() {
                this.x += this.speedX; this.y += this.speedY;
                if (this.x > canvas.width) this.x = 0; if (this.y > canvas.height) this.y = 0;
            }
            draw() {
                ctx.fillStyle = 'rgba(0, 242, 255, 0.4)';
                ctx.beginPath();
                ctx.arc(this.x, this.y, this.size, 0, Math.PI * 2);
                ctx.fill();
            }
        }
        for (let i = 0; i < 80; i++) particles.push(new Particle());
        function animate() {
            ctx.clearRect(0, 0, canvas.width, canvas.height);
            particles.forEach(p => { p.update(); p.draw(); });
            requestAnimationFrame(animate);
        }
        animate();
    </script>
</body>
</html>
