<!DOCTYPE html>
<html lang="ar" dir="rtl">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>تطبيق خُطى الديني - النسخة الذهبية</title>
    <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.4.0/css/all.min.css">
    <style>
        :root {
            --bg-dark: #0f172a; /* خلفية داكنة جداً */
            --card-bg: #1e293b; /* خلفية الكروت */
            --accent-gold: #d4af37; /* ذهبي ملكي */
            --accent-glow: rgba(212, 175, 55, 0.3); /* لمعان ذهبي */
            --text-main: #f8fafc; /* نص أبيض مائل */
            --text-muted: #94a3b8; /* نص رمادي muted */
        }

        * {
            box-sizing: border-box;
            margin: 0;
            padding: 0;
            font-family: 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif;
            -webkit-tap-highlight-color: transparent; /* إزالة تأثير الضغط الأزرق */
        }

        body {
            background-color: var(--bg-dark);
            color: var(--text-main);
            padding-bottom: 80px; /* مسافة لشريط التنقل السفلي */
            min-height: 100vh;
        }

        /* الهيدر العلوي الفخم */
        header {
            background: linear-gradient(135deg, #0f172a, #064e3b, #0f172a);
            padding: 30px 20px;
            text-align: center;
            border-bottom: 2px solid var(--accent-gold);
            box-shadow: 0 4px 20px var(--accent-glow);
            border-bottom-left-radius: 25px;
            border-bottom-right-radius: 25px;
            margin-bottom: 15px;
        }

        header h1 {
            font-size: 26px;
            color: var(--accent-gold);
            margin-bottom: 5px;
            text-shadow: 0 0 10px var(--accent-glow);
            font-weight: 800;
        }

        header p {
            font-size: 14px;
            color: var(--text-muted);
        }

        /* حاويات الشاشات المحدثة */
        .container {
            padding: 20px;
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
            from { opacity: 0; transform: translateY(15px); }
            to { opacity: 1; transform: translateY(0); }
        }

        /* تنسيق كروت الراديو والأذكار الفخمة */
        .audio-card, .dhikr-card, .sira-card {
            background-color: var(--card-bg);
            border-radius: 20px;
            padding: 25px;
            margin-bottom: 20px;
            border: 1px solid #334155;
            box-shadow: 0 4px 6px rgba(0,0,0,0.2);
            transition: all 0.3s ease;
        }

        .dhikr-card:hover, .sira-card:hover {
            border-color: var(--accent-gold);
            box-shadow: 0 0 15px var(--accent-glow);
            transform: translateY(-2px);
        }

        /* عناوين ذهبية داخل الكروت */
        .card-header-gold {
            font-size: 18px;
            color: var(--accent-gold);
            margin-bottom: 15px;
            font-weight: 600;
            display: flex;
            align-items: center;
            gap: 10px;
        }

        .dhikr-text {
            font-size: 17px;
            line-height: 1.7;
            color: var(--text-main);
            margin-bottom: 20px;
            text-align: right;
        }

        /* أزرار التسبيح الذهبية */
        .counter-btn {
            background: linear-gradient(135deg, #334155, #1e293b);
            color: var(--accent-gold);
            border: 1px solid var(--accent-gold);
            padding: 12px 25px;
            border-radius: 30px;
            font-size: 18px;
            cursor: pointer;
            width: 100%;
            display: flex;
            justify-content: space-between;
            align-items: center;
            transition: all 0.2s;
            font-weight: bold;
        }

        .counter-btn:active {
            background-color: var(--accent-gold);
            color: var(--bg-dark);
            box-shadow: 0 0 20px var(--accent-glow);
        }

        /* راديو القرآن والقراء */
        select {
            width: 100%;
            padding: 15px;
            background-color: var(--bg-dark);
            color: white;
            border: 1px solid var(--accent-gold);
            border-radius: 12px;
            margin-bottom: 20px;
            font-size: 16px;
            color: var(--accent-gold);
        }

        audio {
            width: 100%;
            margin-top: 15px;
            accent-color: var(--accent-gold);
        }

        /* تنسيق السيرة النبوية */
        .sira-list {
            list-style: none;
        }

        .sira-item {
            border-bottom: 1px solid #334155;
            padding: 15px 0;
        }

        .sira-item:last-child {
            border-bottom: none;
        }

        .sira-title {
            color: var(--accent-gold);
            font-weight: 600;
            margin-bottom: 5px;
            font-size: 16px;
        }

        .sira-snippet {
            color: var(--text-muted);
            font-size: 14px;
            line-height: 1.5;
        }

        /* شريط التنقل السفلي الفخم (Nav Bar) */
        .nav-bar {
            position: fixed;
            bottom: 0;
            left: 0;
            right: 0;
            background-color: var(--card-bg);
            display: flex;
            justify-content: space-around;
            padding: 15px 0;
            border-top: 2px solid var(--accent-gold);
            box-shadow: 0 -4px 15px rgba(0,0,0,0.4);
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
            font-size: 12px;
            cursor: pointer;
            background: none;
            border: none;
            width: 25%;
        }

        .nav-item i {
            font-size: 24px;
            margin-bottom: 6px;
            transition: all 0.2s ease;
        }

        .nav-item.active {
            color: var(--accent-gold);
        }

        .nav-item.active i {
            transform: translateY(-4px);
            text-shadow: 0 0 10px var(--accent-glow);
        }
    </style>
</head>
<body>

    <header>
        <h1 id="app-title">خُطى الروحاني <i class="fa-solid asleep fa-star-and-crescent" style="color:var(--accent-gold); font-size: 20px;"></i></h1>
        <p id="app-status">تطبيق ديني شامل في كل خطوة</p>
    </header>

    <div class="container">
        
        <div id="quran-page" class="page active">
            <div class="card-header-gold"><i class="fa-solid fa-book-quran"></i> إذاعة وفيديوهات القرآن الكريم</div>
            <div class="audio-card">
                <label style="display:block; text-align:right; margin-bottom:10px; color:var(--text-muted)">اختر محطة الراديو الحي:</label>
                <select id="radio-select" onchange="changeRadio(this.value)">
                    <option value="https://backup.qurango.net/radio/tarteel">إذاعة المصحف المرتل (العفاسي)</option>
                    <option value="https://backup.qurango.net/radio/abdullah_basfar">عبد الله بصفر</option>
                    <option value="https://backup.qurango.net/radio/abdulbasit_mujawwad">عبد الباسط عبد الصمد (مجوّد)</option>
                    <option value="https://backup.qurango.net/radio/maher_al_muaiqly">ماهر المعيقلي</option>
                    <option value="https://backup.qurango.net/radio/minshawi_mujawwad">محمد صديق المنشاوي</option>
                    <option value="https://backup.qurango.net/radio/shuraym">سعود الشريم</option>
                </select>
                <audio id="main-audio" controls src="https://backup.qurango.net/radio/tarteel"></audio>
            </div>
        </div>

        <div id="azkar-page" class="page">
            <div class="card-header-gold"><i class="fa-solid fa-beads"></i> السبحة الإلكترونية وحصن المسلم</div>
            
            <div class="dhikr-card">
                <div class="card-header-gold"><i class="fa-solid fa-cloud-moon"></i> أذكار الصباح (مثال)</div>
                <p class="dhikr-text">"أَصْبَحْنَا وَأَصْبَحَ الْمُلْكُ لِلَّهِ وَالْحَمْدُ لِلَّهِ لَا إِلَهَ إِلَّا اللَّهُ وَحْدَهُ لَا شَرِيكَ لَهُ"</p>
                <button class="counter-btn" onclick="countDhikr(this)"><span>اضغط للتسبيح</span> <strong class="num">0 / 3</strong></button>
            </div>

            <div class="dhikr-card">
                <div class="card-header-gold"><i class="fa-solid fa-mosque"></i> السبحة العامة: سبحان الله وبحمده</div>
                <button class="counter-btn" onclick="countDhikr(this, 100)"><span>اضغط للتسبيح</span> <strong class="numE html>
<html lang="ar" dir="rtl">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>تطبيق خُطى الديني - النسخة الذهبية</title>
    <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.4.0/css/all.min.css">
    <style>
        :root {
            --bg-dark: #0f172a; /* خلفية داكنة جداً */
            --card-bg: #1e293b; /* خلفية الكروت */
            --accent-gold: #d4af37; /* ذهبي ملكي */
            --accent-glow: rgba(212, 175, 55, 0.3); /* لمعان ذهبي */
            --text-main: #f8fafc; /* نص أبيض مائل */
            --text-muted: #94a3b8; /* نص رمادي muted */
        }

        * {
            box-sizing: border-box;
            margin: 0;
            padding: 0;
            font-family: 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif;
            -webkit-tap-highlight-color: transparent; /* إزالة تأثير الضغط الأزرق */
        }

        body {
            background-color: var(--bg-dark);
            color: var(--text-main);
            padding-bottom: 80px; /* مسافة لشريط التنقل السفلي */
            min-height: 100vh;
        }

        /* الهيدر العلوي الفخم */
        header {
            background: linear-gradient(135deg, #0f172a, #064e3b, #0f172a);
            padding: 30px 20px;
            text-align: center;
            border-bottom: 2px solid var(--accent-gold);
            box-shadow: 0 4px 20px var(--accent-glow);
            border-bottom-left-radius: 25px;
            border-bottom-right-radius: 25px;
            margin-bottom: 15px;
        }

        header h1 {
            font-size: 26px;
            color: var(--accent-gold);
            margin-bottom: 5px;
            text-shadow: 0 0 10px var(--accent-glow);
            font-weight: 800;
        }

        header p {
            font-size: 14px;
            color: var(--text-muted);
        }

        /* حاويات الشاشات المحدثة */
        .container {
            padding: 20px;
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
            from { opacity: 0; transform: translateY(15px); }
            to { opacity: 1; transform: translateY(0); }
        }

        /* تنسيق كروت الراديو والأذكار الفخمة */
        .audio-card, .dhikr-card, .sira-card {
            background-color: var(--card-bg);
            border-radius: 20px;
            padding: 25px;
            margin-bottom: 20px;
            border: 1px solid #334155;
            box-shadow: 0 4px 6px rgba(0,0,0,0.2);
            transition: all 0.3s ease;
        }

        .dhikr-card:hover, .sira-card:hover {
            border-color: var(--accent-gold);
            box-shadow: 0 0 15px var(--accent-glow);
            transform: translateY(-2px);
        }

        /* عناوين ذهبية داخل الكروت */
        .card-header-gold {
            font-size: 18px;
            color: var(--accent-gold);
            margin-bottom: 15px;
            font-weight: 600;
            display: flex;
            align-items: center;
            gap: 10px;
        }

        .dhikr-text {
            font-size: 17px;
            line-height: 1.7;
            color: var(--text-main);
            margin-bottom: 20px;
            text-align: right;
        }

        /* أزرار التسبيح الذهبية */
        .counter-btn {
            background: linear-gradient(135deg, #334155, #1e293b);
            color: var(--accent-gold);
            border: 1px solid var(--accent-gold);
            padding: 12px 25px;
            border-radius: 30px;
            font-size: 18px;
            cursor: pointer;
            width: 100%;
            display: flex;
            justify-content: space-between;
            align-items: center;
            transition: all 0.2s;
            font-weight: bold;
        }

        .counter-btn:active {
            background-color: var(--accent-gold);
            color: var(--bg-dark);
            box-shadow: 0 0 20px var(--accent-glow);
        }

        /* راديو القرآن والقراء */
        select {
            width: 100%;
            padding: 15px;
            background-color: var(--bg-dark);
            color: white;
            border: 1px solid var(--accent-gold);
            border-radius: 12px;
            margin-bottom: 20px;
            font-size: 16px;
            color: var(--accent-gold);
        }

        audio {
            width: 100%;
            margin-top: 15px;
            accent-color: var(--accent-gold);
        }

        /* تنسيق السيرة النبوية */
        .sira-list {
            list-style: none;
        }

        .sira-item {
            border-bottom: 1px solid #334155;
            padding: 15px 0;
        }

        .sira-item:last-child {
            border-bottom: none;
        }

        .sira-title {
            color: var(--accent-gold);
            font-weight: 600;
            margin-bottom: 5px;
            font-size: 16px;
        }

        .sira-snippet {
            color: var(--text-muted);
            font-size: 14px;
            line-height: 1.5;
        }

        /* شريط التنقل السفلي الفخم (Nav Bar) */
        .nav-bar {
            position: fixed;
            bottom: 0;
            left: 0;
            right: 0;
            background-color: var(--card-bg);
            display: flex;
            justify-content: space-around;
            padding: 15px 0;
            border-top: 2px solid var(--accent-gold);
            box-shadow: 0 -4px 15px rgba(0,0,0,0.4);
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
            font-size: 12px;
            cursor: pointer;
            background: none;
            border: none;
            width: 25%;
        }

        .nav-item i {
            font-size: 24px;
            margin-bottom: 6px;
            transition: all 0.2s ease;
        }

        .nav-item.active {
            color: var(--accent-gold);
        }

        .nav-item.active i {
            transform: translateY(-4px);
            text-shadow: 0 0 10px var(--accent-glow);
        }
    </style>
</head>
<body>

    <header>
        <h1 id="app-title">خُطى الروحاني <i class="fa-solid asleep fa-star-and-crescent" style="color:var(--accent-gold); font-size: 20px;"></i></h1>
        <p id="app-status">تطبيق ديني شامل في كل خطوة</p>
    </header>

    <div class="container">
        
        <div id="quran-page" class="page active">
            <div class="card-header-gold"><i class="fa-solid fa-book-quran"></i> إذاعة وفيديوهات القرآن الكريم</div>
            <div class="audio-card">
                <label style="display:block; text-align:right; margin-bottom:10px; color:var(--text-muted)">اختر محطة الراديو الحي:</label>
                <select id="radio-select" onchange="changeRadio(this.value)">
                    <option value="https://backup.qurango.net/radio/tarteel">إذاعة المصحف المرتل (العفاسي)</option>
                    <option value="https://backup.qurango.net/radio/abdullah_basfar">عبد الله بصفر</option>
                    <option value="https://backup.qurango.net/radio/abdulbasit_mujawwad">عبد الباسط عبد الصمد (مجوّد)</option>
                    <option value="https://backup.qurango.net/radio/maher_al_muaiqly">ماهر المعيقلي</option>
                    <option value="https://backup.qurango.net/radio/minshawi_mujawwad">محمد صديق المنشاوي</option>
                    <option value="https://backup.qurango.net/radio/shuraym">سعود الشريم</option>
                </select>
                <audio id="main-audio" controls src="https://backup.qurango.net/radio/tarteel"></audio>
            </div>
        </div>

        <div id="azkar-page" class="page">
            <div class="card-header-gold"><i class="fa-solid fa-beads"></i> السبحة الإلكترونية وحصن المسلم</div>
            
            <div class="dhikr-card">
                <div class="card-header-gold"><i class="fa-solid fa-cloud-moon"></i> أذكار الصباح (مثال)</div>
                <p class="dhikr-text">"أَصْبَحْنَا وَأَصْبَحَ الْمُلْكُ لِلَّهِ وَالْحَمْدُ لِلَّهِ لَا إِلَهَ إِلَّا اللَّهُ وَحْدَهُ لَا شَرِيكَ لَهُ"</p>
                <button class="counter-btn" onclick="countDhikr(this)"><span>اضغط للتسبيح</span> <strong class="num">0 / 3</strong></button>
            </div>

            <div class="dhikr-card">
                <div class="card-header-gold"><i class="fa-solid fa-mosque"></i> السبحة العامة: سبحان الله وبحمده</div>
                <button class="counter-btn" onclick="countDhikr(this, 100)"><span>اضغط للتسبيح</span> <strong class="num">0 / 100</strong></button>
            </div>
        </div>

        <div id="sira-page" class="page">
            <div class="card-header-gold"><i class="fa-solid fa-history"></i> محطات من السيرة النبوية العطرة</div>
            <div class="sira-card">
                <ul class="sira-list">
                    <li class="sira-item">
                        <div class="sira-title">المولد المبارك</div>
                        <div class="sira-snippet">ولد النبي صلى الله عليه وسلم في عام الفيل، يتيم الأب، بمكة المكرمة...</div>
                    </li>
                    <li class="sira-item">
                        <div class="sira-title">البعثة النبوية</div>
                        <div class="sira-snippet">نزل عليه الوحي في غار حراء وهو ابن الأربعين، ليبدأ نشر الإسلام('
