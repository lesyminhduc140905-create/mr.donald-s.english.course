<!DOCTYPE html>
<html lang="vi">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>🐣 Mr. Donald's English Course</title>
    <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.4.0/css/all.min.css">
    <link href="https://fonts.googleapis.com/css2?family=Lemon&display=swap" rel="stylesheet">
    <style>
        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
            font-family: 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif;
        }
        
        :root {
            --primary: #4a6bff;
            --secondary: #ff6b6b;
            --accent: #ffd166;
            --success: #4caf50;
            --dark: #333;
            --light: #f8f9fa;
            --gray: #6c757d;
            --light-gray: #e9ecef;
        }
        
        body {
            background-color: #f5f7ff;
            color: var(--dark);
            line-height: 1.6;
            overflow-x: hidden;
        }
        
        .container {
            width: 90%;
            max-width: 1200px;
            margin: 0 auto;
        }
        
        /* Header */
        header {
            background: linear-gradient(135deg, var(--primary), #2a4bcc);
            color: white;
            padding: 1rem 0;
            position: sticky;
            top: 0;
            z-index: 100;
            box-shadow: 0 2px 10px rgba(0, 0, 0, 0.1);
        }
        
        nav {
            display: flex;
            justify-content: space-between;
            align-items: center;
        }
        
        .logo {
            font-size: 1.8rem;
            font-weight: 700;
            display: flex;
            align-items: center;
            cursor: pointer;
        }
        
        .logo i {
            margin-right: 10px;
            color: var(--accent);
        }
        
        .nav-links {
            display: flex;
            list-style: none;
        }
        
        .nav-links li {
            margin-left: 2rem;
        }
        
        .nav-links a {
            color: white;
            text-decoration: none;
            font-weight: 500;
            transition: color 0.3s;
            position: relative;
        }
        
        .nav-links a:hover {
            color: var(--accent);
        }
        
        .btn {
            display: inline-block;
            background: var(--secondary);
            color: white;
            padding: 0.8rem 1.5rem;
            border-radius: 50px;
            text-decoration: none;
            font-weight: 600;
            transition: all 0.3s;
            border: none;
            cursor: pointer;
            position: relative;
            overflow: hidden;
        }
        
        .btn:hover {
            background: #ff5252;
            transform: translateY(-3px);
            box-shadow: 0 5px 15px rgba(255, 107, 107, 0.4);
        }

        .btn-outline {
            background: transparent;
            border: 2px solid var(--secondary);
            color: var(--secondary);
        }

        .btn-outline:hover {
            background: var(--secondary);
            color: white;
        }
        
        /* Hero Section */
        .hero {
            padding: 5rem 0;
            background: linear-gradient(rgba(74, 107, 255, 0.9), rgba(74, 107, 255, 0.8)), url('https://images.unsplash.com/photo-1546410531-bb4caa6b424d?ixlib=rb-4.0.3&auto=format&fit=crop&w=1350&q=80') center/cover;
            color: white;
            text-align: center;
        }
        
        .hero-content {
            max-width: 800px;
            margin: 0 auto;
        }
        
        .hero h1 {
            font-size: 3.5rem;
            margin-bottom: 1rem;
            font-family: 'Lemon', cursive;
            text-shadow: 2px 2px 4px rgba(0,0,0,0.5);
        }
        
        .slogan {
            font-size: 1.8rem;
            font-style: italic;
            margin-bottom: 1rem;
            color: var(--accent);
            text-shadow: 1px 1px 2px rgba(0,0,0,0.5);
        }
        
        .hero p {
            font-size: 1.2rem;
            margin-bottom: 2rem;
            opacity: 0.9;
        }
        
        /* Courses Section */
        .section-title {
            text-align: center;
            margin: 4rem 0 2rem;
            font-size: 2.5rem;
            color: var(--dark);
            position: relative;
        }
        
        .section-title:after {
            content: '';
            display: block;
            width: 80px;
            height: 5px;
            background: var(--secondary);
            margin: 10px auto;
            border-radius: 5px;
        }
        
        .courses {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(300px, 1fr));
            gap: 2rem;
            margin: 3rem 0;
        }
        
        .course-card {
            background: white;
            border-radius: 10px;
            overflow: hidden;
            box-shadow: 0 5px 15px rgba(0, 0, 0, 0.1);
            transition: transform 0.3s;
            cursor: pointer;
        }
        
        .course-card:hover {
            transform: translateY(-10px);
        }
        
        .course-img {
            height: 200px;
            background: var(--primary);
            display: flex;
            align-items: center;
            justify-content: center;
            color: white;
            font-size: 3rem;
        }
        
        .course-content {
            padding: 1.5rem;
        }
        
        .course-content h3 {
            font-size: 1.5rem;
            margin-bottom: 0.5rem;
        }
        
        .course-info {
            display: flex;
            justify-content: space-between;
            margin: 1rem 0;
            color: var(--gray);
        }
        
        /* Features */
        .features {
            background: white;
            padding: 5rem 0;
        }
        
        .features-grid {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(250px, 1fr));
            gap: 2rem;
        }
        
        .feature {
            text-align: center;
            padding: 2rem;
            border-radius: 10px;
            box-shadow: 0 5px 15px rgba(0, 0, 0, 0.05);
            transition: transform 0.3s;
        }
        
        .feature:hover {
            transform: translateY(-5px);
        }
        
        .feature i {
            font-size: 3rem;
            color: var(--primary);
            margin-bottom: 1rem;
        }
        
        /* Testimonials */
        .testimonials {
            background: #f0f3ff;
            padding: 5rem 0;
        }
        
        .testimonial-grid {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(300px, 1fr));
            gap: 2rem;
        }
        
        .testimonial {
            background: white;
            padding: 2rem;
            border-radius: 10px;
            box-shadow: 0 5px 15px rgba(0, 0, 0, 0.05);
        }
        
        .testimonial-content {
            margin-bottom: 1rem;
        }
        
        .testimonial-author {
            display: flex;
            align-items: center;
        }
        
        .author-img {
            width: 50px;
            height: 50px;
            border-radius: 50%;
            background: var(--primary);
            margin-right: 1rem;
            display: flex;
            align-items: center;
            justify-content: center;
            color: white;
            font-weight: bold;
        }
        
        /* Footer */
        footer {
            background: var(--dark);
            color: white;
            padding: 3rem 0;
        }
        
        .footer-content {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(250px, 1fr));
            gap: 2rem;
        }
        
        .footer-section h3 {
            font-size: 1.5rem;
            margin-bottom: 1rem;
            color: var(--accent);
        }
        
        .footer-section ul {
            list-style: none;
        }
        
        .footer-section ul li {
            margin-bottom: 0.5rem;
        }
        
        .footer-section a {
            color: #ddd;
            text-decoration: none;
            transition: color 0.3s;
        }
        
        .footer-section a:hover {
            color: var(--accent);
        }
        
        .social-icons {
            display: flex;
            margin-top: 1rem;
        }
        
        .social-icons a {
            display: flex;
            align-items: center;
            justify-content: center;
            width: 40px;
            height: 40px;
            border-radius: 50%;
            background: rgba(255, 255, 255, 0.1);
            margin-right: 1rem;
            transition: background 0.3s;
        }
        
        .social-icons a:hover {
            background: var(--primary);
        }
        
        .copyright {
            text-align: center;
            margin-top: 3rem;
            padding-top: 1rem;
            border-top: 1px solid rgba(255, 255, 255, 0.1);
        }
        
        /* Course Detail Page */
        .course-detail {
            display: none;
            padding: 2rem 0;
        }

        .course-header {
            background: linear-gradient(rgba(74, 107, 255, 0.9), rgba(74, 107, 255, 0.8)), url('https://images.unsplash.com/photo-1546410531-bb4caa6b424d?ixlib=rb-4.0.3&auto=format&fit=crop&w=1350&q=80') center/cover;
            color: white;
            padding: 3rem;
            border-radius: 10px;
            margin-bottom: 2rem;
        }

        .back-button {
            background: rgba(255, 255, 255, 0.2);
            color: white;
            border: none;
            padding: 0.5rem 1rem;
            border-radius: 50px;
            cursor: pointer;
            margin-bottom: 1rem;
            display: flex;
            align-items: center;
            transition: all 0.3s;
        }

        .back-button:hover {
            background: rgba(255, 255, 255, 0.3);
        }

        .back-button i {
            margin-right: 0.5rem;
        }

        .course-detail-content {
            display: grid;
            grid-template-columns: 2fr 1fr;
            gap: 2rem;
        }

        .course-lessons {
            background: white;
            border-radius: 10px;
            padding: 2rem;
            box-shadow: 0 5px 15px rgba(0, 0, 0, 0.05);
        }

        .lesson-section {
            margin-bottom: 2rem;
        }

        .lesson-section h3 {
            margin-bottom: 1rem;
            padding-bottom: 0.5rem;
            border-bottom: 2px solid var(--light-gray);
        }

        .lesson-item {
            display: flex;
            align-items: center;
            padding: 1rem;
            border-bottom: 1px solid var(--light-gray);
        }

        .lesson-item.locked {
            opacity: 0.6;
        }

        .lesson-icon {
            margin-right: 1rem;
            width: 40px;
            height: 40px;
            border-radius: 50%;
            background: var(--light-gray);
            display: flex;
            align-items: center;
            justify-content: center;
        }

        .lesson-icon.locked {
            background: var(--light-gray);
            color: var(--gray);
        }

        .lesson-icon.unlocked {
            background: var(--success);
            color: white;
        }

        .lesson-info {
            flex: 1;
        }

        .lesson-duration {
            color: var(--gray);
            font-size: 0.9rem;
        }

        .course-sidebar {
            background: white;
            border-radius: 10px;
            padding: 2rem;
            box-shadow: 0 5px 15px rgba(0, 0, 0, 0.05);
            height: fit-content;
        }

        .course-price {
            font-size: 2rem;
            font-weight: bold;
            color: var(--primary);
            margin: 1rem 0;
        }

        .course-features {
            list-style: none;
            margin: 1rem 0;
        }

        .course-features li {
            margin-bottom: 0.5rem;
            display: flex;
            align-items: center;
        }

        .course-features i {
            color: var(--success);
            margin-right: 0.5rem;
        }

        .payment-section {
            margin-top: 2rem;
            padding-top: 1rem;
            border-top: 1px solid var(--light-gray);
        }

        .bank-info {
            background: var(--light-gray);
            padding: 1rem;
            border-radius: 5px;
            margin: 1rem 0;
            font-size: 0.9rem;
        }

        .bank-info p {
            margin-bottom: 0.5rem;
        }

        /* Registration Form */
        .registration-form {
            margin-top: 2rem;
        }

        .form-group {
            margin-bottom: 1rem;
        }

        .form-group label {
            display: block;
            margin-bottom: 0.5rem;
            font-weight: 500;
        }

        .form-group input,
        .form-group textarea {
            width: 100%;
            padding: 0.8rem;
            border: 1px solid #ddd;
            border-radius: 5px;
            font-size: 1rem;
        }

        /* Methods Page */
        .methods-page {
            display: none;
            padding: 2rem 0;
        }

        .method-section {
            background: white;
            border-radius: 10px;
            padding: 2rem;
            margin-bottom: 2rem;
            box-shadow: 0 5px 15px rgba(0, 0, 0, 0.05);
        }

        .method-section h3 {
            color: var(--primary);
            margin-bottom: 1rem;
            display: flex;
            align-items: center;
        }

        .method-section h3 span {
            margin-right: 10px;
            font-size: 1.5rem;
        }

        .method-points {
            list-style: none;
        }

        .method-points li {
            margin-bottom: 1rem;
            padding-left: 1.5rem;
            position: relative;
        }

        .method-points li:before {
            content: "•";
            color: var(--secondary);
            font-weight: bold;
            position: absolute;
            left: 0;
        }

        /* Contact Page */
        .contact-page {
            display: none;
            padding: 2rem 0;
        }

        .contact-info {
            background: white;
            border-radius: 10px;
            padding: 2rem;
            box-shadow: 0 5px 15px rgba(0, 0, 0, 0.05);
        }

        .contact-item {
            display: flex;
            align-items: center;
            margin-bottom: 1.5rem;
        }

        .contact-icon {
            width: 50px;
            height: 50px;
            border-radius: 50%;
            background: var(--primary);
            display: flex;
            align-items: center;
            justify-content: center;
            color: white;
            font-size: 1.5rem;
            margin-right: 1rem;
        }

        .contact-details {
            flex: 1;
        }

        .contact-details a {
            color: var(--primary);
            text-decoration: none;
            transition: color 0.3s;
        }

        .contact-details a:hover {
            color: var(--secondary);
            text-decoration: underline;
        }

        /* Registration Page */
        .registration-page {
            display: none;
            padding: 2rem 0;
        }

        .registration-form-container {
            background: white;
            border-radius: 10px;
            padding: 2rem;
            box-shadow: 0 5px 15px rgba(0, 0, 0, 0.05);
            max-width: 600px;
            margin: 0 auto;
        }

        .registration-form-container h2 {
            text-align: center;
            margin-bottom: 2rem;
            color: var(--primary);
        }

        /* Star Effect */
        .star {
            position: absolute;
            background-color: white;
            border-radius: 50%;
            pointer-events: none;
            opacity: 0.8;
            animation: starAnimation 1s ease-out forwards;
        }

        @keyframes starAnimation {
            0% {
                transform: translate(0, 0) scale(0);
                opacity: 1;
            }
            100% {
                transform: translate(var(--tx), var(--ty)) scale(1);
                opacity: 0;
            }
        }

        /* Neon Effect */
        .neon-text {
            color: #fff;
            text-shadow: 0 0 5px #fff, 0 0 10px #fff, 0 0 15px var(--secondary), 0 0 20px var(--secondary), 0 0 25px var(--secondary);
            animation: neonPulse 2s infinite alternate;
        }

        @keyframes neonPulse {
            from {
                text-shadow: 0 0 5px #fff, 0 0 10px #fff, 0 0 15px var(--secondary), 0 0 20px var(--secondary);
            }
            to {
                text-shadow: 0 0 10px #fff, 0 0 20px #fff, 0 0 30px var(--secondary), 0 0 40px var(--secondary);
            }
        }

        /* Hover Effects */
        .nav-links a, .btn, .course-card, .footer-section a {
            position: relative;
            overflow: hidden;
        }

        .nav-links a::after, .btn::after, .course-card::after, .footer-section a::after {
            content: '';
            position: absolute;
            top: 50%;
            left: 50%;
            width: 5px;
            height: 5px;
            background: rgba(255, 255, 255, 0.5);
            opacity: 0;
            border-radius: 100%;
            transform: scale(1, 1) translate(-50%);
            transform-origin: 50% 50%;
        }

        .nav-links a:hover::after, .btn:hover::after, .course-card:hover::after, .footer-section a:hover::after {
            animation: ripple 1s ease-out;
        }

        @keyframes ripple {
            0% {
                transform: scale(0, 0);
                opacity: 1;
            }
            20% {
                transform: scale(20, 20);
                opacity: 1;
            }
            100% {
                transform: scale(50, 50);
                opacity: 0;
            }
        }

        /* Responsive */
        @media (max-width: 768px) {
            .nav-links {
                display: none;
            }
            
            .hero h1 {
                font-size: 2.5rem;
            }
            
            .slogan {
                font-size: 1.4rem;
            }
            
            .section-title {
                font-size: 2rem;
            }

            .course-detail-content {
                grid-template-columns: 1fr;
            }
        }
    </style>
