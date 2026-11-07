<!DOCTYPE html>
<html lang="en" class="dark scroll-smooth">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>THE ROYAL CROWN INN - Medieval English Smart Hotel</title>
    <!-- Tailwind CSS -->
    <script src="https://cdn.tailwindcss.com"></script>
    <!-- Google Fonts: Cormorant Garamond (Ultra Luxury Serif), Cinzel (Regal Capitals), Noto Serif Thai & Plus Jakarta Sans -->
    <link rel="preconnect" href="https://fonts.googleapis.com">
    <link rel="preconnect" href="https://fonts.gstatic.com" crossorigin>
    <link href="https://fonts.googleapis.com/css2?family=Cinzel:wght@400;600;700;900&family=Cormorant+Garamond:ital,wght@0,400;0,500;0,600;0,700;1,400&family=Noto+Serif+Thai:wght@300;400;600;700&family=Plus+Jakarta+Sans:wght@300;400;500;600;700&display=swap" rel="stylesheet">
    <!-- Lucide Icons -->
    <script src="https://unpkg.com/lucide@latest"></script>
    <script>
        tailwind.config = {
            darkMode: 'class',
            theme: {
                extend: {
                    colors: {
                        medieval: {
                            bg: '#171513',
                            card: '#221F1C',
                            surface: '#2B2622',
                            accent: '#3A2920',
                            gold: '#C9A45C',
                            goldLight: '#E8C87A',
                            goldDark: '#8C6C2E',
                            cream: '#F4EBDD',
                            crimson: '#651F25',
                            crimsonHover: '#852A32',
                            slate: '#8E8B85'
                        }
                    },
                    fontFamily: {
                        serif: ['"Cormorant Garamond"', '"Noto Serif Thai"', 'serif'],
                        cinzel: ['Cinzel', 'serif'],
                        sans: ['"Plus Jakarta Sans"', 'sans-serif'],
                        thaiSerif: ['"Noto Serif Thai"', 'serif']
                    }
                }
            }
        }
    </script>
    <style>
        /* Custom scrollbar for medieval aesthetic */
        ::-webkit-scrollbar {
            width: 8px;
            height: 8px;
        }
        ::-webkit-scrollbar-track {
            background: #171513;
        }
        ::-webkit-scrollbar-thumb {
            background: #3A2920;
            border: 1px solid #C9A45C;
            border-radius: 4px;
        }
        ::-webkit-scrollbar-thumb:hover {
            background: #C9A45C;
        }
        .gold-gradient-text {
            background: linear-gradient(135deg, #FFFDF8 0%, #E8C87A 40%, #C9A45C 70%, #9E7933 100%);
            -webkit-background-clip: text;
            -webkit-text-fill-color: transparent;
        }
        .gold-border {
            border: 1px solid rgba(201, 164, 92, 0.3);
        }
        .gold-border-glow {
            border: 1px solid rgba(201, 164, 92, 0.6);
            box-shadow: 0 0 15px rgba(201, 164, 92, 0.15);
        }
        .bg-castle-pattern {
            background-image: radial-gradient(rgba(201, 164, 92, 0.08) 1px, transparent 0);
            background-size: 24px 24px;
        }
    </style>
</head>
<body class="bg-medieval-bg text-medieval-cream font-sans antialiased selection:bg-medieval-gold selection:text-medieval-bg min-h-screen flex flex-col">

    <!-- TOP ANNOUNCEMENT BAR -->
    <div class="bg-medieval-crimson text-medieval-cream text-xs py-2 px-4 text-center border-b border-medieval-gold/30 flex justify-between items-center">
        <div class="hidden sm:flex items-center gap-2 mx-auto sm:mx-0">
            <i data-lucide="sparkles" class="w-3.5 h-3.5 text-medieval-gold"></i>
            <span class="tracking-wider uppercase font-cinzel text-[11px]">THE ROYAL CROWN INN • LUXURY SMART HOTEL & AI CONCIERGE (โรงแรมหรูสไตล์ปราสาทอังกฤษ)</span>
        </div>
        <div class="flex items-center gap-4 mx-auto sm:mx-0">
            <span class="text-medieval-gold font-medium text-[11px]"><i data-lucide="tag" class="w-3 h-3 inline mr-1"></i> โค้ดส่วนลด: <strong class="underline decoration-medieval-gold font-mono">NEWMEMBER</strong> (ลด 20%)</span>
            <button onclick="toggleAdminMode()" class="px-2.5 py-0.5 rounded bg-medieval-gold/20 hover:bg-medieval-gold text-medieval-gold hover:text-medieval-bg transition text-xs font-cinzel font-semibold border border-medieval-gold/50 flex items-center gap-1 tracking-wider">
                <i data-lucide="shield-alert" class="w-3 h-3"></i> <span id="viewModeText">เข้าสู่ระบบ Admin Dashboard</span>
            </button>
        </div>
    </div>

    <!-- MAIN NAVBAR -->
    <nav class="sticky top-0 z-40 bg-medieval-bg/95 backdrop-blur-md border-b border-medieval-gold/20 shadow-2xl">
        <div class="max-w-7xl mx-auto px-4 sm:px-6 lg:px-8">
            <div class="flex justify-between items-center h-20">
                <!-- Brand Logo -->
                <a href="#home" class="flex items-center gap-3.5 group">
                    <div class="w-12 h-12 rounded-lg border border-medieval-gold bg-medieval-card flex items-center justify-center p-2 group-hover:border-medieval-goldLight transition-colors shadow-lg shadow-medieval-gold/10">
                        <!-- Crown SVG Logo -->
                        <svg class="w-full h-full text-medieval-gold" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="1.5">
                            <path d="M2 4l3 12h14l3-12-6 7-4-8-4 8-6-7z" fill="rgba(201, 164, 92, 0.2)"/>
                            <path d="M3 20h18v2H3z" fill="currentColor"/>
                            <circle cx="12" cy="4" r="1" fill="currentColor"/>
                            <circle cx="2" cy="4" r="1" fill="currentColor"/>
                            <circle cx="22" cy="4" r="1" fill="currentColor"/>
                        </svg>
                    </div>
                    <div>
                        <span class="font-serif text-xl sm:text-2xl font-bold tracking-widest block text-medieval-gold leading-tight">THE ROYAL CROWN INN</span>
                        <span class="text-[9px] tracking-[0.25em] text-medieval-cream/70 font-thaiSerif uppercase block">โรงแรมหรูสไตล์ปราสาทอังกฤษยุคกลาง</span>
                    </div>
                </a>

                <!-- Desktop Navigation Menu -->
                <div class="hidden md:flex items-center gap-7 font-cinzel text-xs tracking-[0.15em] uppercase">
                    <a href="#home" class="hover:text-medieval-gold transition py-1 border-b-2 border-transparent hover:border-medieval-gold">หน้าแรก (Home)</a>
                    <a href="#rooms" class="hover:text-medieval-gold transition py-1 border-b-2 border-transparent hover:border-medieval-gold">ห้องพัก (Suites)</a>
                    <a href="#concierge" class="hover:text-medieval-gold transition py-1 border-b-2 border-transparent hover:border-medieval-gold flex items-center gap-1.5 text-medieval-gold font-semibold">
                        <i data-lucide="bot" class="w-3.5 h-3.5"></i> AI Concierge
                    </a>
                    <a href="#dining" class="hover:text-medieval-gold transition py-1 border-b-2 border-transparent hover:border-medieval-gold">ห้องอาหาร & สปา</a>
                    <a href="#promotions" class="hover:text-medieval-gold transition py-1 border-b-2 border-transparent hover:border-medieval-gold">โปรโมชั่น</a>
                    <a href="#membership" class="hover:text-medieval-gold transition py-1 border-b-2 border-transparent hover:border-medieval-gold">สมาชิก Royal Club</a>
                </div>

                <!-- CTA Action -->
                <div class="hidden sm:flex items-center gap-3">
                    <button onclick="scrollToRooms()" class="px-6 py-2.5 rounded-md bg-medieval-crimson hover:bg-medieval-crimsonHover text-medieval-cream font-thaiSerif font-semibold text-xs tracking-[0.15em] uppercase border border-medieval-gold/40 shadow-xl hover:shadow-medieval-crimson/30 transition duration-300 flex items-center gap-2">
                        <i data-lucide="calendar-check" class="w-4 h-4 text-medieval-gold"></i>
                        จองห้องพัก (BOOK NOW)
                    </button>
                </div>

                <!-- Mobile menu button -->
                <button onclick="toggleMobileMenu()" class="md:hidden p-2 text-medieval-gold hover:bg-medieval-card rounded-md">
                    <i data-lucide="menu" id="menuIcon" class="w-6 h-6"></i>
                </button>
            </div>
        </div>

        <!-- Mobile Menu Container -->
        <div id="mobileMenu" class="hidden md:hidden bg-medieval-card border-b border-medieval-gold/30 px-4 pt-2 pb-6 space-y-3 font-thaiSerif text-xs uppercase tracking-wider">
            <a href="#home" onclick="toggleMobileMenu()" class="block py-2 text-medieval-cream hover:text-medieval-gold">หน้าแรก (Home)</a>
            <a href="#rooms" onclick="toggleMobileMenu()" class="block py-2 text-medieval-cream hover:text-medieval-gold">ห้องพักหรู (Royal Accommodations)</a>
            <a href="#concierge" onclick="toggleMobileMenu()" class="block py-2 text-medieval-gold font-bold">AI Royal Concierge (ผู้ช่วย AI)</a>
            <a href="#dining" onclick="toggleMobileMenu()" class="block py-2 text-medieval-cream hover:text-medieval-gold">ห้องอาหาร & สปา (Restaurant & Spa)</a>
            <a href="#promotions" onclick="toggleMobileMenu()" class="block py-2 text-medieval-cream hover:text-medieval-gold">โปรโมชั่นพิเศษ (Promotions)</a>
            <a href="#membership" onclick="toggleMobileMenu()" class="block py-2 text-medieval-cream hover:text-medieval-gold">ระบบสมาชิก (Member Portal)</a>
            <button onclick="scrollToRooms(); toggleMobileMenu()" class="w-full mt-2 py-3 bg-medieval-crimson text-medieval-cream font-bold text-center rounded tracking-widest">จองห้องพักทันที</button>
        </div>
    </nav>

    <!-- GUEST VIEW PORTAL CONTAINER -->
    <div id="guestPortalView" class="flex-grow">
        
        <!-- HERO SECTION WITH CUSTOM GOTHIC LOBBY IMAGE -->
        <section id="home" class="relative min-h-[90vh] flex items-center justify-center bg-black overflow-hidden border-b border-medieval-gold/30">
            <!-- Background Image: Gothic Castle Luxury Lobby -->
            <div class="absolute inset-0 z-0">
                <img src="https://encrypted-tbn0.gstatic.com/images?q=tbn:ANd9GcT53AqdTcx21aPBvo0af_QfgOp84cePlEK0hbCRIvUkCw&s=10" 
                     onerror="this.onerror=null; this.src='https://images.unsplash.com/photo-1544644181-1484b3fdfc62?q=80&w=1920&auto=format&fit=crop';" 
                     alt="The Royal Crown Inn Medieval Gothic Lobby" 
                     class="w-full h-full object-cover object-center scale-105 filter brightness-75 contrast-110 transition-transform duration-10000 hover:scale-100">
                <div class="absolute inset-0 bg-gradient-to-t from-medieval-bg via-medieval-bg/60 to-black/70"></div>
                <div class="absolute inset-0 bg-[radial-gradient(ellipse_at_center,_var(--tw-gradient-stops))] from-transparent via-medieval-bg/50 to-medieval-bg"></div>
            </div>

            <!-- Hero Content -->
            <div class="relative z-10 max-w-5xl mx-auto px-4 text-center py-24">
                <!-- Royal Badge -->
                <div class="inline-flex items-center gap-2 px-5 py-2 rounded-full bg-medieval-card/90 border border-medieval-gold/50 mb-8 backdrop-blur-md shadow-2xl">
                    <i data-lucide="crown" class="w-4 h-4 text-medieval-gold"></i>
                    <span class="font-thaiSerif text-xs uppercase tracking-[0.2em] text-medieval-gold font-semibold">ปราสาทอังกฤษยุคกลาง ผสานระบบ SMART HOTEL & AI</span>
                </div>

                <h1 class="font-serif text-3xl sm:text-5xl lg:text-7xl font-semibold leading-tight mb-4 tracking-wide gold-gradient-text drop-shadow-2xl">
                    WELCOME TO THE ROYAL CROWN INN
                </h1>
                <h2 class="font-thaiSerif text-xl sm:text-3xl text-medieval-gold font-semibold mb-6 tracking-wide drop-shadow-lg">
                    ยินดีต้อนรับสู่ เดอะ รอยัล คราวน์ อินน์
                </h2>
                
                <p class="font-thaiSerif text-base sm:text-xl text-medieval-cream/90 max-w-3xl mx-auto mb-10 leading-relaxed font-normal">
                    "สัมผัสประสบการณ์การพักผ่อนระดับราชวงศ์ ณ ปราสาทอังกฤษยุคกลาง ผสานเทคโนโลยี Smart Hotel อัจฉริยะ"
                </p>

                <div class="flex flex-col sm:flex-row items-center justify-center gap-4 sm:gap-6">
                    <button onclick="scrollToRooms()" class="w-full sm:w-auto px-9 py-4 rounded-md bg-medieval-crimson hover:bg-medieval-crimsonHover text-medieval-cream font-thaiSerif font-semibold tracking-[0.15em] text-xs uppercase border border-medieval-gold/50 shadow-2xl hover:shadow-medieval-crimson/40 transition duration-300 flex items-center justify-center gap-3">
                        <i data-lucide="shield" class="w-4 h-4 text-medieval-gold"></i>
                        จองห้องพัก / BOOK YOUR STAY
                    </button>
                    <a href="#rooms" class="w-full sm:w-auto px-9 py-4 rounded-md bg-medieval-card/90 hover:bg-medieval-surface text-medieval-gold font-thaiSerif font-semibold tracking-[0.15em] text-xs uppercase border border-medieval-gold/40 hover:border-medieval-gold transition duration-300 flex items-center justify-center gap-3 backdrop-blur-md">
                        <i data-lucide="eye" class="w-4 h-4"></i>
                        สำรวจห้องพัก / EXPLORE ROOMS
                    </a>
                </div>

                <!-- Quick Smart Feature Bar -->
                <div class="grid grid-cols-2 md:grid-cols-4 gap-4 max-w-4xl mx-auto mt-16 pt-8 border-t border-medieval-gold/20 text-xs font-thaiSerif uppercase tracking-wider text-medieval-cream/80">
                    <div class="flex items-center justify-center gap-2">
                        <i data-lucide="sparkles" class="w-4 h-4 text-medieval-gold"></i>
                        <span>AI Concierge 24 ชั่วโมง</span>
                    </div>
                    <div class="flex items-center justify-center gap-2">
                        <i data-lucide="wifi" class="w-4 h-4 text-medieval-gold"></i>
                        <span>Smart Room Automation</span>
                    </div>
                    <div class="flex items-center justify-center gap-2">
                        <i data-lucide="utensils" class="w-4 h-4 text-medieval-gold"></i>
                        <span>สำรับอาหารสไตล์ราชวงศ์</span>
                    </div>
                    <div class="flex items-center justify-center gap-2">
                        <i data-lucide="award" class="w-4 h-4 text-medieval-gold"></i>
                        <span>ทัวร์ปราสาท & สปาผ่อนคลาย</span>
                    </div>
                </div>
            </div>
        </section>

        <!-- ROOM SEARCH & BOOKING BAR SECTION -->
        <section class="relative z-20 -mt-12 max-w-6xl mx-auto px-4">
            <div class="bg-medieval-card border border-medieval-gold/40 rounded-xl p-5 sm:p-7 shadow-2xl backdrop-blur-md">
                <form id="searchFilterForm" onsubmit="handleSearchRooms(event)" class="grid grid-cols-1 sm:grid-cols-2 lg:grid-cols-5 gap-4 items-end font-thaiSerif">
                    <div>
                        <label class="block font-thaiSerif text-[11px] uppercase tracking-wider text-medieval-gold mb-1.5 font-semibold">วันที่เข้าพัก (CHECK-IN)</label>
                        <div class="relative">
                            <input type="date" id="searchCheckIn" class="w-full bg-medieval-bg border border-medieval-gold/30 rounded px-3 py-2.5 text-xs text-medieval-cream focus:border-medieval-gold focus:outline-none" required>
                        </div>
                    </div>
                    <div>
                        <label class="block font-thaiSerif text-[11px] uppercase tracking-wider text-medieval-gold mb-1.5 font-semibold">วันที่ออก (CHECK-OUT)</label>
                        <div class="relative">
                            <input type="date" id="searchCheckOut" class="w-full bg-medieval-bg border border-medieval-gold/30 rounded px-3 py-2.5 text-xs text-medieval-cream focus:border-medieval-gold focus:outline-none" required>
                        </div>
                    </div>
                    <div>
                        <label class="block font-thaiSerif text-[11px] uppercase tracking-wider text-medieval-gold mb-1.5 font-semibold">จำนวนผู้เข้าพัก (GUESTS)</label>
                        <select id="searchGuests" class="w-full bg-medieval-bg border border-medieval-gold/30 rounded px-3 py-2.5 text-xs text-medieval-cream focus:border-medieval-gold focus:outline-none">
                            <option value="all">ทุกจำนวนผู้เข้าพัก</option>
                            <option value="2">2 ท่าน</option>
                            <option value="4">สูงสุด 4 ท่าน</option>
                        </select>
                    </div>
                    <div>
                        <label class="block font-thaiSerif text-[11px] uppercase tracking-wider text-medieval-gold mb-1.5 font-semibold">ประเภทห้องพัก (ROOM TYPE)</label>
                        <select id="searchRoomType" class="w-full bg-medieval-bg border border-medieval-gold/30 rounded px-3 py-2.5 text-xs text-medieval-cream focus:border-medieval-gold focus:outline-none">
                            <option value="all">ห้องพักทั้งหมด</option>
                            <option value="king">Royal King Room</option>
                            <option value="suite">Royal Suite</option>
                            <option value="crown">Crown Luxury Suite</option>
                        </select>
                    </div>
                    <div>
                        <button type="submit" class="w-full py-2.5 bg-medieval-gold hover:bg-medieval-goldLight text-medieval-bg font-thaiSerif font-bold text-xs uppercase tracking-widest rounded transition flex items-center justify-center gap-2 shadow-md">
                            <i data-lucide="search" class="w-4 h-4"></i>
                            ตรวจสอบห้องว่าง
                        </button>
                    </div>
                </form>
            </div>
        </section>

        <!-- ROOMS SECTION -->
        <section id="rooms" class="py-24 max-w-7xl mx-auto px-4 sm:px-6 lg:px-8">
            <div class="text-center max-w-3xl mx-auto mb-16">
                <span class="font-cinzel text-xs uppercase text-medieval-gold tracking-[0.3em] block mb-2 font-semibold">Accommodations & Suites</span>
                <h2 class="font-serif text-3xl sm:text-5xl font-bold text-medieval-cream mb-2">ROYAL ROOMS & SUITES</h2>
                <h3 class="font-thaiSerif text-xl sm:text-2xl text-medieval-gold mb-4">ห้องพักและห้องซูทระดับราชวงศ์</h3>
                <div class="w-20 h-0.5 bg-medieval-gold mx-auto mb-4"></div>
                <p class="font-thaiSerif text-medieval-cream/80 text-sm sm:text-base leading-relaxed">
                    สัมผัสความหรูหราอลังการสไตล์เมดิอีวัล พร้อมสิ่งอำนวยความสะดวกสมาร์ทโฮเต็ลครบครัน
                </p>
            </div>

            <!-- Rooms Grid -->
            <div id="roomsGrid" class="grid grid-cols-1 md:grid-cols-3 gap-8">
                <!-- Royal King Room -->
                <div class="room-card bg-medieval-card border border-medieval-gold/30 rounded-xl overflow-hidden hover:border-medieval-gold transition duration-300 flex flex-col group shadow-xl" data-type="king" data-guests="2">
                    <div class="relative h-64 overflow-hidden">
                        <img src="https://encrypted-tbn0.gstatic.com/images?q=tbn:ANd9GcSTjI4SW_KuGN4QB73RMks1v0HN5-u82Byzb1XhFx7gLA&s=10" 
                             alt="Royal King Room" 
                             class="w-full h-full object-cover group-hover:scale-105 transition duration-700">
                        <div class="absolute top-3 right-3 bg-medieval-bg/90 backdrop-blur-md px-3 py-1 rounded border border-medieval-gold/50">
                            <span class="font-thaiSerif text-[11px] text-medieval-gold font-semibold uppercase tracking-wider">AVAILABLE (ว่าง)</span>
                        </div>
                    </div>
                    <div class="p-6 flex-grow flex flex-col justify-between font-thaiSerif">
                        <div>
                            <div class="flex justify-between items-start mb-2">
                                <h3 class="font-serif font-bold text-xl text-medieval-gold tracking-wide">ROYAL KING ROOM</h3>
                                <span class="font-serif text-xl font-bold text-medieval-cream">฿4,500 <span class="text-xs font-normal text-medieval-cream/60">/คืน</span></span>
                            </div>
                            <p class="text-xs text-medieval-cream/75 mb-4 leading-relaxed">
                                ห้องพักคลาสสิกตกแต่งด้วยงานไม้สัก เตาผิงหินแท้ และหน้าต่างชมวิวสวนปราสาทอังกฤษ
                            </p>
                            <ul class="text-xs text-medieval-cream/85 space-y-2 mb-6 border-y border-medieval-gold/15 py-4">
                                <li class="flex items-center gap-2.5"><i data-lucide="bed" class="w-4 h-4 text-medieval-gold"></i> เตียงคิงไซส์ (1 King Bed)</li>
                                <li class="flex items-center gap-2.5"><i data-lucide="users" class="w-4 h-4 text-medieval-gold"></i> รองรับผู้เข้าพัก 2 ท่าน</li>
                                <li class="flex items-center gap-2.5"><i data-lucide="castle" class="w-4 h-4 text-medieval-gold"></i> วิวทิวทัศน์ปราสาท (Castle View)</li>
                                <li class="flex items-center gap-2.5"><i data-lucide="wifi" class="w-4 h-4 text-medieval-gold"></i> ระบบ Smart Control & High-Speed Wi-Fi</li>
                            </ul>
                        </div>
                        <button onclick="openBookingModal('ROYAL KING ROOM', 4500)" class="w-full py-3 rounded bg-medieval-crimson hover:bg-medieval-crimsonHover text-medieval-cream font-thaiSerif font-semibold text-xs tracking-[0.15em] uppercase transition border border-medieval-gold/30">
                            จองห้องพักนี้ (RESERVE)
                        </button>
                    </div>
                </div>

                <!-- Royal Suite -->
                <div class="room-card bg-medieval-card border border-medieval-gold/30 rounded-xl overflow-hidden hover:border-medieval-gold transition duration-300 flex flex-col group shadow-xl" data-type="suite" data-guests="4">
                    <div class="relative h-64 overflow-hidden">
                        <img src="https://q-xx.bstatic.com/xdata/images/hotel/max500/647612469.jpg?k=7b57d2b8f16f42fd90f80a83ce1e995a4448ce240ae7794c54ea24ecbaf2e231&o=" 
                             alt="Royal Suite" 
                             class="w-full h-full object-cover group-hover:scale-105 transition duration-700">
                        <div class="absolute top-3 right-3 bg-medieval-bg/90 backdrop-blur-md px-3 py-1 rounded border border-medieval-gold/50">
                            <span class="font-thaiSerif text-[11px] text-amber-400 font-semibold uppercase tracking-wider">ALMOST FULL (เหลือน้อย)</span>
                        </div>
                    </div>
                    <div class="p-6 flex-grow flex flex-col justify-between font-thaiSerif">
                        <div>
                            <div class="flex justify-between items-start mb-2">
                                <h3 class="font-serif font-bold text-xl text-medieval-gold tracking-wide">ROYAL SUITE</h3>
                                <span class="font-serif text-xl font-bold text-medieval-cream">฿7,500 <span class="text-xs font-normal text-medieval-cream/60">/คืน</span></span>
                            </div>
                            <p class="text-xs text-medieval-cream/75 mb-4 leading-relaxed">
                                ห้องซูทสุดหรูพร้อมห้องนั่งเล่นแยกส่วน โคมไฟระย้าคริสตัล และบริการพ่อบ้านส่วนตัว
                            </p>
                            <ul class="text-xs text-medieval-cream/85 space-y-2 mb-6 border-y border-medieval-gold/15 py-4">
                                <li class="flex items-center gap-2.5"><i data-lucide="bed" class="w-4 h-4 text-medieval-gold"></i> เตียงคิงไซส์ (1 King Bed)</li>
                                <li class="flex items-center gap-2.5"><i data-lucide="users" class="w-4 h-4 text-medieval-gold"></i> รองรับผู้เข้าพัก 2 - 4 ท่าน</li>
                                <li class="flex items-center gap-2.5"><i data-lucide="armchair" class="w-4 h-4 text-medieval-gold"></i> ห้องนั่งเล่นส่วนตัว & เตาผิง</li>
                                <li class="flex items-center gap-2.5"><i data-lucide="coffee" class="w-4 h-4 text-medieval-gold"></i> ฟรีอาหารเช้าสไตล์ราชวงศ์</li>
                            </ul>
                        </div>
                        <button onclick="openBookingModal('ROYAL SUITE', 7500)" class="w-full py-3 rounded bg-medieval-crimson hover:bg-medieval-crimsonHover text-medieval-cream font-thaiSerif font-semibold text-xs tracking-[0.15em] uppercase transition border border-medieval-gold/30">
                            จองห้องซูทนี้ (RESERVE)
                        </button>
                    </div>
                </div>

                <!-- Crown Luxury Suite -->
                <div class="room-card bg-medieval-card border-2 border-medieval-gold/60 rounded-xl overflow-hidden hover:border-medieval-gold transition duration-300 flex flex-col group shadow-2xl relative" data-type="crown" data-guests="4">
                    <div class="absolute top-0 left-0 bg-medieval-gold text-medieval-bg text-[9px] font-thaiSerif font-bold px-3 py-1 uppercase rounded-br tracking-wider">
                        ห้องพักระดับสูงสุด (MOST PRESTIGIOUS)
                    </div>
                    <div class="relative h-64 overflow-hidden">
                        <img src="https://cf.bstatic.com/xdata/images/hotel/max1024x768/647621410.jpg?k=e8882f652631b5404ac3a64045ba1b69d2bca7fee9b616273e7f9abbf6243af4&o=" 
                             alt="Crown Luxury Suite" 
                             class="w-full h-full object-cover group-hover:scale-105 transition duration-700">
                        <div class="absolute top-3 right-3 bg-medieval-bg/90 backdrop-blur-md px-3 py-1 rounded border border-medieval-gold/50">
                            <span class="font-thaiSerif text-[11px] text-medieval-gold font-semibold uppercase tracking-wider">LIMITED (จำกัด)</span>
                        </div>
                    </div>
                    <div class="p-6 flex-grow flex flex-col justify-between font-thaiSerif">
                        <div>
                            <div class="flex justify-between items-start mb-2">
                                <h3 class="font-serif font-bold text-xl text-medieval-gold tracking-wide">CROWN LUXURY SUITE</h3>
                                <span class="font-serif text-xl font-bold text-medieval-cream">฿12,000 <span class="text-xs font-normal text-medieval-cream/60">/คืน</span></span>
                            </div>
                            <p class="text-xs text-medieval-cream/75 mb-4 leading-relaxed">
                                ที่สุดแห่งความหรูหรา มาพร้อมห้องรับประทานอาหารส่วนตัว และบริการผู้ช่วย AI VIP 24 ชม.
                            </p>
                            <ul class="text-xs text-medieval-cream/85 space-y-2 mb-6 border-y border-medieval-gold/15 py-4">
                                <li class="flex items-center gap-2.5"><i data-lucide="crown" class="w-4 h-4 text-medieval-gold"></i> เตียงมาสเตอร์คิงไซส์</li>
                                <li class="flex items-center gap-2.5"><i data-lucide="users" class="w-4 h-4 text-medieval-gold"></i> รองรับผู้เข้าพัก 2 - 4 ท่าน</li>
                                <li class="flex items-center gap-2.5"><i data-lucide="utensils-crossed" class="w-4 h-4 text-medieval-gold"></i> ห้องรับประทานอาหาร & มินิบาร์ส่วนตัว</li>
                                <li class="flex items-center gap-2.5"><i data-lucide="sparkles" class="w-4 h-4 text-medieval-gold"></i> วิวปราสาทพาโนรามา & ระบบควบคุมอัจฉริยะ</li>
                            </ul>
                        </div>
                        <button onclick="openBookingModal('CROWN LUXURY SUITE', 12000)" class="w-full py-3 rounded bg-medieval-gold hover:bg-medieval-goldLight text-medieval-bg font-thaiSerif font-bold text-xs tracking-[0.15em] uppercase transition shadow-lg">
                            จองห้องพักสุดหรู (RESERVE)
                        </button>
                    </div>
                </div>
            </div>
        </section>

        <!-- AI ROYAL CONCIERGE CHATBOT SECTION -->
        <section id="concierge" class="py-24 bg-medieval-card/60 border-y border-medieval-gold/20 relative bg-castle-pattern">
            <div class="max-w-6xl mx-auto px-4 sm:px-6 lg:px-8">
                <div class="text-center max-w-2xl mx-auto mb-12">
                    <div class="inline-flex items-center gap-2 px-4 py-1.5 rounded-full bg-medieval-card border border-medieval-gold/40 text-medieval-gold text-xs font-thaiSerif mb-3 tracking-wider uppercase">
                        <i data-lucide="bot" class="w-4 h-4"></i> ระบบผู้ช่วยอัจฉริยะ (AI CONCIERGE)
                    </div>
                    <h2 class="font-serif text-3xl sm:text-5xl font-bold text-medieval-gold mb-1">MEET YOUR ROYAL CONCIERGE</h2>
                    <h3 class="font-thaiSerif text-xl text-medieval-cream mb-2">ผู้ช่วย AI พร้อมให้บริการตลอด 24 ชั่วโมง</h3>
                    <p class="text-xs text-medieval-cream/70 font-thaiSerif tracking-wider">สอบถามราคาห้องพัก เวลาเช็คอิน/เช็คเอาต์ เมนูอาหาร หรือคำแนะนำด้วยภาษาธรรมชาติ</p>
                </div>

                <!-- Chatbot Interface Container -->
                <div class="max-w-4xl mx-auto bg-medieval-bg border-2 border-medieval-gold/50 rounded-xl overflow-hidden shadow-2xl flex flex-col h-[540px]">
                    <!-- Chat Header -->
                    <div class="bg-medieval-card px-6 py-4 border-b border-medieval-gold/30 flex items-center justify-between">
                        <div class="flex items-center gap-3.5">
                            <div class="w-10 h-10 rounded-full border border-medieval-gold bg-medieval-bg flex items-center justify-center text-medieval-gold">
                                <i data-lucide="crown" class="w-5 h-5"></i>
                            </div>
                            <div>
                                <h3 class="font-serif font-bold text-base text-medieval-cream tracking-wide">Sir AI - Royal Concierge</h3>
                                <span class="text-[10px] text-emerald-400 flex items-center gap-1 font-thaiSerif">
                                    <span class="w-1.5 h-1.5 rounded-full bg-emerald-400 inline-block animate-pulse"></span> ออนไลน์พร้อมตอบคำถาม (Online)
                                </span>
                            </div>
                        </div>
                        <span class="text-xs font-thaiSerif text-medieval-gold/70 hidden sm:inline tracking-wider">ระบบประมวลผลภาษาธรรมชาติ</span>
                    </div>

                    <!-- Chat Messages Stream -->
                    <div id="chatStream" class="flex-grow p-6 overflow-y-auto space-y-4 font-thaiSerif text-xs">
                        <!-- AI Greeting Message -->
                        <div class="flex gap-3 max-w-[85%]">
                            <div class="w-8 h-8 rounded-full bg-medieval-gold/20 border border-medieval-gold shrink-0 flex items-center justify-center text-medieval-gold">
                                <i data-lucide="bot" class="w-4 h-4"></i>
                            </div>
                            <div class="bg-medieval-card border border-medieval-gold/30 p-4 rounded-2xl rounded-tl-none text-medieval-cream space-y-2">
                                <p class="font-serif text-medieval-gold text-sm font-semibold tracking-wide">ยินดีต้อนรับท่านผู้ทรงเกียรติ!</p>
                                <p class="leading-relaxed">กระผมคือ Sir AI ผู้ช่วยส่วนตัวประจำโรงแรม เดอะ รอยัล คราวน์ อินน์ ท่านสามารถสอบถามราคาห้องพัก เวลา Check-in/Check-out แนะนำห้องพัก หรือบริการสปาได้ทันทีครับ</p>
                                <p class="text-[11px] text-medieval-cream/60">คลิกที่ปุ่มคำถามด่วนด้านล่าง หรือพิมพ์คำถามของท่านได้เลยครับ</p>
                            </div>
                        </div>
                    </div>

                    <!-- Quick Prompt Actions in Thai -->
                    <div class="px-6 py-2.5 bg-medieval-card/40 border-t border-medieval-gold/10 flex items-center gap-2 overflow-x-auto whitespace-nowrap scrollbar-none text-[11px] font-thaiSerif">
                        <span class="text-medieval-gold font-semibold uppercase tracking-wider text-[10px]">คำถามด่วน:</span>
                        <button onclick="sendQuickPrompt('มีห้องพักประเภทไหนบ้าง?')" class="px-3 py-1 bg-medieval-bg border border-medieval-gold/30 hover:border-medieval-gold text-medieval-cream rounded-full transition">มีห้องพักประเภทไหนบ้าง?</button>
                        <button onclick="sendQuickPrompt('แนะนำห้องพักสำหรับ 4 ท่าน')" class="px-3 py-1 bg-medieval-bg border border-medieval-gold/30 hover:border-medieval-gold text-medieval-cream rounded-full transition">แนะนำห้องพักสำหรับ 4 ท่าน</button>
                        <button onclick="sendQuickPrompt('ข้อมูลห้องอาหารและเวลาเช็คอิน')" class="px-3 py-1 bg-medieval-bg border border-medieval-gold/30 hover:border-medieval-gold text-medieval-cream rounded-full transition">ข้อมูลห้องอาหาร & เวลาเช็คอิน</button>
                        <button onclick="sendQuickPrompt('บริการพิเศษของโรงแรม')" class="px-3 py-1 bg-medieval-bg border border-medieval-gold/30 hover:border-medieval-gold text-medieval-cream rounded-full transition">บริการพิเศษของโรงแรม</button>
                    </div>

                    <!-- Chat Input Box -->
                    <form onsubmit="handleChatSubmit(event)" class="p-4 bg-medieval-card border-t border-medieval-gold/30 flex gap-2 font-thaiSerif">
                        <input type="text" id="chatInput" placeholder="พิมพ์คำถามเกี่ยวกับห้องพัก, โปรโมชั่น, หรือการบริการ..." 
                               class="flex-grow bg-medieval-bg border border-medieval-gold/30 rounded-lg px-4 py-2.5 text-xs text-medieval-cream focus:border-medieval-gold focus:outline-none placeholder-medieval-cream/40">
                        <button type="submit" class="px-5 py-2.5 bg-medieval-gold hover:bg-medieval-goldLight text-medieval-bg font-thaiSerif font-bold text-xs uppercase tracking-wider rounded-lg transition flex items-center gap-2">
                            <span>ส่งข้อความ</span>
                            <i data-lucide="send" class="w-3.5 h-3.5"></i>
                        </button>
                    </form>
                </div>
            </div>
        </section>

        <!-- RESTAURANT & SERVICES SHOWCASE -->
        <section id="dining" class="py-24 max-w-7xl mx-auto px-4 sm:px-6 lg:px-8">
            <div class="text-center max-w-3xl mx-auto mb-14">
                <span class="font-cinzel text-xs uppercase text-medieval-gold tracking-[0.3em] block mb-2 font-semibold">Royal Experience</span>
                <h2 class="font-serif text-3xl sm:text-5xl font-bold text-medieval-cream mb-2">RESTAURANT & SERVICES</h2>
                <h3 class="font-thaiSerif text-xl sm:text-2xl text-medieval-gold">ห้องอาหารและบริการระดับราชวงศ์</h3>
                <div class="w-20 h-0.5 bg-medieval-gold mx-auto mt-4"></div>
            </div>

            <!-- Category Navigation Tabs -->
            <div class="flex justify-center gap-2 sm:gap-6 mb-12 overflow-x-auto pb-2 border-b border-medieval-gold/20 font-thaiSerif text-xs tracking-wider uppercase">
                <button onclick="switchServiceTab('diningTab')" id="tabBtn-diningTab" class="service-tab-btn px-4 py-2.5 text-medieval-gold border-b-2 border-medieval-gold font-bold transition">ห้องอาหารและงานเลี้ยง</button>
                <button onclick="switchServiceTab('spaTab')" id="tabBtn-spaTab" class="service-tab-btn px-4 py-2.5 text-medieval-cream/60 hover:text-medieval-gold border-b-2 border-transparent transition">สปาและการผ่อนคลาย</button>
                <button onclick="switchServiceTab('toursTab')" id="tabBtn-toursTab" class="service-tab-btn px-4 py-2.5 text-medieval-cream/60 hover:text-medieval-gold border-b-2 border-transparent transition">ทัวร์ปราสาท & รถรับส่ง</button>
            </div>

            <!-- Tab 1: Royal Dining -->
            <div id="diningTab" class="service-tab-content grid grid-cols-1 md:grid-cols-2 lg:grid-cols-4 gap-6 font-thaiSerif">
                <div class="bg-medieval-card border border-medieval-gold/20 rounded-xl p-6 hover:border-medieval-gold transition">
                    <div class="w-10 h-10 rounded bg-medieval-bg border border-medieval-gold/40 flex items-center justify-center text-medieval-gold mb-4">
                        <i data-lucide="coffee" class="w-5 h-5"></i>
                    </div>
                    <h4 class="font-serif font-bold text-medieval-gold text-lg mb-2">ROYAL BREAKFAST</h4>
                    <p class="text-xs text-medieval-cream/70 mb-4 leading-relaxed">อาหารเช้าสไตล์อังกฤษ ขนมปังอบสดใหม่ เนยสด ชีสบ่ม และชาสมุนไพร</p>
                    <span class="text-[11px] text-medieval-gold font-thaiSerif">เปิดบริการ 06:30 - 10:30 น.</span>
                </div>

                <div class="bg-medieval-card border border-medieval-gold/20 rounded-xl p-6 hover:border-medieval-gold transition">
                    <div class="w-10 h-10 rounded bg-medieval-bg border border-medieval-gold/40 flex items-center justify-center text-medieval-gold mb-4">
                        <i data-lucide="utensils" class="w-5 h-5"></i>
                    </div>
                    <h4 class="font-serif font-bold text-medieval-gold text-lg mb-2">MAIN COURSE FEAST</h4>
                    <p class="text-xs text-medieval-cream/70 mb-4 leading-relaxed">สำรับอาหารค่ำสไตล์ยุคกลาง สเต๊กเนื้อพรีเมียม และไวน์สูตรดั้งเดิม</p>
                    <span class="text-[11px] text-medieval-gold font-thaiSerif">บริการอาหารค่ำทุกวัน</span>
                </div>

                <div class="bg-medieval-card border border-medieval-gold/20 rounded-xl p-6 hover:border-medieval-gold transition">
                    <div class="w-10 h-10 rounded bg-medieval-bg border border-medieval-gold/40 flex items-center justify-center text-medieval-gold mb-4">
                        <i data-lucide="cake" class="w-5 h-5"></i>
                    </div>
                    <h4 class="font-serif font-bold text-medieval-gold text-lg mb-2">AFTERNOON HIGH TEA</h4>
                    <p class="text-xs text-medieval-cream/70 mb-4 leading-relaxed">ชุดชาบ่ายสไตล์อังกฤษ เสิร์ฟพร้อมสคอนส์ ครีมสด และขนมหวานสุดปราณีต</p>
                    <span class="text-[11px] text-medieval-gold font-thaiSerif">บริการ 14:00 - 17:00 น.</span>
                </div>

                <div class="bg-medieval-card border border-medieval-gold/20 rounded-xl p-6 hover:border-medieval-gold transition">
                    <div class="w-10 h-10 rounded bg-medieval-bg border border-medieval-gold/40 flex items-center justify-center text-medieval-gold mb-4">
                        <i data-lucide="concierge-bell" class="w-5 h-5"></i>
                    </div>
                    <h4 class="font-serif font-bold text-medieval-gold text-lg mb-2">ROOM SERVICE 24/7</h4>
                    <p class="text-xs text-medieval-cream/70 mb-4 leading-relaxed">บริการส่งอาหารและเครื่องดื่มถึงห้องพักผ่านระบบ Smart Control ได้ตลอดเวลา</p>
                    <span class="text-[11px] text-medieval-gold font-thaiSerif">ให้บริการ 24 ชั่วโมง</span>
                </div>
            </div>

            <!-- Tab 2: Spa -->
            <div id="spaTab" class="service-tab-content hidden grid grid-cols-1 md:grid-cols-3 gap-6 font-thaiSerif">
                <div class="bg-medieval-card border border-medieval-gold/20 rounded-xl p-6 hover:border-medieval-gold transition">
                    <div class="w-10 h-10 rounded bg-medieval-bg border border-medieval-gold/40 flex items-center justify-center text-medieval-gold mb-4">
                        <i data-lucide="sparkles" class="w-5 h-5"></i>
                    </div>
                    <h4 class="font-serif font-bold text-medieval-gold text-lg mb-2">ROYAL THERMAL SPA</h4>
                    <p class="text-xs text-medieval-cream/70 leading-relaxed">บ่อน้ำแร่ร้อนธรรมชาติและห้องซาวน่าหินเกลือเพื่อการผ่อนคลายขั้นสุด</p>
                </div>
                <div class="bg-medieval-card border border-medieval-gold/20 rounded-xl p-6 hover:border-medieval-gold transition">
                    <div class="w-10 h-10 rounded bg-medieval-bg border border-medieval-gold/40 flex items-center justify-center text-medieval-gold mb-4">
                        <i data-lucide="heart-pulse" class="w-5 h-5"></i>
                    </div>
                    <h4 class="font-serif font-bold text-medieval-gold text-lg mb-2">DEEP TISSUE MASSAGE</h4>
                    <p class="text-xs text-medieval-cream/70 leading-relaxed">บริการนวดน้ำมันอโรมาและนวดผ่อนคลายกล้ามเนื้อโดยเทอราปิสต์ผู้เชี่ยวชาญ</p>
                </div>
                <div class="bg-medieval-card border border-medieval-gold/20 rounded-xl p-6 hover:border-medieval-gold transition">
                    <div class="w-10 h-10 rounded bg-medieval-bg border border-medieval-gold/40 flex items-center justify-center text-medieval-gold mb-4">
                        <i data-lucide="sun" class="w-5 h-5"></i>
                    </div>
                    <h4 class="font-serif font-bold text-medieval-gold text-lg mb-2">HOT STONE THERAPY</h4>
                    <p class="text-xs text-medieval-cream/70 leading-relaxed">ทรีตเมนต์นวดประคบหินภูเขาไฟอุ่น บรรเทาความล้าและบำรุงผิวพรรณ</p>
                </div>
            </div>

            <!-- Tab 3: Tours & Transfers -->
            <div id="toursTab" class="service-tab-content hidden grid grid-cols-1 md:grid-cols-3 gap-6 font-thaiSerif">
                <div class="bg-medieval-card border border-medieval-gold/20 rounded-xl p-6 hover:border-medieval-gold transition">
                    <div class="w-10 h-10 rounded bg-medieval-bg border border-medieval-gold/40 flex items-center justify-center text-medieval-gold mb-4">
                        <i data-lucide="car" class="w-5 h-5"></i>
                    </div>
                    <h4 class="font-serif font-bold text-medieval-gold text-lg mb-2">ROYAL TRANSFER</h4>
                    <p class="text-xs text-medieval-cream/70 leading-relaxed">บริการรถรับ-ส่งสนามบินระดับ VIP ด้วยรถหรูส่วนตัวพร้อมคนขับ</p>
                </div>
                <div class="bg-medieval-card border border-medieval-gold/20 rounded-xl p-6 hover:border-medieval-gold transition">
                    <div class="w-10 h-10 rounded bg-medieval-bg border border-medieval-gold/40 flex items-center justify-center text-medieval-gold mb-4">
                        <i data-lucide="compass" class="w-5 h-5"></i>
                    </div>
                    <h4 class="font-serif font-bold text-medieval-gold text-lg mb-2">GUIDED CASTLE TOUR</h4>
                    <p class="text-xs text-medieval-cream/70 leading-relaxed">กิจกรรมทัวร์ชมประวัติศาสตร์ สถาปัตยกรรมปราสาท และห้องคลังอาวุธยุคกลาง</p>
                </div>
                <div class="bg-medieval-card border border-medieval-gold/20 rounded-xl p-6 hover:border-medieval-gold transition">
                    <div class="w-10 h-10 rounded bg-medieval-bg border border-medieval-gold/40 flex items-center justify-center text-medieval-gold mb-4">
                        <i data-lucide="shield" class="w-5 h-5"></i>
                    </div>
                    <h4 class="font-serif font-bold text-medieval-gold text-lg mb-2">MEDIEVAL ACTIVITIES</h4>
                    <p class="text-xs text-medieval-cream/70 leading-relaxed">กิจกรรมยิงธนูและนกเหยี่ยวในลานปราสาทดั้งเดิม พร้อมครูฝึกดูแล</p>
                </div>
            </div>
        </section>

        <!-- SMART HOTEL SYSTEM FEATURES OVERVIEW -->
        <section class="py-20 bg-medieval-card border-y border-medieval-gold/30">
            <div class="max-w-7xl mx-auto px-4 sm:px-6 lg:px-8">
                <div class="text-center mb-14">
                    <span class="font-cinzel text-xs uppercase text-medieval-gold tracking-[0.25em] block mb-1 font-semibold">INTEGRATED INFORMATION SYSTEM</span>
                    <h2 class="font-serif text-3xl sm:text-4xl font-bold text-medieval-cream">SMART HOTEL SYSTEM</h2>
                    <h3 class="font-thaiSerif text-lg text-medieval-gold mt-1">เทคโนโลยีอัจฉริยะที่ช่วยให้การเข้าพักสะดวกยิ่งขึ้น</h3>
                </div>

                <div class="grid grid-cols-1 sm:grid-cols-2 lg:grid-cols-4 gap-6 font-thaiSerif">
                    <div class="p-6 bg-medieval-bg border border-medieval-gold/30 rounded-xl text-center">
                        <i data-lucide="calendar-check" class="w-8 h-8 text-medieval-gold mx-auto mb-3"></i>
                        <h4 class="font-serif font-bold text-lg text-medieval-gold mb-1">SMART BOOKING</h4>
                        <p class="text-xs text-medieval-cream/70 leading-relaxed">ระบบจองห้องพักออนไลน์ ตรวจสอบห้องว่างเรียลไทม์ และยืนยันผ่าน QR Code</p>
                    </div>
                    <div class="p-6 bg-medieval-bg border border-medieval-gold/30 rounded-xl text-center">
                        <i data-lucide="bot" class="w-8 h-8 text-medieval-gold mx-auto mb-3"></i>
                        <h4 class="font-serif font-bold text-lg text-medieval-gold mb-1">AI CONCIERGE</h4>
                        <p class="text-xs text-medieval-cream/70 leading-relaxed">AI ตอบคำถาม แนะนำห้องพัก และช่วยลดภาระงานซ้ำซ้อนของพนักงาน</p>
                    </div>
                    <div class="p-6 bg-medieval-bg border border-medieval-gold/30 rounded-xl text-center">
                        <i data-lucide="bar-chart-3" class="w-8 h-8 text-medieval-gold mx-auto mb-3"></i>
                        <h4 class="font-serif font-bold text-lg text-medieval-gold mb-1">SMART ANALYTICS</h4>
                        <p class="text-xs text-medieval-cream/70 leading-relaxed">ระบบวิเคราะห์ข้อมูลยอดการจองและอัตราการเข้าพักเพื่อผู้บริหาร</p>
                    </div>
                    <div class="p-6 bg-medieval-bg border border-medieval-gold/30 rounded-xl text-center">
                        <i data-lucide="lock" class="w-8 h-8 text-medieval-gold mx-auto mb-3"></i>
                        <h4 class="font-serif font-bold text-lg text-medieval-gold mb-1">SECURE DATA</h4>
                        <p class="text-xs text-medieval-cream/70 leading-relaxed">จัดเก็บข้อมูลการจองและประวัติสมาชิกอย่างปลอดภัยตามมาตรฐาน</p>
                    </div>
                </div>
            </div>
        </section>

        <!-- PROMOTIONS & MEMBER SYSTEM -->
        <section id="promotions" class="py-24 max-w-7xl mx-auto px-4 sm:px-6 lg:px-8 font-thaiSerif">
            <div class="grid grid-cols-1 lg:grid-cols-2 gap-12 items-start">
                
                <!-- Promotions Column -->
                <div>
                    <div class="mb-8">
                        <span class="font-cinzel text-xs uppercase text-medieval-gold tracking-[0.25em] block mb-1 font-semibold">Special Promotions</span>
                        <h2 class="font-serif text-3xl sm:text-4xl font-bold text-medieval-cream">PROMOTIONS & OFFERS</h2>
                        <h3 class="font-thaiSerif text-xl text-medieval-gold mt-1">โปรโมชั่นและข้อเสนอพิเศษ</h3>
                        <div class="w-16 h-0.5 bg-medieval-gold mt-3"></div>
                    </div>

                    <div class="space-y-6">
                        <!-- Promo 1 -->
                        <div class="bg-medieval-card border-2 border-medieval-gold/40 rounded-xl p-6 relative overflow-hidden flex flex-col sm:flex-row justify-between items-start sm:items-center gap-4">
                            <div>
                                <span class="bg-medieval-crimson text-medieval-cream font-thaiSerif text-[10px] font-bold px-2.5 py-0.5 rounded border border-medieval-gold/40 mb-2 inline-block tracking-wider">ส่วนลด 20% สำหรับสมาชิกใหม่</span>
                                <h3 class="font-serif font-bold text-xl text-medieval-gold">NEW MEMBER SPECIAL</h3>
                                <p class="text-xs text-medieval-cream/70 mt-1">รับส่วนลดทันที 20% เมื่อสมัครสมาชิกและทำการจองห้องพักครั้งแรก</p>
                                <div class="mt-3 text-xs text-medieval-cream/80 font-mono">PROMO CODE: <strong class="text-medieval-gold bg-medieval-bg px-2 py-0.5 rounded border border-medieval-gold/30">NEWMEMBER</strong></div>
                            </div>
                            <button onclick="applyPromoCode('NEWMEMBER', 20)" class="px-4 py-2 bg-medieval-gold hover:bg-medieval-goldLight text-medieval-bg font-thaiSerif font-bold text-xs uppercase tracking-wider rounded shrink-0">
                                ใช้ส่วนลดนี้
                            </button>
                        </div>

                        <!-- Promo 2 -->
                        <div class="bg-medieval-card border border-medieval-gold/30 rounded-xl p-6 flex flex-col sm:flex-row justify-between items-start sm:items-center gap-4">
                            <div>
                                <span class="bg-medieval-surface text-medieval-gold font-thaiSerif text-[10px] font-bold px-2.5 py-0.5 rounded border border-medieval-gold/40 mb-2 inline-block tracking-wider">ส่วนลด 15% วันธรรมดา</span>
                                <h3 class="font-serif font-bold text-xl text-medieval-gold">WEEKDAY SPECIAL</h3>
                                <p class="text-xs text-medieval-cream/70 mt-1">ส่วนลดพิเศษ 15% สำหรับการเข้าพักในวันจันทร์ - พฤหัสบดี</p>
                                <div class="mt-3 text-xs text-medieval-cream/80 font-mono">PROMO CODE: <strong class="text-medieval-gold bg-medieval-bg px-2 py-0.5 rounded border border-medieval-gold/30">WEEKDAY15</strong></div>
                            </div>
                            <button onclick="applyPromoCode('WEEKDAY15', 15)" class="px-4 py-2 bg-medieval-card hover:bg-medieval-surface text-medieval-gold border border-medieval-gold/50 font-thaiSerif font-bold text-xs uppercase tracking-wider rounded shrink-0">
                                ใช้ส่วนลดนี้
                            </button>
                        </div>
                    </div>
                </div>

                <!-- Loyalty Member Hub Column -->
                <div id="membership" class="bg-medieval-card border-2 border-medieval-gold/40 rounded-xl p-6 sm:p-8 shadow-2xl">
                    <div class="flex items-center justify-between mb-6 pb-4 border-b border-medieval-gold/20">
                        <div>
                            <span class="font-cinzel text-xs text-medieval-gold uppercase tracking-[0.2em] block font-semibold">Loyalty Program</span>
                            <h3 class="font-serif font-bold text-2xl text-medieval-cream">MEMBER & LOYALTY POINTS</h3>
                            <h4 class="font-thaiSerif text-sm text-medieval-gold">ระบบสมาชิกและคะแนนสะสม</h4>
                        </div>
                        <div class="w-12 h-12 rounded-full bg-medieval-gold/10 border border-medieval-gold flex items-center justify-center text-medieval-gold">
                            <i data-lucide="shield" class="w-6 h-6"></i>
                        </div>
                    </div>

                    <!-- Member Profile Card -->
                    <div class="bg-medieval-bg border border-medieval-gold/30 rounded-lg p-5 mb-6">
                        <div class="flex justify-between items-center mb-3">
                            <div class="flex items-center gap-3">
                                <div class="w-10 h-10 rounded-full bg-medieval-crimson text-medieval-gold border border-medieval-gold font-serif font-bold flex items-center justify-center text-sm">
                                    HR
                                </div>
                                <div>
                                    <h4 class="font-serif font-bold text-base text-medieval-cream" id="memberNameDisplay">คุณสมชาย วงศ์เทวา (Member)</h4>
                                    <span class="text-[10px] text-medieval-gold font-thaiSerif tracking-wider">สถานะ: Gold VIP Member</span>
                                </div>
                            </div>
                            <span class="text-xs text-medieval-cream/60 font-mono">ID: #RC-88421</span>
                        </div>

                        <div class="mt-4 pt-3 border-t border-medieval-gold/10 flex justify-between items-center">
                            <div>
                                <span class="text-[10px] text-medieval-cream/60 uppercase tracking-wider block">คะแนนสะสมปัจจุบัน (Loyalty Points)</span>
                                <span class="font-serif text-3xl font-bold text-medieval-gold" id="userPointsDisplay">450 <span class="text-xs font-normal text-medieval-cream/70 font-sans">คะแนน</span></span>
                            </div>
                            <span class="text-[10px] text-medieval-cream/60 text-right">เกณฑ์สะสมคะแนน:<br><strong class="text-medieval-gold">ทุก 100 บาท = 1 Point</strong></span>
                        </div>
                    </div>

                    <!-- Redeem Rewards Simulator -->
                    <h4 class="font-thaiSerif font-semibold text-xs text-medieval-gold mb-3 uppercase tracking-wider">สิทธิพิเศษที่สามารถใช้คะแนนแลก:</h4>
                    <div class="space-y-3">
                        <div class="flex justify-between items-center p-3 bg-medieval-bg/60 border border-medieval-gold/20 rounded text-xs">
                            <div>
                                <strong class="text-medieval-cream block font-serif">แลกฟรี! อาหารเช้าสไตล์ราชวงศ์</strong>
                                <span class="text-[10px] text-medieval-cream/60">ใช้ 100 คะแนน</span>
                            </div>
                            <button onclick="redeemReward('อาหารเช้าฟรี', 100)" class="px-3 py-1 bg-medieval-crimson hover:bg-medieval-crimsonHover text-medieval-cream font-thaiSerif font-bold text-[11px] uppercase tracking-wider rounded border border-medieval-gold/30">
                                แลกคะแนน
                            </button>
                        </div>
                        <div class="flex justify-between items-center p-3 bg-medieval-bg/60 border border-medieval-gold/20 rounded text-xs">
                            <div>
                                <strong class="text-medieval-cream block font-serif">แลกฟรี! บัตรเข้าใช้สปาน้ำแร่ร้อน</strong>
                                <span class="text-[10px] text-medieval-cream/60">ใช้ 250 คะแนน</span>
                            </div>
                            <button onclick="redeemReward('สปาน้ำแร่ร้อนฟรี', 250)" class="px-3 py-1 bg-medieval-crimson hover:bg-medieval-crimsonHover text-medieval-cream font-thaiSerif font-bold text-[11px] uppercase tracking-wider rounded border border-medieval-gold/30">
                                แลกคะแนน
                            </button>
                        </div>
                    </div>
                </div>

            </div>
        </section>
    </div>

    <!-- EXECUTIVE ADMIN DASHBOARD VIEW -->
    <div id="adminPortalView" class="hidden flex-grow bg-medieval-bg py-8 px-4 sm:px-6 lg:px-8 max-w-7xl mx-auto w-full font-thaiSerif">
        <!-- Admin Banner Header -->
        <div class="flex flex-col md:flex-row md:items-center justify-between gap-4 bg-medieval-card border-2 border-medieval-gold/50 rounded-xl p-6 mb-8 shadow-2xl">
            <div>
                <div class="flex items-center gap-2">
                    <i data-lucide="shield-check" class="w-6 h-6 text-medieval-gold"></i>
                    <h2 class="font-serif text-2xl sm:text-3xl font-bold text-medieval-gold tracking-wide">ADMIN DASHBOARD</h2>
                </div>
                <p class="text-xs text-medieval-cream/70 tracking-wider mt-1">ระบบสารสนเทศเพื่อการจัดการและวิเคราะห์ข้อมูลโรงแรม (Hotel Information System)</p>
            </div>
            <div class="flex items-center gap-3">
                <span class="text-xs text-medieval-cream/60">ผู้ดูแลระบบ: <strong class="text-medieval-gold font-serif">Hotel Admin Manager</strong></span>
                <button onclick="toggleAdminMode()" class="px-4 py-2 bg-medieval-crimson hover:bg-medieval-crimsonHover text-medieval-cream text-xs font-thaiSerif font-bold uppercase tracking-wider rounded border border-medieval-gold/40">
                    กลับสู่หน้าเว็บไซต์หลัก
                </button>
            </div>
        </div>

        <!-- 4 Top KPI Cards -->
        <div class="grid grid-cols-1 sm:grid-cols-2 lg:grid-cols-4 gap-6 mb-8">
            <div class="bg-medieval-card border border-medieval-gold/30 rounded-xl p-5 shadow-lg">
                <div class="flex justify-between items-center mb-2">
                    <span class="text-xs text-medieval-cream/70 uppercase tracking-wider">ห้องพักทั้งหมด (TOTAL ROOMS)</span>
                    <i data-lucide="building-2" class="w-5 h-5 text-medieval-gold"></i>
                </div>
                <div class="font-serif text-3xl font-bold text-medieval-gold">120</div>
                <span class="text-[10px] text-emerald-400 mt-1 block">พร้อมเปิดให้บริการทุกห้อง</span>
            </div>

            <div class="bg-medieval-card border border-medieval-gold/30 rounded-xl p-5 shadow-lg">
                <div class="flex justify-between items-center mb-2">
                    <span class="text-xs text-medieval-cream/70 uppercase tracking-wider">ห้องที่มีผู้เข้าพัก (OCCUPIED)</span>
                    <i data-lucide="user-check" class="w-5 h-5 text-amber-400"></i>
                </div>
                <div class="font-serif text-3xl font-bold text-amber-400">86</div>
                <span class="text-[10px] text-medieval-cream/60 mt-1 block">อัตราเข้าพัก 71.6%</span>
            </div>

            <div class="bg-medieval-card border border-medieval-gold/30 rounded-xl p-5 shadow-lg">
                <div class="flex justify-between items-center mb-2">
                    <span class="text-xs text-medieval-cream/70 uppercase tracking-wider">ห้องว่างพร้อมจอง (AVAILABLE)</span>
                    <i data-lucide="key-round" class="w-5 h-5 text-emerald-400"></i>
                </div>
                <div class="font-serif text-3xl font-bold text-emerald-400">34</div>
                <span class="text-[10px] text-medieval-cream/60 mt-1 block">รองรับการ Check-in ทันที</span>
            </div>

            <div class="bg-medieval-card border border-medieval-gold/30 rounded-xl p-5 shadow-lg">
                <div class="flex justify-between items-center mb-2">
                    <span class="text-xs text-medieval-cream/70 uppercase tracking-wider">การจองวันนี้ (TODAY'S BOOKINGS)</span>
                    <i data-lucide="calendar" class="w-5 h-5 text-medieval-gold"></i>
                </div>
                <div class="font-serif text-3xl font-bold text-medieval-gold">27</div>
                <span class="text-[10px] text-emerald-400 mt-1 block">+14% เทียบกับเมื่อวาน</span>
            </div>
        </div>

        <!-- Analytics Visuals & Charts Grid -->
        <div class="grid grid-cols-1 lg:grid-cols-3 gap-8 mb-8">
            <!-- Room Occupancy Chart Visual -->
            <div class="lg:col-span-2 bg-medieval-card border border-medieval-gold/30 rounded-xl p-6">
                <div class="flex justify-between items-center mb-6">
                    <h3 class="font-serif font-bold text-medieval-gold text-lg tracking-wide">ROOM OCCUPANCY & REVENUE ANALYTICS</h3>
                    <span class="text-xs text-medieval-cream/50">สถิติรายสัปดาห์</span>
                </div>
                <!-- Simulated CSS Bar Chart -->
                <div class="h-56 flex items-end justify-between gap-2 sm:gap-4 pt-8 px-2 border-b border-medieval-gold/20">
                    <div class="flex-1 flex flex-col items-center gap-2 h-full justify-end">
                        <div class="w-full bg-medieval-gold/40 hover:bg-medieval-gold transition rounded-t" style="height: 60%;"></div>
                        <span class="text-[10px] text-medieval-cream/60">จันทร์</span>
                    </div>
                    <div class="flex-1 flex flex-col items-center gap-2 h-full justify-end">
                        <div class="w-full bg-medieval-gold/50 hover:bg-medieval-gold transition rounded-t" style="height: 72%;"></div>
                        <span class="text-[10px] text-medieval-cream/60">อังคาร</span>
                    </div>
                    <div class="flex-1 flex flex-col items-center gap-2 h-full justify-end">
                        <div class="w-full bg-medieval-gold/60 hover:bg-medieval-gold transition rounded-t" style="height: 65%;"></div>
                        <span class="text-[10px] text-medieval-cream/60">พุธ</span>
                    </div>
                    <div class="flex-1 flex flex-col items-center gap-2 h-full justify-end">
                        <div class="w-full bg-medieval-gold/80 hover:bg-medieval-gold transition rounded-t" style="height: 85%;"></div>
                        <span class="text-[10px] text-medieval-cream/60">พฤหัสบดี</span>
                    </div>
                    <div class="flex-1 flex flex-col items-center gap-2 h-full justify-end">
                        <div class="w-full bg-medieval-gold hover:bg-medieval-goldLight transition rounded-t" style="height: 95%;"></div>
                        <span class="text-[10px] text-medieval-gold font-bold">ศุกร์</span>
                    </div>
                    <div class="flex-1 flex flex-col items-center gap-2 h-full justify-end">
                        <div class="w-full bg-medieval-gold hover:bg-medieval-goldLight transition rounded-t" style="height: 100%;"></div>
                        <span class="text-[10px] text-medieval-gold font-bold">เสาร์</span>
                    </div>
                    <div class="flex-1 flex flex-col items-center gap-2 h-full justify-end">
                        <div class="w-full bg-medieval-gold/75 hover:bg-medieval-gold transition rounded-t" style="height: 80%;"></div>
                        <span class="text-[10px] text-medieval-cream/60">อาทิตย์</span>
                    </div>
                </div>
                <div class="flex justify-between items-center text-xs text-medieval-cream/60 mt-4">
                    <span>วันที่มีการเข้าพักสูงสุด: <strong class="text-medieval-gold">วันเสาร์ (100%)</strong></span>
                    <span>ราคาเฉลี่ยต่อห้อง (ADR): <strong class="text-medieval-gold">฿6,850</strong></span>
                </div>
            </div>

            <!-- Suite Distribution Breakdown -->
            <div class="bg-medieval-card border border-medieval-gold/30 rounded-xl p-6 flex flex-col justify-between">
                <div>
                    <h3 class="font-serif font-bold text-medieval-gold text-lg tracking-wide mb-4">สัดส่วนประเภทห้องพัก</h3>
                    <div class="space-y-4 text-xs">
                        <div>
                            <div class="flex justify-between mb-1">
                                <span>Royal King Rooms (70 ห้อง)</span>
                                <span class="text-medieval-gold font-bold">เข้าพักแล้ว 52 ห้อง</span>
                            </div>
                            <div class="w-full h-2 bg-medieval-bg rounded-full overflow-hidden">
                                <div class="bg-medieval-gold h-full" style="width: 74%;"></div>
                            </div>
                        </div>

                        <div>
                            <div class="flex justify-between mb-1">
                                <span>Royal Suites (35 ห้อง)</span>
                                <span class="text-medieval-gold font-bold">เข้าพักแล้ว 26 ห้อง</span>
                            </div>
                            <div class="w-full h-2 bg-medieval-bg rounded-full overflow-hidden">
                                <div class="bg-medieval-gold h-full" style="width: 74%;"></div>
                            </div>
                        </div>

                        <div>
                            <div class="flex justify-between mb-1">
                                <span>Crown Luxury Suites (15 ห้อง)</span>
                                <span class="text-medieval-gold font-bold">เข้าพักแล้ว 8 ห้อง</span>
                            </div>
                            <div class="w-full h-2 bg-medieval-bg rounded-full overflow-hidden">
                                <div class="bg-medieval-gold h-full" style="width: 53%;"></div>
                            </div>
                        </div>
                    </div>
                </div>

                <div class="mt-6 pt-4 border-t border-medieval-gold/20 text-center">
                    <span class="text-xs text-medieval-cream/70">ระบบ AI วิเคราะห์ราคา: <strong class="text-emerald-400">ทำงานสมบูรณ์</strong></span>
                </div>
            </div>
        </div>

        <!-- Recent Reservations Table -->
        <div class="bg-medieval-card border border-medieval-gold/30 rounded-xl overflow-hidden shadow-xl">
            <div class="p-6 border-b border-medieval-gold/20 flex justify-between items-center">
                <h3 class="font-serif font-bold text-medieval-gold text-lg tracking-wide">รายการการจองล่าสุด (BOOKING LOGS)</h3>
                <span class="text-xs text-medieval-cream/60">อัปเดตเรียลไทม์</span>
            </div>
            <div class="overflow-x-auto">
                <table class="w-full text-left text-xs text-medieval-cream">
                    <thead class="bg-medieval-bg font-thaiSerif text-medieval-gold border-b border-medieval-gold/20 uppercase tracking-wider">
                        <tr>
                            <th class="p-4">Booking ID</th>
                            <th class="p-4">ชื่อลูกค้า (Guest Name)</th>
                            <th class="p-4">ห้องพักที่จอง</th>
                            <th class="p-4">วันที่ Check-In / Out</th>
                            <th class="p-4">ยอดรวมเงินชำระ</th>
                            <th class="p-4">สถานะการจอง</th>
                        </tr>
                    </thead>
                    <tbody id="adminBookingsTable" class="divide-y divide-medieval-gold/10 font-thaiSerif">
                        <tr>
                            <td class="p-4 font-mono text-medieval-gold">#RC-9042</td>
                            <td class="p-4 font-serif text-sm">คุณอาร์เธอร์ เพนเดิลตัน</td>
                            <td class="p-4">Crown Luxury Suite</td>
                            <td class="p-4">12 พ.ย. - 15 พ.ย.</td>
                            <td class="p-4 font-bold text-medieval-cream">฿36,000</td>
                            <td class="p-4"><span class="px-2 py-0.5 rounded bg-emerald-500/20 text-emerald-400 border border-emerald-500/40 text-[10px]">ชำระเงินแล้ว</span></td>
                        </tr>
                        <tr>
                            <td class="p-4 font-mono text-medieval-gold">#RC-9041</td>
                            <td class="p-4 font-serif text-sm">คุณกวินทรา แวนซ์</td>
                            <td class="p-4">Royal Suite</td>
                            <td class="p-4">10 พ.ย. - 12 พ.ย.</td>
                            <td class="p-4 font-bold text-medieval-cream">฿15,000</td>
                            <td class="p-4"><span class="px-2 py-0.5 rounded bg-emerald-500/20 text-emerald-400 border border-emerald-500/40 text-[10px]">ชำระเงินแล้ว</span></td>
                        </tr>
                        <tr>
                            <td class="p-4 font-mono text-medieval-gold">#RC-9040</td>
                            <td class="p-4 font-serif text-sm">คุณเซดริก สเตอร์ลิง</td>
                            <td class="p-4">Royal King Room</td>
                            <td class="p-4">08 พ.ย. - 09 พ.ย.</td>
                            <td class="p-4 font-bold text-medieval-cream">฿4,500</td>
                            <td class="p-4"><span class="px-2 py-0.5 rounded bg-amber-500/20 text-amber-400 border border-amber-500/40 text-[10px]">รอ Check-in</span></td>
                        </tr>
                    </tbody>
                </table>
            </div>
        </div>
    </div>

    <!-- BOOKING MODAL & CONFIRMATION FLOW -->
    <div id="bookingModal" class="fixed inset-0 z-50 hidden bg-black/80 backdrop-blur-sm flex items-center justify-center p-4 overflow-y-auto font-thaiSerif">
        <div class="bg-medieval-card border-2 border-medieval-gold rounded-xl max-w-xl w-full p-6 sm:p-8 relative shadow-2xl">
            <!-- Close Modal -->
            <button onclick="closeBookingModal()" class="absolute top-4 right-4 text-medieval-cream/60 hover:text-medieval-gold">
                <i data-lucide="x" class="w-6 h-6"></i>
            </button>

            <!-- Modal Header -->
            <div class="text-center mb-6">
                <i data-lucide="crown" class="w-8 h-8 text-medieval-gold mx-auto mb-2"></i>
                <h3 class="font-serif text-3xl font-bold text-medieval-gold tracking-wide" id="modalRoomTitle">RESERVE SUITE</h3>
                <p class="text-xs text-medieval-cream/70 font-thaiSerif tracking-wider">กรอกข้อมูลผู้เข้าพักเพื่อยืนยันการจองห้องพักออนไลน์</p>
            </div>

            <!-- Booking Form -->
            <form id="bookingForm" onsubmit="submitBookingForm(event)" class="space-y-4">
                <input type="hidden" id="modalRoomPrice">
                
                <div class="grid grid-cols-1 sm:grid-cols-2 gap-4">
                    <div>
                        <label class="block text-xs text-medieval-gold mb-1 uppercase tracking-wider font-semibold">วันที่เข้าพัก (CHECK-IN)</label>
                        <input type="date" id="bookCheckIn" class="w-full bg-medieval-bg border border-medieval-gold/30 rounded px-3 py-2 text-xs text-medieval-cream focus:border-medieval-gold focus:outline-none" required>
                    </div>
                    <div>
                        <label class="block text-xs text-medieval-gold mb-1 uppercase tracking-wider font-semibold">วันที่ออก (CHECK-OUT)</label>
                        <input type="date" id="bookCheckOut" class="w-full bg-medieval-bg border border-medieval-gold/30 rounded px-3 py-2 text-xs text-medieval-cream focus:border-medieval-gold focus:outline-none" required>
                    </div>
                </div>

                <div>
                    <label class="block text-xs text-medieval-gold mb-1 uppercase tracking-wider font-semibold">ชื่อ-นามสกุล ผู้เข้าพัก</label>
                    <input type="text" id="bookName" placeholder="เช่น คุณสมชาย วงศ์เทวา" class="w-full bg-medieval-bg border border-medieval-gold/30 rounded px-3 py-2 text-xs text-medieval-cream focus:border-medieval-gold focus:outline-none" required>
                </div>

                <div class="grid grid-cols-1 sm:grid-cols-2 gap-4">
                    <div>
                        <label class="block text-xs text-medieval-gold mb-1 uppercase tracking-wider font-semibold">อีเมล (EMAIL)</label>
                        <input type="email" id="bookEmail" placeholder="somchai@email.com" class="w-full bg-medieval-bg border border-medieval-gold/30 rounded px-3 py-2 text-xs text-medieval-cream focus:border-medieval-gold focus:outline-none" required>
                    </div>
                    <div>
                        <label class="block text-xs text-medieval-gold mb-1 uppercase tracking-wider font-semibold">เบอร์โทรศัพท์ (PHONE)</label>
                        <input type="tel" id="bookPhone" placeholder="081-234-5678" class="w-full bg-medieval-bg border border-medieval-gold/30 rounded px-3 py-2 text-xs text-medieval-cream focus:border-medieval-gold focus:outline-none" required>
                    </div>
                </div>

                <div>
                    <label class="block text-xs text-medieval-gold mb-1 uppercase tracking-wider font-semibold">หมายเหตุพิเศษ / คำขอเพิ่มเติม</label>
                    <textarea id="bookNotes" rows="2" placeholder="ประเภทอาหารที่แพ้, เวลาเดินทางถึง, บริการสปา..." class="w-full bg-medieval-bg border border-medieval-gold/30 rounded px-3 py-2 text-xs text-medieval-cream focus:border-medieval-gold focus:outline-none"></textarea>
                </div>

                <div class="pt-4 border-t border-medieval-gold/20 flex justify-between items-center">
                    <div>
                        <span class="text-[10px] text-medieval-cream/60 uppercase tracking-wider block">ยอดรวมโดยประมาณ</span>
                        <span class="font-serif text-2xl font-bold text-medieval-gold" id="modalCalculatedTotal">฿4,500</span>
                    </div>
                    <button type="submit" class="px-6 py-3 bg-medieval-crimson hover:bg-medieval-crimsonHover text-medieval-cream font-thaiSerif font-bold text-xs uppercase tracking-widest rounded border border-medieval-gold/40 shadow-xl">
                        ยืนยันการจองห้องพัก
                    </button>
                </div>
            </form>

            <!-- Booking Confirmation Card Output (Hidden initially) -->
            <div id="bookingConfirmationCard" class="hidden text-center space-y-4 py-4">
                <div class="w-12 h-12 rounded-full bg-emerald-500/20 border border-emerald-500 text-emerald-400 mx-auto flex items-center justify-center">
                    <i data-lucide="check" class="w-6 h-6"></i>
                </div>
                <h4 class="font-serif text-2xl font-bold text-medieval-gold tracking-wide">การจองห้องพักสำเร็จแล้ว!</h4>
                <p class="text-xs text-medieval-cream/70">ระบบได้บันทึกข้อมูลการจองของท่านเข้าสู่ Smart Hotel Information System เรียบร้อยแล้ว</p>

                <div class="bg-medieval-bg border border-medieval-gold/40 p-4 rounded-lg text-left text-xs space-y-2">
                    <div class="flex justify-between border-b border-medieval-gold/20 pb-2">
                        <span class="text-medieval-cream/60">Booking ID:</span>
                        <strong class="text-medieval-gold font-mono" id="confirmID">#RC-9982</strong>
                    </div>
                    <div class="flex justify-between">
                        <span class="text-medieval-cream/60">ชื่อผู้เข้าพัก:</span>
                        <span class="text-medieval-cream font-serif font-bold" id="confirmName">-</span>
                    </div>
                    <div class="flex justify-between">
                        <span class="text-medieval-cream/60">ประเภทห้องพัก:</span>
                        <span class="text-medieval-cream" id="confirmRoom">-</span>
                    </div>
                    <div class="flex justify-between">
                        <span class="text-medieval-cream/60">วันที่เข้าพัก:</span>
                        <span class="text-medieval-cream" id="confirmDates">-</span>
                    </div>
                    <div class="flex justify-between border-t border-medieval-gold/20 pt-2 font-bold">
                        <span class="text-medieval-gold">ยอดรวมชำระสุทธิ:</span>
                        <span class="text-medieval-gold font-serif text-lg" id="confirmTotal">฿0</span>
                    </div>
                </div>

                <!-- QR Code Simulation -->
                <div class="bg-white p-3 rounded-lg w-32 h-32 mx-auto flex flex-col items-center justify-center text-black">
                    <svg class="w-24 h-24 text-black" viewBox="0 0 24 24" fill="currentColor">
                        <path d="M2 2h8v8H2V2zm2 2v4h4V4H4zm9-2h8v8h-8V2zm2 2v4h4V4h-4zM2 14h8v8H2v-8zm2 2v4h4v-4H4zm13-2h4v2h-4v-2zm-4 4h2v4h-2v-4zm2-2h4v2h-4v-2zm2 4h4v2h-4v-2z"/>
                    </svg>
                    <span class="text-[8px] font-mono font-bold mt-1">SMART PASS QR</span>
                </div>

                <button onclick="closeBookingModal()" class="w-full py-2.5 bg-medieval-gold text-medieval-bg font-thaiSerif font-bold text-xs uppercase tracking-widest rounded">
                    ปิดหน้าต่างและกลับสู่หน้าหลัก
                </button>
            </div>
        </div>
    </div>

    <!-- FOOTER -->
    <footer class="bg-medieval-bg border-t border-medieval-gold/30 pt-16 pb-8 text-xs text-medieval-cream/70 font-thaiSerif">
        <div class="max-w-7xl mx-auto px-4 sm:px-6 lg:px-8 grid grid-cols-1 md:grid-cols-4 gap-8 mb-12">
            <div>
                <div class="flex items-center gap-2 mb-4">
                    <div class="w-8 h-8 rounded border border-medieval-gold bg-medieval-card flex items-center justify-center">
                        <i data-lucide="crown" class="w-4 h-4 text-medieval-gold"></i>
                    </div>
                    <span class="font-serif text-lg font-bold text-medieval-gold tracking-wide">THE ROYAL CROWN INN</span>
                </div>
                <p class="text-medieval-cream/60 leading-relaxed mb-4">
                    ประสบการณ์พักผ่อนสุดหรูในปราสาทอังกฤษยุคกลาง ผสานเทคโนโลยีระบบสารสนเทศโรงแรมอัจฉริยะ 
                </p>
                <div class="text-medieval-gold font-cinzel text-[11px] tracking-wider uppercase">Medieval English Hotel Concept</div>
            </div>

            <div>
                <h4 class="font-cinzel text-xs font-bold text-medieval-gold mb-4 tracking-widest uppercase">เมนูด่วน (QUICK LINKS)</h4>
                <ul class="space-y-2">
                    <li><a href="#home" class="hover:text-medieval-gold transition">หน้าแรก (Home)</a></li>
                    <li><a href="#rooms" class="hover:text-medieval-gold transition">ห้องพักหรู (Accommodations)</a></li>
                    <li><a href="#concierge" class="hover:text-medieval-gold transition">ผู้ช่วย AI Concierge</a></li>
                    <li><a href="#dining" class="hover:text-medieval-gold transition">ห้องอาหาร & สปา</a></li>
                </ul>
            </div>

            <div>
                <h4 class="font-cinzel text-xs font-bold text-medieval-gold mb-4 tracking-widest uppercase">ข้อมูลการติดต่อ</h4>
                <ul class="space-y-2">
                    <li class="flex items-center gap-2"><i data-lucide="map-pin" class="w-4 h-4 text-medieval-gold"></i> Sovereign Estate, Medieval Kingdom</li>
                    <li class="flex items-center gap-2"><i data-lucide="phone" class="w-4 h-4 text-medieval-gold"></i> +44 (0) 20 7946 0912</li>
                    <li class="flex items-center gap-2"><i data-lucide="mail" class="w-4 h-4 text-medieval-gold"></i> concierge@royalcrowninn.com</li>
                </ul>
            </div>

            <div>
                <h4 class="font-cinzel text-xs font-bold text-medieval-gold mb-4 tracking-widest uppercase">รายชื่อคณะผู้จัดทำโครงการ</h4>
                <div class="p-4 bg-medieval-card rounded-lg border border-medieval-gold/20 space-y-1 text-xs">
                    <div class="text-medieval-gold font-bold font-cinzel text-[11px] uppercase tracking-wider mb-1">Development Team:</div>
                    <p class="text-medieval-cream/90">• ภูมิภัทร จันทร์พรม (6940018056)</p>
                    <p class="text-medieval-cream/90">• สุนิสา ยมรัตน์ (6940015132)</p>
                    <p class="text-medieval-cream/90">• ภูวิรัทร์ คำเอก (6940066501)</p>
                    <p class="text-medieval-cream/90">• จิรัฏฐ์ ตั้งวัฒนกิตติกุล (6940071512)</p>
                    <p class="text-medieval-cream/90">• วีรภัทร แกล้งกลั่น (6940015001)</p>
                </div>
            </div>
        </div>

        <div class="max-w-7xl mx-auto px-4 sm:px-6 lg:px-8 border-t border-medieval-gold/10 pt-6 flex flex-col sm:flex-row justify-between items-center text-[11px]">
            <p>&copy; 2026 THE ROYAL CROWN INN. สงวนลิขสิทธิ์ระบบสารสนเทศการโรงแรม Cross-Platform OOP.</p>
            <div class="flex items-center gap-4 mt-2 sm:mt-0 font-cinzel">
                <a href="#" class="hover:text-medieval-gold">Privacy Policy</a>
                <span>•</span>
                <a href="#" class="hover:text-medieval-gold">Terms of Service</a>
            </div>
        </div>
    </footer>

    <!-- INTERACTIVE JAVASCRIPT LOGIC -->
    <script>
        // Global App State
        let activeDiscount = 0;
        let activePromoCode = '';
        let userPoints = 450;
        let isAdminView = false;

        // Initialize Lucide Icons on load
        document.addEventListener('DOMContentLoaded', () => {
            lucide.createIcons();
            setDefaultDates();
        });

        // Set Default Check-In and Check-Out Dates
        function setDefaultDates() {
            const today = new Date();
            const tomorrow = new Date(today);
            tomorrow.setDate(tomorrow.getDate() + 2);

            const todayStr = today.toISOString().split('T')[0];
            const tomorrowStr = tomorrow.toISOString().split('T')[0];

            if(document.getElementById('searchCheckIn')) document.getElementById('searchCheckIn').value = todayStr;
            if(document.getElementById('searchCheckOut')) document.getElementById('searchCheckOut').value = tomorrowStr;
            if(document.getElementById('bookCheckIn')) document.getElementById('bookCheckIn').value = todayStr;
            if(document.getElementById('bookCheckOut')) document.getElementById('bookCheckOut').value = tomorrowStr;
        }

        // Toggle Admin Mode
        function toggleAdminMode() {
            isAdminView = !isAdminView;
            const guestView = document.getElementById('guestPortalView');
            const adminView = document.getElementById('adminPortalView');
            const viewText = document.getElementById('viewModeText');

            if(isAdminView) {
                guestView.classList.add('hidden');
                adminView.classList.remove('hidden');
                viewText.innerText = 'Switch to Guest Portal';
            } else {
                guestView.classList.remove('hidden');
                adminView.classList.add('hidden');
                viewText.innerText = 'Switch to Admin Portal';
            }
        }

        // Navigation helpers
        function scrollToRooms() {
            const roomSection = document.getElementById('rooms');
            if(roomSection) roomSection.scrollIntoView({ behavior: 'smooth' });
        }

        function toggleMobileMenu() {
            const menu = document.getElementById('mobileMenu');
            menu.classList.toggle('hidden');
        }

        // Service Tabs switcher
        function switchServiceTab(tabId) {
            document.querySelectorAll('.service-tab-content').forEach(el => el.classList.add('hidden'));
            document.querySelectorAll('.service-tab-btn').forEach(btn => {
                btn.classList.remove('text-medieval-gold', 'border-medieval-gold');
                btn.classList.add('text-medieval-cream/60', 'border-transparent');
            });

            document.getElementById(tabId).classList.remove('hidden');
            const activeBtn = document.getElementById(`tabBtn-${tabId}`);
            activeBtn.classList.remove('text-medieval-cream/60', 'border-transparent');
            activeBtn.classList.add('text-medieval-gold', 'border-medieval-gold');
        }

        // Search & Room Filter Handler
        function handleSearchRooms(e) {
            e.preventDefault();
            const selectedType = document.getElementById('searchRoomType').value;
            const selectedGuests = document.getElementById('searchGuests').value;

            const cards = document.querySelectorAll('.room-card');
            cards.forEach(card => {
                const type = card.getAttribute('data-type');
                const guests = parseInt(card.getAttribute('data-guests'));

                let matchType = (selectedType === 'all' || selectedType === type);
                let matchGuests = (selectedGuests === 'all' || (selectedGuests === '2' && guests === 2) || (selectedGuests === '4' && guests >= 2));

                if (matchType && matchGuests) {
                    card.classList.remove('hidden');
                } else {
                    card.classList.add('hidden');
                }
            });

            scrollToRooms();
        }

        // Booking Modal Operations
        function openBookingModal(roomTitle, pricePerNight) {
            document.getElementById('bookingModal').classList.remove('hidden');
            document.getElementById('bookingForm').classList.remove('hidden');
            document.getElementById('bookingConfirmationCard').classList.add('hidden');
            
            document.getElementById('modalRoomTitle').innerText = roomTitle;
            document.getElementById('modalRoomPrice').value = pricePerNight;
            
            calculateModalTotal();
        }

        function closeBookingModal() {
            document.getElementById('bookingModal').classList.add('hidden');
        }

        function calculateModalTotal() {
            const price = parseFloat(document.getElementById('modalRoomPrice').value || 4500);
            let total = price;
            if (activeDiscount > 0) {
                total = total * (1 - activeDiscount / 100);
            }
            document.getElementById('modalCalculatedTotal').innerText = `$${total.toLocaleString()}` + (activeDiscount > 0 ? ` (${activeDiscount}% OFF)` : '');
        }

        function submitBookingForm(e) {
            e.preventDefault();
            const name = document.getElementById('bookName').value;
            const roomTitle = document.getElementById('modalRoomTitle').innerText;
            const checkIn = document.getElementById('bookCheckIn').value;
            const checkOut = document.getElementById('bookCheckOut').value;
            const price = document.getElementById('modalCalculatedTotal').innerText;
            const randomID = '#RC-' + Math.floor(1000 + Math.random() * 9000);

            // Populate confirmation card
            document.getElementById('confirmID').innerText = randomID;
            document.getElementById('confirmName').innerText = name;
            document.getElementById('confirmRoom').innerText = roomTitle;
            document.getElementById('confirmDates').innerText = `${checkIn} ถึง ${checkOut}`;
            document.getElementById('confirmTotal').innerText = price;

            // Hide form and show confirmation
            document.getElementById('bookingForm').classList.add('hidden');
            document.getElementById('bookingConfirmationCard').classList.remove('hidden');

            // Add to Admin Table dynamically
            const adminTable = document.getElementById('adminBookingsTable');
            const newRow = document.createElement('tr');
            newRow.innerHTML = `
                <td class="p-4 font-mono text-medieval-gold">${randomID}</td>
                <td class="p-4">${name}</td>
                <td class="p-4">${roomTitle}</td>
                <td class="p-4">${checkIn} - ${checkOut}</td>
                <td class="p-4 font-bold text-medieval-cream">${price}</td>
                <td class="p-4"><span class="px-2 py-0.5 rounded bg-emerald-500/20 text-emerald-400 border border-emerald-500/40 text-[10px]">ชำระเงินแล้ว</span></td>
            `;
            adminTable.prepend(newRow);

            // Reward loyalty points ($100 = 1 pt)
            userPoints += 45;
            document.getElementById('userPointsDisplay').innerText = `${userPoints} คะแนน`;
        }

        // Promo Code Logic
        function applyPromoCode(code, discount) {
            activePromoCode = code;
            activeDiscount = discount;
            alert(`นำโค้ดส่วนลด '${code}' มาใช้งานสำเร็จ! ท่านได้รับส่วนลด ${discount}% สำหรับการจองห้องพัก`);
        }

        // Reward Redeem Logic
        function redeemReward(rewardName, pointsNeeded) {
            if (userPoints >= pointsNeeded) {
                userPoints -= pointsNeeded;
                document.getElementById('userPointsDisplay').innerText = `${userPoints} คะแนน`;
                alert(`ทำรายการแลกรับสิทธิ์: ${rewardName} สำเร็จแล้ว!`);
            } else {
                alert(`คะแนนสะสมไม่เพียงพอ! ท่านต้องการ ${pointsNeeded} คะแนนในการแลกสิทธิ์นี้`);
            }
        }

        // AI Concierge Chatbot Simulation
        function handleChatSubmit(e) {
            e.preventDefault();
            const input = document.getElementById('chatInput');
            const query = input.value.trim();
            if(!query) return;

            appendChatMessage('user', query);
            input.value = '';

            // Simulate AI Thinking and response
            setTimeout(() => {
                const response = generateAIResponse(query);
                appendChatMessage('ai', response);
            }, 600);
        }

        function sendQuickPrompt(promptText) {
            appendChatMessage('user', promptText);
            setTimeout(() => {
                const response = generateAIResponse(promptText);
                appendChatMessage('ai', response);
            }, 600);
        }

        function appendChatMessage(sender, text) {
            const chatStream = document.getElementById('chatStream');
            const msgDiv = document.createElement('div');
            
            if (sender === 'user') {
                msgDiv.className = 'flex justify-end font-thaiSerif';
                msgDiv.innerHTML = `
                    <div class="bg-medieval-crimson text-medieval-cream p-3 rounded-2xl rounded-tr-none max-w-[80%] border border-medieval-gold/30">
                        <p>${text}</p>
                    </div>
                `;
            } else {
                msgDiv.className = 'flex gap-3 max-w-[85%] font-thaiSerif';
                msgDiv.innerHTML = `
                    <div class="w-8 h-8 rounded-full bg-medieval-gold/20 border border-medieval-gold shrink-0 flex items-center justify-center text-medieval-gold">
                        <i data-lucide="bot" class="w-4 h-4"></i>
                    </div>
                    <div class="bg-medieval-card border border-medieval-gold/30 p-4 rounded-2xl rounded-tl-none text-medieval-cream space-y-2">
                        <p>${text}</p>
                    </div>
                `;
            }
            chatStream.appendChild(msgDiv);
            chatStream.scrollTop = chatStream.scrollHeight;
            lucide.createIcons();
        }

        function generateAIResponse(query) {
            const q = query.toLowerCase();
            if (q.includes('ห้องพัก') || q.includes('room') || q.includes('ว่าง') || q.includes('แนะนำ')) {
                if (q.includes('4') || q.includes('กลุ่ม') || q.includes('ครอบครัว')) {
                    return "สำหรับผู้เข้าพัก 4 ท่าน กระผมขอแนะนำ <strong>Crown Luxury Suite</strong> (฿12,000/คืน) ซึ่งมีห้องรับประทานอาหารส่วนตัว หรือ <strong>Royal Suite</strong> (฿7,500/คืน) ที่มีห้องนั่งเล่นส่วนตัวกว้างขวางครับ";
                }
                return "โรงแรมของเรามีห้องพัก 3 ประเภทครับ:<br>1. <strong>Royal King Room</strong> (฿4,500/คืน)<br>2. <strong>Royal Suite</strong> (฿7,500/คืน)<br>3. <strong>Crown Luxury Suite</strong> (฿12,000/คืน)<br>ทุกห้องควบคุมระบบไฟและอุณหภูมิด้วยระบบ Smart Control ครับ";
            } else if (q.includes('ราคา') || q.includes('cost') || q.includes('เท่าไหร่')) {
                return "ราคาห้องพักเริ่มต้นที่ <strong>฿4,500/คืน</strong> สำหรับ Royal King Room จนถึง <strong>฿12,000/คืน</strong> สำหรับ Crown Luxury Suite ครับ ท่านสามารถใช้โปรโมชั่น <strong>NEWMEMBER</strong> เพื่อรับส่วนลด 20% ได้ทันทีครับ";
            } else if (q.includes('เช็คอิน') || q.includes('เวลา') || q.includes('check-in') || q.includes('check in')) {
                return "เวลา Check-In เริ่มต้นตั้งแต่ <strong>15:00 น.</strong> และเวลา Check-Out คือไม่เกิน <strong>12:00 น. (เที่ยงวัน)</strong> ครับ หากต้องการเข้าพักก่อนเวลา สามารถแจ้งผ่าน AI Concierge ได้ครับ";
            } else if (q.includes('อาหาร') || q.includes('กิน') || q.includes('เช้า') || q.includes('food')) {
                return "ห้องอาหาร Royal Banquet ให้บริการสำรับอาหารสไตล์อังกฤษยุคกลาง และบริการ In-Room Dining 24 ชั่วโมง โดยบุฟเฟต์อาหารเช้าเปิดบริการ 06:30 - 10:30 น. ครับ";
            } else if (q.includes('บริการ') || q.includes('สปา') || q.includes('ทัวร์') || q.includes('พิเศษ')) {
                return "เรามีบริการสปาน้ำแร่ร้อน ทัวร์ชมปราสาทอังกฤษยุคกลาง กิจกรรมยิงธนู และบริการรถรับ-ส่งสนามบินระดับ VIP ครับ";
            } else {
                return "ยินดีรับใช้ครับท่าน! กระผมสามารถช่วยตรวจสอบราคาห้องพัก แนะนำเมนูอาหาร หรือทำการจองสปาให้ท่านได้เสมอครับ";
            }
        }
    </script>
</body>
</html>
