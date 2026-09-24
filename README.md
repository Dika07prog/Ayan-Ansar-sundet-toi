<!DOCTYPE html>
<html lang="kk" class="scroll-smooth">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Аян & Аңсар — Ұлы той шақыру</title>
    <!-- Tailwind CSS CDN -->
    <script src="https://cdn.tailwindcss.com"></script>
    <!-- Google Fonts -->
    <link rel="preconnect" href="https://fonts.googleapis.com">
    <link rel="preconnect" href="https://fonts.gstatic.com" crossorigin>
    <link href="https://fonts.googleapis.com/css2?family=Montserrat:wght@300;400;500;600;700&family=Playfair+Display:ital,wght@0,400;0,600;0,700;1,400&display=swap" rel="stylesheet">
    <!-- FontAwesome for icons -->
    <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.4.0/css/all.min.css">
    
    <script>
        tailwind.config = {
            theme: {
                extend: {
                    colors: {
                        navy: {
                            900: '#0B132B',
                            800: '#1C2541',
                            700: '#3A506B',
                        },
                        turquoise: {
                            900: '#004643',
                            800: '#006661',
                            600: '#0b8a84',
                            500: '#14b8b2'
                        },
                        gold: {
                            300: '#F4D06F',
                            400: '#E9C46A',
                            500: '#D4AF37',
                            600: '#B8860B',
                        },
                        ivory: '#FAF9F6',
                        cream: '#F4F1EA'
                    },
                    fontFamily: {
                        serif: ['"Playfair Display"', 'serif'],
                        sans: ['"Montserrat"', 'sans-serif']
                    }
                }
            }
        }
    </script>
    <style>
        body {
            font-family: 'Montserrat', sans-serif;
            background-color: #0B132B;
            color: #FAF9F6;
            overflow-x: hidden;
        }
        
        .gold-gradient-text {
            color: #D4AF37;
            text-shadow: 0 0 25px rgba(212, 175, 55, 0.35);
        }

        .kazakh-pattern-bg {
            background-color: #0B132B;
            background-image: radial-gradient(#D4AF37 0.75px, transparent 0.75px), radial-gradient(#D4AF37 0.75px, #0B132B 0.75px);
            background-size: 30px 30px;
            background-position: 0 0, 15px 15px;
            opacity: 0.95;
        }

        .ornament-box {
            position: relative;
            background: rgba(28, 37, 65, 0.75);
            backdrop-filter: blur(10px);
            border: 1px solid rgba(212, 175, 55, 0.35);
        }

        @keyframes floatSlow {
            0%, 100% { transform: translateY(0px) rotate(0deg); }
            50% { transform: translateY(-8px) rotate(0.5deg); }
        }
        .animate-float {
            animation: floatSlow 6s ease-in-out infinite;
        }

        @keyframes goldGlow {
            0%, 100% { box-shadow: 0 0 15px rgba(212, 175, 55, 0.2); }
            50% { box-shadow: 0 0 30px rgba(212, 175, 55, 0.45); }
        }
        .gold-glow {
            animation: goldGlow 4s ease-in-out infinite;
        }
    </style>
</head>
<body class="bg-navy-900 text-ivory antialiased selection:bg-gold-500 selection:text-navy-900">

    <!-- Background Audio Element ("Сүндет той" — Айдар Тұрғанбек) -->
    <!-- Ескерту: Егер музыка файлды өз серверіңізге жүктесеңіз, src ішіне нақты file path немесе direct MP3 сілтемесін қойыңыз -->
    <audio id="bgMusic" loop preload="auto">
        <source src="sundet-toy.mp3" type="audio/mpeg">
        Сіздің браузеріңіз аудио элементті қолдамайды.
    </audio>

    <!-- Floating Fixed Music Toggle Button (Bottom-Right Corner) -->
    <button id="musicToggleBtn" onclick="toggleMusic()" class="fixed bottom-6 right-6 z-50 bg-navy-800/90 hover:bg-navy-700 text-gold-300 border border-gold-500/60 px-4 py-3 rounded-full shadow-2xl backdrop-blur-md transition-all duration-300 flex items-center gap-2.5 text-sm font-medium cursor-pointer gold-glow">
        <span id="musicIcon">▶</span>
        <span id="musicText">Музыканы қосу</span>
    </button>

    <section class="relative min-h-screen flex flex-col items-center justify-center text-center px-4 py-20 kazakh-pattern-bg overflow-hidden">
        <div class="absolute inset-0 bg-gradient-to-b from-navy-900/40 via-navy-900/80 to-navy-900 pointer-events-none"></div>
        <div class="absolute w-[500px] h-[500px] bg-gold-500/10 rounded-full blur-3xl pointer-events-none -top-32 -left-32"></div>
        <div class="absolute w-[400px] h-[400px] bg-turquoise-600/15 rounded-full blur-3xl pointer-events-none -bottom-32 -right-32"></div>

        <div class="relative z-10 max-w-4xl mx-auto w-full border border-gold-500/40 p-8 sm:p-12 rounded-2xl ornament-box shadow-2xl animate-float">
            <!-- Kazakh motifs -->
            <div class="absolute top-3 left-3 text-gold-500/60 text-2xl"><i class="fa-solid fa-kohan"></i></div>
            <div class="absolute top-3 right-3 text-gold-500/60 text-2xl"><i class="fa-solid fa-kohan"></i></div>
            <div class="absolute bottom-3 left-3 text-gold-500/60 text-2xl"><i class="fa-solid fa-kohan"></i></div>
            <div class="absolute bottom-3 right-3 text-gold-500/60 text-2xl"><i class="fa-solid fa-kohan"></i></div>

            <!-- Main Title in Warm Golden Color (#D4AF37) -->
            <h1 class="font-serif text-5xl sm:text-7xl md:text-8xl font-bold gold-gradient-text mb-2 tracking-wide">
                Аян & Аңсар
            </h1>

            <div class="flex items-center justify-center gap-4 my-4">
                <div class="h-[1px] w-16 sm:w-24 bg-gradient-to-r from-transparent to-gold-500"></div>
                <span class="text-gold-400 text-xl font-serif italic">Ұлы той</span>
                <div class="h-[1px] w-16 sm:w-24 bg-gradient-to-l from-transparent to-gold-500"></div>
            </div>

            <!-- Clean First Screen Invitation Text (No ages, no parents) -->
            <div class="bg-navy-800/80 border border-gold-500/30 rounded-xl p-6 sm:p-8 max-w-2xl mx-auto mb-8 shadow-inner">
                <p class="text-base sm:text-lg font-serif italic leading-relaxed text-cream">
                    Ардақты ағайын, қадірлі қонақтар!<br>
                    Сіздерді ұлдарымыз <b><span class="text-gold-400 font-semibold">Аян мен Аңсардың</span></b> сүндет тойына арналған ақ дастарханымыздың қадірлі қонағы болуға шақырамыз.
                    Қуанышымызды бірге бөлісіп, ақ тілектеріңізді білдіруге шақырамыз!
                </p>
            </div>

            <!-- Date & Time badges -->
            <div class="flex flex-wrap justify-center gap-4 sm:gap-8 mb-8">
                <div class="flex items-center gap-3 bg-navy-900/80 px-6 py-3 rounded-full border border-gold-500/40">
                    <i class="fa-regular fa-calendar-days text-gold-400 text-lg"></i>
                    <span class="font-semibold tracking-wide text-gold-300">24 ҚАЗАН 2026</span>
                </div>
                <div class="flex items-center gap-3 bg-navy-900/80 px-6 py-3 rounded-full border border-gold-500/40">
                    <i class="fa-regular fa-clock text-gold-400 text-lg"></i>
                    <span class="font-semibold tracking-wide text-gold-300">19:00</span>
                </div>
            </div>

            <!-- Scroll Down Indicator -->
            <a href="#countdown" class="inline-flex flex-col items-center text-gold-400 hover:text-gold-300 transition-colors mt-2">
                <span class="text-xs tracking-widest uppercase mb-2">Толығырақ</span>
                <i class="fa-solid fa-chevron-down animate-bounce"></i>
            </a>
        </div>
    </section>

    <section id="countdown" class="py-16 px-4 bg-navy-800/60 border-y border-gold-500/20 relative">
        <div class="max-w-4xl mx-auto text-center">
            <h2 class="font-serif text-2xl sm:text-3xl font-bold text-gold-400 mb-2">Тойға дейін қалды</h2>
            <p class="text-ivory/70 text-sm mb-8">Қуанышты сәтке санаулы күндер қалды</p>

            <div class="grid grid-cols-2 sm:grid-cols-4 gap-4 sm:gap-6 max-w-3xl mx-auto">
                <div class="bg-navy-900/90 border border-gold-500/40 rounded-2xl p-4 sm:p-6 gold-glow">
                    <div id="days" class="font-serif text-3xl sm:text-5xl font-bold gold-gradient-text mb-1">00</div>
                    <div class="text-xs sm:text-sm uppercase tracking-widest text-gold-300/80 font-medium">КҮН</div>
                </div>
                <div class="bg-navy-900/90 border border-gold-500/40 rounded-2xl p-4 sm:p-6 gold-glow">
                    <div id="hours" class="font-serif text-3xl sm:text-5xl font-bold gold-gradient-text mb-1">00</div>
                    <div class="text-xs sm:text-sm uppercase tracking-widest text-gold-300/80 font-medium">САҒАТ</div>
                </div>
                <div class="bg-navy-900/90 border border-gold-500/40 rounded-2xl p-4 sm:p-6 gold-glow">
                    <div id="minutes" class="font-serif text-3xl sm:text-5xl font-bold gold-gradient-text mb-1">00</div>
                    <div class="text-xs sm:text-sm uppercase tracking-widest text-gold-300/80 font-medium">МИНУТ</div>
                </div>
                <div class="bg-navy-900/90 border border-gold-500/40 rounded-2xl p-4 sm:p-6 gold-glow">
                    <div id="seconds" class="font-serif text-3xl sm:text-5xl font-bold gold-gradient-text mb-1">00</div>
                    <div class="text-xs sm:text-sm uppercase tracking-widest text-gold-300/80 font-medium">СЕКУНД</div>
                </div>
            </div>
        </div>
    </section>

    <!-- Бірінші беттегі мәтін екінші рет қайталанбас үшін бұл бөлім жинақы, қосымша мәтін/тілек түріне өзгертілді -->
    <section class="py-20 px-4 relative kazakh-pattern-bg">
        <div class="max-w-3xl mx-auto text-center ornament-box p-8 sm:p-14 rounded-3xl shadow-2xl relative">
            <div class="absolute -top-6 left-1/2 transform -translate-x-1/2 bg-navy-900 border border-gold-500 px-6 py-2 rounded-full">
                <span class="text-gold-400 font-serif tracking-widest uppercase text-sm">Қымбатты қонақтарға</span>
            </div>

            <div class="text-gold-400 text-3xl mb-6 mt-4">
                <i class="fa-solid fa-hands-praying"></i>
            </div>


            <div class="space-y-4 text-base sm:text-lg text-cream/90 leading-relaxed font-light mb-8">
                <p>
                    Ата-ана үмітін ақтар ұлдарымыздың жетістігі мен қуанышын өзіңізбен бірге тойлау – біз үшін үлкен мәртебе.
                </p>
                <p>
                    Ақ батаңызды беріп, мерекелік дастарханымыздың 
                </p>
            </div>
            <h2 class="font-serif text-3xl sm:text-4xl font-bold text-gold-300 mb-6">
                Қадірлі қонағы болыңыздар!
            </h2>
        </div>
    </section>

    <section class="py-20 px-4 bg-navy-800/80 border-t border-gold-500/20">
        <div class="max-w-3xl mx-auto">
            <div class="text-center mb-12">
                <h2 class="font-serif text-3xl sm:text-4xl font-bold gold-gradient-text mb-3">Той салтанаты</h2>
                <p class="text-ivory/70">Мерекелік дастархан жайылатын орын және уақыт</p>
            </div>

            <div class="ornament-box p-8 sm:p-12 rounded-3xl shadow-xl">
                <div class="flex items-center gap-4 mb-8 justify-center text-center">
                    <div>
                        <h3 class="font-serif text-3xl sm:text-4xl font-bold text-gold-300 mb-2">«Алтын Жұлдыз»</h3>
                        <p class="text-sm uppercase tracking-widest text-gold-400">Мейрамхана кешені</p>
                    </div>
                </div>

                <div class="space-y-6 max-w-lg mx-auto border-t border-b border-gold-500/20 py-8">
                    <div class="flex items-center gap-4">
                        <div class="w-12 h-12 rounded-2xl bg-gold-500/10 border border-gold-500/40 flex items-center justify-center text-gold-400 text-xl flex-shrink-0">
                            <i class="fa-regular fa-calendar-days"></i>
                        </div>
                        <div>
                            <p class="text-xs uppercase tracking-wider text-gold-400/80 font-semibold">Күні</p>
                            <p class="text-lg text-ivory font-medium">24 қазан 2026 жыл</p>
                        </div>
                    </div>

                    <div class="flex items-center gap-4">
                        <div class="w-12 h-12 rounded-2xl bg-gold-500/10 border border-gold-500/40 flex items-center justify-center text-gold-400 text-xl flex-shrink-0">
                            <i class="fa-regular fa-clock"></i>
                        </div>
                        <div>
                            <p class="text-xs uppercase tracking-wider text-gold-400/80 font-semibold">Уақыты</p>
                            <p class="text-lg text-ivory font-medium">Сағат 19:00</p>
                        </div>
                    </div>

                    <div class="flex items-center gap-4">
                        <div class="w-12 h-12 rounded-2xl bg-gold-500/10 border border-gold-500/40 flex items-center justify-center text-gold-400 text-xl flex-shrink-0">
                            <i class="fa-solid fa-location-dot"></i>
                        </div>
                        <div>
                            <p class="text-xs uppercase tracking-wider text-gold-400/80 font-semibold">Мекенжайы</p>
                            <p class="text-lg text-ivory font-medium">Шымкент қаласы, Тамерлановское шоссе, 234</p>
                        </div>
                    </div>
                </div>
            </div>
        </div>
    </section>

    <section class="py-20 px-4 kazakh-pattern-bg">
        <div class="max-w-3xl mx-auto text-center ornament-box p-8 sm:p-12 rounded-3xl shadow-2xl">
            <h2 class="font-serif text-3xl sm:text-4xl font-bold text-gold-300 mb-3">Сізді тойымызда күтеміз!</h2>
            <p class="text-ivory/70 mb-8">Тойға келетініңізді растап, бізге қуаныш сыйлаңыз</p>

            <div id="rsvpFormContainer">
                <div class="flex flex-col sm:flex-row justify-center gap-4 sm:gap-6 mb-6">
                    <button onclick="handleRSVP('yes')" class="flex-1 bg-gradient-to-r from-turquoise-600 to-turquoise-800 hover:from-turquoise-500 hover:to-turquoise-700 text-ivory font-bold py-5 px-8 rounded-2xl shadow-xl transition-all duration-300 flex items-center justify-center gap-3 border border-turquoise-500/50 group text-lg cursor-pointer">
                        <i class="fa-solid fa-circle-check text-gold-400 text-xl group-hover:scale-125 transition-transform"></i>
                        <span>ҚАТЫСАМЫН</span>
                    </button>
                    <button onclick="handleRSVP('no')" class="flex-1 bg-navy-900/90 hover:bg-navy-800 text-ivory font-bold py-5 px-8 rounded-2xl shadow-xl transition-all duration-300 flex items-center justify-center gap-3 border border-gold-500/40 group text-lg cursor-pointer">
                        <i class="fa-solid fa-circle-xmark text-gold-400 text-xl group-hover:scale-125 transition-transform"></i>
                        <span>ҚАТЫСА АЛМАЙМЫН</span>
                    </button>
                </div>
            </div>

            <!-- Confirmation Message Box -->
            <div id="rsvpMessage" class="hidden bg-navy-900/95 border-2 border-gold-500 p-6 rounded-2xl text-center shadow-2xl">
                <div id="rsvpIcon" class="text-gold-400 text-3xl mb-2"></div>
                <h3 id="rsvpTitle" class="font-serif text-2xl font-bold text-gold-300 mb-2"></h3>
                <p id="rsvpText" class="text-cream text-base"></p>
                <button onclick="resetRSVP()" class="mt-4 text-xs uppercase tracking-widest text-gold-400 underline hover:text-gold-300 cursor-pointer">
                    Жауапты өзгерту
                </button>
            </div>
        </div>
    </section>

    <!-- Соңғы бөлім -->
    <section class="py-24 px-4 bg-navy-900 border-t border-gold-500/30 text-center relative overflow-hidden">
        <div class="absolute inset-0 bg-gradient-to-t from-gold-500/5 via-transparent to-transparent pointer-events-none"></div>
        <div class="max-w-2xl mx-auto ornament-box p-10 sm:p-14 rounded-3xl shadow-2xl relative z-10 gold-glow">
            <h2 class="font-serif text-3xl sm:text-5xl font-bold gold-gradient-text mb-4">
                Аян & Аңсар
            </h2>
            <p class="text-gold-300 text-lg sm:text-xl italic tracking-wider">
                Қуанышта кездескенше!
            </p>
            <div class="flex justify-center gap-4 text-gold-500 text-xl mt-6">
                <i class="fa-solid fa-kohan"></i>
                <i class="fa-solid fa-kohan"></i>
                <i class="fa-solid fa-kohan"></i>
            </div>
        </div>
    </section>

    <script>
        // Countdown Timer Logic to 24 October 2026 19:00:00
        const eventDate = new Date("October 24, 2026 19:00:00").getTime();

        function updateCountdown() {
            const now = new Date().getTime();
            const distance = eventDate - now;

            if (distance < 0) {
                document.getElementById("days").innerText = "00";
                document.getElementById("hours").innerText = "00";
                document.getElementById("minutes").innerText = "00";
                document.getElementById("seconds").innerText = "00";
                return;
            }

            const days = Math.floor(distance / (1000 * 60 * 60 * 24));
            const hours = Math.floor((distance % (1000 * 60 * 60 * 24)) / (1000 * 60 * 60));
            const minutes = Math.floor((distance % (1000 * 60 * 60)) / (1000 * 60));
            const seconds = Math.floor((distance % (1000 * 60)) / 1000);

            document.getElementById("days").innerText = String(days).padStart(2, '0');
            document.getElementById("hours").innerText = String(hours).padStart(2, '0');
            document.getElementById("minutes").innerText = String(minutes).padStart(2, '0');
            document.getElementById("seconds").innerText = String(seconds).padStart(2, '0');
        }

        setInterval(updateCountdown, 1000);
        updateCountdown();

        // Background Music Player & Toggle Logic
        const bgMusic = document.getElementById("bgMusic");
        const musicToggleBtn = document.getElementById("musicToggleBtn");
        const musicIcon = document.getElementById("musicIcon");
        const musicText = document.getElementById("musicText");
        let isPlaying = false;

        function toggleMusic() {
            if (isPlaying) {
                bgMusic.pause();
                isPlaying = false;
                musicIcon.innerText = "▶";
                musicText.innerText = "Музыканы қосу";
            } else {
                bgMusic.play().then(() => {
                    isPlaying = true;
                    musicIcon.innerText = "Ⅱ";
                    musicText.innerText = "Музыканы тоқтату";
                }).catch(err => {
                    console.log("Audio play blocked or error:", err);
                });
            }
        }

        // Auto-play attempt on first user interaction
        window.addEventListener('DOMContentLoaded', () => {
            bgMusic.play().then(() => {
                isPlaying = true;
                musicIcon.innerText = "Ⅱ";
                musicText.innerText = "Музыканы тоқтату";
            }).catch(() => {
                const startAudioOnInteraction = () => {
                    bgMusic.play().then(() => {
                        isPlaying = true;
                        musicIcon.innerText = "Ⅱ";
                        musicText.innerText = "Музыканы тоқтату";
                    }).catch(err => console.log("Interaction play retry failed:", err));
                    window.removeEventListener('click', startAudioOnInteraction);
                    window.removeEventListener('touchstart', startAudioOnInteraction);
                    window.removeEventListener('scroll', startAudioOnInteraction);
                };
                window.addEventListener('click', startAudioOnInteraction, { once: true });
                window.addEventListener('touchstart', startAudioOnInteraction, { once: true });
                window.addEventListener('scroll', startAudioOnInteraction, { once: true });
            });
        });

        // RSVP Handler Logic
        function handleRSVP(status) {
            const formContainer = document.getElementById("rsvpFormContainer");
            const messageBox = document.getElementById("rsvpMessage");
            const rsvpIcon = document.getElementById("rsvpIcon");
            const rsvpTitle = document.getElementById("rsvpTitle");
            const rsvpText = document.getElementById("rsvpText");

            formContainer.classList.add("hidden");
            messageBox.classList.remove("hidden");

            if (status === 'yes') {
                rsvpIcon.className = "fa-solid fa-face-smile-beam text-gold-400 text-3xl mb-2";
                rsvpTitle.innerText = "Қуаныштымыз!";
                rsvpText.innerText = "Келетініңізге қуаныштымыз! Сізді асыға күтеміз және той төрінде қарсы аламыз.";
            } else {
                rsvpIcon.className = "fa-solid fa-heart text-gold-400 text-3xl mb-2";
                rsvpTitle.innerText = "Рақмет!";
                rsvpText.innerText = "Келесі қуанышты күндерде кездесуге жазсын!";
            }
        }

        function resetRSVP() {
            const formContainer = document.getElementById("rsvpFormContainer");
            const messageBox = document.getElementById("rsvpMessage");
            messageBox.classList.add("hidden");
            formContainer.classList.remove("hidden");
        }
    </script>
</body>
</html>
