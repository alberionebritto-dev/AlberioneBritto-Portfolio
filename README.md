# AlberioneBritto-Portfolio
Website describing everything about myself and what I have done
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Alberione Britto | Computer Engineer & Developer</title>
    <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.4.0/css/all.min.css">
    <link rel="preconnect" href="https://fonts.googleapis.com">
    <link rel="preconnect" href="https://fonts.gstatic.com" crossorigin>
    <link href="https://fonts.googleapis.com/css2?family=Poppins:wght@300;400;500;600;700&family=Roboto+Mono:wght@300;400;500&display=swap" rel="stylesheet">
    <style>
        :root {
            --primary: #2563eb;
            --primary-dark: #1d4ed8;
            --secondary: #7c3aed;
            --dark: #1e293b;
            --light: #f8fafc;
            --gray: #64748b;
            --accent: #06b6d4;
            --success: #10b981;
            --shadow: 0 10px 25px rgba(0, 0, 0, 0.08);
            --radius: 12px;
            --transition: all 0.3s cubic-bezier(0.4, 0, 0.2, 1);
        }

        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
        }

        html {
            scroll-behavior: smooth;
        }

        body {
            font-family: 'Poppins', sans-serif;
            color: var(--dark);
            background-color: var(--light);
            line-height: 1.6;
            overflow-x: hidden;
        }

        h1, h2, h3, h4 {
            font-weight: 700;
            line-height: 1.2;
        }

        h1 {
            font-size: 3.5rem;
            background: linear-gradient(135deg, var(--primary), var(--secondary));
            -webkit-background-clip: text;
            background-clip: text;
            color: transparent;
            margin-bottom: 1rem;
        }

        h2 {
            font-size: 2.5rem;
            color: var(--dark);
            position: relative;
            display: inline-block;
            margin-bottom: 3rem;
        }

        h2:after {
            content: '';
            position: absolute;
            bottom: -10px;
            left: 0;
            width: 70px;
            height: 4px;
            background: linear-gradient(to right, var(--primary), var(--accent));
            border-radius: 2px;
        }

        h3 {
            font-size: 1.5rem;
            color: var(--dark);
            margin-bottom: 1rem;
        }

        p {
            font-size: 1.1rem;
            color: var(--gray);
            margin-bottom: 1.5rem;
        }

        .container {
            max-width: 1200px;
            margin: 0 auto;
            padding: 0 2rem;
        }

        section {
            padding: 100px 0;
        }

        .btn {
            display: inline-flex;
            align-items: center;
            gap: 10px;
            background: linear-gradient(135deg, var(--primary), var(--secondary));
            color: white;
            padding: 14px 28px;
            border-radius: var(--radius);
            text-decoration: none;
            font-weight: 600;
            font-size: 1rem;
            border: none;
            cursor: pointer;
            transition: var(--transition);
            box-shadow: 0 4px 15px rgba(37, 99, 235, 0.2);
        }

        .btn:hover {
            transform: translateY(-3px);
            box-shadow: 0 8px 20px rgba(37, 99, 235, 0.3);
        }

        .btn-outline {
            background: transparent;
            border: 2px solid var(--primary);
            color: var(--primary);
            box-shadow: none;
        }

        .btn-outline:hover {
            background: var(--primary);
            color: white;
        }

        /* Header & Navigation */
        header {
            position: fixed;
            top: 0;
            width: 100%;
            z-index: 1000;
            background-color: rgba(255, 255, 255, 0.95);
            backdrop-filter: blur(10px);
            box-shadow: 0 2px 20px rgba(0, 0, 0, 0.05);
            padding: 1.2rem 0;
            transition: var(--transition);
        }

        .header-scrolled {
            padding: 0.8rem 0;
            box-shadow: 0 5px 20px rgba(0, 0, 0, 0.08);
        }

        nav {
            display: flex;
            justify-content: space-between;
            align-items: center;
        }

        .logo {
            font-size: 1.8rem;
            font-weight: 700;
            color: var(--primary);
            text-decoration: none;
            display: flex;
            align-items: center;
            gap: 8px;
        }

        .logo span {
            color: var(--secondary);
        }

        .nav-links {
            display: flex;
            gap: 2.5rem;
            list-style: none;
        }

        .nav-links a {
            color: var(--dark);
            text-decoration: none;
            font-weight: 500;
            font-size: 1rem;
            transition: var(--transition);
            position: relative;
        }

        .nav-links a:hover {
            color: var(--primary);
        }

        .nav-links a:after {
            content: '';
            position: absolute;
            bottom: -5px;
            left: 0;
            width: 0;
            height: 2px;
            background-color: var(--primary);
            transition: var(--transition);
        }

        .nav-links a:hover:after {
            width: 100%;
        }

        .mobile-menu-btn {
            display: none;
            background: none;
            border: none;
            font-size: 1.5rem;
            color: var(--dark);
            cursor: pointer;
        }

        /* Hero Section */
        .hero {
            padding-top: 180px;
            padding-bottom: 100px;
            background: linear-gradient(135deg, #f0f9ff 0%, #fef7ff 100%);
            position: relative;
            overflow: hidden;
        }

        .hero:before {
            content: '';
            position: absolute;
            top: 0;
            left: 0;
            width: 100%;
            height: 100%;
            background: url("data:image/svg+xml,%3Csvg width='60' height='60' viewBox='0 0 60 60' xmlns='http://www.w3.org/2000/svg'%3E%3Cg fill='none' fill-rule='evenodd'%3E%3Cg fill='%232563eb' fill-opacity='0.03'%3E%3Cpath d='M36 34v-4h-2v4h-4v2h4v4h2v-4h4v-2h-4zm0-30V0h-2v4h-4v2h4v4h2V6h4V4h-4zM6 34v-4H4v4H0v2h4v4h2v-4h4v-2H6zM6 4V0H4v4H0v2h4v4h2V6h4V4H6z'/%3E%3C/g%3E%3C/g%3E%3C/svg%3E");
        }

        .hero-content {
            display: grid;
            grid-template-columns: 1fr 1fr;
            gap: 4rem;
            align-items: center;
            position: relative;
            z-index: 1;
        }

        .hero-text h1 {
            font-size: 3.5rem;
            margin-bottom: 1.5rem;
        }

        .hero-text .tagline {
            font-size: 1.2rem;
            color: var(--gray);
            margin-bottom: 2rem;
            font-weight: 400;
        }

        .hero-btns {
            display: flex;
            gap: 1rem;
            margin-top: 2rem;
        }

        .hero-image {
            display: flex;
            justify-content: center;
            align-items: center;
        }

        .code-window {
            background-color: white;
            border-radius: var(--radius);
            box-shadow: var(--shadow);
            overflow: hidden;
            width: 100%;
            max-width: 450px;
        }

        .window-header {
            background-color: var(--dark);
            padding: 12px 20px;
            display: flex;
            gap: 10px;
        }

        .window-dot {
            width: 12px;
            height: 12px;
            border-radius: 50%;
        }

        .dot-red {
            background-color: #ff5f56;
        }

        .dot-yellow {
            background-color: #ffbd2e;
        }

        .dot-green {
            background-color: #27ca3f;
        }

        .window-content {
            padding: 30px;
            font-family: 'Roboto Mono', monospace;
            background-color: #0f172a;
            color: #e2e8f0;
            min-height: 250px;
            font-size: 0.9rem;
        }

        .code-line {
            margin-bottom: 8px;
        }

        .code-comment {
            color: #64748b;
        }

        .code-keyword {
            color: #06b6d4;
        }

        .code-string {
            color: #10b981;
        }

        /* About Section */
        .about {
            background-color: white;
        }

        .about-content {
            display: grid;
            grid-template-columns: 1fr 1fr;
            gap: 4rem;
            align-items: center;
        }

        .about-text h2 {
            margin-bottom: 2rem;
        }

        .about-stats {
            display: grid;
            grid-template-columns: 1fr 1fr;
            gap: 1.5rem;
            margin-top: 2.5rem;
        }

        .stat-item {
            background-color: var(--light);
            padding: 1.5rem;
            border-radius: var(--radius);
            text-align: center;
            transition: var(--transition);
        }

        .stat-item:hover {
            transform: translateY(-5px);
            box-shadow: var(--shadow);
        }

        .stat-number {
            font-size: 2.5rem;
            font-weight: 700;
            color: var(--primary);
            margin-bottom: 0.5rem;
        }

        .stat-label {
            font-size: 1rem;
            color: var(--gray);
        }

        /* Skills Section */
        .skills {
            background-color: #f8fafc;
        }

        .skills-container {
            display: grid;
            grid-template-columns: repeat(auto-fill, minmax(300px, 1fr));
            gap: 2rem;
        }

        .skill-card {
            background-color: white;
            padding: 2rem;
            border-radius: var(--radius);
            box-shadow: var(--shadow);
            transition: var(--transition);
        }

        .skill-card:hover {
            transform: translateY(-10px);
        }

        .skill-icon {
            font-size: 2.5rem;
            margin-bottom: 1.5rem;
            color: var(--primary);
        }

        .skill-tags {
            display: flex;
            flex-wrap: wrap;
            gap: 0.8rem;
            margin-top: 1.5rem;
        }

        .skill-tag {
            background-color: #e0f2fe;
            color: var(--primary);
            padding: 6px 14px;
            border-radius: 50px;
            font-size: 0.9rem;
            font-weight: 500;
        }

        /* Experience & Education */
        .timeline {
            position: relative;
            max-width: 800px;
            margin: 0 auto;
        }

        .timeline:before {
            content: '';
            position: absolute;
            left: 30px;
            top: 0;
            height: 100%;
            width: 2px;
            background-color: #e2e8f0;
        }

        .timeline-item {
            position: relative;
            padding-left: 80px;
            margin-bottom: 3rem;
        }

        .timeline-date {
            position: absolute;
            left: 0;
            top: 0;
            width: 60px;
            text-align: center;
            font-weight: 600;
            color: var(--primary);
            background-color: white;
            padding: 5px 10px;
            border-radius: 20px;
            border: 2px solid #e2e8f0;
        }

        .timeline-content {
            background-color: white;
            padding: 1.5rem;
            border-radius: var(--radius);
            box-shadow: var(--shadow);
        }

        /* Projects */
        .projects-grid {
            display: grid;
            grid-template-columns: repeat(auto-fill, minmax(350px, 1fr));
            gap: 2.5rem;
        }

        .project-card {
            background-color: white;
            border-radius: var(--radius);
            overflow: hidden;
            box-shadow: var(--shadow);
            transition: var(--transition);
        }

        .project-card:hover {
            transform: translateY(-10px);
            box-shadow: 0 20px 40px rgba(0, 0, 0, 0.12);
        }

        .project-img {
            height: 200px;
            background: linear-gradient(135deg, var(--primary), var(--secondary));
            display: flex;
            align-items: center;
            justify-content: center;
            color: white;
            font-size: 3rem;
        }

        .project-content {
            padding: 1.5rem;
        }

        .project-tech {
            display: flex;
            flex-wrap: wrap;
            gap: 0.8rem;
            margin-top: 1rem;
        }

        .project-tech span {
            background-color: #f1f5f9;
            color: var(--gray);
            padding: 4px 12px;
            border-radius: 50px;
            font-size: 0.85rem;
        }

        /* Contact */
        .contact {
            background-color: var(--dark);
            color: white;
        }

        .contact h2 {
            color: white;
        }

        .contact h2:after {
            background: linear-gradient(to right, var(--accent), white);
        }

        .contact-content {
            display: grid;
            grid-template-columns: 1fr 1fr;
            gap: 4rem;
        }

        .contact-info {
            display: flex;
            flex-direction: column;
            gap: 1.5rem;
        }

        .contact-item {
            display: flex;
            align-items: center;
            gap: 1rem;
        }

        .contact-icon {
            width: 50px;
            height: 50px;
            background-color: rgba(255, 255, 255, 0.1);
            border-radius: 50%;
            display: flex;
            align-items: center;
            justify-content: center;
            font-size: 1.2rem;
            color: var(--accent);
        }

        .contact-form {
            background-color: rgba(255, 255, 255, 0.05);
            padding: 2rem;
            border-radius: var(--radius);
        }

        .form-group {
            margin-bottom: 1.5rem;
        }

        .form-control {
            width: 100%;
            padding: 14px;
            background-color: rgba(255, 255, 255, 0.07);
            border: 1px solid rgba(255, 255, 255, 0.1);
            border-radius: 8px;
            color: white;
            font-family: 'Poppins', sans-serif;
            font-size: 1rem;
            transition: var(--transition);
        }

        .form-control:focus {
            outline: none;
            border-color: var(--accent);
        }

        textarea.form-control {
            min-height: 150px;
            resize: vertical;
        }

        /* Footer */
        footer {
            background-color: #0f172a;
            color: #94a3b8;
            padding: 3rem 0;
            text-align: center;
        }

        .footer-social {
            display: flex;
            justify-content: center;
            gap: 1.5rem;
            margin: 2rem 0;
        }

        .footer-social a {
            width: 45px;
            height: 45px;
            background-color: rgba(255, 255, 255, 0.05);
            border-radius: 50%;
            display: flex;
            align-items: center;
            justify-content: center;
            color: white;
            font-size: 1.2rem;
            transition: var(--transition);
        }

        .footer-social a:hover {
            background-color: var(--primary);
            transform: translateY(-3px);
        }

        .copyright {
            margin-top: 2rem;
            font-size: 0.9rem;
            opacity: 0.7;
        }

        /* Responsive */
        @media (max-width: 992px) {
            h1 {
                font-size: 2.8rem;
            }
            
            h2 {
                font-size: 2.2rem;
            }
            
            .hero-content, .about-content, .contact-content {
                grid-template-columns: 1fr;
                gap: 3rem;
            }
            
            .hero {
                padding-top: 150px;
            }
        }

        @media (max-width: 768px) {
            .nav-links {
                display: none;
            }
            
            .mobile-menu-btn {
                display: block;
            }
            
            .mobile-menu {
                position: fixed;
                top: 80px;
                left: 0;
                width: 100%;
                background-color: white;
                padding: 2rem;
                box-shadow: 0 10px 20px rgba(0, 0, 0, 0.1);
                display: flex;
                flex-direction: column;
                gap: 1.5rem;
                transform: translateY(-100%);
                opacity: 0;
                transition: var(--transition);
            }
            
            .mobile-menu.active {
                transform: translateY(0);
                opacity: 1;
            }
            
            .hero-btns {
                flex-direction: column;
            }
            
            .about-stats {
                grid-template-columns: 1fr;
            }
        }

        @media (max-width: 576px) {
            .container {
                padding: 0 1.5rem;
            }
            
            section {
                padding: 70px 0;
            }
            
            h1 {
                font-size: 2.3rem;
            }
            
            h2 {
                font-size: 1.8rem;
            }
            
            .projects-grid {
                grid-template-columns: 1fr;
            }
        }
    </style>
</head>
<body>
    <!-- Header & Navigation -->
    <header id="header">
        <div class="container">
            <nav>
                <a href="#" class="logo"><i class="fas fa-code"></i> Alberione<span>Britto</span></a>
                
                <ul class="nav-links">
                    <li><a href="#home">Home</a></li>
                    <li><a href="#about">About</a></li>
                    <li><a href="#skills">Skills</a></li>
                    <li><a href="#experience">Experience</a></li>
                    <li><a href="#projects">Projects</a></li>
                    <li><a href="#contact">Contact</a></li>
                </ul>
                
                <button class="mobile-menu-btn" id="mobileMenuBtn">
                    <i class="fas fa-bars"></i>
                </button>
            </nav>
            
            <div class="mobile-menu" id="mobileMenu">
                <a href="#home">Home</a>
                <a href="#about">About</a>
                <a href="#skills">Skills</a>
                <a href="#experience">Experience</a>
                <a href="#projects">Projects</a>
                <a href="#contact">Contact</a>
            </div>
        </div>
    </header>

    <!-- Hero Section -->
    <section class="hero" id="home">
        <div class="container">
            <div class="hero-content">
                <div class="hero-text">
                    <h1>Alberione Britto</h1>
                    <p class="tagline">Computer Engineering Student & Passionate Developer</p>
                    <p>Enthusiastic and motivated developer with a strong foundation in software development. Eager to apply academic knowledge and project experience to contribute to innovative software development teams.</p>
                    
                    <div class="hero-btns">
                        <a href="#contact" class="btn">Get In Touch</a>
                        <a href="#projects" class="btn btn-outline">View Projects</a>
                    </div>
                </div>
                
                <div class="hero-image">
                    <div class="code-window">
                        <div class="window-header">
                            <div class="window-dot dot-red"></div>
                            <div class="window-dot do