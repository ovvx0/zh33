<!DOCTYPE html>
<html lang="ar">
<head>
  <meta charset="UTF-8" />
  <title>متجر T1</title>
  <style>
    body {
      background-color: #0e0e0e;
      color: #ffffff;
      font-family: 'Tahoma', sans-serif;
      text-align: center;
      margin: 0;
      padding: 40px;
    }

    h1 {
      color: #bb86fc;
      margin-bottom: 40px;
      font-size: 32px;
    }

    .button-container {
      display: flex;
      flex-wrap: wrap;
      justify-content: center;
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
    }

    .instagram { background-color: #e1306c; }
    .instagram:hover { background-color: #c92a5e; }

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
    }
  </style>
</head>
<body>

  <h1>أهلاً فانزاتي 💜</h1>

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
      <button class="dropbtn whatsapp" onclick="toggleDropdown(this)">📱 WhatsApp</button>
      <div class="dropdown-content">
        <a href="https://wa.me/966XXXXXXXXX" target="_blank">راسلني على واتساب</a>
      </div>
    </div>

    <div class="dropdown">
      <button class="dropbtn telegram" onclick="toggleDropdown(this)">📨 Telegram</button>
      <div class="dropdown-content">
        <a href="https://t.me/YourUsernameHere" target="_blank">@YourUsernameHere</a>
      </div>
    </div>

    <div class="dropdown">
      <button class="dropbtn twitter" onclick="toggleDropdown(this)">🐦 Twitter</button>
      <div class="dropdown-content">
        <a href="https://twitter.com/YourUsernameHere" target="_blank">@YourUsernameHere</a>
      </div>
    </div>

  </div>

  <script>
    function toggleDropdown(button) {
      document.querySelectorAll('.dropdown-content').forEach(drop => {
        if (drop !== button.nextElementSibling) {
          drop.classList.remove('show');
        }
      });

      const dropdown = button.nextElementSibling;
      dropdown.classList.toggle('show');
    }

    window.onclick = function(event) {
      if (!event.target.matches('.dropbtn')) {
        document.querySelectorAll('.dropdown-content').forEach(drop => {
          drop.classList.remove('show');
        });
      }
    };
  </script>

</body>
</html>

