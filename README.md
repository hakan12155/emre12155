<!DOCTYPE html>
<html lang="tr">
<head>
    <meta charset="UTF-8">
    <title>Başarı Merdiveni</title>
</head>
<body>
    <h1>Başarı Merdiveni Uygulamasına Hoşgeldiniz!</h1>
    <p>Buradan çalışma saatlerinizi kaydedebilirsiniz.</p>
</body>
</html>
<!DOCTYPE html>
<html lang="tr">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Mobil Uyumlu Site</title>
    <link rel="stylesheet" href="style.css">
</head>
<body>
    <header>
        <h1>Mobil Uyumlu Web Sitesi</h1>
    </header>

    <nav>
        <ul>
            <li><a href="#">Ana Sayfa</a></li>
            <li><a href="#">Hakkımızda</a></li>
            <li><a href="#">Hizmetler</a></li>
            <li><a href="#">İletişim</a></li>
        </ul>
    </nav>

    <section>
        <h2>Hoşgeldiniz!</h2>
        <p>Bu, mobil uyumlu bir web sitesi örneğidir. Telefonlar ve tabletler dahil her cihazda doğru şekilde görüntülenir.</p>
    </section>

    <footer>
        <p>&copy; 2024 Mobil Uyumlu Web Sitesi. Tüm hakları saklıdır.</p>
    </footer>
</body>
</html>
/* Genel stil */
body {
    font-family: Arial, sans-serif;
    margin: 0;
    padding: 0;
    background-color: #f4f4f4;
}

header {
    background-color: #4CAF50;
    color: white;
    padding: 10px 0;
    text-align: center;
}

nav {
    background-color: #333;
}

nav ul {
    list-style: none;
    margin: 0;
    padding: 0;
    display: flex;
    justify-content: center;
}

nav ul li {
    margin: 0 15px;
}

nav ul li a {
    color: white;
    text-decoration: none;
    padding: 10px 15px;
    display: block;
}

/* Responsive Design için Medya Sorguları */
@media (max-width: 768px) {
    nav ul {
        flex-direction: column;
        align-items: center;
    }

    nav ul li {
        margin: 10px 0;
    }

    section {
        padding: 10px;
    }
}

/* En küçük ekranlar için ekstra stil */
@media (max-width: 480px) {
    header {
        font-size: 18px;
    }

    section h2 {
        font-size: 20px;
    }
}
from flask import Flask, render_template

app = Flask(__name__)

@app.route('/')
def index():
    return render_template('index.html')

if __name__ == '__main__':
    app.run(debug=True)
 
