<!DOCTYPE html>
<html lang="ja">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>コミュニティサイト</title>
    <style>
        body {
            font-family: Arial, sans-serif;
            margin: 0;
            padding: 0;
            text-align: center;
        }
        nav {
            background-color: #333;
            padding: 10px;
        }
        nav a {
            color: white;
            text-decoration: none;
            margin: 0 15px;
        }
        .container {
            padding: 20px;
        }
    </style>
</head>
<body>
    <nav>
        <a href="#home" onclick="showPage('home')">ホーム</a>
        <a href="#profile" onclick="showPage('profile')">プロフィール</a>
        <a href="#community" onclick="showPage('community')">コミュニティ</a>
    </nav>
    
    <div id="home" class="container">ホームページへようこそ！</div>
    <div id="profile" class="container" style="display:none;">プロフィールページです。</div>
    <div id="community" class="container" style="display:none;">コミュニティページです。</div>
    
    <script>
        function showPage(pageId) {
            document.querySelectorAll('.container').forEach(page => {
                page.style.display = 'none';
            });
            document.getElementById(pageId).style.display = 'block';
        }
    </script>
</body>
</html>
