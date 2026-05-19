<!DOCTYPE html>
<html lang="ar" dir="rtl">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>تطبيق خُطى</title>
    <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.4.0/css/all.min.css">
    <style>
        :root {
            --bg-dark: #090d16; /* أسود ملكي عميق */
            --card-bg: #111827; /* رمادي داكن فخم للكروت */
            --accent-gold: #d4af37; /* ذهبي براق جميل */
            --accent-glow: rgba(212, 175, 55, 0.25); /* توهج ذهبي */
            --text-main: #f8fafc; 
            --text-muted: #94a3b8;
        }

        * {
            box-sizing: border-box;
            margin: 0;
            padding: 0;
            font-family: 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif;
            -webkit-tap-highlight-color: transparent;
        }

        body {
            background-color: var(--bg-dark);
            color: var(--text-main);
            padding-bottom: 90px;
            min-height: 100vh;
        }

        /* الهيدر العلوي الفخم */
        header {
            background: linear-gradient(180deg, #111827, #090d16);
            padding: 35px 20px;
            text-align: center;
            border-bottom: 2px solid var(--accent-gold);
            box-shadow: 0 4px 25px var(--accent-glow);
            border-bottom-left-radius: 30px;
            border-bottom-right-radius: 30px;
            margin-bottom: 20px;
        }

        /* اسم التطبيق ذهبي جميل فقط "خطى" */
        header h1 {
            font-size: 32px;
            color: var(--accent-gold);
            letter-spacing: 1px;
            font-weight: 800;
            text-shadow: 0 0 15px var(--accent-glow);
        }

        /* حاوية الشاشات */
        .container {
            padding: 15px;
            max-width: 600px;
            margin: 0 auto;
        }

        .page {
            display: none;
        }

        .page.active {
            display: block;
            animation: fadeIn 0.4s ease-in-out;
        }

        @keyframes fadeIn {
            from { opacity: 0; transform: translateY(12px); }
            to { opacity: 1; transform: translateY(0); }
        }

        /* العناوين الداخلية */
        .section-title {
            font-size: 20px;
            color: var(--accent-gold);
            margin-bottom: 15px;
            display: flex;
            align-items: center;
            gap: 10px;
            font-weight: 600;
            border-bottom: 1px solid rgba(212, 175, 55, 0.2);
            padding-bottom: 8px;
        }

        /* كروت الأقسام المحدثة */
        .premium-card {
            background-color: var(--card-bg);
            border-radius: 18px;
            padding: 20px;
            margin-bottom: 15px;
            border: 1px solid rgba(255, 255, 255, 0.05);
            box-shadow: 0 4px 10px rgba(0,0,0,0.3);
            transition: all 0.3s ease;
        }

        .premium-card:hover {
            border-color: var(--accent-gold);
            box-shadow: 0 0 15px var(--accent-glow);
        }

        .card-sub-title {
            color: var(--accent-gold);
            font-size: 16px;
            margin-bottom: 10px;
            font-weight: 600;
            display: flex;
            align-items: center;
            gap: 8px;
        }

        .content-text {
            font-size: 16px;
            line-height: 1.7;
            color: var(--text-main);
            text-align: justify;
        }

        /* أزرار التسبيح الذكية */
        .counter-btn {
            background: #1f2937;
            color: var(--accent-gold);
            border: 1px solid var(--accent-gold);
            padding: 12px 20px;
            border-radius: 25px;
            font-size: 16px;
            cursor: pointer;
            width: 100%;
            display: flex;
            justify-content: space-between;
            align-items: center;
            margin-top: 15px;
            font-weight: bold;
            transition: all 0.2s;
        }

        .counter-btn:active {
            background-color: var(--accent-gold);
            color: var(--bg-dark);
        }

        /* قوائم الاختيار للقراء والراديو */
        select {
            width: 100%;
            padding: 14px;
            background-color: var(--bg-dark);
            color: var(--accent-gold);
            border: 1px solid var(--accent-gold);
            border-radius: 10px;
            margin-bottom: 15px;
            font-size: 16px;
            font-weight: 500;
            outline: none;
        }

        audio {
            width: 100%;
            margin-top: 10px;
            accent-color: var(--accent-gold);
        }

        /* شريط التنقل السفلي الاحترافي للهواتف */
        .nav-bar {
            position: fixed;
            bottom: 0;
            left: 0;
            right: 0;
            background-color: var(--card-bg);
            display: flex;
            justify-content: space-around;
            padding: 12px 0;
            border-top: 2px solid var(--accent-gold);
            box-shadow: 0 -5px 20px rgba(0,0,0,0.5);
            z-index: 1000;
            border-top-left-radius: 20px;
            border-top-right-radius: 20px;
        }

        .nav-item {
            color: var(--text-muted);
            text-decoration: none;
            display: flex;
            flex-direction: column;
            align-items: center;
            font-size: 11px;
            cursor: pointer;
            background: none;
            border: none;
            width: 25%;
        }

        .nav-item i {
            font-size: 22px;
            margin-bottom: 5px;
            transition: all 0.2s ease;
        }

        .nav-item.active {
            color: var(--accent-gold);
        }

        .nav-item.active i {
            transform: translateY(-4px);
            text-shadow: 0 0 12px var(--accent-glow);
        }
    </style>
</head>
<body>

    <header>
        <h1>خُطى</h1>
    </header>

    <div class="container">
        
        <div id="quran-page" class="page active">
            <div class="section-title"><i class="fa-solid fa-book-quran"></i> المصحف الصوتي المباشر</div>
            <div class="premium-card">
                <label style="display:block; text-align:right; margin-bottom:8px; color:var(--text-muted)">اختر الشيخ والقارئ المفضل:</label>
                <select id="radio-select" onchange="changeRadio(this.value)">
                    <option value="https://backup.qurango.net/radio/tarteel">الشيخ مشاري العفاسي (مرتل)</option>
                    <option value="https://backup.qurango.net/radio/maher_al_muaiqly">الشيخ ماهر المعيقلي</option>
                    <option value="https://backup.qurango.net/radio/abdulbasit_mujawwad">الشيخ عبد الباسط عبد الصمد (مجوّد)</option>
                    <option value="https://backup.qurango.net/radio/minshawi_mujawwad">الشيخ محمد صديق المنشاوي</option>
                    <option value="https://backup.qurango.net/radio/abdullah_basfar">الشيخ عبد الله بصفر</option>
                    <option value="https://backup.qurango.net/radio/shuraym">الشيخ سعود الشريم</option>
                </select>
                <audio id="main-audio" controls src="https://backup.qurango.net/radio/tarteel"></audio>
            </div>
        </div>

        <div id="azkar-page" class="page">
            <div class="section-title"><i class="fa-solid fa-beads"></i> أذكار المسلم والسبحة</div>
            
            <div class="premium-card">
                <div class="card-sub-title"><i class="fa-solid fa-sun"></i> أذكار الصباح</div>
                <p class="content-text">"أَصْبَحْنَا وَأَصْبَحَ الْمُلْكُ لِلَّهِ وَالْحَمْدُ لِلَّهِ لَا إِلَهَ إِلَّا اللَّهُ وَحْدَهُ لَا شَرِيكَ لَهُ، لَهُ الْمُلْكُ وَلَهُ الْحَمْدُ وَهُوَ عَلَى كُلِّ شَيْءٍ قَدِيرٌ"</p>
                <button class="counter-btn" onclick="countDhikr(this)"><span>اضغط للتسبيح</span> <strong class="num">0 / 3</strong></button>
            </div>

            <div class="premium-card">
                <div class="card-sub-title"><i class="fa-solid fa-moon"></i> أذكار المساء</div>
                <p class="content-text">"أَمْسَيْنَا وَأَمْسَى الْمُلْكُ لِلَّهِ وَالْحَمْدُ لِلَّهِ لَا إِلَهَ إِلَّا اللَّهُ وَحْدَهُ لَا شَرِيكَ لَهُ، لَهُ الْمُلْكُ وَلَهُ الْحَمْدُ وَهُوَ عَلَى كُلِّ شَيْءٍ قَدِيرٌ"</p>
                <button class="counter-btn" onclick="countDhikr(this)"><span>اضغط للتسبيح</span> <strong class="num">0 / 3</strong></button>
            </div>

            <div class="premium-card">
                <div class="card-sub-title"><i class="fa-solid fa-star"></i> سبحة حرة ميسرة</div>
                <p class="content-text" style="text-align: center;">"سُبْحَانَ اللَّهِ وَبِحَمْدِهِ ، سُبْحَانَ اللَّهِ الْعَظِيمِ"</p>
                <button class="counter-btn" onclick="countDhikr(this, 100)"><span>اضغط للتسبيح</span> <strong class="num">0 / 100</strong></button>
            </div>
        </div>

        <div id="duas-page" class="page">
            <div class="section-title"><i class="fa-solid fa-hands-praying"></i> جوامع الأدعية المستجابة</div>
            
            <div class="premium-card">
                <div class="card-sub-title">من دعاء القرآن الكريم</div>
                <p class="content-text">"رَبَّنَا آتِنَا فِي الدُّنْيَا حَسَنَةً وَفِي الْآخِرَةِ حَسَنَةً وَقِنَا عَذَابَ النَّارِ"</p>
            </div>

            <div class="premium-card">
                <div class="card-sub-title">طلب الهداية والثبات</div>
                <p class="content-text">"يَا مُقَلِّبَ الْقُلُوبِ ثَبِّتْ قَلْبِي عَلَى دِينِكَ"</p>
            </div>

            <div class="premium-card">
                <div class="card-sub-title">طلب المغفرة والرحمة</div>
                <p class="content-text">"اللَّهُمَّ إِنَّكَ عَفُوٌّ تُحِبُّ الْعَفْوَ فَاعْفُ عَنِّي"</p>
            </div>
        </div>

        <div id="sira-page" class="page">
            <div class="section-title"><i class="fa-solid fa-clock-rotate-left"></i> السيرة النبوية الشريفة</div>
            
            <div class="premium-card">
                <div class="card-sub-title">١. المولد والنشأة</div>
                <p class="content-text">ولد النبي محمد ﷺ في مكة المكرمة في عام الفيل، ونشأ يتيماً حامياً للأمانات، وعُرف بين قومه بالصادق الأمين قبل بعثته الشريفة.</p>
            </div>

            <div class="premium-card">
                <div class="card-sub-title">٢. نزول الوحي والبعثة</div>
                <p class="content-text">نزل الوحي جبريل عليه السلام على النبي ﷺ وهو يتعبد في غار حراء في سن الأربعين، لتنطلق دعوة الإسلام الخالدة من مكة المكرمة.</p>
            </div>

            <div class="premium-card">
                <div class="card-sub-title">٣. الهجرة وبناء الدولة</div>
                <p class="content-text">هاجر الرسول ﷺ وصحابته إلى المدينة المنورة (يثرب) بعد اشتداد الأذى، حيث أسس هناك المسجد النبوي وبنى ركائز الدولة الإسلامية الأولى.</p>
            </div>
        </div>

    </div>

    <nav class="nav-bar">
        <button class="nav-item active" onclick="switchPage('quran-page', this)"><i class="fa-solid fa-book-open"></i>القرآن</button>
        <button class="nav-item" onclick="switchPage('azkar-page', this)"><i class="fa-solid fa-beads"></i>الأذكار</button>
        <button class="nav-item" onclick="switchPage('duas-page', this)"><i class="fa-solid fa-hands-praying"></i>الأدعية</button>
        <button class="nav-item" onclick="switchPage('sira-page', this)"><i class="fa-solid fa-clock-rotate-left"></i>السيرة</button>
    </nav>

    <script>
        // دالة التنقل السلس بين الأقسام الأربعة
        function switchPage(pageId, element) {
            document.querySelectorAll('.page').forEach(page => page.classList.remove('active'));
            document.querySelectorAll('.nav-item').forEach(item => item.classList.remove('active'));
            
            document.getElementById(pageId).classList.add('active');
            element.classList.add('active');
        }

        // دالة تغيير بث راديو القراء
        function changeRadio(url) {
            const audio = document.getElementById('main-audio');
            audio.src = url;
            audio.play();
        }

        // دالة العداد الذكي للسبحة والأذكار مع دعم الاهتزاز
        function countDhikr(btn, max = 3) {
            const strong = btn.querySelector('.num');
            let current = parseInt(strong.innerText.split(' / ')[0]);
            let target = parseInt(strong.innerText.split(' / ')[1]);
            
            if (current < target) {
                current++;
                strong.innerText = `${current} / ${target}`;
                
                // ميزة الاهتزاز الفيدباك للهواتف الذكية عند الضغط
                if (navigator.vibrate) navigator.vibrate(45);
                
                // تميز كرت الذكر عند اكتماله بالكامل
                if (current === target) {
                    btn.style.backgroundColor = '#d4af37';
                    btn.style.borderColor = '#ffffff';
                    btn.style.color = '#090d16';
                    btn.innerHTML = '<span>✅ تم بحمد الله</span> <strong class="num">' + target + ' / ' + target + '</strong>';
                }
            }
        }
    </script>
</body>
</html>
