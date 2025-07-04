<!DOCTYPE html>
<html lang="id">
<head>
  <meta charset="UTF-8">
  <title>Form Kirim Pesan</title>
  <style>
    body { font-family: Arial; padding: 20px; background: #fdf5e6; }
    input, textarea { width: 100%; padding: 10px; margin-bottom: 10px; }
    button { padding: 10px 20px; background: brown; color: white; border: none; cursor: pointer; }
  </style>
</head>
<body>
  <h2>Kirim Pesan</h2>
  <form action="simpan.php" method="POST">
    <input type="text" name="nama" placeholder="Nama kamu" required>
    <textarea name="pesan" placeholder="Tulis pesanmu di sini..." rows="5" required></textarea>
    <button type="submit">Kirim</button>
  </form>
</body>
</html>
<?php>
if ($_SERVER["REQUEST_METHOD"] == "POST") {
    $nama = htmlspecialchars($_POST["nama"]);
    $pesan = htmlspecialchars($_POST["pesan"]);
    $baris = "[" . date("Y-m-d H:i:s") . "] $nama: $pesan\n";
    file_put_contents("pesan.txt", $baris, FILE_APPEND | LOCK_EX);
    echo "<h2>Pesan berhasil dikirim!</h2>";
    echo "<p><a href='index.html'>Kembali</a></p>";
} else {
    echo "Akses tidak valid.";
}
?>
