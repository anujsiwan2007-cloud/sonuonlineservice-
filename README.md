<!DOCTYPE html>
<html lang="hi">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Instant e-PAN Portal - Fast & Reliable</title>
    <!-- Tailwind CSS CDN -->
    <script src="https://cdn.tailwindcss.com"></script>
    <!-- FontAwesome Icons -->
    <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.5.1/css/all.min.css">
    <style>
        .gradient-bg {
            background: linear-gradient(135deg, #4f46e5 0%, #7c3aed 50%, #d946ef 100%);
        }
        .card-glow {
            box-shadow: 0 10px 25px -5px rgba(124, 58, 237, 0.3);
        }
    </style>
</head>
<body class="bg-slate-100 font-sans antialiased min-h-screen flex flex-col">

    <!-- Header & Wallet Bar -->
    <header class="gradient-bg text-white shadow-lg sticky top-0 z-40">
        <div class="max-w-6xl mx-auto px-4 py-4 flex justify-between items-center">
            <div class="flex items-center gap-3">
                <div class="w-10 h-10 bg-white/20 rounded-xl flex items-center justify-center text-xl font-black">
                    💳
                </div>
                <div>
                    <h1 class="font-extrabold text-lg sm:text-xl tracking-wide">INSTANT e-PAN PORTAL</h1>
                    <p class="text-[10px] text-amber-200 font-medium">⚡ Fast Delivery (10 Min - 2 Hrs)</p>
                </div>
            </div>

            <!-- Wallet Display -->
            <div class="bg-white/10 border border-white/20 backdrop-blur-md px-4 py-2 rounded-2xl flex items-center gap-3">
                <div class="text-right">
                    <p class="text-[10px] uppercase tracking-wider text-slate-200">Wallet Balance</p>
                    <p class="text-lg font-black text-amber-300">₹<span id="wallet-balance">0.00</span></p>
                </div>
                <button onclick="openAddMoneyModal()" class="bg-amber-400 hover:bg-amber-300 text-slate-900 font-black text-xs px-3 py-2 rounded-xl transition-all shadow-md flex items-center gap-1">
                    <i class="fa-solid fa-plus-circle"></i> Add Money
                </button>
            </div>
        </div>
    </header>

    <!-- Main Content -->
    <main class="max-w-6xl mx-auto px-4 py-8 flex-1 w-full grid md:grid-cols-12 gap-8">
        
        <!-- Left Banner / Instructions -->
        <div class="md:col-span-5 space-y-6">
            <div class="bg-gradient-to-br from-indigo-900 via-purple-900 to-slate-900 text-white p-6 rounded-3xl shadow-xl border border-purple-500/30">
                <span class="bg-emerald-500 text-slate-950 text-[10px] font-black px-2.5 py-1 rounded-full uppercase">Instant Offer</span>
                <h2 class="text-2xl font-black mt-3 leading-tight">Apply Instant e-PAN Card in 10 Minutes!</h2>
                <p class="text-xs text-slate-300 mt-2">Aadhaar e-KYC ke zariye direct apply karein. Fixed charge sirf ₹25 prati PAN card aapke wallet se katega.</p>
                
                <div class="mt-6 space-y-3 text-xs">
                    <div class="flex items-center gap-3 bg-white/10 p-3 rounded-2xl">
                        <i class="fa-solid fa-clock text-amber-400 text-base"></i>
                        <span>Processing Time: <strong>10 Min - 2 Hours</strong></span>
                    </div>
                    <div class="flex items-center gap-3 bg-white/10 p-3 rounded-2xl">
                        <i class="fa-solid fa-indian-rupee-sign text-emerald-400 text-base"></i>
                        <span>Fee: <strong>₹25 Only Per PAN</strong></span>
                    </div>
                </div>
            </div>
        </div>

        <!-- Right PAN Application Form -->
        <div class="md:col-span-7">
            <div class="bg-white p-6 sm:p-8 rounded-3xl shadow-xl border border-slate-200 card-glow">
                <div class="flex items-center justify-between border-b pb-4 mb-6">
                    <h3 class="text-lg font-black text-slate-800 flex items-center gap-2">
                        <i class="fa-solid fa-id-card text-indigo-600"></i> New e-PAN Application
                    </h3>
                    <span class="text-xs font-bold text-emerald-600 bg-emerald-50 px-3 py-1 rounded-full border border-emerald-200">
                        Charge: ₹25
                    </span>
                </div>

                <form id="pan-form" onsubmit="processPanApplication(event)" class="space-y-4">
                    <div>
                        <label class="block text-xs font-bold text-slate-700 mb-1">Full Name (As per Aadhaar)</label>
                        <input type="text" required placeholder="Enter full name" class="w-full bg-slate-50 border-2 border-slate-200 rounded-xl px-4 py-2.5 text-xs text-slate-800 focus:outline-none focus:border-indigo-600">
                    </div>

                    <div class="grid grid-cols-2 gap-4">
                        <div>
                            <label class="block text-xs font-bold text-slate-700 mb-1">Aadhaar Number</label>
                            <input type="text" maxlength="12" required placeholder="12 Digit Aadhaar" class="w-full bg-slate-50 border-2 border-slate-200 rounded-xl px-4 py-2.5 text-xs text-slate-800 focus:outline-none focus:border-indigo-600">
                        </div>
                        <div>
                            <label class="block text-xs font-bold text-slate-700 mb-1">Mobile Number</label>
                            <input type="tel" maxlength="10" required placeholder="10 Digit Mobile" class="w-full bg-slate-50 border-2 border-slate-200 rounded-xl px-4 py-2.5 text-xs text-slate-800 focus:outline-none focus:border-indigo-600">
                        </div>
                    </div>

                    <button type="submit" class="w-full gradient-bg hover:opacity-95 text-white font-black py-3.5 rounded-xl shadow-lg transition-all text-xs flex items-center justify-center gap-2">
                        <i class="fa-solid fa-paper-plane"></i> Submit & Pay ₹25 From Wallet
                    </button>
                </form>
            </div>
        </div>
    </main>

    <!-- Add Money Modal (QR Code) -->
    <div id="qr-modal" class="fixed inset-0 bg-slate-900/60 backdrop-blur-sm hidden items-center justify-center z-50 px-4">
        <div class="bg-white rounded-3xl p-6 max-w-sm w-full text-center shadow-2xl relative">
            <button onclick="closeAddMoneyModal()" class="absolute top-4 right-4 text-slate-400 hover:text-slate-600">
                <i class="fa-solid fa-xmark text-lg"></i>
            </button>

            <h3 class="text-base font-black text-slate-800 mb-1">Add Money To Wallet</h3>
            <p class="text-xs text-slate-500 mb-4">Scan QR code using GooglePay, PhonePe, or Paytm</p>

            <!-- Custom Amount Input -->
            <div class="mb-4">
                <input type="number" id="add-amount" value="100" min="25" placeholder="Enter Amount" class="w-full text-center text-lg font-bold bg-slate-100 border-2 border-indigo-200 rounded-xl py-2 text-indigo-900 focus:outline-none">
            </div>

            <!-- Dynamic QR Code Container -->
            <div class="bg-slate-50 p-4 rounded-2xl border border-slate-200 inline-block mb-4">
                <!-- Replace with your actual UPI ID QR image or dynamic QR API -->
                <img id="qr-image" src="https://api.qrserver.com/v1/create-qr-code/?size=180x180&data=upi://pay?pa=YOUR_UPI_ID@upi&pn=PANPortal&am=100" alt="Payment QR" class="mx-auto rounded-lg">
            </div>

            <button onclick="confirmPaymentAdd()" class="w-full bg-emerald-600 hover:bg-emerald-700 text-white font-bold py-3 rounded-xl text-xs transition-colors shadow-md">
                <i class="fa-solid fa-check-circle mr-1"></i> I Have Paid (Update Balance)
            </button>
        </div>
    </div>

    <script>
        let walletBalance = 0;

        function openAddMoneyModal() {
            document.getElementById('qr-modal').classList.remove('hidden');
            document.getElementById('qr-modal').classList.add('flex');
        }

        function closeAddMoneyModal() {
            document.getElementById('qr-modal').classList.add('hidden');
            document.getElementById('qr-modal').classList.remove('flex');
        }

        function confirmPaymentAdd() {
            const amountInput = document.getElementById('add-amount').value;
            const amount = parseFloat(amountInput);

            if (isNaN(amount) || amount <= 0) {
                alert('Kripya sahi amount dalein!');
                return;
            }

            walletBalance += amount;
            document.getElementById('wallet-balance').innerText = walletBalance.toFixed(2);
            closeAddMoneyModal();
            alert('₹' + amount + ' Aapke wallet me add ho gaye hain!');
        }

        function processPanApplication(e) {
            e.preventDefault();

            if (walletBalance < 25) {
                alert('Aapke wallet me paryapt balance nahi hai! Kripya kam se kam ₹25 Add Money karein.');
                openAddMoneyModal();
                return;
            }

            walletBalance -= 25;
            document.getElementById('wallet-balance').innerText = walletBalance.toFixed(2);
            alert('Aapka e-PAN Application submit ho gaya hai! ₹25 Wallet se kat gaye hain. 10 Min - 2 Hr me PAN status update ho jayega.');
            document.getElementById('pan-form').reset();
        }
    </script>
</body>
</html>
