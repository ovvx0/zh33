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
      background-color: #6200ee;
      color: white;
      padding: 14px 20px;
      font-size: 16px;
      border: none;
      border-radius: 8px;
      cursor: pointer;
      transition: background-color 0.3s ease;
    }

    .dropbtn:hover {
      background-color: #3700b3;
    }

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

  <h1>Welcome to T1 Store</h1>

  <div class="button-container">

    <div class="dropdown">
      <button class="dropbtn" onclick="toggleDropdown(this)">📸 Instagram</button>
      <div class="dropdown-content">
        <a href="https://instagram.com/z.h3rr" target="_blank">@z.h3rr</a>
      </div>
    </div>

    <div class="dropdown">
      <button class="dropbtn" onclick="toggleDropdown(this)">👻 Snapchat</button>
      <div class="dropdown-content">
        <a href="https://snapchat.com/add/z.h3r" target="_blank">@z.h3r</a>
      </div>
    </div>

    <div class="dropdown">
      <button class="dropbtn" onclick="toggleDropdown(this)">💬 WhatsApp</button>
      <div class="dropdown-content">
        <a href="https://wa.me/966XXXXXXXXX" target="_blank">WhatsApp Me</a>
      </div>
    </div>

    <div class="dropdown">
      <button class="dropbtn" onclick="toggleDropdown(this)">📨 Telegram</button>
      <div class="dropdown-content">
        <a href="https://t.me/YourUsernameHere" target="_blank">@YourUsernameHere</a>
      </div>
    </div>

    <div class="dropdown">
      <button class="dropbtn" onclick="toggleDropdown(this)">🐦 Twitter</button>
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
