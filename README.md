<!DOCTYPE html>
<html lang="ar" dir="rtl">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>تطبيق خُطى الديني</title>
    <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.4.0/css/all.min.css">
    <style>
        :root {
            --bg-dark: #0f172a;
            --card-bg: #1e293b;
            --accent-green: #10b981;
            --accent-glow: rgba(16, 185, 129, 0.2);
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
            padding-bottom: 80px;
            min-height: 100vh;
        }

        /* الهيدر العلوي */
        header {
            background: linear-gradient(135deg, #064e3b, #0f172a);
            padding: 25px 20px;
            text-align: center;
            border-bottom: 2px solid var(--accent-green);
            box-shadow: 0 4px 20px var(--accent-glow);
            border-bottom-left-radius: 20px;
            border-bottom-right-radius: 20px;
        }

        header h1 {
            font-size: 24px;
            color: var(--accent-green);
            margin-bottom: 5px;
            text-shadow: 0 0 10px var(--accent-glow);
        }

        header p {
            font-size: 14px;
            color: var(--text-muted);
        }

        /* حاويات الشاشات */
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
            animation: fadeIn 0.4s ease-in
