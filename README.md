<!DOCTYPE html>
<html lang="id">
<head>
  <meta charset="UTF-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1.0"/>
  <title>Hakiman - Portofolio</title>
  <link href="https://fonts.googleapis.com/css2?family=Poppins:wght@500&display=swap" rel="stylesheet" />
  <style>
    * {
      box-sizing: border-box;
      padding: 0;
      margin: 0;
    }

    body {
      font-family: 'Poppins', sans-serif;
      background: black url('alok3.gif') no-repeat center center fixed;
      background-size: cover;
      height: 100vh;
      display: flex;
      align-items: center;
      justify-content: center;
      color: white;
    }

    .container {
      text-align: center;
      padding: 20px;
      max-width: 500px;
      width: 100%;
    }

    .profile-img {
      width: 120px;
      height: 120px;
      border-radius: 50%;
      object-fit: cover;
      border: 3px solid white;
      margin-bottom: 20px;
    }

    .name {
      font-size: 24px;
      font-weight: bold;
      margin-bottom: 8px;
      height: 30px;
    }

    .desc {
      font-size: 14px;
      color: #ccc;
      margin-bottom: 20px;
    }

    .social-icons img {
      width: 30px;
      margin: 5px;
      filter: brightness(0) invert(1);
      transition: transform 0.3s ease;
    }

    .social-icons img:hover {
      transform: scale(1.2);
    }

    .buttons a {
      display: block;
      background: white;
      color: black;
      text-decoration: none;
      margin: 10px auto;
      padding: 12px;
      border-radius: 30px;
      width: 80%;
      max-width: 250px;
      font-weight: bold;
      transition: transform 0.2s ease;
    }

    .buttons a:hover {
      transform: scale(1.05);
    }

    @media (max-width: 480px) {
      .name {
        font-size: 20px;
      }
      .desc {
        font-size: 13px;
      }
    }
  </style>
</head>
<body>

  <div class="container">
    <img src="ui11.png" alt="Foto Profil" class="profile-img" />
    <div class="name" id="typed-name"></div>
    <div class="desc">INFORMATICS ENTHUSIAST • TECH GENERALIST • GAME • CYBER • CODE</div>

    <div class="social-icons">
      <a href="https://www.tiktok.com/@hans_.py?_t=ZS-8wFFLQvU5Bf&_r=1" target="_blank"><img src="tiktok1.png" alt="TikTok"></a>
      <a href="https://www.instagram.com/hakiman_nurkholis" target="_blank"><img src="ig.png" alt="Instagram"></a>
      <a href="https://www.youtube.com/@Hans.pyyyyy" target="_blank"><img src="yt.png" alt="YouTube"></a>
      <a href="https://github.com/hans_.pyy/" target="_blank"><img src="gt.png" alt="GitHub"></a>
      <a href="https://t.me/hans_.py" target="_blank"><img src="tl.png" alt="Telegram"></a>
      <a href="https://www.facebook.com/profile.php?id=61576289065160" target="_blank"><img src="fb.png" alt="Facebook"></a>
    </div>

    <div class="buttons">
      <a href="https://piandi.vercel.app" target="_blank">Portofolio</a>
      <a href="https://piandi.vercel.app/#achievements" target="_blank">Pencapaian</a>
      <a href="https://piandi.vercel.app/hans-freefire" target="_blank">Game Hans</a>
    </div>
  </div>

  <script>
    const typedName = document.getElementById('typed-name');
    const names = ['HAKIMAN NURHOLIS', 'Hans'];
    let index = 0;
    let charIndex = 0;
    let deleting = false;

    function type() {
      let currentName = names[index];
      if (deleting) {
        typedName.textContent = currentName.substring(0, charIndex--);
        if (charIndex < 0) {
          deleting = false;
          index = (index + 1) % names.length;
        }
      } else {
        typedName.textContent = currentName.substring(0, charIndex++);
        if (charIndex > currentName.length) {
          deleting = true;
          setTimeout(type, 1000);
          return;
        }
      }
      setTimeout(type, deleting ? 50 : 100);
    }

    type();
  </script>

</body>
</html>
