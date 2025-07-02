 <!DOCTYPE html>
<html lang="id">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>Website Kelas 9B - SMPN 1 Pangkalan Lada</title>
  <style>
    body {
      margin: 0;
      font-family: 'Segoe UI', sans-serif;
      background-color: #fffaf0;
    }

    header {
      background-color: #8b4513;
      color: white;
      padding: 20px;
      text-align: center;
      position: relative;
    }

    nav {
      background-color: #fdd9a0;
      padding: 15px;
      display: flex;
      flex-wrap: wrap;
      justify-content: center;
      gap: 10px;
    }

    nav button {
      background-color: #f4c488;
      border: none;
      border-radius: 10px;
      padding: 10px 15px;
      font-weight: bold;
      cursor: pointer;
    }

    nav button:hover {
      background-color: #e0a96d;
    }

    #content {
      padding: 20px;
      text-align: center;
    }

    footer {
      background-color: #8b4513;
      color: white;
      text-align: center;
      padding: 20px;
    }

    .footer-link a {
      color: white;
      margin: 0 10px;
      text-decoration: none;
      font-weight: bold;
    }

    .music-btn {
      background-color: #f4c488;
      border: none;
      padding: 10px 20px;
      border-radius: 10px;
      margin-top: 10px;
      cursor: pointer;
    }

    #login-btn {
      position: absolute;
      right: 20px;
      top: 20px;
      background-color: #f4c488;
      padding: 8px 12px;
      border-radius: 8px;
      border: none;
      font-weight: bold;
    }

    img {
      max-width: 100%;
      border-radius: 10px;
      margin: 10px;
    }

    textarea {
      margin-top: 10px;
      border-radius: 8px;
      padding: 8px;
      width: 80%;
    }

    ul {
      list-style-type: none;
      padding: 0;
    }

    ul li {
      background-color: #ffe0b2;
      margin: 5px auto;
      padding: 8px;
      width: 80%;
      border-radius: 10px;
    }
  </style>
</head>
<body>

  <header>
    <button id="login-btn">Login Admin</button>
    <h1>SMPN 1 PANGKALAN LADA</h1>
    <h2>Website Kelas 9B</h2>
  </header>

  <nav>
    <button onclick="showContent('struktur')">Struktur Kelas</button>
    <button onclick="showContent('anggota')">Anggota Siswa</button>
    <button onclick="showContent('tatatertib')">Tata Tertib</button>
    <button onclick="showContent('kebersihan')">Peraturan Kebersihan</button>
    <button onclick="showContent('jadwal')">Jadwal Pelajaran</button>
    <button onclick="showContent('piket')">Jadwal Piket</button>
    <button onclick="showContent('tugas')">Tugas / PR</button>
    <button onclick="showContent('galeri')">Galeri Foto</button>
    <button onclick="showContent('komentar')">Pesan & Komentar</button>
  </nav>

  <div id="content">
    <h3>Selamat datang di Website Kelas 9B!</h3>
    <p>Klik menu di atas untuk melihat informasi penting dan seru seputar kelas kita 😊</p>
  </div>

  <footer>
    <p>Website Kelas 9B | Designed by: APutraN</p>
    <div class="footer-link">
      <a href="https://instagram.com" target="_blank">Instagram</a> |
      <a href="https://tiktok.com" target="_blank">TikTok</a>
    </div>
    <button class="music-btn" onclick="toggleMusic()">🎵 Putar Musik</button>
    <audio id="background-music" src="https://www.soundhelix.com/examples/mp3/SoundHelix-Song-1.mp3" loop></audio>
  </footer>

  <script>
    function showContent(menu) {
      const content = document.getElementById('content');
      switch (menu) {
        case 'struktur':
          content.innerHTML = "<h3>Struktur Kelas 9B</h3><p>Ketua: Putra<br>Wakil: Alif<br>Sekretaris: Rani<br>Bendahara: Salsa</p>";
          break;
        case 'anggota':
          content.innerHTML = "<h3>Anggota Siswa</h3><ul><li>Putra</li><li>Alif</li><li>Rani</li><li>Salsa</li><li>Iqbal</li><li>Nabila</li><li>Farhan</li><li>Dinda</li></ul>";
          break;
        case 'tatatertib':
          content.innerHTML = "<h3>Tata Tertib Kelas</h3><ol><li>Datang sebelum pukul 07.00</li><li>Berpakaian rapi & lengkap</li><li>Tidak membawa HP saat pelajaran</li><li>Bersikap sopan dan saling menghormati</li></ol>";
          break;
        case 'kebersihan':
          content.innerHTML = "<h3>Peraturan Kebersihan</h3><ul><li>Buang sampah pada tempatnya</li><li>Piket setiap hari sesuai jadwal</li><li>Tidak mencoret meja/kursi</li></ul>";
          break;
        case 'jadwal':
          content.innerHTML = `
            <h3>Jadwal Pelajaran</h3>
            <p><b>Senin:</b> PKN, B. Indonesia, Matematika<br>
            <b>Selasa:</b> IPA, IPS, PJOK<br>
            <b>Rabu:</b> B. Inggris, Seni Budaya, Prakarya<br>
            <b>Kamis:</b> B. Daerah, Matematika, PAI<br>
            <b>Jumat:</b> IPA, Informatika</p>
          `;
          break;
        case 'piket':
          content.innerHTML = `
            <h3>Jadwal Piket</h3>
            <ul>
              <li>Senin: Putra, Alif</li>
              <li>Selasa: Rani, Iqbal</li>
              <li>Rabu: Dinda, Farhan</li>
              <li>Kamis: Nabila, Salsa</li>
              <li>Jumat: Semua!</li>
            </ul>
          `;
          break;
        case 'tugas':
          content.innerHTML = `
            <h3>Tugas / PR</h3>
            <ul>
              <li>MTK: Halaman 45 nomor 1-10 (Kumpul Jumat)</li>
              <li>IPA: Buat laporan percobaan</li>
              <li>Bahasa Indonesia: Analisis puisi</li>
            </ul>
          `;
          break;
        case 'galeri':
          content.innerHTML = `
            <h3>Galeri Foto</h3>
            <img src="https://source.unsplash.com/400x250/?school" alt="Foto Sekolah">
            <img src="https://source.unsplash.com/400x250/?students" alt="Foto Siswa">
          `;
          break;
        case 'komentar':
          content.innerHTML = `
            <h3>Pesan & Komentar</h3>
            <textarea id="commentInput" rows="4" placeholder="Tulis komentar..."></textarea><br>
            <button onclick="addComment()">Kirim</button>
            <ul id="commentList"></ul>
          `;
          loadComments();
          break;
      }
    }

    function toggleMusic() {
      const music = document.getElementById('background-music');
      if (music.paused) {
        music.play();
      } else {
        music.pause();
      }
    }

    function addComment() {
      const input = document.getElementById('commentInput');
      const comment = input.value.trim();
      if (comment !== "") {
        let comments = JSON.parse(localStorage.getItem('comments')) || [];
        comments.push(comment);
        localStorage.setItem('comments', JSON.stringify(comments));
        input.value = "";
        loadComments();
      }
    }

    function loadComments() {
      const list = document.getElementById('commentList');
      list.innerHTML = "";
      const comments = JSON.parse(localStorage.getItem('comments')) || [];
      comments.forEach(c => {
        const li = document.createElement('li');
        li.textContent = c;
        list.appendChild(li);
      });
    }
  </script>

</body>
</html>