</head>
<body>
    <!-- Header -->
    <header>
        <div class="container">
            <nav>
                <div class="logo" onclick="showHomePage()">
                    <span>🐣</span>
                    <span> Mr. Donald's English</span>
                </div>
                <ul class="nav-links">
                    <li><a href="#" onclick="showHomePage(); return false;">HOME</a></li>
                    <li><a href="#" onclick="showCourseDetail('academic-speaking'); return false;">COURSES</a></li>
                    <li><a href="#" onclick="showMethodsPage(); return false;">METHODS</a></li>
                    <li><a href="#" onclick="showAboutPage(); return false;">ABOUT US</a></li>
                    <li><a href="#" onclick="showContactPage(); return false;">CONTACT</a></li>
                </ul>
                <a href="#" class="btn" onclick="showRegistrationPage(); return false;">ĐĂNG KÝ NGAY</a>
            </nav>
        </div>
    </header>

    <!-- Main Content -->
    <div id="main-content">
        <!-- Hero Section -->
        <section class="hero">
            <div class="container">
                <div class="hero-content">
                    <h1>Mr. Donald's English Course</h1><br>
                    <h2><p class="slogan"><b>"To master something, you'll have to live with it."</b></p><h2>
                    <p>Are you ready to take your English to the next level? Donald's courses are engineered for those who want to build strong communication skills, boost confidence, and use English naturally. With engaging lessons, practical exercises, and a supportive learning environment, you will not only learn English but also live it.</p>
                    <a href="#" class="btn" onclick="showRegistrationPage(); return false;">Khám phá khóa học <i class="fas fa-arrow-right"></i></a>
                </div>
            </div>
        </section>

        <!-- Courses Section -->
        <section class="container">
            <h2 class="section-title">Khóa học nổi bật</h2>
            <div class="courses">
                <div class="course-card" onclick="showCourseDetail('academic-speaking')">
                    <div class="course-img">
                        <i class="fas fa-comments"></i>
                    </div>
                    <div class="course-content">
                        <h3>Academic Speaking</h3>
                        <p>This course is designed for students who need to improve their English for academic purposes. You will learn how to express ideas clearly in presentations, discussions, and academic writing contexts. The lessons focus on critical thinking, structured speaking, and formal communication skills. By the end, you will feel confident using English in academic settings.</p>
                        <div class="course-info">
                            <span><i class="far fa-clock"></i> 3-6 Months</span>
                            <span><i class="fas fa-user-graduate"></i> 0 Students</span>
                        </div>
                        <a href="#" class="btn" onclick="showCourseDetail('academic-speaking'); return false;">Details</a>
                    </div>
                </div>
                
                <div class="course-card" onclick="showCourseDetail('english-workplace')">
                    <div class="course-img">
                        <i class="fas fa-briefcase"></i>
                    </div>
                    <div class="course-content">
                        <h3>English In Workplace</h3>
                        <p>This course helps learners develop effective English communication skills for professional environments. You will practice real workplace scenarios such as meetings, emails, phone calls, and interviews. The training emphasizes clarity, politeness, and professionalism in business communication. It is ideal for employees, job-seekers, and anyone aiming to succeed in the workplace.</p>
                        <div class="course-info">
                            <span><i class="far fa-clock"></i> 3 Months</span>
                            <span><i class="fas fa-user-graduate"></i> 0 Students</span>
                        </div>
                        <a href="#" class="btn" onclick="showCourseDetail('english-workplace'); return false;">Details</a>
                    </div>
                </div>
                
                <div class="course-card" onclick="showCourseDetail('daily-speaking')">
                    <div class="course-img">
                        <i class="fas fa-film"></i>
                    </div>
                    <div class="course-content">
                        <h3>Daily-life Speaking</h3>
                        <p>This course focuses on improving your everyday English for real-life situations. You will practice conversations for shopping, traveling, socializing, and daily problem-solving. The lessons are practical, interactive, and easy to apply immediately. By the end, you will feel more natural and fluent in daily communication.</p>
                        <div class="course-info">
                            <span><i class="far fa-clock"></i> 3 Months</span>
                            <span><i class="fas fa-user-graduate"></i> 0 Students</span>
                        </div>
                        <a href="#" class="btn" onclick="showCourseDetail('daily-speaking'); return false;">Details</a>
                    </div>
                </div>
            </div>
        </section>

        <!-- Features Section -->
        <section class="features">
            <div class="container">
                <h2 class="section-title">Why should students register for Donald's English Course?</h2>
                <div class="features-grid">
                    <div class="feature">
                        <i class="fas fa-chalkboard-teacher"></i>
                        <h3>Teaching Methods</h3>
                        <p>We focus not only on grammar and vocabulary but also on real communication skills for school, work, and daily life. With clear methods, interactive practice, and personalized support, students gain both confidence and fluency. At Donald's English Course, learning English feels natural, useful, and inspiring.</p>
                    </div>
                    
                    <div class="feature">
                        <i class="fas fa-laptop-code"></i>
                        <h3>Minigames & Events</h3>
                        <p>Students join exciting games, roleplays, and challenges that make speaking English fun and natural. We also organize events such as debates, and cultural exchange activities, giving learners the chance to practice in real contexts. These experiences not only improve language skills but also build confidence, teamwork, and creativity.</p>
                    </div>
                    
                    <div class="feature">
                        <i class="fas fa-handshake"></i>
                        <h3>Guaranteed Outcomes</h3>
                        <p>At Donald's English Course, we are committed to real progress. Every student receives clear learning goals and regular feedback to track improvement. By the end of each course, you will confidently use English in the exact context you signed up for. Our teaching methods ensure that results are practical, measurable, and lasting.</p>
                    </div>
                    
                    <div class="feature">
                        <i class="fas fa-users"></i>
                        <h3>Community</h3>
                        <p>Learning doesn't stop in the classroom. Our students join an active online community on social media where they can share tips, ask questions, and practice English every day. Teachers regularly post mini-lessons, challenges, and useful resources to keep learners motivated. It's a supportive space to connect with classmates, celebrate progress, and grow together.</p>
                    </div>
                </div>
            </div>
        </section>

        <!-- Testimonials Section -->
        <section class="testimonials">
            <div class="container">
                <h2 class="section-title">Học viên nói gì về chúng tôi?</h2>
                <div class="testimonial-grid">
                    <div class="testimonial">
                        <div class="testimonial-content">
                            <p>"Khóa học đã thay đổi khả năng giao tiếp tiếng Anh của tôi. Tôi từ một người ngại nói đã có thể tự tin giao tiếp với đối tác nước ngoài."</p>
                        </div>
                        <div class="testimonial-author">
                            <div class="author-img">NM</div>
                            <div>
                                <h4>Nguyễn Minh</h4>
                                <p>Khóa "Academic Speaking"</p>
                            </div>
                        </div>
                    </div>
                    
                    <div class="testimonial">
                        <div class="testimonial-content">
                            <p>"Phương pháp dạy học dễ hiểu, giáo viên hỗ trợ nhiệt tình. Tôi đã áp dụng được ngay các kiến thức học được nhằm hỗ trợ cho công việc của mình."</p>
                        </div>
                        <div class="testimonial-author">
                            <div class="author-img">LT</div>
                            <div>
                                <h4>Lan Trinh</h4>
                                <p>Khóa "Tiếng Anh Công sở"</p>
                            </div>
                        </div>
                    </div>
                    
                    <div class="testimonial">
                        <div class="testimonial-content">
                            <p>"Tôi đã tham gia nhiều khóa học tiếng Anh nhưng khóa học này thực sự khác biệt. Phương pháp học qua phim ảnh giúp tôi nhớ lâu và sử dụng tự nhiên."</p>
                        </div>
                        <div class="testimonial-author">
                            <div class="author-img">TH</div>
                            <div>
                                <h4>Trần Hiếu</h4>
                                <p>Khóa "Giao Tiếp Đời Sống"</p>
                            </div>
                        </div>
                    </div>
                </div>
            </div>
        </section>
    </div>

    <!-- Course Detail Pages -->
    <!-- Academic Speaking Course Detail -->
    <div id="course-detail-academic-speaking" class="course-detail container">
        <button class="back-button" onclick="showHomePage()"><i class="fas fa-arrow-left"></i> Back to Home</button>
        
        <div class="course-header">
            <h2>Academic Speaking Course</h2>
            <p>Master the art of academic communication with our comprehensive speaking course designed for students and professionals.</p>
        </div>

        <div class="course-detail-content">
            <div class="course-lessons">
                <h3>Course Curriculum</h3>
                
                <div class="lesson-section">
                    <h3>Week 1-2: Foundations of Academic Speaking</h3>
                    <div class="lesson-item locked">
                        <div class="lesson-icon locked">
                            <i class="fas fa-lock"></i>
                        </div>
                        <div class="lesson-info">
                            <h4>Lesson 1: Introduction to Academic Discourse</h4>
                            <p>Understanding formal vs. informal language in academic settings</p>
                        </div>
                        <div class="lesson-duration">45 min</div>
                    </div>
                    <div class="lesson-item locked">
                        <div class="lesson-icon locked">
                            <i class="fas fa-lock"></i>
                        </div>
                        <div class="lesson-info">
                            <h4>Lesson 2: Structuring Academic Presentations</h4>
                            <p>Learn how to organize your ideas for clear academic presentations</p>
                        </div>
                        <div class="lesson-duration">60 min</div>
                    </div>
                </div>

                <div class="lesson-section">
                    <h3>Week 3-4: Advanced Discussion Techniques</h3>
                    <div class="lesson-item locked">
                        <div class="lesson-icon locked">
                            <i class="fas fa-lock"></i>
                        </div>
                        <div class="lesson-info">
                            <h4>Lesson 3: Participating in Academic Debates</h4>
                            <p>Strategies for effective argumentation and counter-argumentation</p>
                        </div>
                        <div class="lesson-duration">50 min</div>
                    </div>
                    <div class="lesson-item locked">
                        <div class="lesson-icon locked">
                            <i class="fas fa-lock"></i>
                        </div>
                        <div class="lesson-info">
                            <h4>Lesson 4: Critical Thinking in Academic Discourse</h4>
                            <p>Developing analytical skills for academic discussions</p>
                        </div>
                        <div class="lesson-duration">55 min</div>
                    </div>
                </div>

                <div class="lesson-section">
                    <h3>Week 5-6: Presentation & Defense Skills</h3>
                    <div class="lesson-item locked">
                        <div class="lesson-icon locked">
                            <i class="fas fa-lock"></i>
                        </div>
                        <div class="lesson-info">
                            <h4>Lesson 5: Delivering Effective Academic Presentations</h4>
                            <p>Mastering tone, pace, and body language for academic settings</p>
                        </div>
                        <div class="lesson-duration">60 min</div>
                    </div>
                    <div class="lesson-item locked">
                        <div class="lesson-icon locked">
                            <i class="fas fa-lock"></i>
                        </div>
                        <div class="lesson-info">
                            <h4>Lesson 6: Defending Your Research</h4>
                            <p>Techniques for answering questions and defending your work</p>
                        </div>
                        <div class="lesson-duration">65 min</div>
                    </div>
                </div>
            </div>

            <div class="course-sidebar">
                <h3>Course Information</h3>
                <div class="course-price">4.320.000 VNĐ</div>
                
                <ul class="course-features">
                    <li><i class="fas fa-check-circle"></i> 12 weeks (3 sessions/week)</li>
                    <li><i class="fas fa-check-circle"></i> 24 detailed lessons</li>
                    <li><i class="fas fa-check-circle"></i> 6 assessment tests</li>
                    <li><i class="fas fa-check-circle"></i> 1-1 support with instructor</li>
                    <li><i class="fas fa-check-circle"></i> Lifetime access to materials</li>
                    <li><i class="fas fa-check-circle"></i> Certificate of completion</li>
                </ul>

                <div class="payment-section">
                    <h4>Register for this course</h4>
                    <p>Please transfer to the following account:</p>
                    <div class="bank-info">
                        <p><strong>Bank:</strong> Vietcombank</p>
                        <p><strong>Account Number:</strong> 3703 2855 91</p>
                        <p><strong>Account Holder:</strong> LE SY MINH DUC</p>
                        <p><strong>Content:</strong> Your Name - Phone - Academic Speaking</p>
                    </div>

                    <div class="registration-form">
                        <p>After transferring, please fill in your information:</p>
                        <div class="form-group">
                            <label for="name">Full Name</label>
                            <input type="text" id="name" placeholder="Enter your full name">
                        </div>
                        <div class="form-group">
                            <label for="phone">Phone Number</label>
                            <input type="tel" id="phone" placeholder="Enter your phone number">
                        </div>
                        <div class="form-group">
                            <label for="email">Email</label>
                            <input type="email" id="email" placeholder="Enter your email">
                        </div>
                        <button class="btn">Submit Registration</button>
                    </div>
                </div>
            </div>
        </div>
    </div>

    <!-- English in Workplace Course Detail -->
    <div id="course-detail-english-workplace" class="course-detail container">
        <button class="back-button" onclick="showHomePage()"><i class="fas fa-arrow-left"></i> Back to Home</button>
        
        <div class="course-header">
            <h2>English in Workplace Course</h2>
            <p>Enhance your professional communication skills for success in international business environments.</p>
        </div>

        <div class="course-detail-content">
            <div class="course-lessons">
                <h3>Course Curriculum</h3>
                
                <div class="lesson-section">
                    <h3>Week 1-2: Professional Communication Basics</h3>
                    <div class="lesson-item locked">
                        <div class="lesson-icon locked">
                            <i class="fas fa-lock"></i>
                        </div>
                        <div class="lesson-info">
                            <h4>Lesson 1: Business Email Etiquette</h4>
                            <p>Writing professional emails with appropriate tone and structure</p>
                        </div>
                        <div class="lesson-duration">40 min</div>
                    </div>
                    <div class="lesson-item locked">
                        <div class="lesson-icon locked">
                            <i class="fas fa-lock"></i>
                        </div>
                        <div class="lesson-info">
                            <h4>Lesson 2: Effective Phone Communication</h4>
                            <p>Mastering professional phone conversations and video calls</p>
                        </div>
                        <div class="lesson-duration">45 min</div>
                    </div>
                </div>

                <div class="lesson-section">
                    <h3>Week 3-4: Meetings & Presentations</h3>
                    <div class="lesson-item locked">
                        <div class="lesson-icon locked">
                            <i class="fas fa-lock"></i>
                        </div>
                        <div class="lesson-info">
                            <h4>Lesson 3: Participating in Meetings</h4>
                            <p>Contributing effectively to business meetings and discussions</p>
                        </div>
                        <div class="lesson-duration">50 min</div>
                    </div>
                    <div class="lesson-item locked">
                        <div class="lesson-icon locked">
                            <i class="fas fa-lock"></i>
                        </div>
                        <div class="lesson-info">
                            <h4>Lesson 4: Delivering Business Presentations</h4>
                            <p>Structuring and delivering impactful professional presentations</p>
                        </div>
                        <div class="lesson-duration">55 min</div>
                    </div>
                </div>

                <div class="lesson-section">
                    <h3>Week 5-6: Negotiation & Networking</h3>
                    <div class="lesson-item locked">
                        <div class="lesson-icon locked">
                            <i class="fas fa-lock"></i>
                        </div>
                        <div class="lesson-info">
                            <h4>Lesson 5: Business Negotiation Skills</h4>
                            <p>Language and strategies for successful business negotiations</p>
                        </div>
                        <div class="lesson-duration">60 min</div>
                    </div>
                    <div class="lesson-item locked">
                        <div class="lesson-icon locked">
                            <i class="fas fa-lock"></i>
                        </div>
                        <div class="lesson-info">
                            <h4>Lesson 6: Professional Networking</h4>
                            <p>Building relationships and networking in professional settings</p>
                        </div>
                        <div class="lesson-duration">50 min</div>
                    </div>
                </div>
            </div>

            <div class="course-sidebar">
                <h3>Course Information</h3>
                <div class="course-price">2.880.000 VNĐ</div>
                
                <ul class="course-features">
                    <li><i class="fas fa-check-circle"></i> 9 weeks (3 sessions/week)</li>
                    <li><i class="fas fa-check-circle"></i> 18 detailed lessons</li>
                    <li><i class="fas fa-check-circle"></i> 4 assessment tests</li>
                    <li><i class="fas fa-check-circle"></i> 1-1 support with instructor</li>
                    <li><i class="fas fa-check-circle"></i> Lifetime access to materials</li>
                    <li><i class="fas fa-check-circle"></i> Certificate of completion</li>
                </ul>

                <div class="payment-section">
                    <h4>Register for this course</h4>
                    <p>Please transfer to the following account:</p>
                    <div class="bank-info">
                        <p><strong>Bank:</strong> Vietcombank</p>
                        <p><strong>Account Number:</strong> 3703 2855 91</p>
                        <p><strong>Account Holder:</strong> LE SY MINH DUC</p>
                        <p><strong>Content:</strong> Your Name - Phone - Workplace English</p>
                    </div>

                    <div class="registration-form">
                        <p>After transferring, please fill in your information:</p>
                        <div class="form-group">
                            <label for="name-w">Full Name</label>
                            <input type="text" id="name-w" placeholder="Enter your full name">
                        </div>
                        <div class="form-group">
                            <label for="phone-w">Phone Number</label>
                            <input type="tel" id="phone-w" placeholder="Enter your phone number">
                        </div>
                        <div class="form-group">
                            <label for="email-w">Email</label>
                            <input type="email" id="email-w" placeholder="Enter your email">
                        </div>
                        <button class="btn">Submit Registration</button>
                    </div>
                </div>
            </div>
        </div>
    </div>

    <!-- Daily-life Speaking Course Detail -->
    <div id="course-detail-daily-speaking" class="course-detail container">
        <button class="back-button" onclick="showHomePage()"><i class="fas fa-arrow-left"></i> Back to Home</button>
        
        <div class="course-header">
            <h2>Daily-life Speaking Course</h2>
            <p>Build confidence in everyday English conversations for travel, socializing, and daily interactions.</p>
        </div>

        <div class="course-detail-content">
            <div class="course-lessons">
                <h3>Course Curriculum</h3>
                
                <div class="lesson-section">
                    <h3>Week 1-2: Everyday Conversations</h3>
                    <div class="lesson-item locked">
                        <div class="lesson-icon locked">
                            <i class="fas fa-lock"></i>
                        </div>
                        <div class="lesson-info">
                            <h4>Lesson 1: Greetings and Introductions</h4>
                            <p>Mastering basic social interactions and polite conversation starters</p>
                        </div>
                        <div class="lesson-duration">35 min</div>
                    </div>
                    <div class="lesson-item locked">
                        <div class="lesson-icon locked">
                            <i class="fas fa-lock"></i>
                        </div>
                        <div class="lesson-info">
                            <h4>Lesson 2: Shopping and Dining Out</h4>
                            <p>Essential phrases for shopping, ordering food, and transactions</p>
                        </div>
                        <div class="lesson-duration">40 min</div>
                    </div>
                </div>

                <div class="lesson-section">
                    <h3>Week 3-4: Travel & Directions</h3>
                    <div class="lesson-item locked">
                        <div class="lesson-icon locked">
                            <i class="fas fa-lock"></i>
                        </div>
                        <div class="lesson-info">
                            <h4>Lesson 3: Asking for and Giving Directions</h4>
                            <p>Navigating cities and understanding directions in English</p>
                        </div>
                        <div class="lesson-duration">45 min</div>
                    </div>
                    <div class="lesson-item locked">
                        <div class="lesson-icon locked">
                            <i class="fas fa-lock"></i>
                        </div>
                        <div class="lesson-info">
                            <h4>Lesson 4: Travel Conversations</h4>
                            <p>Handling airports, hotels, and transportation in English</p>
                        </div>
                        <div class="lesson-duration">50 min</div>
                    </div>
                </div>

                <div class="lesson-section">
                    <h3>Week 5-6: Social & Emergency Situations</h3>
                    <div class="lesson-item locked">
                        <div class="lesson-icon locked">
                            <i class="fas fa-lock"></i>
                        </div>
                        <div class="lesson-info">
                            <h4>Lesson 5: Making Friends and Small Talk</h4>
                            <p>Building relationships through casual conversations</p>
                        </div>
                        <div class="lesson-duration">40 min</div>
                    </div>
                    <div class="lesson-item locked">
                        <div class="lesson-icon locked">
                            <i class="fas fa-lock"></i>
                        </div>
                        <div class="lesson-info">
                            <h4>Lesson 6: Handling Emergencies</h4>
                            <p>Essential language for health issues and emergency situations</p>
                        </div>
                        <div class="lesson-duration">45 min</div>
                    </div>
                </div>
            </div>

            <div class="course-sidebar">
                <h3>Course Information</h3>
                <div class="course-price">2.520.000 VNĐ</div>
                
                <ul class="course-features">
                    <li><i class="fas fa-check-circle"></i> 9 weeks (3 sessions/week)</li>
                    <li><i class="fas fa-check-circle"></i> 18 detailed lessons</li>
                    <li><i class="fas fa-check-circle"></i> 4 assessment tests</li>
                    <li><i class="fas fa-check-circle"></i> 1-1 support with instructor</li>
                    <li><i class="fas fa-check-circle"></i> Lifetime access to materials</li>
                    <li><i class="fas fa-check-circle"></i> Certificate of completion</li>
                </ul>

                <div class="payment-form">
                    <h4>Register for this course</h4>
                    <p>Please transfer to the following account:</p>
                    <div class="bank-info">
                        <p><strong>Bank:</strong> Vietcombank</p>
                        <p><strong>Account Number:</strong> 3703 2855 91</p>
                        <p><strong>Account Holder:</strong> LE SY MINH DUC</p>
                        <p><strong>Content:</strong> Your Name - Phone - Daily English</p>
                    </div>

                    <div class="registration-form">
                        <p>After transferring, please fill in your information:</p>
                        <div class="form-group">
                            <label for="name-d">Full Name</label>
                            <input type="text" id="name-d" placeholder="Enter your full name">
                        </div>
                        <div class="form-group">
                            <label for="phone-d">Phone Number</label>
                            <input type="tel" id="phone-d" placeholder="Enter your phone number">
                        </div>
                        <div class="form-group">
                            <label for="email-d">Email</label>
                            <input type="email" id="email-d" placeholder="Enter your email">
                        </div>
                        <button class="btn">Submit Registration</button>
                    </div>
                </div>
            </div>
        </div>
    </div>

    <!-- Methods Page -->
    <div id="methods-page" class="methods-page container">
        <button class="back-button" onclick="showHomePage()"><i class="fas fa-arrow-left"></i> Back to Home</button>
        
        <h2 class="section-title">Teaching Methods</h2>
        
        <div class="method-section">
            <h3><span>🔑</span> Phương pháp No.1 - Critical Thinking & Reasoning (Tư duy phản biện)</h3>
            <p>Why Critical Thinking & Reasoning Are Indispensable in Donald's Communication Courses:</p><br>
            <ul class="method-points">
                <li><strong>Clarity & Precision</strong> - Speaking is not just about producing words—it's about delivering clear ideas. Critical thinking helps learners structure their thoughts logically, so they avoid vague or rambling answers.</li>
                <li><strong>Relevance & Depth</strong> - In real-life communication, people expect relevant and well-reasoned responses. Reasoning skills train students to go beyond surface-level answers, making their speech more persuasive and impactful.</li>
                <li><strong>Confidence in Expression</strong> - Many learners struggle with hesitation because they're unsure what to say. When they are trained to analyze, evaluate, and justify their opinions, they can speak with conviction and confidence.</li>
                <li><strong>Adaptability in Conversation</strong> - Critical thinking equips learners to listen actively, process information, and respond appropriately on the spot. This skill is especially important in Q&A, debates, workplace meetings, and IELTS/TOEIC speaking tests.</li>
                <li><strong>Problem-Solving Through Language</strong> - Real communication often involves solving problems, persuading others, or negotiating. Reasoning skills allow learners to build arguments, explain their ideas, and reach understanding effectively.</li>
            </ul>
            <p>→ Critical thinking and reasoning are integrated into every activity—students don't just memorize phrases. They learn how to think before they speak, organize ideas, and support them with examples, which makes their English more natural, logical, and influential.</p>
        </div>
        
        <div class="method-section">
            <h3><span>🔥</span> Phương pháp No.2 - Debate (Tranh luận & Biện luận)</h3>
            <p>The Role of Debate in Donald's Speaking Courses:</p><br>
            <ul class="method-points">
                <li><strong>Sharpens Critical Thinking</strong> - Debate forces learners to evaluate multiple perspectives, weigh evidence, and anticipate counterarguments. This develops analytical thinking rather than memorized or shallow answers.</li>
                <li><strong>Strengthens Reasoning & Logic</strong> - To win a debate, students must build clear, structured arguments. They learn how to present claims, support them with reasons/examples, and reach logical conclusions—exactly the reasoning process needed in effective communication.</li>
                <li><strong>Boosts Fluency & Confidence</strong> - Speaking under time pressure trains students to think on their feet. They gain the ability to express opinions confidently without overthinking grammar.</li>
                <li><strong>Enhances Persuasive Communication</strong> - Debate teaches rhetorical strategies: how to persuade, emphasize, and emotionally engage the audience. These skills transfer directly to workplace communication, academic speaking, and even IELTS/TOEIC tasks.</li>
                <li><strong>Promotes Active Listening & Quick Response</strong> - Debaters don't just talk — they must listen carefully, catch weaknesses in the opponent's points, and respond logically. This turns passive learners into active communicators.</li>
            </ul>
            <p>→ Debate is not treated as competition, but as a training ground for clear reasoning, persuasive speaking, and agile thinking. Students learn to defend their ideas, challenge respectfully, and communicate with authority—skills that are indispensable in both exams and real life.</p>
        </div>
        
        <div class="method-section">
            <h3><span>🎤</span> Phương pháp No.3 - Presentation (Thuyết Trình)</h3>
            <p>The Role of Presentation in Speaking Courses:</p><br>
            <ul class="method-points">
                <li><strong>Organizes Thought & Reasoning</strong> - Presentations train students to structure ideas logically: introduction → main points → conclusion. This reflects critical thinking—choosing what's most relevant, arranging it clearly, and delivering with purpose.</li>
                <li><strong>Develops Persuasive & Informative Skills</strong> - Unlike debate (which is combative), presentations are about delivering knowledge or convincing an audience. Learners practice explaining concepts, persuading stakeholders, or presenting solutions—real-world communication skills.</li>
                <li><strong>Builds Confidence & Stage Presence</strong> - Standing in front of an audience requires self-assurance. Regular presentations help students manage anxiety, improve body language, and project their voice.</li>
                <li><strong>Improves Use of Supporting Evidence</strong> - To strengthen their points, learners must use examples, statistics, stories, or visuals. This nurtures reasoning skills—how to back up claims effectively.</li>
                <li><strong>Enhances Audience Awareness</strong> - Presenters must adapt language and style depending on who they're speaking to (teachers, colleagues, clients, examiners). This makes their communication flexible and professional.</li>
            </ul>
            <p>→ Presentations are framed as real-life practice—from short personal introductions to formal project pitches. Students don't just "read slides"; they learn to think critically, organize ideas persuasively, and deliver with impact, preparing them for both academic and professional contexts.</p>
        </div>
        
        <div class="method-section">
            <h3><span>🎭</span> Phương pháp No.4 - Voice Acting & Role-play (Lồng tiếng & Nhập vai)</h3>
            <p>The Role of Voice Acting & Role-Play in Speaking Courses:</p><br>
            <ul class="method-points">
                <li><strong>Critical Thinking in Context</strong> - In role-play, students must step into a situation (e.g., at the airport, in a job interview, or negotiating with a client). This requires analyzing the scenario, anticipating challenges, and making quick, logical decisions in English.</li>
                <li><strong>Reasoning Through Reactions</strong> - Unlike scripted speaking, role-play pushes learners to justify their responses on the spot. For example: "Why should we hire you?" → The student must reason and defend their strengths, not just recite lines.</li>
                <li><strong>Fluency & Adaptability</strong> - Voice acting adds improvisation and emotion—students adapt tone, stress, and pace depending on the role. This helps them sound more natural, not robotic.</li>
                <li><strong>Confidence & Expressiveness</strong> - Many learners speak too flatly or shyly. Role-play lets them practice enthusiasm, empathy, or authority, which strengthens their presence.</li>
                <li><strong>Real-World Transfer</strong> - Role-play mirrors daily communication: ordering food, resolving conflict, giving customer service, persuading a boss, or comforting a friend. Students develop not only language but also social intelligence.</li>
            </ul>
            <p>→ Voice acting & role-play turn classrooms into mini real-life simulations. Instead of passively practicing phrases, students learn to think critically, reason through responses, and adapt emotionally, making their English dynamic, flexible, and human.</p>
        </div>
    </div>

    <!-- Contact Page -->
    <div id="contact-page" class="contact-page container">
        <button class="back-button" onclick="showHomePage()"><i class="fas fa-arrow-left"></i> Back to Home</button>
        
        <h2 class="section-title">Contact Information</h2>
        
        <div class="contact-info">
            <div class="contact-item">
                <div class="contact-icon">
                    <i class="fab fa-instagram"></i>
                </div>
                <div class="contact-details">
                    <h3>Instagram</h3>
                    <p><a href="https://www.instagram.com/kingbenjamin.md?igsh=ZGYycWFrdnpwNHd4&utm_source=qr" target="_blank">@kingbenjamin.md</a></p>
                </div>
            </div>
            
            <div class="contact-item">
                <div class="contact-icon">
                    <i class="fas fa-phone"></i>
                </div>
                <div class="contact-details">
                    <h3>Phone Number</h3>
                    <p>0703285591</p>
                </div>
            </div>
            
            <div class="contact-item">
                <div class="contact-icon">
                    <i class="fab fa-whatsapp"></i>
                </div>
                <div class="contact-details">
                    <h3>Zalo</h3>
                    <p>0703285591</p>
                </div>
            </div>
        </div>
    </div>

    <!-- Registration Page -->
    <div id="registration-page" class="registration-page container">
        <button class="back-button" onclick="showHomePage()"><i class="fas fa-arrow-left"></i> Back to Home</button>
        
        <div class="registration-form-container">
            <h2>Registration Form</h2>
            <p>Please fill in your information to get consultation:</p>
            
            <div class="form-group">
                <label for="reg-name">Full Name</label>
                <input type="text" id="reg-name" placeholder="Enter your full name">
            </div>
            
            <div class="form-group">
                <label for="reg-phone">Phone Number</label>
                <input type="tel" id="reg-phone" placeholder="Enter your phone number">
            </div>
            
            <div class="form-group">
                <label for="reg-zalo">Zalo Number</label>
                <input type="tel" id="reg-zalo" placeholder="Enter your Zalo number">
            </div>
            
            <div class="form-group">
                <label for="reg-dob">Date of Birth</label>
                <input type="date" id="reg-dob">
            </div>
            
            <div class="form-group">
                <label for="reg-question">Your Question</label>
                <textarea id="reg-question" rows="4" placeholder="Enter your question or what you want to know"></textarea>
            </div>
            
            <button class="btn">Submit Registration</button>
        </div>
    </div>

    <!-- About Page (Discord) -->
    <div id="about-page" class="container" style="display: none; padding: 2rem 0; text-align: center;">
        <button class="back-button" onclick="showHomePage()"><i class="fas fa-arrow-left"></i> Back to Home</button>
        
        <h2 class="section-title">Join Our Community</h2>
        
        <div style="background: white; padding: 2rem; border-radius: 10px; box-shadow: 0 5px 15px rgba(0,0,0,0.05); max-width: 600px; margin: 0 auto;">
            <div style="font-size: 4rem; margin-bottom: 1rem;">
                <i class="fab fa-discord" style="color: #5865F2;"></i>
            </div>
            <h3>Join our Discord Community</h3>
            <p>Connect with other students, participate in discussions, and get additional learning resources.</p>
            <a href="https://discord.gg/EeFqNj7ZTv" target="_blank" class="btn" style="margin-top: 1rem;">Join Discord</a>
        </div>
    </div>

    <!-- Footer -->
    <footer>
        <div class="container">
            <div class="footer-content">
                <div class="footer-section">
                    <h3>Mr. Donald's English</h3>
                    <p>Nền tảng học tiếng Anh giao tiếp uy tín cho học viên.</p>
                    <div class="social-icons">
                        <a href="#"><i class="fab fa-facebook-f"></i></a>
                        <a href="#"><i class="fab fa-youtube"></i></a>
                        <a href="#"><i class="fab fa-tiktok"></i></a>
                        <a href="#"><i class="fab fa-instagram"></i></a>
                    </div>
                </div>
                
                <div class="footer-section">
                    <h3>COURSES</h3>
                    <ul>
                        <li><a href="#" onclick="showCourseDetail('academic-speaking'); return false;">Academic Speaking</a></li>
                        <li><a href="#" onclick="showCourseDetail('english-workplace'); return false;">English in Workplace</a></li>
                        <li><a href="#" onclick="showCourseDetail('daily-speaking'); return false;">Daily-life Speaking</a></li>
                    </ul>
                </div>
                
                <div class="footer-section">
                    <h3>LINKS</h3>
                    <ul>
                        <li><a href="#" onclick="showAboutPage(); return false;">Về chúng tôi</a></li>
                        <li><a href="#" onclick="showMethodsPage(); return false;">Phương pháp giảng dạy</a></li>
                        <li><a href="#">Chính sách bảo mật</a></li>
                    </ul>
                </div>
                
                <div class="footer-section">
                    <h3>CONTACT</h3>
                    <p><i class="fas fa-map-marker-alt"></i> Phường Kim Giang, Quận Thanh Xuân, Hà Nội.</p>
                    <p><i class="fas fa-phone"></i> (+84) 703285591</p>
                    <p><i class="fas fa-envelope"></i> lesyminhduc140905@gmail.com</p>
                </div>
            </div>
            
            <div class="copyright">
                <p>&copy; 2025 Mr. Donald's English Course. Tất cả quyền được bảo lưu.</p>
            </div>
        </div>
    </footer>

    <script>
        // Function to show course detail
        function showCourseDetail(courseId) {
            document.getElementById('main-content').style.display = 'none';
            document.getElementById('methods-page').style.display = 'none';
            document.getElementById('contact-page').style.display = 'none';
            document.getElementById('registration-page').style.display = 'none';
            document.getElementById('about-page').style.display = 'none';
            
            // Hide all course details first
            const courseDetails = document.querySelectorAll('.course-detail');
            courseDetails.forEach(course => {
                course.style.display = 'none';
            });
            
            // Show the selected course detail
            document.getElementById('course-detail-' + courseId).style.display = 'block';
            
            // Scroll to top
            window.scrollTo(0, 0);
        }
        
        // Function to show home page
        function showHomePage() {
            document.getElementById('main-content').style.display = 'block';
            document.getElementById('methods-page').style.display = 'none';
            document.getElementById('contact-page').style.display = 'none';
            document.getElementById('registration-page').style.display = 'none';
            document.getElementById('about-page').style.display = 'none';
            
            // Hide all course details
            const courseDetails = document.querySelectorAll('.course-detail');
            courseDetails.forEach(course => {
                course.style.display = 'none';
            });
            
            // Scroll to top
            window.scrollTo(0, 0);
        }
        
        // Function to show methods page
        function showMethodsPage() {
            document.getElementById('main-content').style.display = 'none';
            document.getElementById('methods-page').style.display = 'block';
            document.getElementById('contact-page').style.display = 'none';
            document.getElementById('registration-page').style.display = 'none';
            document.getElementById('about-page').style.display = 'none';
            
            // Hide all course details
            const courseDetails = document.querySelectorAll('.course-detail');
            courseDetails.forEach(course => {
                course.style.display = 'none';
            });
            
            // Scroll to top
            window.scrollTo(0, 0);
        }
        
        // Function to show contact page
        function showContactPage() {
            document.getElementById('main-content').style.display = 'none';
            document.getElementById('methods-page').style.display = 'none';
            document.getElementById('contact-page').style.display = 'block';
            document.getElementById('registration-page').style.display = 'none';
            document.getElementById('about-page').style.display = 'none';
            
            // Hide all course details
            const courseDetails = document.querySelectorAll('.course-detail');
            courseDetails.forEach(course => {
                course.style.display = 'none';
            });
            
            // Scroll to top
            window.scrollTo(0, 0);
        }
        
        // Function to show registration page
        function showRegistrationPage() {
            document.getElementById('main-content').style.display = 'none';
            document.getElementById('methods-page').style.display = 'none';
            document.getElementById('contact-page').style.display = 'none';
            document.getElementById('registration-page').style.display = 'block';
            document.getElementById('about-page').style.display = 'none';
            
            // Hide all course details
            const courseDetails = document.querySelectorAll('.course-detail');
            courseDetails.forEach(course => {
                course.style.display = 'none';
            });
            
            // Scroll to top
            window.scrollTo(0, 0);
        }
        
        // Function to show about page
        function showAboutPage() {
            document.getElementById('main-content').style.display = 'none';
            document.getElementById('methods-page').style.display = 'none';
            document.getElementById('contact-page').style.display = 'none';
            document.getElementById('registration-page').style.display = 'none';
            document.getElementById('about-page').style.display = 'block';
            
            // Hide all course details
            const courseDetails = document.querySelectorAll('.course-detail');
            courseDetails.forEach(course => {
                course.style.display = 'none';
            });
            
            // Scroll to top
            window.scrollTo(0, 0);
        }

        // JavaScript for interactive elements
        document.addEventListener('DOMContentLoaded', function() {
            const buttons = document.querySelectorAll('.btn');
            const links = document.querySelectorAll('.nav-links a, .footer-section a');
            
            // Add ripple effect to buttons
            buttons.forEach(button => {
                button.addEventListener('mouseenter', function() {
                    this.style.transform = 'translateY(-3px)';
                    createStars(this);
                });
                
                button.addEventListener('mouseleave', function() {
                    this.style.transform = 'translateY(0)';
                });
            });
            
            // Add ripple effect to links
            links.forEach(link => {
                link.addEventListener('mouseenter', function() {
                    createStars(this);
                });
            });
            
            // Create stars effect
            function createStars(element) {
                const rect = element.getBoundingClientRect();
                const count = 8;
                
                for (let i = 0; i < count; i++) {
                    const star = document.createElement('div');
                    star.classList.add('star');
                    
                    const size = Math.random() * 6 + 4;
                    star.style.width = `${size}px`;
                    star.style.height = `${size}px`;
                    
                    const x = Math.random() * rect.width;
                    const y = Math.random() * rect.height;
                    
                    const tx = (Math.random() - 0.5) * 100;
                    const ty = (Math.random() - 0.5) * 100;
                    
                    star.style.setProperty('--tx', `${tx}px`);
                    star.style.setProperty('--ty', `${ty}px`);
                    
                    star.style.left = `${x}px`;
                    star.style.top = `${y}px`;
                    
                    element.appendChild(star);
                    
                    setTimeout(() => {
                        star.remove();
                    }, 1000);
                }
            }
            
            // Simple animation for features on scroll
            const features = document.querySelectorAll('.feature');
            
            function checkScroll() {
                features.forEach(feature => {
                    const position = feature.getBoundingClientRect().top;
                    const screenPosition = window.innerHeight / 1.3;
                    
                    if (position < screenPosition) {
                        feature.style.opacity = 1;
                        feature.style.transform = 'translateY(0)';
                    }
                });
            }
            
            // Set initial state for animation
            features.forEach(feature => {
                feature.style.opacity = 0;
                feature.style.transform = 'translateY(20px)';
                feature.style.transition = 'all 0.5s ease';
            });
            
            window.addEventListener('scroll', checkScroll);
            checkScroll(); // Check on initial load
        });
    </script>
</body>
</html>
