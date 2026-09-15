<!DOCTYPE html>
<html lang="ar" dir="rtl">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>سراج جروب - الاستشارات الرقمية والتحول التقني</title>
    <!-- استيراد خط كاييرو (Cairo) -->
    <link href="https://fonts.googleapis.com/css2?family=Cairo:wght@300;400;600;700;900&display=swap" rel="stylesheet">
    <!-- FontAwesome للأيقونات -->
    <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.4.0/css/all.min.css">
    
    <style>
        :root {
            --primary-color: #07090e;
            --accent-color: #38bdf8;
            --accent-glow: rgba(56, 189, 248, 0.4);
            --secondary-color: #0284c7;
            --text-light: #f8fafc;
            --text-gray: #94a3b8;
            --bg-glass: rgba(15, 23, 42, 0.65);
            --border-glass: rgba(255, 255, 255, 0.08);
        }

        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
            font-family: 'Cairo', sans-serif;
            scroll-behavior: smooth;
        }

        body {
            background-color: var(--primary-color);
            color: var(--text-light);
            overflow-x: hidden;
            min-height: 100vh;
        }

        /* خلفية تفاعلية مع حركات الموجات */
        .wave-background {
            position: fixed;
            top: 0;
            left: 0;
            width: 100%;
            height: 100%;
            z-index: -1;
            background: radial-gradient(circle at 50% 50%, #0f172a 0%, #07090e 100%);
            overflow: hidden;
            pointer-events: none;
        }

        .wave {
            position: absolute;
            bottom: 0;
            left: 0;
            width: 200%;
            height: 100%;
            background: url('data:image/svg+xml;utf8,<svg viewBox="0 0 1200 120" xmlns="http://www.w3.org/2000/svg" preserveAspectRatio="none"><path d="M0,0 C150,90 350,-40 500,40 C650,120 900,20 1200,60 L1200,120 L0,120 Z" fill="rgba(56, 189, 248, 0.06)"/></svg>');
            background-repeat: repeat-x;
            background-size: 50% 350px;
            transition: transform 0.1s ease-out;
        }

        .wave.wave1 {
            animation: animateWave 20s linear infinite;
            z-index: 1;
            opacity: 0.8;
            bottom: 0;
        }

        .wave.wave2 {
            animation: animateWave-2 12s linear infinite;
            z-index: 2;
            opacity: 0.5;
            bottom: 15px;
        }

        .wave.wave3 {
            animation: animateWave 16s linear infinite;
            z-index: 3;
            opacity: 0.3;
            bottom: 30px;
        }

        @keyframes animateWave {
            0% { transform: translateX(0); }
            100% { transform: translateX(-50%); }
        }

        @keyframes animateWave-2 {
            0% { transform: translateX(-50%); }
            100% { transform: translateX(0); }
        }

        /* شريط التنقل */
        header {
            position: fixed;
            top: 0;
            left: 0;
            width: 100%;
            display: flex;
            justify-content: space-between;
            align-items: center;
            padding: 20px 8%;
            z-index: 1000;
            backdrop-filter: blur(15px);
            background: rgba(7, 9, 14, 0.8);
            border-bottom: 1px solid var(--border-glass);
            transition: 0.3s ease;
        }

        .logo {
            font-size: 1.8rem;
            font-weight: 900;
            color: var(--text-light);
            text-decoration: none;
            display: flex;
            align-items: center;
            gap: 10px;
        }

        .logo span {
            color: var(--accent-color);
            text-shadow: 0 0 15px var(--accent-glow);
        }

        .logo i {
            color: var(--accent-color);
        }

        nav ul {
            display: flex;
            list-style: none;
            gap: 30px;
        }

        nav ul li a {
            color: var(--text-gray);
            text-decoration: none;
            font-weight: 600;
            transition: 0.3s;
            font-size: 1rem;
            position: relative;
        }

        nav ul li a::after {
            content: '';
            position: absolute;
            bottom: -5px;
            left: 0;
            width: 0;
            height: 2px;
            background: var(--accent-color);
            transition: width 0.3s ease;
        }

        nav ul li a:hover::after, nav ul li a.active::after {
            width: 100%;
        }

        nav ul li a:hover, nav ul li a.active {
            color: var(--accent-color);
        }

        /* زر القائمة للهواتف */
        .menu-toggle {
            display: none;
            font-size: 1.5rem;
            color: var(--text-light);
            cursor: pointer;
            background: none;
            border: none;
        }

        /* القسم الرئيسي (Hero Section) */
        .hero {
            height: 100vh;
            display: flex;
            align-items: center;
            justify-content: center;
            padding: 0 8%;
            position: relative;
            z-index: 10;
            text-align: center;
        }

        .hero-content {
            max-width: 850px;
            margin-top: 50px;
            transition: transform 0.15s cubic-bezier(0.25, 1, 0.5, 1);
        }

        .hero-badge {
            display: inline-flex;
            align-items: center;
            gap: 8px;
            padding: 6px 18px;
            background: rgba(56, 189, 248, 0.08);
            color: var(--accent-color);
            border: 1px solid rgba(56, 189, 248, 0.25);
            border-radius: 30px;
            font-size: 0.9rem;
            font-weight: 600;
            margin-bottom: 25px;
            box-shadow: inset 0 0 10px rgba(56, 189, 248, 0.05);
        }

        .hero h1 {
            font-size: 3.6rem;
            font-weight: 900;
            line-height: 1.25;
            margin-bottom: 20px;
            background: linear-gradient(135deg, #fff 30%, var(--text-gray) 100%);
            -webkit-background-clip: text;
            -webkit-text-fill-color: transparent;
        }

        .hero p {
            font-size: 1.15rem;
            color: var(--text-gray);
            margin-bottom: 20px;
            line-height: 1.7;
        }

        /* قسم الخدمات الاستشارية */
        .services-section {
            padding: 110px 8%;
            position: relative;
            z-index: 10;
        }

        .section-title {
            text-align: center;
            margin-bottom: 60px;
        }

        .section-title h2 {
            font-size: 2.6rem;
            font-weight: 800;
            margin-bottom: 15px;
            color: #fff;
        }

        .section-title p {
            color: var(--text-gray);
            font-size: 1.1rem;
        }

        .services-grid {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(310px, 1fr));
            gap: 30px;
        }

        .service-card {
            background: var(--bg-glass);
            border: 1px solid var(--border-glass);
            padding: 45px 30px;
            border-radius: 24px;
            backdrop-filter: blur(15px);
            transition: 0.4s cubic-bezier(0.25, 1, 0.5, 1);
            position: relative;
            overflow: hidden;
            box-shadow: 0 10px 30px rgba(0, 0, 0, 0.3);
        }

        .service-card::before {
            content: '';
            position: absolute;
            top: 0;
            left: 0;
            width: 100%;
            height: 3px;
            background: linear-gradient(90deg, transparent, var(--accent-color), transparent);
            opacity: 0;
            transition: 0.4s;
        }

        .service-card:hover {
            transform: translateY(-12px);
            border-color: rgba(56, 189, 248, 0.3);
            box-shadow: 0 20px 40px rgba(0, 0, 0, 0.5), 0 0 20px rgba(56, 189, 248, 0.1);
        }

        .service-card:hover::before {
            opacity: 1;
        }

        .service-card i {
            font-size: 2.8rem;
            color: var(--accent-color);
            margin-bottom: 25px;
            display: inline-block;
            transition: transform 0.3s;
        }

        .service-card:hover i {
            transform: scale(1.1) rotate(5deg);
        }

        .service-card h3 {
            font-size: 1.45rem;
            margin-bottom: 15px;
            font-weight: 700;
            color: #fff;
        }

        .service-card p {
            color: var(--text-gray);
            line-height: 1.65;
            font-size: 0.98rem;
        }

        /* تذييل الصفحة */
        footer {
            text-align: center;
            padding: 40px 8%;
            background: rgba(5, 7, 11, 0.95);
            border-top: 1px solid var(--border-glass);
            position: relative;
            z-index: 10;
            color: var(--text-gray);
            font-size: 0.95rem;
        }

        /* استجابة الهواتف المحمولة المتقدمة */
        @media (max-width: 992px) {
            .hero h1 {
                font-size: 2.8rem;
            }
            nav ul {
                position: fixed;
                top: 80px;
                right: -100%;
                width: 100%;
                height: calc(100vh - 80px);
                background: rgba(7, 9, 14, 0.95);
                backdrop-filter: blur(20px);
                flex-direction: column;
                align-items: center;
                justify-content: center;
                gap: 35px;
                transition: 0.4s ease-in-out;
                border-top: 1px solid var(--border-glass);
            }
            nav ul.active {
                right: 0;
            }
            nav ul li a {
                font-size: 1.3rem;
            }
            .menu-toggle {
                display: block;
            }
        }

        @media (max-width: 576px) {
            .hero h1 {
                font-size: 2.2rem;
            }
            .hero p {
                font-size: 1rem;
            }
            header {
                padding: 15px 5%;
            }
            .services-section {
                padding: 80px 5%;
            }
        }
    </style>
</head>
<body>

    <!-- خلفية تفاعلية وموجات متحركة -->
    <div class="wave-background" id="waveBg">
        <div class="wave wave1"></div>
        <div class="wave wave2"></div>
        <div class="wave wave3"></div>
    </div>

    <!-- شريط التنقل المتطور -->
    <header id="header">
        <a href="#" class="logo">
            <i class="fa-solid fa-chart-line"></i>
            سراج <span>جروب</span>
        </a>
        <nav>
            <ul id="navLinks">
                <li><a href="#" class="active">الرئيسية</a></li>
                <li><a href="#services">خدماتنا</a></li>
                <li><a href="#about">من نحن</a></li>
            </ul>
        </nav>
        <button class="menu-toggle" id="menuToggle" aria-label="فتح القائمة">
            <i class="fa-solid fa-bars"></i>
        </button>
    </header>

    <!-- القسم الرئيسي -->
    <section class="hero">
        <div class="hero-content" id="heroContent">
            <div class="hero-badge">
                <i class="fa-solid fa-bolt"></i> شريكك الأمثل في التحول الرقمي
            </div>
            <h1>نضيء طريقك نحو النمو الرقمي المتسارع والريادة التقنية</h1>
            <p>نبتكر استراتيجيات رقمية وحلول تحليلية متقدمة ترفع من كفاءة أعمالك وتضمن لك التفوق التنافسي في السوق المستهدف.</p>
        </div>
    </section>

    <!-- قسم الخدمات الاستشارية -->
    <section id="services" class="services-section">
        <div class="section-title">
            <h2>خدمات الاستشارات الرقمية</h2>
            <p>حلول استراتيجية مدروسة خصيصاً لتعزيز حضورك الرقمي وتحقيق أهدافك</p>
        </div>
        <div class="services-grid">
            <div class="service-card">
                <i class="fa-solid fa-chess"></i>
                <h3>استراتيجيات التحول الرقمي</h3>
                <p>إعادة هندسة العمليات الإدارية والتشغيلية ودمج أحدث التقنيات لزيادة الإنتاجية وتقليل التكاليف التشغيلية.</p>
            </div>
            <div class="service-card">
                <i class="fa-solid fa-bullseye"></i>
                <h3>الحملات الإعلانية والتسويق</h3>
                <p>إدارة وتوجيه الحملات الإعلانية المدفوعة باحترافية تامة لضمان أعلى عائد استثماري (ROI) والوصول للجمهور الفعلي.</p>
            </div>
            <div class="service-card">
                <i class="fa-solid fa-magnifying-glass-chart"></i>
                <h3>تحسين محركات البحث (SEO)</h3>
                <p>هندسة وتطوير بنية المواقع وتحليل الكلمات المفتاحية لضمان الصدارة في نتائج البحث وزيادة الزيارات العضوية المستهدفة.</p>
            </div>
            <div class="service-card">
                <i class="fa-solid fa-laptop-code"></i>
                <h3>استشارات الويب وتجربة المستخدم</h3>
                <p>توجيه فني واحترافي في تصميم واجهات المستخدم وصفحات الهبوط التفاعلية لرفع معدلات التحويل والمبيعات.</p>
            </div>
            <div class="service-card">
                <i class="fa-solid fa-chart-pie"></i>
                <h3>تحليل البيانات والأداء</h3>
                <p>تحويل مؤشرات الأداء والبيانات المعقدة إلى رؤى استراتيجية واضحة تساعد الإدارة العليا على اتخاذ قرارات دقيقة.</p>
            </div>
            <div class="service-card">
                <i class="fa-solid fa-handshake-angle"></i>
                <h3>استشارات النطاقات والعلامة</h3>
                <p>اختيار النطاقات الاحترافية، بناء الهوية الرقمية، وحماية الأصول التقنية للشركات والمؤسسات بفاعلية.</p>
            </div>
        </div>
    </section>

    <!-- تذييل الصفحة -->
    <footer>
        <p>جميع الحقوق محفوظة &copy; 2026 شركة سراج جروب للاستشارات الرقمية</p>
    </footer>

    <!-- جافاسكريبت تفاعلية متطورة للمتحركات وحركة الماوس / اللمس -->
    <script>
        // تشغيل وإيقاف القائمة الجانبية للهواتف
        const menuToggle = document.getElementById('menuToggle');
        const navLinks = document.getElementById('navLinks');
        const menuIcon = menuToggle.querySelector('i');

        menuToggle.addEventListener('click', () => {
            navLinks.classList.toggle('active');
            if (navLinks.classList.contains('active')) {
                menuIcon.classList.replace('fa-bars', 'fa-xmark');
            } else {
                menuIcon.classList.replace('fa-xmark', 'fa-bars');
            }
        });

        // إغلاق القائمة عند النقر على أي رابط في الهواتف
        document.querySelectorAll('nav ul li a').forEach(link => {
            link.addEventListener('click', () => {
                navLinks.classList.remove('active');
                menuIcon.classList.replace('fa-xmark', 'fa-bars');
            });
        });

        // تأثير تفاعل حركة الماوس أو اللمس في الهاتف على القسم الرئيسي والخلفية
        const heroContent = document.getElementById('heroContent');
        const waveBg = document.getElementById('waveBg');

        let mouseX = 0;
        let mouseY = 0;
        let currentX = 0;
        let currentY = 0;

        window.addEventListener('mousemove', (e) => {
            mouseX = (e.clientX / window.innerWidth - 0.5) * 25;
            mouseY = (e.clientY / window.innerHeight - 0.5) * 25;
        });

        // دعم حركة اللمس على الهواتف والأجهزة اللوحية
        window.addEventListener('touchmove', (e) => {
            if (e.touches.length > 0) {
                mouseX = (e.touches[0].clientX / window.innerWidth - 0.5) * 20;
                mouseY = (e.touches[0].clientY / window.innerHeight - 0.5) * 20;
            }
        });

        function animate() {
            currentX += (mouseX - currentX) * 0.1;
            currentY += (mouseY - currentY) * 0.1;

            if (heroContent) {
                heroContent.style.transform = `translate(${currentX}px, ${currentY}px)`;
            }

            const waves = document.querySelectorAll('.wave');
            waves.forEach((wave, index) => {
                const speed = (index + 1) * 0.5;
                wave.style.transform = `translateX(${-currentX * speed}px)`;
            });

            requestAnimationFrame(animate);
        }
        animate();

        // تأثير تغيير خلفية الهيدر عند التمرير
        window.addEventListener('scroll', () => {
            const header = document.getElementById('header');
            if (window.scrollY > 40) {
                header.style.background = 'rgba(7, 9, 14, 0.95)';
                header.style.padding = '15px 8%';
                header.style.boxShadow = '0 10px 30px rgba(0,0,0,0.5)';
            } else {
                header.style.background = 'rgba(7, 9, 14, 0.8)';
                header.style.padding = '20px 8%';
                header.style.boxShadow = 'none';
            }
        });
    </script>
</body>
</html>
