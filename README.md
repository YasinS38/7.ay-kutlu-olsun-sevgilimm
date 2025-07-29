<!DOCTYPE html>
<html lang="tr">
<head>
  <meta charset="UTF-8">
  <title>Aleyna & Yasin – 7. Ayımız</title>
  <style>
    body {
      margin: 0;
      font-family: 'Segoe UI', sans-serif;
      background: linear-gradient(to right, #ffe4e1, #fff0f5);
      color: #333;
    }

    header {
      text-align: center;
      padding: 40px;
      background-color: #ff99aa;
      color: white;
    }

    header h1 {
      margin: 0;
      font-size: 38px;
    }

    .photos {
      display: flex;
      flex-direction: column;
      align-items: center;
      gap: 30px;
      padding: 30px;
    }

    .photos img {
      width: 300px;
      height: auto;
      border-radius: 15px;
      box-shadow: 0 5px 15px rgba(0,0,0,0.2);
    }

    .photos p {
      margin-top: 10px;
      font-style: italic;
      font-size: 16px;
      color: #cc3366;
      text-align: center;
    }

    .dates {
      text-align: center;
      background-color: #ffc6d0;
      padding: 20px;
      font-size: 18px;
    }

    .message {
      max-width: 900px;
      margin: 40px auto;
      padding: 30px;
      background-color: #fff;
      border-radius: 15px;
      box-shadow: 0 0 20px rgba(0,0,0,0.1);
      font-size: 18px;
      line-height: 1.7;
    }

    .poll {
      text-align: center;
      padding: 40px;
    }

    .poll h2 {
      font-size: 26px;
    }

    button {
      background-color: #ff4d88;
      color: white;
      border: none;
      padding: 14px 28px;
      font-size: 18px;
      border-radius: 8px;
      cursor: pointer;
      transition: background 0.3s;
    }

    button:hover {
      background-color: #ff1a75;
    }

    .heart-rain {
      position: fixed;
      top: 0;
      left: 0;
      width: 100%;
      height: 100%;
      pointer-events: none;
      z-index: 999;
    }

    .heart {
      position: absolute;
      color: red;
      font-size: 24px;
      animation: fall 3s linear infinite;
    }

    @keyframes fall {
      0% {
        transform: translateY(-100px) rotate(0deg);
        opacity: 1;
      }
      100% {
        transform: translateY(100vh) rotate(360deg);
        opacity: 0;
      }
    }
  </style>
</head>
<body>

<header>
  <h1>7 Ay Oldu Aleyna ❤️</h1>
</header>

<div class="photos">
  <div>
    <img src="foto1.jpg" alt="Birlikte Fotoğraf 1">
    <p>“Bu gülüş için dünyayı yakarım.”</p>
  </div>
  <div>
    <img src="foto2.jpg" alt="Birlikte Fotoğraf 2">
    <p>“Sen yanımda ol, dünya umrumda değil.”</p>
  </div>
  <div>
    <img src="foto3.jpg" alt="Birlikte Fotoğraf 3">
    <p>“Gözlerine bakınca tüm savaşlar duruyor içimde.”</p>
  </div>
</div>

<div class="dates">
  <p>📌 <strong>Tanışma Tarihimiz:</strong> 5 Kasım – Snapchat üzerinden, MSÜ Polislik hakkında konuştuk 👮‍♀️</p>
  <p>📌 <strong>İlk Buluşmamız:</strong> 30 Aralık – Göz göze geldik, kalbimiz aynı anda attı 💞</p>
</div>

<div class="message">
  <h2>Seninle başlamak, en güzel karardı...</h2>
  <p>Aleyna,</p>
  <p>O gün Snapchat’te yazdığında, konumuz sadece polislikti belki ama kalbim o andan itibaren farklı atmaya başladı. Senin sesin, bakışın, düşüncelerin… Hepsi içime işledi. Şimdi 7 ay sonra, dönüp baktığımda “iyi ki yazmışsın” diyorum. Çünkü o gün kader çizgim değişti.</p>
  
  <p>Sana sadece aşık değilim, sana hayranım. Gücüne, kalbine, hayallerine. Seni sadece sevdiğim için değil, sana inandığım için yanındayım. Zor zamanlar yaşadık, yaşıyoruz… Ama asla yalnız değilsin. Bu yolda el ele yürüyoruz ve birlikte her şeyi aşacağız.</p>

  <p>Sana her baktığımda huzur buluyorum. Kokunu düşündüğümde içim ısınıyor. Yanında olmadığım her saniye bile sana olan sevgimi azaltmıyor. Aksine daha da büyüyor.</p>

  <p>Seninle sadece bu 7 ayı değil, kalan tüm ömrümü paylaşmak istiyorum. Ağladığında gözyaşlarını silmek, güldüğünde kahkahana ortak olmak, sustuğunda seni duymak istiyorum. Saçlarımız beyazladığında bile, aynı gözlerle bakmak istiyorum sana.</p>

  <p>Seninle her anı paylaşmak, her gülüşünü görmek, her hayalini desteklemek için buradayım. Seninle birlikte yaşlanmak, hayatı seninle yaşamak istiyorum.</p>
  <p>Bu 7 ay, sadece bir başlangıç. Daha nice aylar, yıllar ve anılar biriktireceğiz. Her anımızı değerli kılacağız. Seninle birlikte her şey daha güzel, daha anlamlı.</p>
  <p>İyi ki geldin hayatıma. İyi ki varsın. Ve iyi ki biz olduk.</p>

  <p>7. ayımız kutlu olsun Aleyna! ❤️</p>
  
  <p>♥ Yasin</p>
</div>

<div class="poll">
  <h2>💍 Küçük Bir Soru...</h2>
  <p><strong>7li aylar değil… Saçlarımızın beyazlığına var mısın Aleyna?</strong></p>
  <button onclick="showHearts()">Evet, sonsuza dek!</button>
</div>

<div class="heart-rain" id="heartRain"></div>

<script>
  function showHearts() {
    const container = document.getElementById('heartRain');
    for (let i = 0; i < 30; i++) {
      const heart = document.createElement('div');
      heart.className = 'heart';
      heart.style.left = Math.random() * 100 + 'vw';
      heart.style.animationDuration = (Math.random() * 2 + 2) + 's';
      heart.innerHTML = '❤️';
      container.appendChild(heart);
      setTimeout(() => heart.remove(), 4000);
    }
    alert('Ben çoktan EVET dedim bile ❤️');
  }
</script>

</body>
</html>
