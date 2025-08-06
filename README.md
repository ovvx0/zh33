
<html lang="ar">
<head>
  <meta charset="UTF-8" />
  <title>خاص </title>
  <style>
    /* شاشة البداية */
    #intro {
      position: fixed;
      top: 0;
      left: 0;
      width: 100%;
      height: 100%;
      background-color: #0e0e0e;
      color: #ffffff;
      display: flex;
      justify-content: center;
      align-items: center;
      font-size: 36px;
      font-family: 'Tahoma', sans-serif;
      z-index: 9999;
      opacity: 1;
      animation: fadeOut 2.5s ease forwards;
      animation-delay: 1.5s;
    }

    @keyframes fadeOut {
      0% { opacity: 1; }
      100% { opacity: 0; visibility: hidden; }
    }

    body {
      background-color: #0e0e0e;
      color: #ffffff;
      font-family: 'Tahoma', sans-serif;
      text-align: center;
      margin: 0;
      padding: 40px;
    }

    h1 {
      color: #ffffff;
      margin-bottom: 40px;
      font-size: 32px;
    }

    .button-container {
      display: flex;
      flex-direction: column;
      align-items: center;
      gap: 20px;
    }

    .dropdown {
      position: relative;
      display: inline-block;
    }

    .dropbtn {
      color: white;
      padding: 14px 20px;
      font-size: 16px;
      border: none;
      border-radius: 8px;
      cursor: pointer;
      transition: background-color 0.3s ease;
      width: 220px;
    }

    .instagram { background-color: #cb2be0; }
    .instagram:hover { background-color: #c225c7; }

    .snapchat { background-color: #fffc00; color: #000; }
    .snapchat:hover { background-color: #e6e200; }

    .whatsapp { background-color: #25d366; }
    .whatsapp:hover { background-color: #1da851; }

    .telegram { background-color: #0088cc; }
    .telegram:hover { background-color: #007ab8; }

    .twitter { background-color: #14171a; }
    .twitter:hover { background-color: #000000; }

    .dropdown-content {
      display: none;
      position: absolute;
      background-color: #1f1f1f;
      min-width: 200px;
      border-radius: 6px;
      box-shadow: 0 4px 8px rgba(0,0,0,0.2);
      z-index: 1;
      text-align: center;
      left: 0;
      opacity: 0;
      transform: translateY(-10px);
      transition: opacity 0.3s ease, transform 0.3s ease;
    }

    .dropdown-content a {
      color: #ffffff;
      padding: 14px;
      text-decoration: none;
      display: block;
      font-weight: bold;
      font-size: 16px;
      transition: background-color 0.2s ease;
    }

    .dropdown-content a:hover {
      background-color: #2a2a2a;
    }

    .show {
      display: block;
      opacity: 1 !important;
      transform: translateY(0) !important;
    }
  </style>
</head>
<body>

  <!-- شاشة ترحيب -->
  <div id="intro">أهلاً  </div>

  <!-- صوت الضغط -->
  <audio id="clickSound" src="https://cdn.pixabay.com/audio/2022/03/15/audio_f7c8d1b66b.mp3" preload="auto"></audio>

 <h1>🎈أهلاً </h1>

  <div class="button-container">

    <div class="dropdown">
      <button class="dropbtn instagram" onclick="toggleDropdown(this)">📸 Instagram</button>
      <div class="dropdown-content">
        <a href="https://instagram.com/z.h3rr" target="_blank">@z.h3rr</a>
      </div>
    </div>

    <div class="dropdown">
      <button class="dropbtn snapchat" onclick="toggleDropdown(this)">👻 Snapchat</button>
      <div class="dropdown-content">
        <a href="https://snapchat.com/add/z.h3r" target="_blank">@z.h3r</a>
      </div>
    </div>

    <div class="dropdown">
      <button class="dropbtn whatsapp" onclick="toggleDropdown(this)"> WhatsApp</button>
      <div class="dropdown-content">
        <a href="https://wa.me/966XXXXXXXXX" target="_blank">راسلني على واتساب</a>
      </div>
    </div>

    <div class="dropdown">
      <button class="dropbtn telegram" onclick="toggleDropdown(this)"> Telegram</button>
      <div class="dropdown-content">
        <a href="https://t.me/YourUsernameHere" target="_blank">@YourUsernameHere</a>
      </div>
    </div>

    <div class="dropdown">
      <button class="dropbtn twitter" onclick="toggleDropdown(this)">X Twitter</button>
      <div class="dropdown-content">
        <a href="https://twitter.com/YourUsernameHere" target="_blank">@YourUsernameHere</a>
      </div>
    </div>

  </div>

 <script>
  const sound = document.getElementById("clickSound");

  function toggleDropdown(button) {
    sound.currentTime = 0;
    sound.play();

    document.querySelectorAll('.dropdown-content').forEach(drop => {
      if (drop !== button.nextElementSibling) {
        drop.classList.remove('show');
      }
    });

    const dropdown = button.nextElementSibling;

    if (dropdown.classList.contains('show')) {
      dropdown.classList.remove('show');
    } else {
      dropdown.style.display = 'block';
      setTimeout(() => {
        dropdown.classList.add('show');
      }, 10);
    }
  }

  // إغلاق القوائم عند الضغط خارجها
  window.onclick = function(event) {
    if (!event.target.matches('.dropbtn')) {
      document.querySelectorAll('.dropdown-content').forEach(drop => {
        drop.classList.remove('show');
      });
    }
  };

  // 🎯 التعامل مع الضغط مرتين على الأزرار
  document.querySelectorAll('.dropbtn').forEach(button => {
    button.addEventListener('dblclick', (e) => {
      const bubble = document.createElement('div');
      bubble.textContent = 'اهدأ اهدأ ';
      bubble.style.position = 'absolute';
      bubble.style.top = '-30px';
      bubble.style.left = '50%';
      bubble.style.transform = 'translateX(-50%)';
      bubble.style.background = '#ff5e5e';
      bubble.style.color = 'white';
      bubble.style.padding = '5px 10px';
      bubble.style.borderRadius = '10px';
      bubble.style.fontSize = '14px';
      bubble.style.opacity = '0';
      bubble.style.transition = 'opacity 0.3s ease, transform 0.3s ease';
      bubble.style.zIndex = '1000';

      button.style.position = 'relative';
      button.appendChild(bubble);

      // ظهور الفقاعة
      setTimeout(() => {
        bubble.style.opacity = '1';
        bubble.style.transform = 'translateX(-50%) translateY(-10px)';
      }, 10);

      // اختفاء بعد ثانيتين
      setTimeout(() => {
        bubble.style.opacity = '0';
        bubble.style.transform = 'translateX(-50%) translateY(-20px)';
        setTimeout(() => {
          bubble.remove();
        }, 300);
      }, 2000);
    });
  });

  // تغيير لون h1 بعد شاشة الترحيب
  setTimeout(() => {
    document.querySelector("h1").style.color = "white";
  }, 4000);
</script>


</body>
</html>
