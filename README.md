# Redouan-kelious
we are here to help you 
<html lang="fr" dir="ltr">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Redouane Kelious - Conseiller en Style & Développement Personnel</title>
    <link href="https://fonts.googleapis.com/css2?family=Playfair+Display:wght@400;700&family=Lato:wght@300;400;700&family=Amiri:wght@400;700&display=swap" rel="stylesheet">
    <script src="https://cdn.tailwindcss.com"></script>
    <script src="https://cdnjs.cloudflare.com/ajax/libs/gsap/3.12.2/gsap.min.js"></script>
    <script src="https://cdnjs.cloudflare.com/ajax/libs/gsap/3.12.2/ScrollTrigger.min.js"></script>
    <style>
        :root {
            --gold: #D4AF37;
            --deep-green: #0F4C3A;
            --sand: #F4E4C1;
            --charcoal: #2C3E50;
        }
        
        body {
            font-family: 'Lato', sans-serif;
            background-color: #FAFAFA;
            overflow-x: hidden;
        }
        
        .font-display {
            font-family: 'Playfair Display', serif;
        }
        
        .font-arabic {
            font-family: 'Amiri', serif;
        }
        
        .gold-gradient {
            background: linear-gradient(135deg, #D4AF37 0%, #F4E4C1 50%, #D4AF37 100%);
            -webkit-background-clip: text;
            -webkit-text-fill-color: transparent;
            background-clip: text;
        }
        
        .hero-pattern {
            background-image: 
                radial-gradient(circle at 20% 50%, rgba(212, 175, 55, 0.1) 0%, transparent 50%),
                radial-gradient(circle at 80% 80%, rgba(15, 76, 58, 0.1) 0%, transparent 50%);
        }
        
        .geometric-pattern {
            background-image: url("data:image/svg+xml,%3Csvg width='60' height='60' viewBox='0 0 60 60' xmlns='http://www.w3.org/2000/svg'%3E%3Cg fill='none' fill-rule='evenodd'%3E%3Cg fill='%23D4AF37' fill-opacity='0.05'%3E%3Cpath d='M36 34v-4h-2v4h-4v2h4v4h2v-4h4v-2h-4zm0-30V0h-2v4h-4v2h4v4h2V6h4V4h-4zM6 34v-4H4v4H0v2h4v4h2v-4h4v-2H6zM6 4V0H4v4H0v2h4v4h2V6h4V4H6z'/%3E%3C/g%3E%3C/g%3E%3C/svg%3E");
        }
        
        .card-hover {
            transition: all 0.4s cubic-bezier(0.4, 0, 0.2, 1);
        }
        
        .card-hover:hover {
            transform: translateY(-10px);
            box-shadow: 0 20px 40px rgba(212, 175, 55, 0.2);
        }
        
        .btn-gold {
            background: linear-gradient(135deg, #D4AF37 0%, #B8941F 100%);
            transition: all 0.3s ease;
        }
        
        .btn-gold:hover {
            transform: scale(1.05);
            box-shadow: 0 10px 30px rgba(212, 175, 55, 0.4);
        }
        
        .nav-blur {
            backdrop-filter: blur(10px);
            background: rgba(255, 255, 255, 0.9);
        }
        
        .reveal-text {
            opacity: 0;
            transform: translateY(30px);
        }
        
        .islamic-geometry {
            position: absolute;
            width: 400px;
            height: 400px;
            opacity: 0.1;
            pointer-events: none;
        }
        
        .whatsapp-float {
            position: fixed;
            bottom: 30px;
            right: 30px;
            z-index: 100;
            animation: pulse 2s infinite;
        }
        
        @keyframes pulse {
            0%, 100% { transform: scale(1); }
            50% { transform: scale(1.1); }
        }
        
        .service-icon {
            background: linear-gradient(135deg, #0F4C3A 0%, #1A6B52 100%);
        }
    </style>
</head>
<body class="text-gray-800">

    <!-- Navigation -->
    <nav class="fixed w-full z-50 nav-blur border-b border-yellow-200/30 transition-all duration-300" id="navbar">
        <div class="max-w-7xl mx-auto px-4 sm:px-6 lg:px-8">
            <div class="flex justify-between items-center h-20">
                <div class="flex items-center">
                    <span class="font-display text-2xl font-bold text-emerald-900 tracking-wider">RK</span>
                    <span class="ml-2 text-sm text-yellow-600 font-arabic hidden sm:block">رضوان كليوس</span>
                </div>
                <div class="hidden md:flex space-x-8">
                    <a href="#accueil" class="text-gray-700 hover:text-yellow-600 transition-colors font-medium">Accueil</a>
                    <a href="#services" class="text-gray-700 hover:text-yellow-600 transition-colors font-medium">Services</a>
                    <a href="#apropos" class="text-gray-700 hover:text-yellow-600 transition-colors font-medium">À Propos</a>
                    <a href="#contact" class="text-gray-700 hover:text-yellow-600 transition-colors font-medium">Contact</a>
                </div>
                <button onclick="toggleMenu()" class="md:hidden text-gray-700">
                    <svg class="w-6 h-6" fill="none" stroke="currentColor" viewBox="0 0 24 24"><path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M4 6h16M4 12h16M4 18h16"/></svg>
                </button>
            </div>
        </div>
        <!-- Mobile Menu -->
        <div id="mobile-menu" class="hidden md:hidden bg-white border-t">
            <div class="px-4 pt-2 pb-4 space-y-2">
                <a href="#accueil" class="block py-2 text-gray-700">Accueil</a>
                <a href="#services" class="block py-2 text-gray-700">Services</a>
                <a href="#apropos" class="block py-2 text-gray-700">À Propos</a>
                <a href="#contact" class="block py-2 text-gray-700">Contact</a>
            </div>
        </div>
    </nav>

    <!-- Hero Section -->
    <section id="accueil" class="relative min-h-screen flex items-center justify-center hero-pattern geometric-pattern pt-20 overflow-hidden">
        <div class="absolute inset-0 opacity-20">
            <svg class="islamic-geometry top-0 right-0" viewBox="0 0 200 200">
                <path fill="#D4AF37" d="M100,10 L190,100 L100,190 L10,100 Z M100,30 L170,100 L100,170 L30,100 Z"/>
            </svg>
        </div>
        
        <div class="max-w-7xl mx-auto px-4 sm:px-6 lg:px-8 relative z-10 text-center">
            <div class="reveal-text">
                <p class="text-yellow-600 font-arabic text-xl mb-4 tracking-widest">بسم الله الرحمن الرحيم</p>
                <h1 class="font-display text-5xl md:text-7xl font-bold text-emerald-900 mb-6 leading-tight">
                    Redouane <span class="gold-gradient">Kelious</span>
                </h1>
                <p class="text-xl md:text-2xl text-gray-600 mb-4 font-light">Conseiller en Style & Épanouissement Personnel</p>
                <p class="text-gray-500 max-w-2xl mx-auto mb-10 text-lg">
                    Accompagnement sur mesure pour la communauté arabe : développez votre style unique et trouvez l'équilibre dans votre vie personnelle et professionnelle.
                </p>
                <div class="flex flex-col sm:flex-row gap-4 justify-center">
                    <a href="#contact" class="btn-gold text-white px-8 py-4 rounded-full font-semibold text-lg shadow-lg inline-flex items-center justify-center gap-2">
                        <span>Commencer l'aventure</span>
                        <svg class="w-5 h-5" fill="none" stroke="currentColor" viewBox="0 0 24 24"><path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M17 8l4 4m0 0l-4 4m4-4H3"/></svg>
                    </a>
                    <a href="#services" class="border-2 border-emerald-800 text-emerald-900 px-8 py-4 rounded-full font-semibold text-lg hover:bg-emerald-50 transition-all">
                        Découvrir mes services
                    </a>
                </div>
            </div>
        </div>
        
        <div class="absolute bottom-10 left-1/2 transform -translate-x-1/2 animate-bounce">
            <svg class="w-6 h-6 text-yellow-600" fill="none" stroke="currentColor" viewBox="0 0 24 24"><path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M19 14l-7 7m0 0l-7-7m7 7V3"/></svg>
        </div>
    </section>

    <!-- Stats Section -->
    <section class="py-20 bg-emerald-900 text-white relative overflow-hidden">
        <div class="absolute inset-0 opacity-10" style="background-image: url('data:image/svg+xml,%3Csvg width=\'40\' height=\'40\' viewBox=\'0 0 40 40\' xmlns=\'http://www.w3.org/2000/svg\'%3E%3Cg fill=\'%23ffffff\' fill-opacity=\'0.4\' fill-rule=\'evenodd\'%3E%3Cpath d=\'M0 40L40 0H20L0 20M40 40V20L20 40\'/%3E%3C/g%3E%3C/svg%3E');"></div>
        <div class="max-w-7xl mx-auto px-4 sm:px-6 lg:px-8 relative z-10">
            <div class="grid grid-cols-1 md:grid-cols-3 gap-8 text-center">
                <div class="reveal-text">
                    <div class="text-4xl font-bold text-yellow-400 mb-2 counter" data-target="500">0</div>
                    <div class="text-emerald-100">Clients accompagnés</div>
                </div>
                <div class="reveal-text">
                    <div class="text-4xl font-bold text-yellow-400 mb-2 counter" data-target="10">0</div>
                    <div class="text-emerald-100">Années d'expérience</div>
                </div>
                <div class="reveal-text">
                    <div class="text-4xl font-bold text-yellow-400 mb-2 counter" data-target="100">0</div>
                    <div class="text-emerald-100">% Engagement personnel</div>
                </div>
            </div>
        </div>
    </section>

    <!-- Services Section -->
    <section id="services" class="py-24 bg-white relative">
        <div class="max-w-7xl mx-auto px-4 sm:px-6 lg:px-8">
            <div class="text-center mb-16 reveal-text">
                <h2 class="font-display text-4xl md:text-5xl font-bold text-emerald-900 mb-4">Mes Services</h2>
                <div class="w-24 h-1 bg-yellow-500 mx-auto mb-6"></div>
                <p class="text-gray-600 max-w-2xl mx-auto text-lg">
                    Des conseils adaptés à vos valeurs et à votre culture pour un développement harmonieux
                </p>
            </div>

            <div class="grid grid-cols-1 md:grid-cols-2 lg:grid-cols-3 gap-8">
                <!-- Style Conseil -->
                <div class="group card-hover bg-white rounded-2xl overflow-hidden shadow-lg border border-gray-100 reveal-text">
                    <div class="h-48 bg-gradient-to-br from-yellow-100 to-yellow-50 flex items-center justify-center relative overflow-hidden">
                        <div class="absolute inset-0 opacity-20 geometric-pattern"></div>
                        <svg class="w-20 h-20 text-yellow-600 relative z-10" fill="none" stroke="currentColor" viewBox="0 0 24 24"><path stroke-linecap="round" stroke-linejoin="round" stroke-width="1.5" d="M16 11V7a4 4 0 00-8 0v4M5 9h14l1 12H4L5 9z"/></svg>
                    </div>
                    <div class="p-8">
                        <h3 class="font-display text-2xl font-bold text-emerald-900 mb-3">Conseil en Style</h3>
                        <p class="text-gray-600 mb-4">
                            Personnal shopping, analyse colorimétrique, et création d'une garde-robe qui reflète votre personnalité tout en respectant vos valeurs.
                        </p>
                        <ul class="space-y-2 text-sm text-gray-500 mb-6">
                            <li class="flex items-center"><span class="text-yellow-500 mr-2">✦</span> Analyse morphologique</li>
                            <li class="flex items-center"><span class="text-yellow-500 mr-2">✦</span> Shopping accompagné</li>
                            <li class="flex items-center"><span class="text-yellow-500 mr-2">✦</span> Dress code professionnel</li>
                        </ul>
                    </div>
                </div>

                <!-- Développement Personnel -->
                <div class="group card-hover bg-white rounded-2xl overflow-hidden shadow-lg border border-gray-100 reveal-text">
                    <div class="h-48 bg-gradient-to-br from-emerald-100 to-emerald-50 flex items-center justify-center relative overflow-hidden">
                        <div class="absolute inset-0 opacity-20 geometric-pattern"></div>
                        <svg class="w-20 h-20 text-emerald-700 relative z-10" fill="none" stroke="currentColor" viewBox="0 0 24 24"><path stroke-linecap="round" stroke-linejoin="round" stroke-width="1.5" d="M12 6.253v13m0-13C10.832 5.477 9.246 5 7.5 5S4.168 5.477 3 6.253v13C4.168 18.477 5.754 18 7.5 18s3.332.477 4.5 1.253m0-13C13.168 5.477 14.754 5 16.5 5c1.747 0 3.332.477 4.5 1.253v13C19.832 18.477 18.247 18 16.5 18c-1.746 0-3.332.477-4.5 1.253"/></svg>
                    </div>
                    <div class="p-8">
                        <h3 class="font-display text-2xl font-bold text-emerald-900 mb-3">Développement Personnel</h3>
                        <p class="text-gray-600 mb-4">
                            Coaching pour atteindre vos objectifs, gestion du stress, et équilibre entre vie professionnelle et spirituelle.
                        </p>
                        <ul class="space-y-2 text-sm text-gray-500 mb-6">
                            <li class="flex items-center"><span class="text-emerald-500 mr-2">✦</span> Fixation d'objectifs</li>
                            <li class="flex items-center"><span class="text-emerald-500 mr-2">✦</span> Gestion du temps</li>
                            <li class="flex items-center"><span class="text-emerald-500 mr-2">✦</span> Confiance en soi</li>
                        </ul>
                    </div>
                </div>

                <!-- Image de Marque -->
                <div class="group card-hover bg-white rounded-2xl overflow-hidden shadow-lg border border-gray-100 reveal-text">
                    <div class="h-48 bg-gradient-to-br from-amber-100 to-orange-50 flex items-center justify-center relative overflow-hidden">
                        <div class="absolute inset-0 opacity-20 geometric-pattern"></div>
                        <svg class="w-20 h-20 text-amber-700 relative z-10" fill="none" stroke="currentColor" viewBox="0 0 24 24"><path stroke-linecap="round" stroke-linejoin="round" stroke-width="1.5" d="M11 4a2 2 0 114 0v1a1 1 0 001 1h3a1 1 0 011 1v3a1 1 0 01-1 1h-1a2 2 0 100 4h1a1 1 0 011 1v3a1 1 0 01-1 1h-3a1 1 0 01-1-1v-1a2 2 0 10-4 0v1a1 1 0 01-1 1H7a1 1 0 01-1-1v-3a1 1 0 00-1-1H4a2 2 0 110-4h1a1 1 0 001-1V7a1 1 0 011-1h3a1 1 0 001-1V4z"/></svg>
                    </div>
                    <div class="p-8">
                        <h3 class="font-display text-2xl font-bold text-emerald-900 mb-3">Image de Marque</h3>
                        <p class="text-gray-600 mb-4">
                            Construisez une présence authentique sur les réseaux sociaux et dans votre carrière tout en restant fidèle à vos racines.
                        </p>
                        <ul class="space-y-2 text-sm text-gray-500 mb-6">
                            <li class="flex items-center"><span class="text-amber-500 mr-2">✦</span> Personal branding</li>
                            <li class="flex items-center"><span class="text-amber-500 mr-2">✦</span> Communication assertive</li>
                            <li class="flex items-center"><span class="text-amber-500 mr-2">✦</span> Networking efficace</li>
                        </ul>
                    </div>
                </div>
            </div>
        </div>
    </section>

    <!-- About Section -->
    <section id="apropos" class="py-24 bg-gradient-to-b from-gray-50 to-white relative overflow-hidden">
        <div class="max-w-7xl mx-auto px-4 sm:px-6 lg:px-8">
            <div class="grid grid-cols-1 lg:grid-cols-2 gap-16 items-center">
                <div class="relative reveal-text">
                    <div class="absolute -top-4 -left-4 w-24 h-24 border-t-4 border-l-4 border-yellow-500"></div>
                    <div class="absolute -bottom-4 -right-4 w-24 h-24 border-b-4 border-r-4 border-emerald-800"></div>
                    <div class="bg-emerald-900 rounded-2xl p-8 text-white relative z-10 shadow-2xl">
                        <div class="font-arabic text-3xl text-yellow-400 mb-4 text-center">"الأناقة هي لغة الصمت الجميل"</div>
                        <p class="text-center text-emerald-100 italic">"L'élégance est la langue du beau silence"</p>
                    </div>
                </div>
                
                <div class="reveal-text">
                    <h2 class="font-display text-4xl font-bold text-emerald-900 mb-6">Pourquoi me faire confiance ?</h2>
                    <p class="text-gray-600 mb-6 text-lg leading-relaxed">
                        Fort d'une expérience riche auprès de la communauté arabe en Europe et au Moyen-Orient, je comprends les défis uniques de concilier modernité et traditions.
                    </p>
                    <p class="text-gray-600 mb-8 text-lg leading-relaxed">
                        Mon approche combine expertise en style vestimentaire et coaching développement personnel, avec une sensibilité particulière aux valeurs islamiques et culturelles arabes.
                    </p>
                    
                    <div class="space-y-4">
                        <div class="flex items-start">
                            <div class="flex-shrink-0 w-12 h-12 rounded-full bg-yellow-100 flex items-center justify-center mr-4">
                                <svg class="w-6 h-6 text-yellow-600" fill="none" stroke="currentColor" viewBox="0 0 24 24"><path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M5 13l4 4L19 7"/></svg>
                            </div>
                            <div>
                                <h4 class="font-bold text-emerald-900">Approche Culturelle</h4>
                                <p class="text-gray-600">Respect des valeurs et traditions arabes</p>
                            </div>
                        </div>
                        <div class="flex items-start">
                            <div class="flex-shrink-0 w-12 h-12 rounded-full bg-yellow-100 flex items-center justify-center mr-4">
                                <svg class="w-6 h-6 text-yellow-600" fill="none" stroke="currentColor" viewBox="0 0 24 24"><path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M5 13l4 4L19 7"/></svg>
                            </div>
                            <div>
                                <h4 class="font-bold text-emerald-900">Confidentialité Absolue</h4>
                                <p class="text-gray-600">Votre vie privée est sacrée</p>
                            </div>
                        </div>
                        <div class="flex items-start">
                            <div class="flex-shrink-0 w-12 h-12 rounded-full bg-yellow-100 flex items-center justify-center mr-4">
                                <svg class="w-6 h-6 text-yellow-600" fill="none" stroke="currentColor" viewBox="0 0 24 24"><path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M5 13l4 4L19 7"/></svg>
                            </div>
                            <div>
                                <h4 class="font-bold text-emerald-900">Disponibilité Internationale</h4>
                                <p class="text-gray-600">Consultations en ligne et présentiel</p>
                            </div>
                        </div>
                    </div>
                </div>
            </div>
        </div>
    </section>

    <!-- Contact Section -->
    <section id="contact" class="py-24 bg-emerald-900 relative overflow-hidden">
        <div class="absolute inset-0 opacity-10">
            <svg class="w-full h-full" viewBox="0 0 100 100" preserveAspectRatio="none">
                <path d="M0,0 L100,0 L100,100 L0,100 Z" fill="none" stroke="#D4AF37" stroke-width="0.5"/>
                <path d="M0,0 Q50,50 100,0" fill="none" stroke="#D4AF37" stroke-width="0.5"/>
               
