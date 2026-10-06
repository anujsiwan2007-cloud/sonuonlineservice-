<!DOCTYPE html>
<html lang="hi" class="scroll-smooth">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>SONU CYBER - Online Service Portal | Goreakothi, Siwan, Bihar</title>
    
    <!-- Tailwind CSS CDN -->
    <script src="https://cdn.tailwindcss.com"></script>
    <!-- FontAwesome Icons -->
    <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.5.1/css/all.min.css">
    <!-- Google Fonts -->
    <link rel="preconnect" href="https://fonts.googleapis.com">
    <link rel="preconnect" href="https://fonts.gstatic.com" crossorigin>
    <link href="https://fonts.googleapis.com/css2?family=Tiro+Devanagari+Hindi&family=Poppins:wght@400;500;600;700;800;900&family=Outfit:wght@400;500;600;700;800&display=display" rel="stylesheet">

    <script>
        tailwind.config = {
            theme: {
                extend: {
                    fontFamily: {
                        sans: ['Outfit', 'sans-serif'],
                        poppins: ['Poppins', 'sans-serif'],
                        hindi: ['Tiro Devanagari Hindi', 'serif'],
                    },
                    colors: {
                        saffron: '#FF671F',
                        saffronDark: '#D94D00',
                        emeraldGov: '#047857',
                        cyberBlue: '#1E40AF',
                        cyberViolet: '#6D28D9',
                        roseAccent: '#E11D48',
                        goldAshok: '#D97706',
                    },
                    boxShadow: {
                        'vibrant': '0 10px 30px -10px rgba(255, 103, 31, 0.3)',
                        'card-glow': '0 8px 30px rgba(0, 0, 0, 0.08)',
                        'hover-glow': '0 20px 40px -15px rgba(30, 64, 175, 0.25)',
                    }
                }
            }
        }
    </script>

    <style>
        body {
            font-family: 'Outfit', sans-serif;
            background-color: #f8fafc;
        }

        .gradient-hero {
            background: linear-gradient(135deg, #020617 0%, #0f172a 40%, #1e1b4b 100%);
        }

        .badge-glow {
            box-shadow: 0 0 15px rgba(255, 103, 31, 0.5);
        }

        /* Glassmorphism */
        .glass-card {
            background: rgba(255, 255, 255, 0.95);
            backdrop-filter: blur(12px);
        }

        /* Custom Scrollbar */
        ::-webkit-scrollbar { width: 8px; }
        ::-webkit-scrollbar-track { background: #f1f5f9; }
        ::-webkit-scrollbar-thumb { background: #FF671F; border-radius: 4px; }
        ::-webkit-scrollbar-thumb:hover { background: #D94D00; }

        .active-tab-btn {
            background-color: #FF671F !important;
            color: #ffffff !important;
            box-shadow: 0 4px 15px rgba(255, 103, 31, 0.4);
        }

        @keyframes pulse-border {
            0%, 100% { border-color: rgba(255, 103, 31, 1); }
            50% { border-color: rgba(16, 185, 129, 1); }
        }

        .pulsing-border {
            animation: pulse-border 3s infinite;
        }
    </style>
</head>
<body class="text-slate-800 antialiased selection:bg-saffron selection:text-white">

    <div class="bg-gradient-to-r from-slate-950 via-indigo-950 to-slate-950 text-white text-xs py-2 px-4 border-b border-indigo-900/50 sticky top-0 z-50">
        <div class="max-w-7xl mx-auto flex flex-wrap justify-between items-center gap-2">
            <!-- Left Location & Shop Details -->
            <div class="flex items-center gap-2 overflow-x-auto py-0.5">
                <span class="inline-flex items-center gap-1.5 px-2.5 py-0.5 rounded-full bg-saffron text-slate-950 font-black text-[11px]">
                    <i class="fa-solid fa-location-dot"></i> GOREAKOTHI, SIWAN
                </span>
                <span class="text-slate-300 hidden sm:inline text-[11px] font-medium">
                    <i class="fa-solid fa-map-pin text-saffron mr-1"></i> College Road, Goreakothi, Siwan, Bihar - 841434
                </span>
            </div>

            <!-- Right Direct Action Phone & WhatsApp -->
            <div class="flex items-center gap-3 ml-auto text-[11px] font-bold">
                <a href="tel:8227002020" class="bg-blue-600 hover:bg-blue-700 text-white px-3 py-1 rounded-full transition-all flex items-center gap-1.5 shadow-md">
                    <i class="fa-solid fa-phone-volume text-amber-300"></i>
                    <span>Call: 8227002020</span>
                </a>
                <a href="https://wa.me/918227002020?text=Hello%20Sonu%20Cyber%20Goreakothi,%20mujhe%20online%20service%20ke%20baare%20me%20jaankari%20chahiye." target="_blank" class="bg-emerald-600 hover:bg-emerald-700 text-white px-3 py-1 rounded-full transition-all flex items-center gap-1.5 shadow-md">
                    <i class="fa-brands fa-whatsapp text-lg"></i>
                    <span>WhatsApp</span>
                </a>
            </div>
        </div>
    </div>

    <header class="bg-slate-900 text-white border-b border-white/10 shadow-xl relative z-40">
        <div class="max-w-7xl mx-auto px-4 sm:px-6 lg:px-8 py-3.5">
            <div class="flex items-center justify-between gap-4">
                
                <!-- Main Brand Emblem & Shop Name -->
                <a href="#home" class="flex items-center gap-3 group">
                    <div class="w-12 h-12 rounded-2xl bg-gradient-to-tr from-saffron via-amber-500 to-emerald-500 p-0.5 shadow-lg group-hover:scale-105 transition-transform">
                        <div class="w-full h-full bg-slate-950 rounded-[14px] flex flex-col items-center justify-center border border-white/20">
                            <span class="font-black text-saffron text-lg leading-none">SC</span>
                            <span class="text-[8px] font-extrabold text-emerald-400">SIWAN</span>
                        </div>
                    </div>
                    <div>
                        <div class="flex items-center gap-2">
                            <h1 class="text-xl sm:text-2xl font-black font-poppins tracking-tight bg-gradient-to-r from-white via-amber-200 to-saffron bg-clip-text text-transparent">
                                SONU CYBER
                            </h1>
                            <span class="bg-emerald-500/20 text-emerald-300 border border-emerald-500/40 text-[10px] font-black px-2 py-0.5 rounded-md">VERIFIED</span>
                        </div>
                        <p class="text-[11px] text-slate-300 font-medium tracking-wide flex items-center gap-1">
                            <i class="fa-solid fa-graduation-cap text-saffron"></i> College Road, Goreakothi (Siwan)
                        </p>
                    </div>
                </a>

                <!-- Middle Search Input Bar -->
                <div class="hidden lg:flex flex-1 max-w-md mx-6">
                    <div class="relative w-full">
                        <input type="text" id="global-search" onkeyup="liveSearchServices()" placeholder="🔍 Khoj: Aadhaar, PAN, RTPS, Admit Card, Photo..." class="w-full bg-slate-950 border-2 border-saffron/40 rounded-xl px-4 py-2.5 pl-10 text-xs text-white placeholder-slate-400 focus:outline-none focus:border-emerald-400 transition-all shadow-inner">
                        <i class="fa-solid fa-magnifying-glass absolute left-3.5 top-3.5 text-saffron text-xs"></i>
                    </div>
                </div>

                <!-- Govt Emblem & Fast Link Buttons -->
                <div class="hidden sm:flex items-center gap-2">
                    <div class="bg-white/10 px-3 py-1.5 rounded-xl border border-white/10 text-center">
                        <p class="text-[9px] font-bold text-slate-300 uppercase">Government Portal</p>
                        <p class="text-[11px] font-extrabold text-saffron">Direct Link Support</p>
                    </div>
                    <a href="https://maps.google.com/?q=College+Road+Goreakothi+Siwan+Bihar+841434" target="_blank" class="bg-slate-800 hover:bg-slate-700 text-white p-2.5 rounded-xl border border-white/10 transition-colors text-xs font-bold flex items-center gap-1" title="Open Google Maps Location">
                        <i class="fa-solid fa-map-location-dot text-saffron"></i>
                        <span class="hidden md:inline">Map</span>
                    </a>
                </div>

            </div>

            <!-- Mobile Search Bar -->
            <div class="mt-3 lg:hidden">
                <input type="text" id="mobile-search" onkeyup="liveSearchServices(true)" placeholder="🔍 Kisi bhi service ko khoje (Aadhaar, RTPS, Form...)" class="w-full bg-slate-950 border-2 border-saffron/50 rounded-xl px-4 py-2 text-xs text-white placeholder-slate-400 focus:outline-none focus:border-emerald-400">
            </div>
        </div>
    </header>

    <section id="home" class="gradient-hero text-white py-10 lg:py-14 relative overflow-hidden border-b-4 border-saffron">
        <div class="max-w-7xl mx-auto px-4 sm:px-6 lg:px-8 relative z-10">
            <div class="grid lg:grid-cols-12 gap-8 items-center">
                
                <!-- Left Title & Intro -->
                <div class="lg:col-span-7 space-y-4 text-center lg:text-left">
                    <div class="inline-flex items-center gap-2 px-3.5 py-1 rounded-full bg-saffron/20 border border-saffron/50 text-xs font-bold text-saffron backdrop-blur-md">
                        <i class="fa-solid fa-star text-amber-300"></i> Goreakothi Siwan Ka Reliable Online Cyber Cafe
                    </div>

                    <h2 class="text-2xl sm:text-4xl lg:text-5xl font-black font-poppins leading-tight">
                        Sabhi Digital va Sarkari Kaam <br>
                        <span class="bg-gradient-to-r from-saffron via-amber-300 to-emerald-400 bg-clip-text text-transparent">
                            Aasani Se Step-By-Step Karo!
                        </span>
                    </h2>

                    <p class="text-slate-300 text-xs sm:text-sm font-hindi leading-relaxed max-w-xl mx-auto lg:mx-0">
                        Aadhaar, PAN Card, Bihar RTPS (Jati, Aay, Niwas), Voter ID, College Admission, Job Forms, Passport Photo aur Payment ka direct link aur step-by-step jankari yahan uplabdha hai.
                    </p>

                    <!-- Direct Contact Callouts -->
                    <div class="pt-2 flex flex-wrap items-center justify-center lg:justify-start gap-3">
                        <a href="tel:8227002020" class="bg-saffron hover:bg-saffronDark text-white font-bold px-5 py-3 rounded-xl shadow-lg shadow-saffron/30 transition-all text-xs flex items-center gap-2 hover:scale-105">
                            <i class="fa-solid fa-phone text-sm"></i> Call Now: 8227002020
                        </a>
                        <a href="#guided-wizard" class="bg-emerald-600 hover:bg-emerald-700 text-white font-bold px-5 py-3 rounded-xl shadow-lg transition-all text-xs flex items-center gap-2 hover:scale-105">
                            <i class="fa-solid fa-hand-pointer text-sm"></i> Interactive Step Guide
                        </a>
                    </div>
                </div>

                <!-- Right Quick Stats Card -->
                <div class="lg:col-span-5">
                    <div class="bg-slate-900/90 border-2 border-saffron/30 p-6 rounded-3xl shadow-2xl backdrop-blur-md space-y-4">
                        <div class="flex items-center justify-between border-b border-white/10 pb-3">
                            <div class="flex items-center gap-2">
                                <span class="text-2xl">🏛️</span>
                                <div>
                                    <h3 class="font-bold text-white text-sm font-poppins">Official Portal Direct Links</h3>
                                    <p class="text-[10px] text-emerald-400 font-bold">100% Genuine & Verified Direct Websites</p>
                                </div>
                            </div>
                        </div>

                        <div class="grid grid-cols-2 gap-2 text-xs">
                            <div class="bg-white/10 p-2.5 rounded-xl border border-white/10 text-center font-bold text-saffron">
                                <i class="fa-solid fa-id-card block text-base mb-1"></i> Aadhaar UIDAI
                            </div>
                            <div class="bg-white/10 p-2.5 rounded-xl border border-white/10 text-center font-bold text-emerald-400">
                                <i class="fa-solid fa-landmark block text-base mb-1"></i> Bihar RTPS
                            </div>
                            <div class="bg-white/10 p-2.5 rounded-xl border border-white/10 text-center font-bold text-amber-300">
                                <i class="fa-solid fa-credit-card block text-base mb-1"></i> PAN NSDL/IT
                            </div>
                            <div class="bg-white/10 p-2.5 rounded-xl border border-white/10 text-center font-bold text-sky-300">
                                <i class="fa-solid fa-graduation-cap block text-base mb-1"></i> Scholarship
                            </div>
                        </div>

                        <div class="bg-amber-500/10 border border-amber-500/30 p-3 rounded-xl text-[11px] text-amber-200 text-center font-medium">
                            📍 <strong>Dukan Ka Pata:</strong> College Road, Goreakothi, Siwan, Bihar - 841434
                        </div>
                    </div>
                </div>

            </div>
        </div>
    </section>

    <section id="guided-wizard" class="py-14 bg-gradient-to-b from-slate-100 to-white border-b border-slate-200">
        <div class="max-w-7xl mx-auto px-4 sm:px-6 lg:px-8">
            
            <div class="text-center max-w-3xl mx-auto mb-10">
                <span class="inline-block px-3 py-1 rounded-full bg-saffron text-white text-xs font-black uppercase tracking-widest mb-2 shadow-md">
                    🎯 STEP-BY-STEP EASY WORKFLOW
                </span>
                <h2 class="text-2xl sm:text-3xl font-black text-slate-900 font-poppins">Aapko Konsa Kaam Karna Hai?</h2>
                <p class="text-slate-600 text-xs sm:text-sm mt-1 font-hindi">Niche category chuniye, apna kaam select kariye aur direct official link ya step guide paiye!</p>
            </div>

            <!-- STEP 1: CATEGORY SELECTION TABS -->
            <div class="mb-8">
                <p class="text-center text-xs font-bold text-slate-500 uppercase tracking-wider mb-3">Step 1: Main Category Select Karein</p>
                <div class="flex flex-wrap items-center justify-center gap-2.5" id="wizard-tab-buttons">
                    <button onclick="switchWizardTab('govt', event)" class="wizard-tab-btn active-tab-btn px-4 py-2.5 rounded-xl font-bold text-xs transition-all flex items-center gap-2 border border-slate-300 bg-white text-slate-700 hover:border-saffron">
                        <i class="fa-solid fa-building-columns text-saffron"></i> Sarkari Services
                    </button>
                    <button onclick="switchWizardTab('education', event)" class="wizard-tab-btn px-4 py-2.5 rounded-xl font-bold text-xs transition-all flex items-center gap-2 border border-slate-300 bg-white text-slate-700 hover:border-cyberBlue">
                        <i class="fa-solid fa-graduation-cap text-cyberBlue"></i> Education & Scholarship
                    </button>
                    <button onclick="switchWizardTab('jobs', event)" class="wizard-tab-btn px-4 py-2.5 rounded-xl font-bold text-xs transition-all flex items-center gap-2 border border-slate-300 bg-white text-slate-700 hover:border-emeraldGov">
                        <i class="fa-solid fa-briefcase text-emeraldGov"></i> Job & Vacancy
                    </button>
                    <button onclick="switchWizardTab('travel', event)" class="wizard-tab-btn px-4 py-2.5 rounded-xl font-bold text-xs transition-all flex items-center gap-2 border border-slate-300 bg-white text-slate-700 hover:border-roseAccent">
                        <i class="fa-solid fa-train text-roseAccent"></i> Travel & Bills
                    </button>
                    <button onclick="switchWizardTab('photo', event)" class="wizard-tab-btn px-4 py-2.5 rounded-xl font-bold text-xs transition-all flex items-center gap-2 border border-slate-300 bg-white text-slate-700 hover:border-cyberViolet">
                        <i class="fa-solid fa-camera text-cyberViolet"></i> Photo & Documents
                    </button>
                </div>
            </div>

            <!-- STEP 2 & 3 CONTAINER -->
            <div class="bg-white rounded-3xl p-6 sm:p-8 border-2 border-indigo-100 shadow-hover-glow max-w-5xl mx-auto">
                <div id="wizard-dynamic-content">
                    <!-- Dynamic Content populated via JavaScript -->
                </div>
            </div>

        </div>
    </section>

    <section id="all-services" class="py-16 bg-slate-50">
        <div class="max-w-7xl mx-auto px-4 sm:px-6 lg:px-8">
            
            <div class="text-center max-w-3xl mx-auto mb-12">
                <span class="inline-block px-3 py-1 rounded-full bg-emeraldGov text-white text-xs font-black uppercase tracking-widest mb-2 shadow-md">
                    ⚡ DIRECT ACTION PORTALS
                </span>
                <h2 class="text-2xl sm:text-3xl font-black text-slate-900 font-poppins">Sabhi Services Ke Direct Link & Details</h2>
                <p class="text-slate-600 text-xs mt-1">Niche har kaam ka direct link aur step-by-step details diye gaye hain.</p>
                <div class="w-20 h-1.5 bg-gradient-to-r from-saffron to-emeraldGov mx-auto mt-3 rounded-full"></div>
            </div>

            <div class="grid md:grid-cols-2 lg:grid-cols-3 gap-6" id="services-cards-grid">

                <!-- CARD 1: AADHAAR -->
                <div class="service-box bg-white rounded-2xl border-2 border-slate-200 p-6 shadow-card-glow hover:border-saffron transition-all border-t-8 border-t-saffron">
                    <div class="flex items-center justify-between mb-3">
                        <div class="w-12 h-12 rounded-2xl bg-saffron/10 text-saffron flex items-center justify-center text-xl font-black">
                            <i class="fa-solid fa-address-card"></i>
                        </div>
                        <span class="text-[10px] font-black bg-orange-100 text-saffron px-2.5 py-1 rounded-full border border-orange-200">UIDAI OFFICIAL</span>
                    </div>

                    <h3 class="text-lg font-black text-slate-900 font-poppins">AADHAAR SERVICES</h3>
                    <p class="text-xs text-slate-500 mb-4 font-hindi">Aadhaar Download, Update, PVC Card, Biometrics Lock/Unlock</p>

                    <div class="space-y-2 mb-6 text-xs">
                        <a href="https://myaadhaar.uidai.gov.in/genricDownloadAadhaar" target="_blank" class="w-full bg-slate-100 hover:bg-saffron hover:text-white p-2.5 rounded-xl font-bold flex items-center justify-between transition-colors">
                            <span><i class="fa-solid fa-download mr-2 text-saffron"></i> 1. Download Aadhaar PDF</span>
                            <i class="fa-solid fa-arrow-up-right-from-square text-[10px]"></i>
                        </a>
                        <a href="https://myaadhaar.uidai.gov.in/check-aadhaar-validity" target="_blank" class="w-full bg-slate-100 hover:bg-saffron hover:text-white p-2.5 rounded-xl font-bold flex items-center justify-between transition-colors">
                            <span><i class="fa-solid fa-circle-check mr-2 text-saffron"></i> 2. Check Aadhaar Status</span>
                            <i class="fa-solid fa-arrow-up-right-from-square text-[10px]"></i>
                        </a>
                        <a href="https://myaadhaar.uidai.gov.in/order-pvc-card" target="_blank" class="w-full bg-slate-100 hover:bg-saffron hover:text-white p-2.5 rounded-xl font-bold flex items-center justify-between transition-colors">
                            <span><i class="fa-solid fa-box-archive mr-2 text-saffron"></i> 3. Order Aadhaar PVC Card</span>
                            <i class="fa-solid fa-arrow-up-right-from-square text-[10px]"></i>
                        </a>
                    </div>

                    <a href="https://myaadhaar.uidai.gov.in/" target="_blank" class="w-full bg-saffron hover:bg-saffronDark text-white font-black py-3 rounded-xl transition-all text-xs flex items-center justify-center gap-2 shadow-md">
                        <i class="fa-solid fa-globe"></i> Open Main UIDAI Portal
                    </a>
                </div>

                <!-- CARD 2: PAN CARD -->
                <div class="service-box bg-white rounded-2xl border-2 border-slate-200 p-6 shadow-card-glow hover:border-cyberBlue transition-all border-t-8 border-t-cyberBlue">
                    <div class="flex items-center justify-between mb-3">
                        <div class="w-12 h-12 rounded-2xl bg-blue-100 text-cyberBlue flex items-center justify-center text-xl font-black">
                            <i class="fa-solid fa-id-card-clip"></i>
                        </div>
                        <span class="text-[10px] font-black bg-blue-100 text-cyberBlue px-2.5 py-1 rounded-full border border-blue-200">INCOME TAX / NSDL</span>
                    </div>

                    <h3 class="text-lg font-black text-slate-900 font-poppins">PAN CARD SERVICES</h3>
                    <p class="text-xs text-slate-500 mb-4 font-hindi">New Instant PAN Card, Name/DOB Correction, PAN-Aadhaar Link</p>

                    <div class="space-y-2 mb-6 text-xs">
                        <a href="https://eportal.incometax.gov.in/iec/foservices/#/pre-login/instant-e-pan" target="_blank" class="w-full bg-slate-100 hover:bg-cyberBlue hover:text-white p-2.5 rounded-xl font-bold flex items-center justify-between transition-colors">
                            <span><i class="fa-solid fa-plus-circle mr-2 text-cyberBlue"></i> 1. New Instant e-PAN</span>
                            <i class="fa-solid fa-arrow-up-right-from-square text-[10px]"></i>
                        </a>
                        <a href="https://www.onlineservices.nsdl.com/paam/endUserRegisterContact.html" target="_blank" class="w-full bg-slate-100 hover:bg-cyberBlue hover:text-white p-2.5 rounded-xl font-bold flex items-center justify-between transition-colors">
                            <span><i class="fa-solid fa-wrench mr-2 text-cyberBlue"></i> 2. PAN Correction Application</span>
                            <i class="fa-solid fa-arrow-up-right-from-square text-[10px]"></i>
                        </a>
                        <a href="https://eportal.incometax.gov.in/iec/foservices/#/pre-login/link-aadhaar" target="_blank" class="w-full bg-slate-100 hover:bg-cyberBlue hover:text-white p-2.5 rounded-xl font-bold flex items-center justify-between transition-colors">
                            <span><i class="fa-solid fa-link mr-2 text-cyberBlue"></i> 3. Link PAN with Aadhaar</span>
                            <i class="fa-solid fa-arrow-up-right-from-square text-[10px]"></i>
                        </a>
                    </div>

                    <a href="https://eportal.incometax.gov.in/" target="_blank" class="w-full bg-cyberBlue hover:bg-indigo-900 text-white font-black py-3 rounded-xl transition-all text-xs flex items-center justify-center gap-2 shadow-md">
                        <i class="fa-solid fa-globe"></i> Open Income Tax Portal
                    </a>
                </div>

                <!-- CARD 3: BIHAR RTPS -->
                <div class="service-box bg-white rounded-2xl border-2 border-slate-200 p-6 shadow-card-glow hover:border-emeraldGov transition-all border-t-8 border-t-emeraldGov">
                    <div class="flex items-center justify-between mb-3">
                        <div class="w-12 h-12 rounded-2xl bg-emerald-100 text-emeraldGov flex items-center justify-center text-xl font-black">
                            <i class="fa-solid fa-landmark-flag"></i>
                        </div>
                        <span class="text-[10px] font-black bg-emerald-100 text-emerald-800 px-2.5 py-1 rounded-full border border-emerald-200">SERVICES PLUS BIHAR</span>
                    </div>

                    <h3 class="text-lg font-black text-slate-900 font-poppins">BIHAR RTPS CERTIFICATES</h3>
                    <p class="text-xs text-slate-500 mb-4 font-hindi">Jati (Caste), Aay (Income), Niwas (Residence), NCL, EWS Certificate</p>

                    <div class="space-y-2 mb-6 text-xs">
                        <a href="https://serviceonline.bihar.gov.in/" target="_blank" class="w-full bg-slate-100 hover:bg-emeraldGov hover:text-white p-2.5 rounded-xl font-bold flex items-center justify-between transition-colors">
                            <span><i class="fa-solid fa-file-pen mr-2 text-emeraldGov"></i> 1. Apply Jati / Aay / Niwas</span>
                            <i class="fa-solid fa-arrow-up-right-from-square text-[10px]"></i>
                        </a>
                        <a href="https://serviceonline.bihar.gov.in/officials/Citizen/TrackApplicationStatus.do" target="_blank" class="w-full bg-slate-100 hover:bg-emeraldGov hover:text-white p-2.5 rounded-xl font-bold flex items-center justify-between transition-colors">
                            <span><i class="fa-solid fa-magnifying-glass-location mr-2 text-emeraldGov"></i> 2. Track Application Status</span>
                            <i class="fa-solid fa-arrow-up-right-from-square text-[10px]"></i>
                        </a>
                        <a href="https://serviceonline.bihar.gov.in/officials/Citizen/CertificateDownload.do" target="_blank" class="w-full bg-slate-100 hover:bg-emeraldGov hover:text-white p-2.5 rounded-xl font-bold flex items-center justify-between transition-colors">
                            <span><i class="fa-solid fa-file-arrow-down mr-2 text-emeraldGov"></i> 3. Download Certificate PDF</span>
                            <i class="fa-solid fa-arrow-up-right-from-square text-[10px]"></i>
                        </a>
                    </div>

                    <a href="https://serviceonline.bihar.gov.in/" target="_blank" class="w-full bg-emeraldGov hover:bg-emerald-900 text-white font-black py-3 rounded-xl transition-all text-xs flex items-center justify-center gap-2 shadow-md">
                        <i class="fa-solid fa-globe"></i> Open Official Bihar RTPS Site
                    </a>
                </div>

                <!-- CARD 4: VOTER ID -->
                <div class="service-box bg-white rounded-2xl border-2 border-slate-200 p-6 shadow-card-glow hover:border-goldAshok transition-all border-t-8 border-t-goldAshok">
                    <div class="flex items-center justify-between mb-3">
                        <div class="w-12 h-12 rounded-2xl bg-amber-100 text-goldAshok flex items-center justify-center text-xl font-black">
                            <i class="fa-solid fa-check-to-slot"></i>
                        </div>
                        <span class="text-[10px] font-black bg-amber-100 text-goldAshok px-2.5 py-1 rounded-full border border-amber-200">ECI VOTERS</span>
                    </div>

                    <h3 class="text-lg font-black text-slate-900 font-poppins">VOTER ID CARD</h3>
                    <p class="text-xs text-slate-500 mb-4 font-hindi">Naya Voter ID Register Karein, Correction Karein, EPIC Card Download</p>

                    <div class="space-y-2 mb-6 text-xs">
                        <a href="https://voters.eci.gov.in/form6" target="_blank" class="w-full bg-slate-100 hover:bg-goldAshok hover:text-white p-2.5 rounded-xl font-bold flex items-center justify-between transition-colors">
                            <span><i class="fa-solid fa-user-plus mr-2 text-goldAshok"></i> 1. New Voter Registration (Form 6)</span>
                            <i class="fa-solid fa-arrow-up-right-from-square text-[10px]"></i>
                        </a>
                        <a href="https://voters.eci.gov.in/form8" target="_blank" class="w-full bg-slate-100 hover:bg-goldAshok hover:text-white p-2.5 rounded-xl font-bold flex items-center justify-between transition-colors">
                            <span><i class="fa-solid fa-user-gear mr-2 text-goldAshok"></i> 2. Voter Correction (Form 8)</span>
                            <i class="fa-solid fa-arrow-up-right-from-square text-[10px]"></i>
                        </a>
                        <a href="https://voters.eci.gov.in/download-epic" target="_blank" class="w-full bg-slate-100 hover:bg-goldAshok hover:text-white p-2.5 rounded-xl font-bold flex items-center justify-between transition-colors">
                            <span><i class="fa-solid fa-download mr-2 text-goldAshok"></i> 3. Download Voter EPIC Card</span>
                            <i class="fa-solid fa-arrow-up-right-from-square text-[10px]"></i>
                        </a>
                    </div>

                    <a href="https://voters.eci.gov.in/" target="_blank" class="w-full bg-goldAshok hover:bg-amber-700 text-white font-black py-3 rounded-xl transition-all text-xs flex items-center justify-center gap-2 shadow-md">
                        <i class="fa-solid fa-globe"></i> Open ECI Voters Portal
                    </a>
                </div>

                <!-- CARD 5: PASSPORT & DRIVING LICENSE -->
                <div class="service-box bg-white rounded-2xl border-2 border-slate-200 p-6 shadow-card-glow hover:border-cyberViolet transition-all border-t-8 border-t-cyberViolet">
                    <div class="flex items-center justify-between mb-3">
                        <div class="w-12 h-12 rounded-2xl bg-purple-100 text-cyberViolet flex items-center justify-center text-xl font-black">
                            <i class="fa-solid fa-passport"></i>
                        </div>
                        <span class="text-[10px] font-black bg-purple-100 text-cyberViolet px-2.5 py-1 rounded-full border border-purple-200">PASSPORT / PARIVAHAN</span>
                    </div>

                    <h3 class="text-lg font-black text-slate-900 font-poppins">PASSPORT & LICENCE</h3>
                    <p class="text-xs text-slate-500 mb-4 font-hindi">Fresh Passport Application, Learner Licence, DL Renewal</p>

                    <div class="space-y-2 mb-6 text-xs">
                        <a href="https://www.passportindia.gov.in/" target="_blank" class="w-full bg-slate-100 hover:bg-cyberViolet hover:text-white p-2.5 rounded-xl font-bold flex items-center justify-between transition-colors">
                            <span><i class="fa-solid fa-plane-departure mr-2 text-cyberViolet"></i> 1. Passport Seva Portal</span>
                            <i class="fa-solid fa-arrow-up-right-from-square text-[10px]"></i>
                        </a>
                        <a href="https://parivahan.gov.in/parivahan//en/content/mparivahan" target="_blank" class="w-full bg-slate-100 hover:bg-cyberViolet hover:text-white p-2.5 rounded-xl font-bold flex items-center justify-between transition-colors">
                            <span><i class="fa-solid fa-id-badge mr-2 text-cyberViolet"></i> 2. Driving Licence (Parivahan)</span>
                            <i class="fa-solid fa-arrow-up-right-from-square text-[10px]"></i>
                        </a>
                        <a href="https://crsorgi.gov.in/" target="_blank" class="w-full bg-slate-100 hover:bg-cyberViolet hover:text-white p-2.5 rounded-xl font-bold flex items-center justify-between transition-colors">
                            <span><i class="fa-solid fa-baby mr-2 text-cyberViolet"></i> 3. Birth / Death Certificate (CRS)</span>
                            <i class="fa-solid fa-arrow-up-right-from-square text-[10px]"></i>
                        </a>
                    </div>

                    <a href="https://parivahan.gov.in/" target="_blank" class="w-full bg-cyberViolet hover:bg-purple-900 text-white font-black py-3 rounded-xl transition-all text-xs flex items-center justify-center gap-2 shadow-md">
                        <i class="fa-solid fa-globe"></i> Open Parivahan Govt Portal
                    </a>
                </div>

                <!-- CARD 6: ELECTRICITY BILL & BUSINESS -->
                <div class="service-box bg-white rounded-2xl border-2 border-slate-200 p-6 shadow-card-glow hover:border-roseAccent transition-all border-t-8 border-t-roseAccent">
                    <div class="flex items-center justify-between mb-3">
                        <div class="w-12 h-12 rounded-2xl bg-rose-100 text-roseAccent flex items-center justify-center text-xl font-black">
                            <i class="fa-solid fa-bolt"></i>
                        </div>
                        <span class="text-[10px] font-black bg-rose-100 text-roseAccent px-2.5 py-1 rounded-full border border-rose-200">BIHAR UTILITY / UDYAM</span>
                    </div>

                    <h3 class="text-lg font-black text-slate-900 font-poppins">BILL PAYMENT & UDYAM</h3>
                    <p class="text-xs text-slate-500 mb-4 font-hindi">SBPDCL/NBPDCL Bijli Bill Payment, Udyam MSME, GST Registration</p>

                    <div class="space-y-2 mb-6 text-xs">
                        <a href="https://www.sbpdcl.co.in/" target="_blank" class="w-full bg-slate-100 hover:bg-roseAccent hover:text-white p-2.5 rounded-xl font-bold flex items-center justify-between transition-colors">
                            <span><i class="fa-solid fa-plug mr-2 text-roseAccent"></i> 1. SBPDCL Bijli Bill Online</span>
                            <i class="fa-solid fa-arrow-up-right-from-square text-[10px]"></i>
                        </a>
                        <a href="https://udyamregistration.gov.in/" target="_blank" class="w-full bg-slate-100 hover:bg-roseAccent hover:text-white p-2.5 rounded-xl font-bold flex items-center justify-between transition-colors">
                            <span><i class="fa-solid fa-building mr-2 text-roseAccent"></i> 2. Udyam MSME Registration</span>
                            <i class="fa-solid fa-arrow-up-right-from-square text-[10px]"></i>
                        </a>
                        <a href="https://www.gst.gov.in/" target="_blank" class="w-full bg-slate-100 hover:bg-roseAccent hover:text-white p-2.5 rounded-xl font-bold flex items-center justify-between transition-colors">
                            <span><i class="fa-solid fa-file-invoice-dollar mr-2 text-roseAccent"></i> 3. GST Services Portal</span>
                            <i class="fa-solid fa-arrow-up-right-from-square text-[10px]"></i>
                        </a>
                    </div>

                    <a href="https://udyamregistration.gov.in/" target="_blank" class="w-full bg-roseAccent hover:bg-rose-800 text-white font-black py-3 rounded-xl transition-all text-xs flex items-center justify-center gap-2 shadow-md">
                        <i class="fa-solid fa-globe"></i> Open MSME Udyam Site
                    </a>
                </div>

            </div>
        </div>
    </section>

    <section id="photo-studio" class="py-14 bg-slate-950 text-white relative overflow-hidden border-t-4 border-emeraldGov">
        <div class="max-w-7xl mx-auto px-4 sm:px-6 lg:px-8">
            <div class="text-center max-w-2xl mx-auto mb-8">
                <span class="px-3 py-1 rounded-full bg-saffron text-slate-950 text-xs font-black uppercase tracking-widest">
                    📸 FREE PHOTO SIZE TOOL
                </span>
                <h2 class="text-2xl sm:text-3xl font-black font-poppins mt-2">Passport Photo Resizer Tool</h2>
                <p class="text-slate-400 text-xs mt-1 font-hindi">Apni photo upload karein, size select karein aur frame me preview dekhein. Sonu Cyber me high quality printout lein.</p>
            </div>

            <div class="bg-slate-900 rounded-3xl p-6 lg:p-8 border-2 border-indigo-500/30 shadow-2xl max-w-4xl mx-auto">
                <div class="grid md:grid-cols-12 gap-8 items-center">
                    
                    <div class="md:col-span-7 space-y-4">
                        <div>
                            <label class="block text-xs font-bold text-saffron mb-1.5">1. Select Photo Printing Standard *</label>
                            <select id="studio-size-select" onchange="changeStudioPhotoFrame()" class="w-full bg-slate-950 border border-saffron/40 text-white text-xs rounded-xl p-3 focus:outline-none focus:ring-2 focus:ring-saffron font-bold">
                                <option value="passport">Passport Size (3.5 cm x 4.5 cm) - Exam & Govt Forms</option>
                                <option value="stamp">Stamp / 2x2 Inch (Passport / Visa Standard)</option>
                                <option value="size_3x4">3x4 cm Small Photo Size</option>
                                <option value="size_4x6">4x6 Inch Postcard Photo Size</option>
                            </select>
                        </div>

                        <div>
                            <label class="block text-xs font-bold text-saffron mb-1.5">2. Choose Photo File From Mobile / Computer *</label>
                            <input type="file" id="studio-photo-file" accept="image/*" onchange="loadStudioPhotoPreview(event)" class="w-full text-xs text-slate-400 file:mr-4 file:py-2.5 file:px-4 file:rounded-xl file:border-0 file:text-xs file:font-black file:bg-saffron file:text-white hover:file:bg-saffronDark cursor-pointer bg-slate-950 rounded-xl border border-indigo-500/30 p-1">
                        </div>

                        <div class="bg-slate-950 p-3.5 rounded-xl border border-white/10 space-y-1 text-xs">
                            <p class="font-bold text-emerald-400 flex items-center gap-1.5"><i class="fa-solid fa-print"></i> Shop Printing Rates Available At Sonu Cyber:</p>
                            <p class="text-slate-400 text-[11px]">Passport Photo Sets (6, 12, 32 Copies), HD Glossy Color Prints, Urgent Lamination & Document Photocopy.</p>
                        </div>
                    </div>

                    <!-- Live Frame Box -->
                    <div class="md:col-span-5 flex flex-col items-center justify-center border-t md:border-t-0 md:border-l border-white/10 pt-6 md:pt-0 md:pl-8">
                        <p class="text-xs font-bold text-slate-400 mb-2 uppercase tracking-wider">Live Frame Preview</p>
                        
                        <div id="studio-frame-box" class="w-36 h-44 bg-slate-950 border-4 border-dashed border-saffron/80 rounded-2xl flex items-center justify-center overflow-hidden shadow-2xl relative transition-all">
                            <img id="studio-preview-img" src="" alt="Photo Preview" class="hidden w-full h-full object-cover">
                            <div id="studio-placeholder" class="text-center p-3">
                                <i class="fa-solid fa-image text-4xl text-slate-700 mb-2"></i>
                                <p class="text-[10px] text-slate-500 font-bold">Upload photo to see live frame size</p>
                            </div>
                        </div>

                        <span id="studio-dimension-label" class="mt-3 text-[10px] font-mono bg-saffron/20 text-saffron border border-saffron/40 px-3 py-1 rounded-full font-bold">
                            Dimension: 3.5cm x 4.5cm
                        </span>
                    </div>

                </div>
            </div>
        </div>
    </section>

    <section id="contact" class="py-16 bg-white border-t border-slate-200">
        <div class="max-w-7xl mx-auto px-4 sm:px-6 lg:px-8">
            <div class="grid lg:grid-cols-12 gap-10 items-start">
                
                <!-- Shop Details Block -->
                <div class="lg:col-span-5 space-y-6">
                    <div>
                        <span class="px-3 py-1 rounded-full bg-saffron text-white text-xs font-black uppercase tracking-widest shadow-md">📍 Visit Us In Goreakothi</span>
                        <h2 class="text-2xl sm:text-3xl font-black text-slate-900 font-poppins mt-2">SONU CYBER</h2>
                        <p class="text-xs text-slate-600 mt-1 font-hindi">Goreakothi aur aas-paas ke sabhi logo ke liye vishwasniya digital cyber cafe.</p>
                    </div>

                    <div class="bg-slate-50 p-6 rounded-3xl border-2 border-slate-200 space-y-4 text-xs">
                        <div class="flex items-start gap-3">
                            <div class="w-10 h-10 rounded-xl bg-saffron/10 text-saffron flex items-center justify-center text-lg font-bold shrink-0">
                                <i class="fa-solid fa-shop"></i>
                            </div>
                            <div>
                                <p class="font-bold text-slate-900 text-sm">Shop Address</p>
                                <p class="text-slate-600 font-hindi mt-0.5">College Road, Goreakothi, Siwan, Bihar - 841434</p>
                                <a href="https://maps.google.com/?q=College+Road+Goreakothi+Siwan+Bihar+841434" target="_blank" class="inline-flex items-center gap-1 text-saffron font-bold text-[11px] mt-1 hover:underline">
                                    <i class="fa-solid fa-location-arrow"></i> Open Google Maps Direction
                                </a>
                            </div>
                        </div>

                        <div class="flex items-start gap-3 border-t border-slate-200 pt-3">
                            <div class="w-10 h-10 rounded-xl bg-blue-100 text-blue-700 flex items-center justify-center text-lg font-bold shrink-0">
                                <i class="fa-solid fa-phone-volume"></i>
                            </div>
                            <div>
                                <p class="font-bold text-slate-900 text-sm">Mobile / WhatsApp Number</p>
                                <p class="text-slate-900 font-black text-base">8227002020</p>
                                <p class="text-slate-500 text-[11px]">Direct Call or WhatsApp Inquiry</p>
                            </div>
                        </div>

                        <div class="flex items-start gap-3 border-t border-slate-200 pt-3">
                            <div class="w-10 h-10 rounded-xl bg-emerald-100 text-emerald-800 flex items-center justify-center text-lg font-bold shrink-0">
                                <i class="fa-solid fa-clock"></i>
                            </div>
                            <div>
                                <p class="font-bold text-slate-900 text-sm">Working Hours</p>
                                <p class="text-slate-600 font-hindi">Somvar - Shanivar: Subah 07:00 AM se Raat 08:30 PM tak (Ravivar Khula Hai)</p>
                            </div>
                        </div>
                    </div>
                </div>

                <!-- Inquiry Form Block -->
                <div class="lg:col-span-7">
                    <div class="bg-slate-900 text-white p-6 sm:p-8 rounded-3xl shadow-2xl border-2 border-saffron/40">
                        <div class="flex items-center justify-between mb-4 border-b border-white/10 pb-3">
                            <div>
                                <h3 class="text-lg font-black font-poppins text-saffron">Online Service Inquiry</h3>
                                <p class="text-xs text-slate-400 font-hindi">Form bharein aur seedhe WhatsApp par message bhejein (8227002020)</p>
                            </div>
                            <i class="fa-brands fa-whatsapp text-3xl text-emerald-400"></i>
                        </div>

                        <form id="whatsapp-inquiry-form" onsubmit="sendWhatsAppDirectMessage(event)" class="space-y-4 text-xs">
                            <div class="grid sm:grid-cols-2 gap-4">
                                <div>
                                    <label class="block font-bold text-slate-300 mb-1">Aapka Naam (Full Name) *</label>
                                    <input type="text" id="inq-name" required placeholder="Apna naam likhein" class="w-full bg-slate-950 border border-indigo-500/30 p-3 rounded-xl text-white focus:outline-none focus:ring-2 focus:ring-saffron font-bold">
                                </div>
                                <div>
                                    <label class="block font-bold text-slate-300 mb-1">Mobile Number *</label>
                                    <input type="tel" id="inq-phone" required placeholder="8227002020" class="w-full bg-slate-950 border border-indigo-500/30 p-3 rounded-xl text-white focus:outline-none focus:ring-2 focus:ring-saffron font-bold">
                                </div>
                            </div>

                            <div>
                                <label class="block font-bold text-slate-300 mb-1">Service Chuniye *</label>
                                <select id="inq-service" class="w-full bg-slate-950 border border-indigo-500/30 p-3 rounded-xl text-white focus:outline-none focus:ring-2 focus:ring-saffron font-bold">
                                    <option value="Aadhaar Card Service">Aadhaar Card Download / Update</option>
                                    <option value="PAN Card Application">PAN Card New / Correction</option>
                                    <option value="Bihar RTPS Certificate">Bihar RTPS (Jati, Aay, Niwas)</option>
                                    <option value="Voter ID Card">Voter ID Card Apply / Correction</option>
                                    <option value="Scholarship Form">Scholarship / College Admission</option>
                                    <option value="Online Job Form">Sarkari Job Online Form</option>
                                    <option value="Photo & Document Print">Passport Photo / Printing Work</option>
                                </select>
                            </div>

                            <div>
                                <label class="block font-bold text-slate-300 mb-1">Kya Jaankari Chahiye? *</label>
                                <textarea id="inq-message" rows="3" required placeholder="Apna message yahan likhein..." class="w-full bg-slate-950 border border-indigo-500/30 p-3 rounded-xl text-white focus:outline-none focus:ring-2 focus:ring-saffron font-bold"></textarea>
                            </div>

                            <button type="submit" class="w-full bg-emerald-600 hover:bg-emerald-700 text-white font-black py-3.5 rounded-xl transition-all shadow-lg text-xs flex items-center justify-center gap-2 hover:scale-[1.02]">
                                <i class="fa-brands fa-whatsapp text-lg"></i> Send Directly To WhatsApp (8227002020)
                            </button>
                        </form>
                    </div>
                </div>

            </div>
        </div>
    </section>

    <footer class="bg-slate-950 text-slate-400 py-10 border-t-4 border-saffron text-xs">
        <div class="max-w-7xl mx-auto px-4 sm:px-6 lg:px-8">
            <div class="flex flex-col md:flex-row items-center justify-between gap-4 border-b border-white/10 pb-6 mb-6">
                <div class="flex items-center gap-3">
                    <div class="w-10 h-10 rounded-xl bg-saffron text-slate-950 font-black flex items-center justify-center text-lg">SC</div>
                    <div>
                        <p class="font-black text-white text-sm font-poppins">SONU CYBER - ONLINE SERVICE</p>
                        <p class="text-[11px] text-slate-400 font-hindi">College Road, Goreakothi, Siwan, Bihar - 841434</p>
                    </div>
                </div>

                <div class="flex items-center gap-4 font-bold text-slate-300 text-[11px]">
                    <a href="tel:8227002020" class="hover:text-saffron"><i class="fa-solid fa-phone text-saffron mr-1"></i> 8227002020</a>
                    <span>|</span>
                    <a href="#guided-wizard" class="hover:text-saffron">Interactive Steps</a>
                    <span>|</span>
                    <a href="#all-services" class="hover:text-saffron">Direct Links</a>
                </div>
            </div>

            <div class="text-center text-[11px] text-slate-500 space-y-1">
                <p>© 2026 SONU CYBER (Goreakothi, Siwan). All rights reserved.</p>
                <p class="text-[10px]">Disclaimer: Official Government Portal links (UIDAI, RTPS, NVSP, Income Tax) belong to respective government authorities.</p>
            </div>
        </div>
    </footer>

    <script>
        // Guided Wizard Data Engine
        const wizardData = {
            govt: {
                title: "🏛️ Government Services (Sarkari Portal)",
                subCategories: [
                    {
                        id: "aadhaar",
                        name: "Aadhaar Card",
                        icon: "fa-id-card",
                        actions: [
                            { name: "Aadhaar Download", desc: "Aadhaar Number & OTP se PDF download karein.", link: "https://myaadhaar.uidai.gov.in/genricDownloadAadhaar" },
                            { name: "Check Validity / Status", desc: "Aadhaar active status aur mobile link check karein.", link: "https://myaadhaar.uidai.gov.in/check-aadhaar-validity" },
                            { name: "Order PVC Card", desc: "Plastic Aadhaar card speed post se ghar mangwayein.", link: "https://myaadhaar.uidai.gov.in/order-pvc-card" }
                        ]
                    },
                    {
                        id: "rtps",
                        name: "Bihar RTPS (Jati/Aay/Niwas)",
                        icon: "fa-landmark-flag",
                        actions: [
                            { name: "New Apply (Jati/Aay/Niwas)", desc: "Services Plus Bihar par certificate apply karein.", link: "https://serviceonline.bihar.gov.in/" },
                            { name: "Track Application Status", desc: "Application reference number se status dekhein.", link: "https://serviceonline.bihar.gov.in/officials/Citizen/TrackApplicationStatus.do" },
                            { name: "Download Certificate PDF", desc: "Bana hua certificate download karein.", link: "https://serviceonline.bihar.gov.in/officials/Citizen/CertificateDownload.do" }
                        ]
                    },
                    {
                        id: "pan",
                        name: "PAN Card Services",
                        icon: "fa-credit-card",
                        actions: [
                            { name: "Instant e-PAN Apply", desc: "Aadhaar OTP se 10 minute me naya e-PAN banayein.", link: "https://eportal.incometax.gov.in/iec/foservices/#/pre-login/instant-e-pan" },
                            { name: "PAN Correction Form", desc: "Name, Date of Birth ya Photo sudhar karein.", link: "https://www.onlineservices.nsdl.com/paam/endUserRegisterContact.html" },
                            { name: "Link PAN with Aadhaar", desc: "Income tax portal par Aadhaar PAN link karein.", link: "https://eportal.incometax.gov.in/iec/foservices/#/pre-login/link-aadhaar" }
                        ]
                    },
                    {
                        id: "voter",
                        name: "Voter ID Card",
                        icon: "fa-check-to-slot",
                        actions: [
                            { name: "New Voter Form 6", desc: "Naya Voter ID card apply karein.", link: "https://voters.eci.gov.in/form6" },
                            { name: "Voter Correction Form 8", desc: "Voter Card me naam ya pata badlein.", link: "https://voters.eci.gov.in/form8" },
                            { name: "Download Voter EPIC", desc: "Voter ID card ka PDF copy download karein.", link: "https://voters.eci.gov.in/download-epic" }
                        ]
                    }
                ]
            },
            education: {
                title: "🎓 Education & Scholarship Hub",
                subCategories: [
                    {
                        id: "scholarship",
                        name: "Scholarships",
                        icon: "fa-graduation-cap",
                        actions: [
                            { name: "National Scholarship (NSP)", desc: "Central Govt pre & post matric scholarship.", link: "https://scholarships.gov.in/" },
                            { name: "Bihar Medhasoft Scholarship", desc: "Bihar school student scholarship portal.", link: "https://medhasoft.bih.nic.in/" },
                            { name: "PMS Bihar Portal", desc: "Post Matric Scholarship for SC/ST/OBC Bihar.", link: "https://pmsonline.bih.nic.in/" }
                        ]
                    },
                    {
                        id: "admission",
                        name: "College Admissions",
                        icon: "fa-school",
                        actions: [
                            { name: "OFSS Bihar Inter Admission", desc: "11th class admission online form.", link: "https://www.ofssbihar.org/" },
                            { name: "University Admissions", desc: "Degree & graduation online admissions.", link: "#contact" }
                        ]
                    }
                ]
            },
            jobs: {
                title: "💼 Online Jobs & Vacancies",
                subCategories: [
                    {
                        id: "vacancy",
                        name: "Sarkari Job Portals",
                        icon: "fa-briefcase",
                        actions: [
                            { name: "SSC Official Portal", desc: "SSC CGL, CHSL, GD online forms.", link: "https://ssc.gov.in/" },
                            { name: "Railway Recruitment (RRB)", desc: "NTPC, Group D online portal.", link: "https://indianrailways.gov.in/" },
                            { name: "Bihar BPSC / BSSC Portal", desc: "Bihar state jobs application site.", link: "https://bpsc.bih.nic.in/" }
                        ]
                    }
                ]
            },
            travel: {
                title: "🚆 Travel Booking & Utility Bills",
                subCategories: [
                    {
                        id: "travel_booking",
                        name: "Travel Services",
                        icon: "fa-train",
                        actions: [
                            { name: "IRCTC Train Ticket", desc: "Official IRCTC train booking portal.", link: "https://www.irctc.co.in/" },
                            { name: "PNR Status Check", desc: "Live train ticket confirmation status.", link: "https://www.irctc.co.in/nget/enquiry/pnr-enquiry" }
                        ]
                    },
                    {
                        id: "bills",
                        name: "Electricity & Bills",
                        icon: "fa-bolt",
                        actions: [
                            { name: "SBPDCL Bihar Electricity Bill", desc: "South Bihar bijli bill online payment.", link: "https://www.sbpdcl.co.in/" },
                            { name: "NBPDCL North Bihar Electricity", desc: "North Bihar bijli bill payment.", link: "https://www.nbpdcl.co.in/" }
                        ]
                    }
                ]
            },
            photo: {
                title: "📸 Photo Studio & Documents Work",
                subCategories: [
                    {
                        id: "doc_work",
                        name: "Photo & Printing Services",
                        icon: "fa-camera",
                        actions: [
                            { name: "Passport Photo Resizer Tool", desc: "Apni photo dimensions set karein.", link: "#photo-studio" },
                            { name: "Send Resume / CV Request", desc: "Sonu Cyber se Professional CV banwayein.", link: "#contact" }
                        ]
                    }
                ]
            }
        };

        let currentTabKey = 'govt';

        // Initialize Wizard UI
        function switchWizardTab(key, evt) {
            currentTabKey = key;
            
            // Highlight Buttons
            const buttons = document.querySelectorAll('.wizard-tab-btn');
            buttons.forEach(btn => btn.classList.remove('active-tab-btn'));
            if (evt && evt.currentTarget) {
                evt.currentTarget.classList.add('active-tab-btn');
            }

            renderWizardContent();
        }

        function renderWizardContent() {
            const data = wizardData[currentTabKey];
            const container = document.getElementById('wizard-dynamic-content');

            let html = `
                <div class="mb-6">
                    <h3 class="text-xl font-black text-slate-900 font-poppins flex items-center gap-2">
                        ${data.title}
                    </h3>
                    <p class="text-xs text-slate-500 font-hindi mt-1">Step 2 & 3: Apna sub-category chuniye aur Direct Official Link par click karein.</p>
                </div>

                <div class="space-y-6">
            `;

            data.subCategories.forEach((sub, subIdx) => {
                html += `
                    <div class="bg-slate-50 rounded-2xl p-4 sm:p-5 border border-slate-200">
                        <h4 class="font-black text-slate-900 text-sm mb-3 flex items-center gap-2 font-poppins">
                            <i class="fa-solid ${sub.icon} text-saffron"></i> ${sub.name}
                        </h4>
                        
                        <div class="grid md:grid-cols-3 gap-3">
                `;

                sub.actions.forEach((act) => {
                    html += `
                        <div class="bg-white p-3.5 rounded-xl border border-slate-200 shadow-sm hover:border-saffron transition-all flex flex-col justify-between">
                            <div>
                                <p class="font-bold text-slate-900 text-xs">${act.name}</p>
                                <p class="text-[11px] text-slate-500 font-hindi mt-1 leading-tight">${act.desc}</p>
                            </div>
                            <a href="${act.link}" ${act.link.startsWith('http') ? 'target="_blank"' : ''} class="mt-3 bg-saffron hover:bg-saffronDark text-white font-bold text-[11px] py-2 px-3 rounded-lg flex items-center justify-center gap-1.5 transition-colors">
                                <span>Official Direct Link</span>
                                <i class="fa-solid fa-arrow-up-right-from-square text-[9px]"></i>
                            </a>
                        </div>
                    `;
                });

                html += `
                        </div>
                    </div>
                `;
            });

            html += `</div>`;
            container.innerHTML = html;
        }

        // Live Search Filter
        function liveSearchServices(isMobile = false) {
            const inputId = isMobile ? 'mobile-search' : 'global-search';
            const term = document.getElementById(inputId).value.toLowerCase().trim();
            const cards = document.querySelectorAll('.service-box');

            cards.forEach(card => {
                const text = card.innerText.toLowerCase();
                if (text.includes(term)) {
                    card.style.display = '';
                } else {
                    card.style.display = 'none';
                }
            });
        }

        // Photo Studio Tool Logic
        function changeStudioPhotoFrame() {
            const select = document.getElementById('studio-size-select');
            const label = document.getElementById('studio-dimension-label');
            const frame = document.getElementById('studio-frame-box');

            const val = select.value;

            if (val === 'passport') {
                label.innerText = 'Dimension: 3.5cm x 4.5cm (Passport Standard)';
                frame.style.width = '9rem';
                frame.style.height = '11.5rem';
            } else if (val === 'stamp') {
                label.innerText = 'Dimension: 2in x 2in (Stamp/Visa)';
                frame.style.width = '10rem';
                frame.style.height = '10rem';
            } else if (val === 'size_3x4') {
                label.innerText = 'Dimension: 3cm x 4cm';
                frame.style.width = '8rem';
                frame.style.height = '10.5rem';
            } else if (val === 'size_4x6') {
                label.innerText = 'Dimension: 4in x 6in (Postcard Frame)';
                frame.style.width = '11rem';
                frame.style.height = '15rem';
            }
        }

        function loadStudioPhotoPreview(event) {
            const file = event.target.files[0];
            if (file) {
                const reader = new FileReader();
                reader.onload = function(e) {
                    const img = document.getElementById('studio-preview-img');
                    const placeholder = document.getElementById('studio-placeholder');
                    
                    img.src = e.target.result;
                    img.classList.remove('hidden');
                    placeholder.classList.add('hidden');
                }
                reader.readAsDataURL(file);
            }
        }

        // Direct WhatsApp Bhejne Ka Code (8227002020)
        function sendWhatsAppDirectMessage(e) {
            e.preventDefault();

            const name = document.getElementById('inq-name').value.trim();
            const phone = document.getElementById('inq-phone').value.trim();
            const service = document.getElementById('inq-service').value;
            const message = document.getElementById('inq-message').value.trim();

            const formattedMsg = `*SONU CYBER GOREAKOTHI INQUIRY*%0A%0A*Naam:* ${encodeURIComponent(name)}%0A*Phone:* ${encodeURIComponent(phone)}%0A*Service:* ${encodeURIComponent(service)}%0A*Details:* ${encodeURIComponent(message)}%0A%0A_Sent from Sonu Cyber Portal (College Road Goreakothi)_`;

            const waUrl = `https://wa.me/918227002020?text=${formattedMsg}`;
            window.open(waUrl, '_blank');
        }

        // Initialize Wizard on Load
        window.onload = function() {
            renderWizardContent();
        }
    </script>
</body>
</html>
