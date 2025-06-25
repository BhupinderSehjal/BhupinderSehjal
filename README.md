<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Bhupinder Sehjal - Full-Stack .NET Developer</title>
    <style>
        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
        }

        :root {
            --primary-color: #00D4FF;
            --secondary-color: #0099CC;
            --accent-color: #FF6B6B;
            --bg-dark: #0D1117;
            --bg-card: #161B22;
            --bg-light: #1C2128;
            --text-primary: #ffffff;
            --text-secondary: #8B949E;
            --border-color: #30363D;
            --gradient-1: linear-gradient(135deg, #667eea 0%, #764ba2 100%);
            --gradient-2: linear-gradient(135deg, #f093fb 0%, #f5576c 100%);
            --gradient-3: linear-gradient(135deg, #4facfe 0%, #00f2fe 100%);
            --gradient-4: linear-gradient(135deg, #43e97b 0%, #38f9d7 100%);
        }

        body {
            font-family: 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif;
            background: var(--bg-dark);
            color: var(--text-primary);
            line-height: 1.6;
            overflow-x: hidden;
            position: relative;
        }

        /* Animated Background */
        .animated-bg {
            position: fixed;
            top: 0;
            left: 0;
            width: 100%;
            height: 100%;
            z-index: -1;
            background: linear-gradient(45deg, #0D1117, #161B22, #1C2128, #0D1117);
            background-size: 400% 400%;
            animation: gradientFlow 15s ease infinite;
        }

        @keyframes gradientFlow {
            0% { background-position: 0% 50%; }
            50% { background-position: 100% 50%; }
            100% { background-position: 0% 50%; }
        }

        /* Floating geometric shapes */
        .floating-shapes {
            position: fixed;
            top: 0;
            left: 0;
            width: 100%;
            height: 100%;
            pointer-events: none;
            z-index: -1;
            overflow: hidden;
        }

        .shape {
            position: absolute;
            opacity: 0.1;
            animation: float 20s infinite ease-in-out;
        }

        .shape:nth-child(1) {
            width: 80px;
            height: 80px;
            background: var(--gradient-1);
            border-radius: 50%;
            top: 20%;
            left: 10%;
            animation-delay: 0s;
        }

        .shape:nth-child(2) {
            width: 120px;
            height: 120px;
            background: var(--gradient-2);
            clip-path: polygon(50% 0%, 0% 100%, 100% 100%);
            top: 60%;
            right: 20%;
            animation-delay: 5s;
        }

        .shape:nth-child(3) {
            width: 100px;
            height: 100px;
            background: var(--gradient-3);
            border-radius: 20%;
            top: 40%;
            left: 80%;
            animation-delay: 10s;
        }

        .shape:nth-child(4) {
            width: 60px;
            height: 60px;
            background: var(--gradient-4);
            clip-path: polygon(25% 0%, 75% 0%, 100% 50%, 75% 100%, 25% 100%, 0% 50%);
            top: 80%;
            left: 30%;
            animation-delay: 15s;
        }

        @keyframes float {
            0%, 100% { transform: translateY(0px) rotate(0deg); }
            33% { transform: translateY(-30px) rotate(120deg); }
            66% { transform: translateY(30px) rotate(240deg); }
        }

        .container {
            max-width: 1200px;
            margin: 0 auto;
            padding: 20px;
            position: relative;
            z-index: 1;
        }

        /* Enhanced Header */
        .header {
            text-align: center;
            padding: 80px 0;
            background: linear-gradient(135deg, rgba(0,212,255,0.1), rgba(0,153,204,0.1));
            backdrop-filter: blur(20px);
            border: 1px solid rgba(255,255,255,0.1);
            border-radius: 30px;
            margin-bottom: 50px;
            position: relative;
            overflow: hidden;
        }

        .header::before {
            content: '';
            position: absolute;
            top: -50%;
            left: -50%;
            width: 200%;
            height: 200%;
            background: conic-gradient(from 0deg, transparent, var(--primary-color), transparent);
            animation: rotate 10s linear infinite;
            z-index: -1;
        }

        .header::after {
            content: '';
            position: absolute;
            inset: 2px;
            background: var(--bg-dark);
            border-radius: 28px;
            z-index: -1;
        }

        @keyframes rotate {
            0% { transform: rotate(0deg); }
            100% { transform: rotate(360deg); }
        }

        .header h1 {
            font-size: clamp(2.5rem, 5vw, 4rem);
            margin-bottom: 20px;
            background: linear-gradient(45deg, var(--primary-color), #fff, var(--secondary-color));
            -webkit-background-clip: text;
            -webkit-text-fill-color: transparent;
            background-clip: text;
            text-shadow: 0 0 30px rgba(0,212,255,0.5);
            animation: glow 3s ease-in-out infinite alternate;
        }

        @keyframes glow {
            from { filter: drop-shadow(0 0 10px rgba(0,212,255,0.5)); }
            to { filter: drop-shadow(0 0 30px rgba(0,212,255,0.8)); }
        }

        .typing-animation {
            font-size: clamp(1.2rem, 3vw, 1.8rem);
            color: var(--text-secondary);
            font-weight: 600;
            height: 60px;
            display: flex;
            align-items: center;
            justify-content: center;
        }

        .typing-text {
            border-right: 3px solid var(--primary-color);
            padding-right: 10px;
            animation: blink 1s infinite;
        }

        @keyframes blink {
            0%, 50% { border-color: var(--primary-color); }
            51%, 100% { border-color: transparent; }
        }

        /* Enhanced Navigation */
        .nav-buttons {
            display: flex;
            justify-content: center;
            gap: 20px;
            margin: 40px 0;
            flex-wrap: wrap;
        }

        .nav-btn {
            padding: 15px 30px;
            background: linear-gradient(45deg, var(--primary-color), var(--secondary-color));
            color: var(--bg-dark);
            text-decoration: none;
            border-radius: 50px;
            font-weight: bold;
            font-size: 1rem;
            transition: all 0.4s cubic-bezier(0.25, 0.46, 0.45, 0.94);
            position: relative;
            overflow: hidden;
            text-transform: uppercase;
            letter-spacing: 1px;
        }

        .nav-btn::before {
            content: '';
            position: absolute;
            top: 0;
            left: -100%;
            width: 100%;
            height: 100%;
            background: linear-gradient(90deg, transparent, rgba(255,255,255,0.3), transparent);
            transition: left 0.5s;
        }

        .nav-btn:hover::before {
            left: 100%;
        }

        .nav-btn:hover {
            transform: translateY(-5px) scale(1.05);
            box-shadow: 0 15px 40px rgba(0,212,255,0.4);
            background: linear-gradient(45deg, var(--secondary-color), var(--primary-color));
        }

        /* Enhanced Cards */
        .card {
            background: rgba(22, 27, 34, 0.8);
            backdrop-filter: blur(20px);
            border: 1px solid rgba(255,255,255,0.1);
            border-radius: 25px;
            padding: 40px;
            margin: 30px 0;
            position: relative;
            overflow: hidden;
            transition: all 0.5s cubic-bezier(0.25, 0.46, 0.45, 0.94);
        }

        .card::before {
            content: '';
            position: absolute;
            top: 0;
            left: 0;
            right: 0;
            bottom: 0;
            background: linear-gradient(45deg, transparent, rgba(0,212,255,0.05), transparent);
            opacity: 0;
            transition: opacity 0.3s ease;
        }

        .card:hover::before {
            opacity: 1;
        }

        .card:hover {
            transform: translateY(-10px);
            border-color: var(--primary-color);
            box-shadow: 0 20px 60px rgba(0,212,255,0.2);
        }

        .card h3 {
            color: var(--primary-color);
            margin-bottom: 20px;
            font-size: 1.8rem;
            position: relative;
            display: inline-block;
        }

        .card h3::after {
            content: '';
            position: absolute;
            bottom: -5px;
            left: 0;
            width: 0;
            height: 3px;
            background: linear-gradient(90deg, var(--primary-color), var(--secondary-color));
            transition: width 0.3s ease;
        }

        .card:hover h3::after {
            width: 100%;
        }

        /* Enhanced Skills Grid */
        .skills-grid {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(280px, 1fr));
            gap: 25px;
            margin: 40px 0;
        }

        .skill-item {
            background: rgba(28, 33, 40, 0.9);
            backdrop-filter: blur(15px);
            border: 1px solid rgba(255,255,255,0.1);
            border-radius: 20px;
            padding: 30px;
            text-align: center;
            transition: all 0.4s cubic-bezier(0.25, 0.46, 0.45, 0.94);
            position: relative;
            overflow: hidden;
        }

        .skill-item::before {
            content: '';
            position: absolute;
            top: -50%;
            left: -50%;
            width: 200%;
            height: 200%;
            background: radial-gradient(circle, var(--primary-color) 0%, transparent 70%);
            opacity: 0;
            transition: opacity 0.3s ease;
            z-index: -1;
        }

        .skill-item:hover::before {
            opacity: 0.1;
        }

        .skill-item:hover {
            transform: translateY(-10px) scale(1.02);
            border-color: var(--primary-color);
            box-shadow: 0 15px 40px rgba(0,212,255,0.3);
        }

        .skill-icon {
            font-size: 3.5rem;
            margin-bottom: 15px;
            background: linear-gradient(45deg, var(--primary-color), var(--secondary-color));
            -webkit-background-clip: text;
            -webkit-text-fill-color: transparent;
            background-clip: text;
            display: inline-block;
            animation: bounce 2s ease-in-out infinite;
        }

        @keyframes bounce {
            0%, 20%, 50%, 80%, 100% { transform: translateY(0); }
            40% { transform: translateY(-10px); }
            60% { transform: translateY(-5px); }
        }

        /* Enhanced Progress Bars */
        .progress-container {
            margin: 30px 0;
        }

        .progress-item {
            margin: 25px 0;
            position: relative;
        }

        .progress-label {
            display: flex;
            justify-content: space-between;
            margin-bottom: 10px;
            font-weight: bold;
            font-size: 1.1rem;
        }

        .progress-bar {
            width: 100%;
            height: 12px;
            background: rgba(48, 54, 61, 0.8);
            border-radius: 10px;
            overflow: hidden;
            position: relative;
        }

        .progress-fill {
            height: 100%;
            background: linear-gradient(90deg, var(--primary-color), var(--secondary-color), var(--primary-color));
            background-size: 200% 100%;
            border-radius: 10px;
            transition: width 2s cubic-bezier(0.25, 0.46, 0.45, 0.94);
            position: relative;
            animation: shimmer 3s infinite;
        }

        @keyframes shimmer {
            0% { background-position: -200% 0; }
            100% { background-position: 200% 0; }
        }

        /* Enhanced Statistics */
        .stats-grid {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(220px, 1fr));
            gap: 25px;
            margin: 40px 0;
        }

        .stat-card {
            background: rgba(28, 33, 40, 0.9);
            backdrop-filter: blur(15px);
            border: 1px solid rgba(255,255,255,0.1);
            border-radius: 20px;
            padding: 30px;
            text-align: center;
            transition: all 0.4s cubic-bezier(0.25, 0.46, 0.45, 0.94);
            cursor: pointer;
            position: relative;
            overflow: hidden;
        }

        .stat-card::before {
            content: '';
            position: absolute;
            top: 0;
            left: 0;
            right: 0;
            bottom: 0;
            background: linear-gradient(135deg, var(--gradient-1), var(--gradient-2));
            opacity: 0;
            transition: opacity 0.3s ease;
        }

        .stat-card:hover::before {
            opacity: 0.1;
        }

        .stat-card:hover {
            transform: translateY(-10px) scale(1.05);
            border-color: var(--primary-color);
            box-shadow: 0 20px 50px rgba(0,212,255,0.3);
        }

        .stat-number {
            font-size: 3rem;
            font-weight: bold;
            background: linear-gradient(45deg, var(--primary-color), var(--secondary-color));
            -webkit-background-clip: text;
            -webkit-text-fill-color: transparent;
            background-clip: text;
            margin-bottom: 10px;
            position: relative;
            z-index: 1;
        }

        .stat-label {
            color: var(--text-secondary);
            font-size: 1rem;
            font-weight: 500;
            position: relative;
            z-index: 1;
        }

        /* Enhanced Timeline */
        .timeline {
            position: relative;
            padding: 40px 0;
        }

        .timeline::before {
            content: '';
            position: absolute;
            left: 50%;
            top: 0;
            bottom: 0;
            width: 4px;
            background: linear-gradient(to bottom, var(--primary-color), var(--secondary-color));
            transform: translateX(-50%);
            border-radius: 2px;
        }

        .timeline-item {
            position: relative;
            margin: 40px 0;
            width: 50%;
            padding: 30px;
            background: rgba(28, 33, 40, 0.9);
            backdrop-filter: blur(15px);
            border: 1px solid rgba(255,255,255,0.1);
            border-radius: 15px;
            transition: all 0.3s ease;
        }

        .timeline-item:nth-child(odd) {
            left: 0;
            text-align: right;
            padding-right: 50px;
        }

        .timeline-item:nth-child(even) {
            left: 50%;
            text-align: left;
            padding-left: 50px;
        }

        .timeline-item:hover {
            transform: scale(1.02);
            border-color: var(--primary-color);
            box-shadow: 0 10px 30px rgba(0,212,255,0.2);
        }

        .timeline-dot {
            position: absolute;
            top: 30px;
            width: 20px;
            height: 20px;
            background: var(--primary-color);
            border-radius: 50%;
            border: 4px solid var(--bg-dark);
            box-shadow: 0 0 20px rgba(0,212,255,0.5);
            z-index: 2;
        }

        .timeline-item:nth-child(odd) .timeline-dot {
            right: -10px;
        }

        .timeline-item:nth-child(even) .timeline-dot {
            left: -10px;
        }

        /* Enhanced Interactive Elements */
        .interactive-section {
            margin: 50px 0;
            padding: 40px;
            background: rgba(22, 27, 34, 0.8);
            backdrop-filter: blur(20px);
            border: 1px solid rgba(255,255,255,0.1);
            border-radius: 25px;
            position: relative;
            overflow: hidden;
        }

        .tab-container {
            margin: 30px 0;
        }

        .tab-buttons {
            display: flex;
            gap: 15px;
            margin-bottom: 30px;
            flex-wrap: wrap;
            justify-content: center;
        }

        .tab-btn {
            padding: 15px 25px;
            background: rgba(48, 54, 61, 0.8);
            color: var(--text-primary);
            border: 1px solid rgba(255,255,255,0.1);
            border-radius: 25px;
            cursor: pointer;
            transition: all 0.3s cubic-bezier(0.25, 0.46, 0.45, 0.94);
            font-weight: 500;
            font-size: 0.95rem;
        }

        .tab-btn:hover {
            transform: translateY(-2px);
            border-color: var(--primary-color);
        }

        .tab-btn.active {
            background: linear-gradient(45deg, var(--primary-color), var(--secondary-color));
            color: var(--bg-dark);
            transform: translateY(-2px);
            box-shadow: 0 5px 15px rgba(0,212,255,0.3);
        }

        .tab-content {
            display: none;
            padding: 30px;
            background: rgba(13, 17, 23, 0.8);
            border-radius: 15px;
            border: 1px solid rgba(255,255,255,0.05);
        }

        .tab-content.active {
            display: block;
            animation: slideIn 0.5s ease-out;
        }

        @keyframes slideIn {
            from { 
                opacity: 0; 
                transform: translateY(20px) scale(0.95); 
            }
            to { 
                opacity: 1; 
                transform: translateY(0) scale(1); 
            }
        }

        /* Enhanced Particles */
        .particle {
            position: absolute;
            width: 6px;
            height: 6px;
            background: var(--primary-color);
            border-radius: 50%;
            animation: particleFloat 8s infinite ease-in-out;
            box-shadow: 0 0 10px rgba(0,212,255,0.5);
        }

        @keyframes particleFloat {
            0%, 100% { 
                transform: translateY(0px) translateX(0px) rotate(0deg); 
                opacity: 0.3; 
            }
            33% { 
                transform: translateY(-80px) translateX(40px) rotate(120deg); 
                opacity: 1; 
            }
            66% { 
                transform: translateY(-40px) translateX(-40px) rotate(240deg); 
                opacity: 0.5; 
            }
        }

        /* Scroll Indicator */
        .scroll-indicator {
            position: fixed;
            top: 0;
            left: 0;
            width: 100%;
            height: 4px;
            background: rgba(255,255,255,0.1);
            z-index: 1000;
        }

        .scroll-progress {
            height: 100%;
            background: linear-gradient(90deg, var(--primary-color), var(--secondary-color));
            width: 0%;
            transition: width 0.1s ease;
        }

        /* Responsive Design */
        @media (max-width: 768px) {
            .header {
                padding: 60px 20px;
                margin-bottom: 30px;
            }
            
            .nav-buttons {
                flex-direction: column;
                align-items: center;
                gap: 15px;
            }
            
            .nav-btn {
                width: 100%;
                max-width: 300px;
                text-align: center;
            }
            
            .skills-grid {
                grid-template-columns: 1fr;
                gap: 20px;
            }
            
            .stats-grid {
                grid-template-columns: repeat(2, 1fr);
                gap: 20px;
            }
            
            .timeline::before {
                left: 30px;
            }
            
            .timeline-item {
                width: 100%;
                left: 0 !important;
                text-align: left !important;
                padding: 20px 20px 20px 60px !important;
            }
            
            .timeline-dot {
                left: 20px !important;
            }
            
            .tab-buttons {
                flex-direction: column;
                align-items: center;
            }
            
            .tab-btn {
                width: 100%;
                max-width: 250px;
            }
        }

        @media (max-width: 480px) {
            .container {
                padding: 15px;
            }
            
            .card {
                padding: 25px;
                margin: 20px 0;
            }
            
            .stats-grid {
                grid-template-columns: 1fr;
            }
        }

        /* Custom Scrollbar */
        ::-webkit-scrollbar {
            width: 8px;
        }

        ::-webkit-scrollbar-track {
            background: var(--bg-dark);
        }

        ::-webkit-scrollbar-thumb {
            background: linear-gradient(45deg, var(--primary-color), var(--secondary-color));
            border-radius: 4px;
        }

        ::-webkit-scrollbar-thumb:hover {
            background: linear-gradient(45deg, var(--secondary-color), var(--primary-color));
        }
    </style>
</head>
<body>
    <!-- Animated Background -->
    <div class="animated-bg"></div>
    
    <!-- Floating Shapes -->
    <div class="floating-shapes">
        <div class="shape"></div>
        <div class="shape"></div>
        <div class="shape"></div>
        <div class="shape"></div>
    </div>
    
    <!-- Scroll Indicator -->
    <div class="scroll-indicator">
        <div class="scroll-progress"></div>
    </div>

    <div class="container">
        <!-- Enhanced Header Section -->
        <div class="header">
            <h1>👨‍💻 Bhupinder Sehjal</h1>
            <div class="typing-animation">
                <span class="typing-text" id="typing-text">Full-Stack .NET Developer</span>
            </div>
        </div>

        <!-- Enhanced Navigation -->
        <div class="nav-buttons">
            <a href="https://linkedin.com/in/@bhupindersehjal" class="nav-btn">🔗 LinkedIn</a>
            <a href="mailto:bhupindersehjal9@gmail.com" class="nav-btn">📧 Email</a>
            <a href="#" class="nav-btn">🌐 Portfolio</a>
            <a href="#" class="nav-btn">📄 Resume</a>
        </div>

        <!-- Professional Summary -->
        <div class="card">
            <h3>🚀 Professional Summary</h3>
            <p>Passionate Full-Stack .NET Developer with 5+ years of expertise in crafting scalable, high-performance web applications. Specializing in ASP.NET Core, Entity Framework, and cutting-edge frontend technologies. Committed to delivering exceptional user experiences through clean code architecture, performance optimization, and innovative problem-solving approaches.</p>
        </div>

        <!-- Skills Section -->
        <div class="card">
            <h3>💼 Technical Expertise</h3>
            <div class="skills-grid">
                <div class="skill-item">
                    <div class="skill-icon">🔧</div>
                    <h4>Backend Development</h4>
                    <p>.NET Core, ASP.NET, C#, Entity Framework, Web APIs</p>
                </div>
                <div class="skill-item">
                    <div class="skill-icon">🎨</div>
                    <h4>Frontend Development</h4>
                    <p>HTML5, CSS3, JavaScript, React, Angular, Bootstrap</p>
                </div>
                <div class="skill-item">
                    <div class="skill-icon">🛢️</div>
                    <h4>Database</h4>
                    <p>SQL Server, MySQL, PostgreSQL, MongoDB</p>
                </div>
                <div class="skill-item">
                    <div class="skill-icon">☁️</div>
                    <h4>Cloud & DevOps</h4>
                    <p>Azure, AWS, Docker, Kubernetes, CI/CD</p>
                </div>
            </div>
        </div>

        <!-- Skills Progress -->
        <div class="card">
            <h3>📊 Skill Proficiency</h3>
            <div class="progress-container">
                <div class="progress-item">
                    <div class="progress-label">
                        <span>ASP.NET Core</span>
                        <span>95%</span>
                    </div>
                    <div class="progress-bar">
                        <div class="progress-fill" data-width="95"></div>
                    </div>
                </div>
                <div class="progress-item">
                    <div class="progress-label">
                        <span>Entity Framework</span>
                        <span>90%</span>
                    </div>
                    <div class="progress-bar">
                        <div class="progress-fill" data-width="90"></div>
                    </div>
                </div>
                <div class="progress-item">
                    <div class="progress-label">
                        <span>JavaScript/TypeScript</span>
                        <span>85%</span>
                    </div>
                    <div class="progress-bar">
                        <div class="progress-fill" data-width="85"></div>
                    </div>
                </div>
                <div class="progress-item">
                    <div class="progress-label">
                        <span>React/Angular</span>
                        <span>80%</span>
                    </div>
                    <div class="progress-bar">
                        <div class="progress-fill" data-width="80"></div>
                    </div>
                </div>
                <div class="progress-item">
                    <div class="progress-label">
                        <span>Cloud Technologies</span>
                        <span>75%</span>
                    </div>
                    <div class="progress-bar">
                        <div class="progress-fill" data-width="75"></div>
                    </div>
                </div>
            </div>
        </div>

        <!-- Statistics -->
        <div class="card">
            <h3>📈 Professional Statistics</h3>
            <div class="stats-grid">
                <div class="stat-card" onclick="animateNumber(this)">
                    <div class="stat-number" data-target="25">0</div>
                    <div class="stat-label">Projects Completed</div>
                </div>
                <div class="stat-card" onclick="animateNumber(this)">
                    <div class="stat-number" data-target="5">0</div>
                    <div class="stat-label">Years Experience</div>
                </div>
                <div class="stat-card" onclick="animateNumber(this)">
                    <div class="stat-number" data-target="1250">0</div>
                    <div class="stat-label">LinkedIn Followers</div>
                </div>
                <div class="stat-card" onclick="animateNumber(this)">
                    <div class="stat-number" data-target="15">0</div>
                    <div class="stat-label">Technologies Mastered</div>
                </div>
            </div>
        </div>

        <!-- Interactive Tabs -->
        <div class="interactive-section">
            <h3>🎯 Explore My Journey</h3>
            <div class="tab-container">
                <div class="tab-buttons">
                    <button class="tab-btn active" onclick="showTab('projects')">📱 Projects</button>
                    <button class="tab-
