<!DOCTYPE html>
<html lang="ar" dir="rtl" class="scroll-smooth">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>شركة سراج | حلول التسويق الاستراتيجي للشركات المتميزة</title>
    
    <!-- Google Fonts: Cairo -->
    <link rel="preconnect" href="https://fonts.googleapis.com">
    <link rel="preconnect" href="https://fonts.gstatic.com" crossorigin>
    <link href="https://fonts.googleapis.com/css2?family=Cairo:wght@300;400;600;700;800&display=swap" rel="stylesheet">
    
    <!-- Font Awesome Icons -->
    <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.4.0/css/all.min.css">
    
    <!-- Tailwind CSS CDN -->
    <script src="https://cdn.tailwindcss.com"></script>
    <script>
        tailwind.config = {
            theme: {
                extend: {
                    colors: {
                        seraj: {
                            blue: '#0F172A',
                            accent: '#2563EB',
                            gold: '#F59E0B',
                            lightGold: '#FEF3C7',
                            bg: '#F8FAFC'
                        }
                    },
                    fontFamily: {
                        cairo: ['Cairo', 'sans-serif']
                    }
                }
            }
        }
    </script>
    
    <style>
        body {
            font-family: 'Cairo', sans-serif;
            background-color: #F8FAFC;
            color: #1E293B;
            overflow-x: hidden;
        }

        /* Glassmorphism Header */
        .glass-header {
            background: rgba(255, 255, 255, 0.9);
            backdrop-filter: blur(12px);
            -webkit-backdrop-filter: blur(12px);
        }

        /* Soft Image Frame Effect */
        .image-frame {
            position: relative;
        }
        .image-frame::before {
            content: '';
            position: absolute;
            inset: -8px;
            background: linear-gradient(135deg, #2563EB 0%, #F59E0B 100%);
            border-radius: 1.5rem;
            z-index: 0;
            opacity: 0.2;
            filter: blur(12px);
        }

        /* Modal custom animation */
        .modal {
            transition: opacity 0.3s ease, visibility 0.3s ease;
        }
        .modal.active {
            opacity: 1;
            visibility: visible;
        }
    </style>
</head>
<body class="antialiased flex flex-col min-h-screen">

    <header id="navbar" class="fixed top-0 left-0 right-0 z-50 transition-all duration-300 py-4 glass-header border-b border-slate-100">
        <div class="max-w-7xl mx-auto px-6 flex items-center justify-between">
            <!-- Brand Logo -->
            <a href="#" class="flex items-center gap-3 group">
                <div class="w-10 h-10 rounded-xl bg-gradient-to-tr from-seraj-accent to-seraj-gold flex items-center justify-center text-white shadow-md group-hover:scale-105 transition-transform duration-300">
                    <i class="fa-solid fa-lightbulb text-xl"></i>
                </div>
                <div>
                    <span class="text-2xl font-extrabold text-seraj-blue tracking-tight">سِرَاج</span>
                    <span class="text-xs block text-seraj-accent font-semibold -mt-1">للتسويق والاستشارات</span>
                </div>
            </a>

            <!-- Desktop Navigation -->
            <nav class="hidden md:flex items-center gap-8 font-semibold text-slate-600">
                <a href="#hero" class="hover:text-seraj-accent transition-colors">الرئيسية</a>
                <a href="#about" class="hover:text-seraj-accent transition-colors">عن سراج</a>
                <a href="#services" class="hover:text-seraj-accent transition-colors">خدماتنا</a>
            </nav>

            <!-- CTA Button -->
            <div class="hidden md:block">
                <button onclick="openModal()" class="bg-seraj-accent hover:bg-blue-700 text-white px-6 py-2.5 rounded-full font-bold shadow-md shadow-blue-500/20 hover:shadow-blue-500/30 transition-all duration-300 hover:-translate-y-0.5">
                    تواصل معنا
                </button>
            </div>

            <!-- Mobile Menu Toggle -->
            <button id="menu-btn" class="md:hidden text-slate-700 text-2xl focus:outline-none p-2">
                <i class="fa-solid fa-bars"></i>
            </button>
        </div>

        <!-- Mobile Menu Dropdown -->
        <div id="mobile-menu" class="hidden md:hidden bg-white border-b border-slate-100 px-6 py-4 flex flex-col gap-4 font-semibold text-slate-700 shadow-xl">
            <a href="#hero" class="hover:text-seraj-accent transition-colors py-1">الرئيسية</a>
            <a href="#about" class="hover:text-seraj-accent transition-colors py-1">عن سراج</a>
            <a href="#services" class="hover:text-seraj-accent transition-colors py-1">خدماتنا</a>
            <button onclick="openModal()" class="w-full bg-seraj-accent text-white py-2.5 rounded-xl font-bold mt-2">
                تواصل معنا
            </button>
        </div>
    </header>

    <main class="flex-grow pt-24">

        <section id="hero" class="py-12 md:py-20 px-6 max-w-7xl mx-auto">
            <div class="grid grid-cols-1 lg:grid-cols-12 gap-12 items-center">
                
                <!-- Hero Content -->
                <div class="lg:col-span-7 space-y-6 text-center lg:text-right">
                    <div class="inline-flex items-center gap-2 bg-seraj-lightGold text-amber-800 px-4 py-1.5 rounded-full text-sm font-bold border border-amber-200">
                        <i class="fa-solid fa-handshake text-seraj-gold"></i>
                        <span>شريكك للتسويق والاستراتيجية</span>
                    </div>

                    <h1 class="text-3xl md:text-5xl font-extrabold text-seraj-blue leading-tight">
                        ندعم ونرعى الشركات <br class="hidden sm:inline">
                        <span class="text-transparent bg-clip-text bg-gradient-to-r from-seraj-accent to-blue-600">ذات الأفضلية والميزة التنافسية</span>
                    </h1>

                    <p class="text-slate-600 text-base md:text-lg leading-relaxed max-w-2xl mx-auto lg:mx-0">
                        في شركة <strong class="text-seraj-blue font-bold">سراج</strong>، نعمل على دعم الشركات المتميزة في السوق من خلال تسويق حديث واستراتيجي يبرز نجاحها، ويساعدها على الوصول إلى جمهورها المستهدف بالشكل الأفضل.
                    </p>

                    <div class="flex flex-col sm:flex-row gap-4 justify-center lg:justify-start pt-2">
                        <button onclick="openModal()" class="bg-seraj-accent hover:bg-blue-700 text-white px-8 py-3.5 rounded-xl font-bold text-base shadow-lg shadow-blue-500/20 transition-all duration-300 hover:-translate-y-0.5 flex items-center justify-center gap-2">
                            <span>ابدأ معنا اليوم</span>
                            <i class="fa-solid fa-arrow-left text-sm"></i>
                        </button>
                        <a href="#about" class="bg-white hover:bg-slate-50 text-slate-700 border border-slate-200 px-8 py-3.5 rounded-xl font-bold text-base transition-all duration-300 flex items-center justify-center gap-2">
                            <span>اقرأ عن رؤيتنا</span>
                        </a>
                    </div>
                </div>

                <!-- Hero Image -->
                <div class="lg:col-span-5">
                    <div class="image-frame relative">
                        <div class="relative z-10 rounded-2xl overflow-hidden shadow-xl bg-white border-4 border-white">
                            <img 
                                src="http://googleusercontent.com/image_collection/image_retrieval/15026019610335697618_0" 
                                alt="شراكة ونجاح بين رجال أعمال - شركة سراج" 
                                class="w-full h-auto object-cover hover:scale-105 transition-transform duration-500"
                                onerror="this.onerror=null; this.src='https://placehold.co/600x400/0F172A/FFF?text=Seraj+Partnership';"
                            >
                            <div class="absolute bottom-0 inset-x-0 bg-gradient-to-t from-slate-900/80 via-slate-900/40 to-transparent p-6 text-white">
                                <p class="font-bold text-base">شراكة قائمة على الثقة والنجاح</p>
                                <p class="text-xs text-slate-200 mt-1">نسلط الضوء على تميزك ونقاط قوتك في السوق</p>
                            </div>
                        </div>
                    </div>
                </div>

            </div>
        </section>

        <section id="about" class="py-16 bg-white border-y border-slate-100">
            <div class="max-w-7xl mx-auto px-6">
                <div class="max-w-3xl mx-auto text-center space-y-4">
                    <span class="text-seraj-accent font-bold text-sm uppercase">فلسفتنا في العمل</span>
                    <h2 class="text-2xl md:text-3xl font-extrabold text-seraj-blue">لماذا نركز على الشركات المتميزة؟</h2>
                    <p class="text-slate-600 text-base md:text-lg leading-relaxed">
                        نؤمن بأن الشركات التي تقدم جودة حقيقية وميزة تنافسية تستحق أن تكون في مقدمة السوق. دورنا في <span class="font-bold text-seraj-blue">سراج</span> هو توفير الحلول التسويقية والتنفيذية التي تعكس هذا التميز وتضمن وصول رسالتكم بوضوح واحترافية.
                    </p>
                </div>

                <!-- Simple Cards -->
                <div class="grid grid-cols-1 md:grid-cols-3 gap-8 mt-12">
                    <div class="p-8 rounded-2xl bg-seraj-bg border border-slate-100 space-y-3">
                        <div class="w-12 h-12 rounded-xl bg-blue-100 text-seraj-accent flex items-center justify-center text-xl font-bold">
                            <i class="fa-solid fa-bullseye"></i>
                        </div>
                        <h3 class="text-lg font-bold text-seraj-blue">تسويق استراتيجي</h3>
                        <p class="text-slate-600 text-sm leading-relaxed">
                            خطط تسويقية مدروسة تناسب طبيعة نشاطك وتخاطب جمهورك بشكل مباشر وفعال.
                        </p>
                    </div>

                    <div class="p-8 rounded-2xl bg-seraj-bg border border-slate-100 space-y-3">
                        <div class="w-12 h-12 rounded-xl bg-amber-100 text-seraj-gold flex items-center justify-center text-xl font-bold">
                            <i class="fa-solid fa-award"></i>
                        </div>
                        <h3 class="text-lg font-bold text-seraj-blue">إبراز الميزة التنافسية</h3>
                        <p class="text-slate-600 text-sm leading-relaxed">
                            تركيز الضوء على نقاط القوة التي تجعل شركتك الأفضل والأجدر بالاختيار.
                        </p>
                    </div>

                    <div class="p-8 rounded-2xl bg-seraj-bg border border-slate-100 space-y-3">
                        <div class="w-12 h-12 rounded-xl bg-slate-200 text-slate-800 flex items-center justify-center text-xl font-bold">
                            <i class="fa-solid fa-handshake-angle"></i>
                        </div>
                        <h3 class="text-lg font-bold text-seraj-blue">رعاية الشراكة</h3>
                        <p class="text-slate-600 text-sm leading-relaxed">
                            نعمل كفريق واحد مع شركتك لضمان استمرار التميز والنمو في السوق.
                        </p>
                    </div>
                </div>
            </div>
        </section>

        <section id="services" class="py-16 md:py-24 px-6 max-w-7xl mx-auto">
            <div class="text-center max-w-2xl mx-auto mb-12 space-y-2">
                <span class="text-seraj-accent font-bold text-sm">كيف نخدمك؟</span>
                <h2 class="text-2xl md:text-3xl font-extrabold text-seraj-blue">خدمات تسويقية متكاملة</h2>
            </div>

            <div class="grid grid-cols-1 md:grid-cols-3 gap-8">
                <!-- Service 1 -->
                <div class="bg-white p-8 rounded-2xl border border-slate-200 hover:border-seraj-accent hover:shadow-lg transition-all duration-300">
                    <div class="w-12 h-12 rounded-xl bg-blue-50 text-seraj-accent flex items-center justify-center text-xl mb-4">
                        <i class="fa-solid fa-rectangle-ad"></i>
                    </div>
                    <h3 class="text-lg font-bold text-seraj-blue mb-2">إدارة الحملات التسويقية</h3>
                    <p class="text-slate-600 text-sm leading-relaxed">
                        تخطيط وإدارة الحملات الإعلانية على المنصات المناسبة لتحقيق التواجد المطلوب.
                    </p>
                </div>

                <!-- Service 2 -->
                <div class="bg-white p-8 rounded-2xl border border-slate-200 hover:border-seraj-accent hover:shadow-lg transition-all duration-300">
                    <div class="w-12 h-12 rounded-xl bg-amber-50 text-seraj-gold flex items-center justify-center text-xl mb-4">
                        <i class="fa-solid fa-pen-nib"></i>
                    </div>
                    <h3 class="text-lg font-bold text-seraj-blue mb-2">تعزيز الهوية والرسالة</h3>
                    <p class="text-slate-600 text-sm leading-relaxed">
                        صياغة المحتوى وإبراز الرسائل التسويقية التي تعكس جودة الخدمات والمنتجات.
                    </p>
                </div>

                <!-- Service 3 -->
                <div class="bg-white p-8 rounded-2xl border border-slate-200 hover:border-seraj-accent hover:shadow-lg transition-all duration-300">
                    <div class="w-12 h-12 rounded-xl bg-blue-50 text-seraj-accent flex items-center justify-center text-xl mb-4">
                        <i class="fa-solid fa-compass"></i>
                    </div>
                    <h3 class="text-lg font-bold text-seraj-blue mb-2">الاستشارات التسويقية</h3>
                    <p class="text-slate-600 text-sm leading-relaxed">
                        تقديم التوجيه والرأي الاستشاري لتجاوز التحديات واقتناص الفرص في السوق.
                    </p>
                </div>
            </div>
        </section>

        <section class="py-12 px-6 max-w-7xl mx-auto my-4">
            <div class="bg-gradient-to-br from-seraj-blue to-slate-800 text-white rounded-3xl p-8 md:p-12 shadow-xl text-center space-y-6">
                <h2 class="text-2xl md:text-3xl font-extrabold">
                    هل تمتلك شركتك الميزة التنافسية وترغب في الانطلاق؟
                </h2>
                <p class="text-slate-300 text-sm md:text-base max-w-xl mx-auto">
                    نحن هنا لنكون ذراعك التسويقي الاستراتيجي. تواصل معنا اليوم لمناقشة كيفية تسويق تميزك بشكل أفضل.
                </p>
                <div class="pt-2">
                    <button onclick="openModal()" class="bg-seraj-gold hover:bg-amber-600 text-slate-900 font-extrabold text-base px-8 py-3.5 rounded-xl shadow-md transition-all duration-300 hover:scale-105">
                        تواصل مع فريق سراج
                    </button>
                </div>
            </div>
        </section>

    </main>

    <footer class="bg-slate-900 text-slate-400 py-10 border-t border-slate-800">
        <div class="max-w-7xl mx-auto px-6">
            <div class="flex flex-col md:flex-row items-center justify-between gap-6">
                <!-- Footer Brand -->
                <div class="flex items-center gap-3">
                    <div class="w-8 h-8 rounded-lg bg-gradient-to-tr from-seraj-accent to-seraj-gold flex items-center justify-center text-white font-bold">
                        <i class="fa-solid fa-lightbulb text-sm"></i>
                    </div>
                    <span class="text-lg font-bold text-white">شركة سراج للتسويق</span>
                </div>

                <!-- Copyright -->
                <p class="text-xs text-slate-500">
                    جميع الحقوق محفوظة &copy; <span id="year"></span> شركة سراج
                </p>
            </div>
        </div>
    </footer>

    <div id="contact-modal" class="modal opacity-0 invisible fixed inset-0 z-50 flex items-center justify-center p-4 bg-slate-900/60 backdrop-blur-sm">
        <div class="bg-white rounded-2xl max-w-lg w-full p-6 md:p-8 shadow-2xl relative">
            <!-- Close Button -->
            <button onclick="closeModal()" class="absolute top-4 left-4 text-slate-400 hover:text-slate-600 text-xl w-8 h-8 flex items-center justify-center rounded-full hover:bg-slate-100">
                <i class="fa-solid fa-xmark"></i>
            </button>

            <div class="text-center mb-6">
                <h3 class="text-xl font-bold text-seraj-blue">تواصل مع شركة سراج</h3>
                <p class="text-slate-500 text-xs mt-1">قم بتعبئة النموذج وسنقوم بالتواصل معك قريبًا</p>
            </div>

            <form id="contact-form" onsubmit="handleFormSubmit(event)" class="space-y-4">
                <div>
                    <label class="block text-xs font-semibold text-slate-700 mb-1">الاسم / اسم الشركة</label>
                    <input type="text" required class="w-full px-4 py-2.5 rounded-xl border border-slate-200 focus:outline-none focus:border-seraj-accent text-sm" placeholder="أدخل اسمك أو اسم الشركة">
                </div>

                <div>
                    <label class="block text-xs font-semibold text-slate-700 mb-1">رقم التواصل</label>
                    <input type="tel" required class="w-full px-4 py-2.5 rounded-xl border border-slate-200 focus:outline-none focus:border-seraj-accent text-sm" placeholder="أدخل رقم الهاتف أو الواتساب">
                </div>

                <div>
                    <label class="block text-xs font-semibold text-slate-700 mb-1">تفاصيل إضافية (اختياري)</label>
                    <textarea rows="3" class="w-full px-4 py-2.5 rounded-xl border border-slate-200 focus:outline-none focus:border-seraj-accent text-sm" placeholder="اكتب نبذة مختصرة عن نشاط شركتك"></textarea>
                </div>

                <button type="submit" class="w-full bg-seraj-accent hover:bg-blue-700 text-white font-bold py-3 rounded-xl transition-colors shadow-md text-sm">
                    إرسال البيانات
                </button>
            </form>

            <div id="form-success" class="hidden text-center py-6 space-y-3">
                <div class="w-12 h-12 rounded-full bg-green-100 text-green-600 flex items-center justify-center mx-auto text-xl">
                    <i class="fa-solid fa-check"></i>
                </div>
                <h4 class="text-base font-bold text-slate-800">تم استلام طلبك بنجاح!</h4>
                <p class="text-slate-500 text-xs">شكرًا لتواصلك مع سراج. سيتواصل معك أحد مستشارينا في أقرب وقت ممكن.</p>
                <button onclick="closeModal()" class="mt-2 text-xs text-seraj-accent font-bold hover:underline">إغلاق النافذة</button>
            </div>
        </div>
    </div>

    <script>
        // Dynamic copyright year
        document.getElementById('year').textContent = new Date().getFullYear();

        // Mobile Menu Toggle Logic
        const menuBtn = document.getElementById('menu-btn');
        const mobileMenu = document.getElementById('mobile-menu');

        menuBtn.addEventListener('click', () => {
            mobileMenu.classList.toggle('hidden');
        });

        document.querySelectorAll('#mobile-menu a').forEach(link => {
            link.addEventListener('click', () => {
                mobileMenu.classList.add('hidden');
            });
        });

        // Header Shadow on Scroll
        const navbar = document.getElementById('navbar');
        window.addEventListener('scroll', () => {
            if (window.scrollY > 20) {
                navbar.classList.add('shadow-md');
            } else {
                navbar.classList.remove('shadow-md');
            }
        });

        // Modal Open/Close Logic
        const modal = document.getElementById('contact-modal');
        const contactForm = document.getElementById('contact-form');
        const formSuccess = document.getElementById('form-success');

        function openModal() {
            modal.classList.add('active');
            contactForm.classList.remove('hidden');
            formSuccess.classList.add('hidden');
            contactForm.reset();
        }

        function closeModal() {
            modal.classList.remove('active');
        }

        modal.addEventListener('click', (e) => {
            if (e.target === modal) {
                closeModal();
            }
        });

        // Form Submit Handler
        function handleFormSubmit(event) {
            event.preventDefault();
            contactForm.classList.add('hidden');
            formSuccess.classList.remove('hidden');
        }
    </script>
</body>
</html>
