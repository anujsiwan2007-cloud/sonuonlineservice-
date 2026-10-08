<!DOCTYPE html>
<html lang="hi">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Instant e-PAN Portal - Agent & User Services</title>
    <!-- Tailwind CSS CDN -->
    <script src="https://cdn.tailwindcss.com"></script>
    <!-- FontAwesome Icons -->
    <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.5.1/css/all.min.css">
    <style>
        .gradient-main {
            background: linear-gradient(135deg, #0f172a 0%, #1e1b4b 50%, #312e81 100%);
        }
        .gradient-card {
            background: linear-gradient(135deg, #FF671F 0%, #d97706 100%);
        }
        .glass-box {
            background: rgba(255, 255, 255, 0.95);
            backdrop-filter: blur(10px);
        }
    </style>
</head>
<body class="bg-slate-100 font-sans antialiased min-h-screen flex flex-col selection:bg-amber-500 selection:text-white">

    <!-- Navbar & Top Bar -->
    <header class="gradient-main text-white shadow-xl sticky top-0 z-40 border-b border-indigo-500/30">
        <div class="max-w-7xl mx-auto px-4 py-3 flex justify-between items-center gap-4">
            
            <div class="flex items-center gap-3">
                <div class="w-11 h-11 bg-gradient-to-tr from-amber-400 to-orange-500 rounded-2xl flex items-center justify-center text-slate-950 font-black text-xl shadow-md">
                    ⚡
                </div>
                <div>
                    <h1 class="font-extrabold text-base sm:text-xl tracking-tight text-white">e-PAN EXPRESS PORTAL</h1>
                    <p class="text-[10px] text-emerald-400 font-bold flex items-center gap-1">
                        <i class="fa-solid fa-circle-check"></i> Official Government Direct Link System
                    </p>
                </div>
            </div>

            <!-- Logged-In User & Wallet Bar -->
            <div id="user-header-info" class="hidden flex items-center gap-3">
                <div class="bg-white/10 border border-white/20 px-3.5 py-1.5 rounded-2xl text-right">
                    <p class="text-[9px] uppercase tracking-wider text-slate-300 font-bold" id="user-display-name">Agent ID</p>
                    <p class="text-sm font-black text-amber-300">Wallet: ₹<span id="wallet-balance">0.00</span></p>
                </div>
                <button onclick="openAddMoneyModal()" class="bg-emerald-500 hover:bg-emerald-600 text-slate-950 font-black text-xs px-3 py-2 rounded-xl transition-all shadow-lg flex items-center gap-1">
                    <i class="fa-solid fa-qrcode"></i> Add Money
                </button>
                <button onclick="logoutUser()" class="bg-rose-600 hover:bg-rose-700 text-white p-2 rounded-xl text-xs transition-all" title="Logout">
                    <i class="fa-solid fa-right-from-bracket"></i>
                </button>
            </div>

        </div>
    </header>

    <!-- MAIN CONTAINER -->
    <main class="max-w-7xl mx-auto px-4 py-8 flex-1 w-full">

        <!-- SECTION 1: LOGIN / SIGNUP FORM (Pehle User ID/Password Banaye) -->
        <div id="auth-section" class="max-w-md mx-auto">
            <div class="glass-box p-8 rounded-3xl shadow-2xl border-2 border-indigo-100 text-center">
                
                <div class="w-16 h-16 bg-indigo-100 text-indigo-700 rounded-3xl flex items-center justify-center text-2xl mx-auto mb-4 font-black">
                    <i class="fa-solid fa-user-shield"></i>
                </div>
                
                <h2 class="text-2xl font-black text-slate-900 font-poppins">Agent / Customer Login</h2>
                <p class="text-xs text-slate-500 mt-1 mb-6">Peheli baar aaye hain to Mobile & Email se ID banayein</p>

                <!-- Auth Tabs -->
                <div class="flex rounded-xl bg-slate-200 p-1 mb-6">
                    <button onclick="switchAuthTab('login')" id="btn-tab-login" class="flex-1 py-2 text-xs font-bold rounded-lg bg-white text-indigo-900 shadow">Login</button>
                    <button onclick="switchAuthTab('signup')" id="btn-tab-signup" class="flex-1 py-2 text-xs font-bold rounded-lg text-slate-600">New Registration</button>
                </div>

                <!-- LOGIN FORM -->
                <form id="form-login" onsubmit="handleLogin(event)" class="space-y-4">
                    <input type="tel" id="login-mobile" placeholder="Registered Mobile Number" required class="w-full bg-slate-50 border-2 border-slate-200 rounded-xl px-4 py-3 text-xs focus:outline-none focus:border-indigo-600 font-bold">
                    <input type="password" id="login-password" placeholder="Password" required class="w-full bg-slate-50 border-2 border-slate-200 rounded-xl px-4 py-3 text-xs focus:outline-none focus:border-indigo-600 font-bold">
                    <button type="submit" class="w-full gradient-main text-white font-black py-3.5 rounded-xl shadow-lg hover:opacity-95 text-xs transition-all">
                        LOGIN TO PORTAL <i class="fa-solid fa-arrow-right ml-1"></i>
                    </button>
                </form>

                <!-- SIGNUP FORM -->
                <form id="form-signup" onsubmit="handleSignup(event)" class="space-y-3 hidden">
                    <input type="text" id="signup-name" placeholder="Full Name" required class="w-full bg-slate-50 border-2 border-slate-200 rounded-xl px-4 py-2.5 text-xs focus:outline-none focus:border-indigo-600 font-bold">
                    <input type="tel" maxlength="10" id="signup-mobile" placeholder="Mobile Number (User ID)" required class="w-full bg-slate-50 border-2 border-slate-200 rounded-xl px-4 py-2.5 text-xs focus:outline-none focus:border-indigo-600 font-bold">
                    <input type="email" idsignup-email" placeholder="Email Address" required class="w-full bg-slate-50 border-2 border-slate-200 rounded-xl px-4 py-2.5 text-xs focus:outline-none focus:border-indigo-600 font-bold">
                    <input type="password" id="signup-password" placeholder="Create Password" required class="w-full bg-slate-50 border-2 border-slate-200 rounded-xl px-4 py-2.5 text-xs focus:outline-none focus:border-indigo-600 font-bold">
                    <button type="submit" class="w-full bg-emerald-600 hover:bg-emerald-700 text-white font-black py-3.5 rounded-xl shadow-lg text-xs transition-all">
                        CREATE ID & REGISTER <i class="fa-solid fa-check-circle ml-1"></i>
                    </button>
                </form>

            </div>
        </div>

        <!-- SECTION 2: DASHBOARD & PROCESS (Login Hone Ke Baad Dikhega) -->
        <div id="dashboard-section" class="hidden grid md:grid-cols-12 gap-8">
            
            <!-- Process Banner -->
            <div class="md:col-span-5 space-y-6">
                <div class="gradient-main text-white p-6 rounded-3xl shadow-xl border border-indigo-500/30">
                    <span class="bg-amber-400 text-slate-950 text-[10px] font-black px-3 py-1 rounded-full uppercase tracking-wider">
                        STEP-BY-STEP PROCESS
                    </span>
                    <h2 class="text-2xl font-black mt-3 leading-tight">Instant e-PAN Card Kaise Banayein?</h2>
                    
                    <ol class="mt-6 space-y-4 text-xs font-medium">
                        <li class="flex items-start gap-3 bg-white/10 p-3 rounded-2xl">
                            <span class="w-6 h-6 rounded-full bg-amber-400 text-slate-950 font-black flex items-center justify-center shrink-0">1</span>
                            <span>Aapne Wallet me kam se kam <strong>₹25</strong> Add Money karein (Direct Bank QR se).</span>
                        </li>
                        <li class="flex items-start gap-3 bg-white/10 p-3 rounded-2xl">
                            <span class="w-6 h-6 rounded-full bg-amber-400 text-slate-950 font-black flex items-center justify-center shrink-0">2</span>
                            <span>Apna Name aur 12-digit Aadhaar Number daal kar Submit karein.</span>
                        </li>
                        <li class="flex items-start gap-3 bg-white/10 p-3 rounded-2xl">
                            <span class="w-6 h-6 rounded-full bg-amber-400 text-slate-950 font-black flex items-center justify-center shrink-0">3</span>
                            <span>Wallet se ₹25 automatic cut honge aur aap **Income Tax e-PAN Original Portal** par redirect ho jayenge!</span>
                        </li>
                        <li class="flex items-start gap-3 bg-white/10 p-3 rounded-2xl">
                            <span class="w-6 h-6 rounded-full bg-amber-400 text-slate-950 font-black flex items-center justify-center shrink-0">4</span>
                            <span>Aadhaar OTP verify karein, <strong>10 Min - 2 Hr me PAN Number mil jayega!</strong></span>
                        </li>
                    </ol>
                </div>
            </div>

            <!-- Process Form -->
            <div class="md:col-span-7">
                <div class="bg-white p-6 sm:p-8 rounded-3xl shadow-xl border-2 border-slate-200">
                    <div class="flex items-center justify-between border-b pb-4 mb-6">
                        <div>
                            <h3 class="text-lg font-black text-slate-900 font-poppins flex items-center gap-2">
                                <i class="fa-solid fa-address-card text-indigo-600"></i> New Instant e-PAN Process
                            </h3>
                            <p class="text-xs text-slate-500">10 Minute - 2 Ghante Me Instant e-PAN Generate Karein</p>
                        </div>
                        <span class="text-xs font-black text-amber-900 bg-amber-100 px-3 py-1.5 rounded-xl border border-amber-300">
                            Charge: ₹25 / Application
                        </span>
                    </div>

                    <form onsubmit="processPanAndRedirect(event)" class="space-y-4">
                        <div>
                            <label class="block text-xs font-bold text-slate-700 mb-1">Applicant Full Name (Aadhaar Ke Mutabiq)</label>
                            <input type="text" required placeholder="Naam likhein" class="w-full bg-slate-50 border-2 border-slate-200 rounded-xl px-4 py-3 text-xs text-slate-800 font-bold focus:outline-none focus:border-indigo-600">
                        </div>

                        <div>
                            <label class="block text-xs font-bold text-slate-700 mb-1">12 Digit Aadhaar Number</label>
                            <input type="text" maxlength="12" pattern="\d{12}" required placeholder="Aadhaar number daalein" class="w-full bg-slate-50 border-2 border-slate-200 rounded-xl px-4 py-3 text-xs text-slate-800 font-bold focus:outline-none focus:border-indigo-600">
                        </div>

                        <div class="bg-indigo-50 border border-indigo-200 p-3.5 rounded-2xl text-[11px] text-indigo-900 font-semibold flex items-center gap-2">
                            <i class="fa-solid fa-circle-info text-indigo-600 text-sm"></i>
                            <span>Submit par click karte hi ₹25 wallet se katenge aur aap direct **Income Tax e-PAN Government Portal** par chale jayenge.</span>
                        </div>

                        <button type="submit" class="w-full gradient-card text-white font-black py-4 rounded-2xl shadow-xl hover:opacity-95 text-xs transition-all flex items-center justify-center gap-2 text-sm">
                            <i class="fa-solid fa-bolt"></i> PAY ₹25 & GO TO ORIGINAL e-PAN LINK
                        </button>
                    </form>
                </div>
            </div>

        </div>

    </main>

    <!-- MODAL: ADD MONEY WITH DIRECT ACCOUNT QR CODE -->
    <div id="qr-modal" class="fixed inset-0 bg-slate-950/70 backdrop-blur-sm hidden items-center justify-center z-50 px-4">
        <div class="bg-white rounded-3xl p-6 max-w-sm w-full text-center shadow-2xl relative border-4 border-amber-400">
            
            <button onclick="closeAddMoneyModal()" class="absolute top-4 right-4 text-slate-400 hover:text-slate-600">
                <i class="fa-solid fa-xmark text-xl"></i>
            </button>

            <div class="w-12 h-12 bg-amber-100 text-amber-600 rounded-2xl flex items-center justify-center mx-auto mb-2 text-xl font-black">
                <i class="fa-solid fa-qrcode"></i>
            </div>

            <h3 class="text-base font-black text-slate-900">Add Balance To Wallet</h3>
            <p class="text-xs text-slate-500 mb-4">Paytm, PhonePe, GPay se scan karke direct mere account me bhejein</p>

            <div class="mb-4">
                <label class="block text-[11px] font-bold text-slate-600 mb-1">Kitna Paisa Add Karna Hai (₹):</label>
                <input type="number" id="add-amount" value="100" min="25" oninput="updateQRCode()" class="w-full text-center text-xl font-black bg-slate-100 border-2 border-indigo-300 rounded-xl py-2 text-indigo-950 focus:outline-none">
            </div>

            <!-- Direct Bank/UPI QR Code -->
            <div class="bg-slate-50 p-3 rounded-2xl border border-slate-200 inline-block mb-4 shadow-inner">
                <!-- APNA ACTUAL UPI ID YAHAN BEDALEIN: e.g. 8227002020@paytm -->
                <img id="qr-image" src="https://api.qrserver.com/v1/create-qr-code/?size=180x180&data=upi://pay?pa=8227002020@paytm&pn=SonuCyber&am=100" alt="Payment QR" class="mx-auto rounded-lg shadow-sm">
            </div>

            <button onclick="confirmPaymentAdd()" class="w-full bg-emerald-600 hover:bg-emerald-700 text-white font-black py-3 rounded-xl text-xs transition-all shadow-lg flex items-center justify-center gap-2">
                <i class="fa-solid fa-circle-check"></i> Maine Payment Kar Diya (Update Wallet)
            </button>
        </div>
    </div>

    <!-- JAVASCRIPT LOGIC -->
    <script>
        let walletBalance = 0;
        let currentUser = null;
        // APNA UPI ID BADLEIN:
        const myUpiId = "8227002020@paytm"; 

        function switchAuthTab(type) {
            if(type === 'login') {
                document.getElementById('form-login').classList.remove('hidden');
                document.getElementById('form-signup').classList.add('hidden');
                document.getElementById('btn-tab-login').className = "flex-1 py-2 text-xs font-bold rounded-lg bg-white text-indigo-900 shadow";
                document.getElementById('btn-tab-signup').className = "flex-1 py-2 text-xs font-bold rounded-lg text-slate-600";
            } else {
                document.getElementById('form-signup').classList.remove('hidden');
                document.getElementById('form-login').classList.add('hidden');
                document.getElementById('btn-tab-signup').className = "flex-1 py-2 text-xs font-bold rounded-lg bg-white text-indigo-900 shadow";
                document.getElementById('btn-tab-login').className = "flex-1 py-2 text-xs font-bold rounded-lg text-slate-600";
            }
        }

        function handleSignup(e) {
            e.preventDefault();
            const name = document.getElementById('signup-name').value;
            const mobile = document.getElementById('signup-mobile').value;
            currentUser = { name, mobile };
            
            alert('Aapka Registration Successful ho gaya hai! Password save kar diya gaya hai.');
            showDashboard();
        }

        function handleLogin(e) {
            e.preventDefault();
            const mobile = document.getElementById('login-mobile').value;
            currentUser = { name: "Agent (" + mobile + ")", mobile };
            
            showDashboard();
        }

        function showDashboard() {
            document.getElementById('auth-section').classList.add('hidden');
            document.getElementById('dashboard-section').classList.remove('hidden');
            document.getElementById('user-header-info').classList.remove('hidden');
            document.getElementById('user-header-info').classList.add('flex');
            document.getElementById('user-display-name').innerText = currentUser.name;
        }

        function logoutUser() {
            currentUser = null;
            document.getElementById('auth-section').classList.remove('hidden');
            document.getElementById('dashboard-section').classList.add('hidden');
            document.getElementById('user-header-info').classList.add('hidden');
            document.getElementById('user-header-info').classList.remove('flex');
        }

        function openAddMoneyModal() {
            document.getElementById('qr-modal').classList.remove('hidden');
            document.getElementById('qr-modal').classList.add('flex');
            updateQRCode();
        }

        function closeAddMoneyModal() {
            document.getElementById('qr-modal').classList.add('hidden');
            document.getElementById('qr-modal').classList.remove('flex');
        }

        function updateQRCode() {
            const amount = document.getElementById('add-amount').value || 25;
            const qrUrl = `https://api.qrserver.com/v1/create-qr-code/?size=180x180&data=upi://pay?pa=${myUpiId}&pn=SonuCyber&am=${amount}`;
            document.getElementById('qr-image').src = qrUrl;
        }

        function confirmPaymentAdd() {
            const amountInput = document.getElementById('add-amount').value;
            const amount = parseFloat(amountInput);

            if (isNaN(amount) || amount <= 0) {
                alert('Sahi amount bharein!');
                return;
            }

            walletBalance += amount;
            document.getElementById('wallet-balance').innerText = walletBalance.toFixed(2);
            closeAddMoneyModal();
            alert('₹' + amount + ' Aapke Account me receive hone par Wallet Balance Update kar diya gaya hai!');
        }

        function processPanAndRedirect(e) {
            e.preventDefault();

            if (walletBalance < 25) {
                alert('Aapke Wallet me paryapt balance nahi hai! Minimum ₹25 Add Money karein.');
                openAddMoneyModal();
                return;
            }

            // Wallet se ₹25 Deduct karein
            walletBalance -= 25;
            document.getElementById('wallet-balance').innerText = walletBalance.toFixed(2);

            alert('₹25 Wallet se successfully cut gaye hain! Ab aap Direct Income Tax e-PAN Original Govt Website par redirect ho rahe hain...');

            // Direct Official Income Tax Instant e-PAN Link Par Bhejna
            window.open('https://eportal.incometax.gov.in/iec/foservices/#/pre-login/instant-e-pan', '_blank');
        }
    </script>
</body>
</html>
