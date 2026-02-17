<!DOCTYPE html>
<html lang="id">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>GPdI Anugerah | Website Resmi</title>
    <script src="https://cdn.tailwindcss.com"></script>
    <link href="https://fonts.googleapis.com/css2?family=Plus+Jakarta+Sans:wght@400;600;800&display=swap" rel="stylesheet">
    <link href="https://unpkg.com/aos@2.3.1/dist/aos.css" rel="stylesheet">
    <script>tailwind.config = { darkMode: 'class' }</script>
    <style>
        body { font-family: 'Plus Jakarta Sans', sans-serif; scroll-behavior: smooth; }
        .hero-section { background: linear-gradient(rgba(15, 23, 42, 0.75), rgba(15, 23, 42, 0.75)), url('https://images.unsplash.com/photo-1438232992991-995b7058bbb3?auto=format&fit=crop&w=1500&q=80'); background-size: cover; background-position: center; }
        .glass { background: rgba(255, 255, 255, 0.1); backdrop-filter: blur(10px); border: 1px solid rgba(255, 255, 255, 0.2); }
        * { transition: background-color 0.3s ease, color 0.3s ease; }
    </style>
</head>
<body class="bg-slate-50 dark:bg-slate-900 text-slate-900 dark:text-slate-100 transition-colors duration-300">

    <nav class="bg-white/90 dark:bg-slate-900/90 backdrop-blur-md sticky top-0 z-50 border-b dark:border-slate-800">
        <div class="container mx-auto px-6 py-4 flex justify-between items-center">
            <a href="#" class="text-2xl font-black text-blue-800 dark:text-blue-400 uppercase">GPdI<span class="text-orange-500"> Anugerah</span></a>
            <div class="hidden md:flex space-x-8 font-bold text-sm uppercase tracking-widest">
                <a href="#home">Beranda</a>
                <a href="#warta">Warta</a>
                <a href="#jadwal">Jadwal</a>
                <a href="#galeri">Galeri</a>
                <a href="#layanan">Layanan</a>
            </div>
            <button onclick="toggleDarkMode()" class="p-2 bg-slate-100 dark:bg-slate-800 rounded-full">🌓</button>
        </div>
    </nav>

    <header id="home" class="hero-section h-[80vh] flex items-center justify-center text-center text-white px-6">
        <div data-aos="fade-up">
            <h1 class="text-5xl md:text-7xl font-extrabold mb-6 leading-tight">Bertumbuh Dalam <br><span class="text-orange-400">Kasih & Iman</span></h1>
            <div class="glass p-6 rounded-3xl inline-block mb-4">
                <p class="text-xs uppercase tracking-widest mb-3 font-bold text-blue-200" id="timerLabel">Ibadah Berikutnya Dalam:</p>
                <div id="countdown" class="flex gap-6 text-3xl md:text-4xl font-black"></div>
            </div>
        </div>
    </header>

    <main class="container mx-auto px-6 py-20">
        <section id="warta" class="mb-32 scroll-mt-nav">
            <h2 class="text-4xl font-black mb-12">Warta <span class="text-blue-600">Jemaat</span></h2>
            <div class="grid md:grid-cols-3 gap-8">
                <div class="md:col-span-2 bg-white dark:bg-slate-800 p-8 md:p-12 rounded-[2.5rem] shadow-xl relative overflow-hidden">
                    <div class="absolute top-0 right-0 bg-orange-500 text-white px-8 py-3 rounded-bl-3xl font-black text-xs uppercase">Utama</div>
                    <h3 id="displayWartaTitle" class="text-3xl font-extrabold mb-6 dark:text-white">Memuat Warta...</h3>
                    <ul id="displayWartaPoints" class="space-y-4 text-slate-600 dark:text-slate-300"></ul>
                </div>
                <div id="displayPetugasCard" class="bg-slate-900 text-white p-8 rounded-[2.5rem] shadow-xl">
                    <h4 class="text-xl font-bold mb-6 border-b border-slate-700 pb-2 text-orange-400 uppercase tracking-tighter">Petugas Utama</h4>
                    <div id="displayPetugasContent" class="space-y-4"></div>
                </div>
            </div>
        </section>

        <section id="jadwal" class="mb-32 scroll-mt-nav" data-aos="fade-up">
            <h2 class="text-4xl font-black mb-12 text-center">Jadwal <span class="text-blue-600">Pelayanan Minggu Ini</span></h2>
            <div id="displayJadwalContainer" class="grid lg:grid-cols-3 gap-8"></div>
        </section>

        <section id="galeri" class="mb-32 scroll-mt-nav">
            <h2 class="text-4xl font-black mb-12 text-center">Galeri <span class="text-orange-500">Kegiatan</span></h2>
            <div id="displayGaleri" class="grid grid-cols-2 md:grid-cols-4 gap-4"></div>
        </section>

        <section id="layanan" class="bg-blue-600 p-8 md:p-12 rounded-[3rem] text-white shadow-2xl">
            <div class="grid lg:grid-cols-2 gap-12">
                <div>
                    <h2 class="text-5xl font-black mb-4 uppercase tracking-tighter">Layanan Jemaat</h2>
                    <p class="text-blue-100 mb-8">Pilih jenis layanan yang Anda butuhkan. Kami siap melayani keperluan administrasi dan rohani Anda.</p>
                    
                    <div class="space-y-4">
                        <div class="p-6 bg-white/10 rounded-2xl border border-white/20">
                            <h4 class="font-bold mb-2 uppercase text-orange-400">Pendaftaran Jemaat Baru</h4>
                            <p class="text-sm opacity-80">Menjadi bagian dari keluarga besar kami dengan mendaftarkan data keluarga Anda secara digital.</p>
                        </div>
                    </div>
                </div>

                <div class="bg-white dark:bg-slate-900 p-8 rounded-[2rem] text-slate-900 shadow-inner">
                    <div class="flex gap-4 mb-6 border-b dark:border-slate-800 pb-4 overflow-x-auto">
                        <button onclick="switchForm('umum')" id="tabUmum" class="text-[10px] font-black text-blue-600 border-b-2 border-blue-600 pb-2 whitespace-nowrap uppercase">Umum/Doa</button>
                        <button onclick="switchForm('baptis')" id="tabBaptis" class="text-[10px] font-black text-slate-400 pb-2 whitespace-nowrap uppercase">Baptisan</button>
                        <button onclick="switchForm('jemaat')" id="tabJemaat" class="text-[10px] font-black text-slate-400 pb-2 whitespace-nowrap uppercase">Jemaat Baru</button>
                    </div>

                    <form id="formUmum" onsubmit="handleFormSubmit(event)" class="space-y-4">
                        <input type="text" id="formName" placeholder="Nama Lengkap" required class="w-full p-4 bg-slate-50 dark:bg-slate-800 dark:text-white rounded-xl border border-slate-200 dark:border-slate-700">
                        <select id="formService" class="w-full p-4 bg-slate-50 dark:bg-slate-800 dark:text-white rounded-xl border border-slate-200 dark:border-slate-700">
                            <option>Layanan Doa</option>
                            <option>Konseling</option>
                            <option>Informasi Lainnya</option>
                        </select>
                        <textarea id="formMessage" placeholder="Pesan Anda" class="w-full p-4 bg-slate-50 dark:bg-slate-800 dark:text-white rounded-xl border border-slate-200 dark:border-slate-700 h-32"></textarea>
                        <button type="submit" class="w-full bg-orange-500 text-white font-black py-4 rounded-xl hover:bg-orange-600 transition uppercase tracking-widest">Kirim Pesan</button>
                    </form>

                    <form id="formBaptis" onsubmit="handleBaptisSubmit(event)" class="hidden space-y-3">
                        <input type="text" id="bapNama" placeholder="Nama Lengkap" required class="w-full p-3 bg-slate-50 dark:bg-slate-800 dark:text-white rounded-xl border border-slate-200 dark:border-slate-700 text-sm">
                        <div class="grid grid-cols-2 gap-3">
                            <input type="text" id="bapTtl" placeholder="Tempat, Tgl Lahir" class="p-3 bg-slate-50 dark:bg-slate-800 dark:text-white rounded-xl border border-slate-200 dark:border-slate-700 text-sm">
                            <input type="number" id="bapUsia" placeholder="Usia" class="p-3 bg-slate-50 dark:bg-slate-800 dark:text-white rounded-xl border border-slate-200 dark:border-slate-700 text-sm">
                        </div>
                        <input type="text" id="bapWali" placeholder="Nama Wali/Orang Tua" class="w-full p-3 bg-slate-50 dark:bg-slate-800 dark:text-white rounded-xl border border-slate-200 dark:border-slate-700 text-sm">
                        <textarea id="bapAlamat" placeholder="Alamat Domisili" class="w-full p-3 bg-slate-50 dark:bg-slate-800 dark:text-white rounded-xl border border-slate-200 dark:border-slate-700 text-sm h-20"></textarea>
                        <div class="space-y-2">
                            <label class="text-[10px] font-bold text-slate-400 uppercase">Dokumen (Link G-Drive):</label>
                            <input type="text" id="bapLinkKK" placeholder="Link KK" class="w-full p-3 bg-blue-50 dark:bg-slate-800 dark:text-white rounded-xl border border-blue-100 dark:border-slate-700 text-xs">
                            <input type="text" id="bapLinkAkte" placeholder="Link Akte Kelahiran" class="w-full p-3 bg-purple-50 dark:bg-slate-800 dark:text-white rounded-xl border border-purple-100 dark:border-slate-700 text-xs">
                        </div>
                        <button type="submit" class="w-full bg-blue-600 text-white font-black py-4 rounded-xl hover:bg-blue-700 transition uppercase tracking-widest mt-2">Daftar Baptisan</button>
                    </form>

                    <form id="formJemaat" onsubmit="handleJemaatSubmit(event)" class="hidden space-y-3">
                        <div class="grid grid-cols-2 gap-3">
                            <input type="text" id="jemNama" placeholder="Nama Lengkap" required class="p-3 bg-slate-50 dark:bg-slate-800 dark:text-white rounded-xl border border-slate-200 dark:border-slate-700 text-sm">
                            <input type="text" id="jemNik" placeholder="NIK" required class="p-3 bg-slate-50 dark:bg-slate-800 dark:text-white rounded-xl border border-slate-200 dark:border-slate-700 text-sm">
                        </div>
                        <textarea id="jemAlamat" placeholder="Alamat Sesuai KTP" required class="w-full p-3 bg-slate-50 dark:bg-slate-800 dark:text-white rounded-xl border border-slate-200 dark:border-slate-700 text-sm h-16"></textarea>
                        
                        <div class="flex items-center gap-4 p-3 bg-slate-50 dark:bg-slate-800 rounded-xl border dark:border-slate-700">
                            <span class="text-[10px] font-bold text-slate-400 uppercase">Status Sakramen:</span>
                            <label class="text-xs dark:text-white flex items-center gap-1"><input type="radio" name="sakramen" value="Baptis" checked> Baptis</label>
                            <label class="text-xs dark:text-white flex items-center gap-1"><input type="radio" name="sakramen" value="Belum"> Belum</label>
                        </div>

                        <div class="grid grid-cols-2 gap-3">
                            <input type="text" id="jemNikah" placeholder="Data Pernikahan" class="p-3 bg-slate-50 dark:bg-slate-800 dark:text-white rounded-xl border border-slate-200 dark:border-slate-700 text-sm">
                            <input type="text" id="jemAnak" placeholder="Data Anak" class="p-3 bg-slate-50 dark:bg-slate-800 dark:text-white rounded-xl border border-slate-200 dark:border-slate-700 text-sm">
                        </div>
                        
                        <input type="text" id="jemLinkKK" placeholder="Link G-Drive Foto KK" required class="w-full p-3 bg-emerald-50 dark:bg-slate-800 dark:text-white rounded-xl border border-emerald-100 dark:border-slate-700 text-xs">
                        
                        <button type="submit" class="w-full bg-emerald-600 text-white font-black py-4 rounded-xl hover:bg-emerald-700 transition uppercase tracking-widest mt-2">Daftar Jemaat</button>
                    </form>
                </div>
            </div>
        </section>
    </main>

    <footer class="bg-slate-900 text-slate-500 py-12 text-center">
        <p class="text-white font-bold mb-2 uppercase">GPdI Anugerah</p>
        <p class="text-[10px] opacity-40 uppercase tracking-widest">© 2026 Seluruh Hak Cipta Dilindungi.</p>
    </footer>

    <script src="https://unpkg.com/aos@2.3.1/dist/aos.js"></script>
    <script>
        AOS.init();

        function render() {
            const db = JSON.parse(localStorage.getItem('church_db')) || {
                warta: { title: "Melangkah dengan Iman", points: ["Selamat Datang di GPdI Anugerah"], pdt: "-", lit: "-" },
                jadwalSesi: {
                    ibadah1: { wl: "-", s1: "-", s2: "-", p1: "-", p2: "-", p3: "-", pj1: "-", pj2: "-", pk1: "-", pk2: "-", pk3: "-", mm: "-" },
                    ibadah2: { wl: "-", s1: "-", s2: "-", p1: "-", p2: "-", p3: "-", pj1: "-", pj2: "-", pk1: "-", pk2: "-", pk3: "-", mm: "-" },
                    ibadah3: { wl: "-", s1: "-", s2: "-", p1: "-", p2: "-", p3: "-", pj1: "-", pj2: "-", pk1: "-", pk2: "-", pk3: "-", mm: "-" }
                },
                galeri: [], inbox: [], baptisan: [], jemaatBaru: []
            };

            document.getElementById('displayWartaTitle').innerText = db.warta.title;
            document.getElementById('displayWartaPoints').innerHTML = db.warta.points.map(p => `<li>• ${p}</li>`).join('');
            document.getElementById('displayPetugasContent').innerHTML = `<p class='text-xs text-slate-400'>PENGKHOTBAH</p><p class='font-bold mb-4'>${db.warta.pdt}</p><p class='text-xs text-slate-400'>LITURGOS</p><p class='font-bold'>${db.warta.lit}</p>`;

            const container = document.getElementById('displayJadwalContainer');
            container.innerHTML = "";
            for (let i = 1; i <= 3; i++) {
                const data = db.jadwalSesi[`ibadah${i}`];
                container.innerHTML += `
                    <div class="bg-white dark:bg-slate-800 rounded-[2.5rem] p-8 shadow-xl border dark:border-slate-700">
                        <h3 class="text-xl font-black mb-6 text-blue-600 uppercase border-b pb-4">Ibadah ${i}</h3>
                        <div class="space-y-3 text-xs">
                            <div class="flex justify-between"><span>WL</span><b>${data.wl}</b></div>
                            <div class="flex justify-between border-b pb-2"><span>Singer</span><b>${data.s1}, ${data.s2}</b></div>
                            <div class="py-2"><p class="text-slate-400 font-bold text-[9px]">PUNDI-PUNDI</p><b>${data.p1}, ${data.p2}, ${data.p3}</b></div>
                            <div class="flex justify-between border-b pb-2"><span>Penyambut</span><b>${data.pj1}, ${data.pj2}</b></div>
                            <div class="py-2"><p class="text-slate-400 font-bold text-[9px]">PARKIR</p><b>${data.pk1}, ${data.pk2}, ${data.pk3}</b></div>
                            <div class="flex justify-between"><span>Multimedia</span><b>${data.mm}</b></div>
                        </div>
                    </div>`;
            }

            document.getElementById('displayGaleri').innerHTML = db.galeri.map(g => `<img src='${g.url}' class='rounded-3xl aspect-square object-cover shadow-lg hover:scale-105 transition'>`).join('');
        }

        function switchForm(type) {
            const forms = ['formUmum', 'formBaptis', 'formJemaat'];
            const tabs = ['tabUmum', 'tabBaptis', 'tabJemaat'];
            
            forms.forEach(f => document.getElementById(f).classList.add('hidden'));
            tabs.forEach(t => {
                document.getElementById(t).classList.replace('text-blue-600', 'text-slate-400');
                document.getElementById(t).classList.remove('border-b-2', 'border-blue-600');
            });

            const activeForm = type === 'umum' ? 'formUmum' : (type === 'baptis' ? 'formBaptis' : 'formJemaat');
            const activeTab = type === 'umum' ? 'tabUmum' : (type === 'baptis' ? 'tabBaptis' : 'tabJemaat');

            document.getElementById(activeForm).classList.remove('hidden');
            document.getElementById(activeTab).classList.replace('text-slate-400', 'text-blue-600');
            document.getElementById(activeTab).classList.add('border-b-2', 'border-blue-600');
        }

        function handleFormSubmit(e) {
            e.preventDefault();
            let db = JSON.parse(localStorage.getItem('church_db'));
            db.inbox.push({ 
                name: document.getElementById('formName').value, 
                service: document.getElementById('formService').value, 
                message: document.getElementById('formMessage').value, 
                time: new Date().toLocaleString() 
            });
            localStorage.setItem('church_db', JSON.stringify(db));
            alert("Pesan Terkirim ke GPdI Anugerah!"); e.target.reset();
        }

        function handleBaptisSubmit(e) {
            e.preventDefault();
            let db = JSON.parse(localStorage.getItem('church_db'));
            db.baptisan.push({
                nama: document.getElementById('bapNama').value,
                ttl: document.getElementById('bapTtl').value,
                usia: document.getElementById('bapUsia').value,
                wali: document.getElementById('bapWali').value,
                alamat: document.getElementById('bapAlamat').value,
                fotoKK: document.getElementById('bapLinkKK').value,
                fotoAkte: document.getElementById('bapLinkAkte').value,
                time: new Date().toLocaleString()
            });
            localStorage.setItem('church_db', JSON.stringify(db));
            alert("Pendaftaran Baptisan Terkirim!"); e.target.reset();
        }

        function handleJemaatSubmit(e) {
            e.preventDefault();
            let db = JSON.parse(localStorage.getItem('church_db'));
            if(!db.jemaatBaru) db.jemaatBaru = [];
            
            const sakramen = document.querySelector('input[name="sakramen"]:checked').value;

            db.jemaatBaru.push({
                nama: document.getElementById('jemNama').value,
                nik: document.getElementById('jemNik').value,
                alamat: document.getElementById('jemAlamat').value,
                sakramen: sakramen,
                pernikahan: document.getElementById('jemNikah').value || "-",
                anak: document.getElementById('jemAnak').value || "-",
                fotoKK: document.getElementById('jemLinkKK').value,
                time: new Date().toLocaleString()
            });
            localStorage.setItem('church_db', JSON.stringify(db));
            alert("Pendaftaran Jemaat Baru Berhasil Terkirim!"); e.target.reset();
        }

        function updateTimer() {
            const now = new Date();
            const schedules = [8, 9, 10];
            let nextService = null;
            let isLive = false;

            for (let hour of schedules) {
                let start = new Date(now); start.setHours(hour, 0, 0, 0);
                let end = new Date(start.getTime() + 90 * 60000);
                if (now >= start && now <= end) { isLive = true; break; }
            }

            let targetDate = new Date(now);
            targetDate.setDate(now.getDate() + (7 - now.getDay()) % 7);
            for (let hour of schedules) {
                let serviceTime = new Date(targetDate); serviceTime.setHours(hour, 0, 0, 0);
                if (serviceTime.getTime() > now.getTime()) { nextService = serviceTime; break; }
            }
            if (!nextService && !isLive) {
                nextService = new Date(targetDate); nextService.setDate(targetDate.getDate() + 7); nextService.setHours(8, 0, 0);
            }

            const countdownContainer = document.getElementById("countdown");
            if (isLive) {
                document.getElementById('timerLabel').innerText = "Status:";
                countdownContainer.innerHTML = `<a href="#" class="bg-red-600 px-6 py-2 rounded-xl animate-pulse text-lg">LIVE SEKARANG</a>`;
            } else {
                const diff = nextService - now;
                const h = Math.floor(diff / 3600000);
                const m = Math.floor((diff % 3600000) / 60000);
                countdownContainer.innerHTML = `<div>${h}<span class='text-xs opacity-50 block'>JAM</span></div><div>${m}<span class='text-xs opacity-50 block'>MENIT</span></div>`;
            }
        }

        function toggleDarkMode() {
            document.documentElement.classList.toggle('dark');
            localStorage.theme = document.documentElement.classList.contains('dark') ? 'dark' : 'light';
        }

        if (localStorage.theme === 'dark') document.documentElement.classList.add('dark');
        setInterval(updateTimer, 1000);
        window.onload = render;
    </script>
</body>
</html>
