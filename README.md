# Lab8_php_database
Nama: Doni Alvero <p>
Nim: 312410663 <P>
Kelas: TI.24.A.5 <P>
Jurusan: Teknik Informatika <p>
Mata Kuliah: Pemograman Web 1 <p>

### Menjalankan MySQL Server
menunjukkan bahwa lingkungan pengembangan web lokal (web server dan database) pada komputer tersebut sedang aktif dan berjalan normal. Tujuan Utamanya Digunakan untuk menghidupkan `(Start)` dan mematikan `(Stop)` modul-modul server utama. Apache `(Web Server)`: Berjalan `(Running)` pada Port 80 dan 443 & MySQL `(Database Server)`: Berjalan `(Running)` pada Port 3306. Web Server xammp
<img width="953" height="642" alt="Web Server xammp" src="https://github.com/user-attachments/assets/eb4e7e6b-bc20-41a4-9799-abc32e8cd79f" />

### Membuat Database 
langkah-langkah dalam mengelola database menggunakan phpMyAdmin pada lingkungan lokal `(http://localhost)`.
1.  `(Membuat Database1.jpg)`: Menunjukkan proses pembuatan database baru. Database diberi nama latihan1 dengan collation utf8mb4_general_ci.
<img width="1918" height="1017" alt="Membuat Database1" src="https://github.com/user-attachments/assets/553a4d43-8c8e-4136-8c06-d8735e624ebf" />
2.  `(Membuat Database2.jpg)`: Menunjukkan struktur dari sebuah tabel di dalam database. Nama tabelnya adalah tbl_barang `(kemungkinan besar di dalam database latihan1 atau database lain bernama latihan)`. Tabel ini memiliki kolom-kolom untuk data barang seperti id_barang `(PRIMARY KEY, AUTO_INCREMENT)`, kategori, nama, gambar, harga_beli `(DECIMAL)`, harga_jual `(DECIMAL)`, dan stok.
<img width="1918" height="1018" alt="Membuat Database2" src="https://github.com/user-attachments/assets/7ca73746-4b6e-4349-95bd-07ddbc4fcfea" />

### Membuat Tabel 
1. id_barang: Kunci utama `(Primary Key)` yang akan bertambah nilainya secara otomatis `(auto_increment)`.
2. kategori dan nama: Untuk menyimpan data teks `(VARCHAR)` barang.
3. gambar: Kemungkinan untuk menyimpan nama file atau path gambar.
4. harga_beli dan harga_jual: Menggunakan tipe data DECIMAL`(10,0)`, cocok untuk menyimpan nilai mata uang atau harga.
5. stok: Untuk menyimpan jumlah stok barang menggunakan bilangan bulat `(INT)`.
<img width="1918" height="1018" alt="Membuat Tabel" src="https://github.com/user-attachments/assets/107f2c5e-2c33-4331-a508-07b2a8a2abf0" />

### Menambahkan Data dicmd
menambahkan 6 data produk ke tabel data_barang menggunakan query INSERT via CLI dan memverifikasi keberhasilannya menggunakan query SELECT.
<img width="1918" height="927" alt="Menambahkan Data cmd" src="https://github.com/user-attachments/assets/de2355df-cad5-48a8-8714-a0817ea23bef" />

### mengakses direktory pada web server dengan mengakses URL
Halaman ini adalah daftar isi (direktori) dari folder Lab8_php_database yang berada di dalam lingkungan server lokal Index of `(http://localhost/Lab8_php_database/)`. 
<img width="1918" height="1020" alt="index" src="https://github.com/user-attachments/assets/769cd6d0-047b-44ca-b195-9396817a1ba1" />

### Membuat file koneksi database
menunjukkan hasil eksekusi dari file koneksidatabase.php di browser `(http://localhost/Lab8_php_database/koneksidatabase.php)`. Teks yang ditampilkan di halaman tersebut adalah: "Koneksi berhasil".
<img width="1918" height="1017" alt="koneksi database" src="https://github.com/user-attachments/assets/a3c2645d-5de1-4b18-a707-be28c4abe143" />

### menampilkan data `(Read)`
Aplikasi web berhasil terhubung dengan database & menampilkan data dari tabel data_barang `(atau sejenisnya)` dalam bentuk tabel yang rapi di browser.
<img width="1918" height="831" alt="Menampilkan Data Index" src="https://github.com/user-attachments/assets/e6483709-e2c4-4bd0-82d8-cc6474bf00db" />

### Menambah Data `(Create)`
Data yang Diinput: Sebuah produk baru dengan ID HP007, Nama Asus ROG Phone 9 Pro `(kategori Gaming)`, Harga Beli Rp 22.000.000, Harga Jual Rp 18.000.000, Stok 100, dan disertai unggahan file foto & di mana data dikumpulkan dari form dan siap dikirim ke database saat tombol "Tambah Handphone" ditekan.di mana data dikumpulkan dari form dan siap dikirim ke database saat tombol "Tambah Handphone" ditekan.
<img width="1917" height="677" alt="Menambah Data (Create)1" src="https://github.com/user-attachments/assets/ac4f4120-1a03-4a8c-9bbd-3544f784a3cd" />

### Mengubah Data `(Update)`
Verifikasi Produk baru dengan ID HP007 `(Asus ROG Phone 9 Pro)` telah berhasil ditambahkan ke baris terakhir tabel.
<img width="1918" height="1018" alt="Menambah Data (Create)2" src="https://github.com/user-attachments/assets/ab7ddb00-2026-4f8c-b426-d6123a31635e" />

###Menghapus Data `(Delete)`
1. Saat tombol Hapus pada baris data HP007 diklik, sebuah pop-up konfirmasi muncul & Ini adalah langkah keamanan standar untuk mencegah penghapusan data yang tidak disengaja.
<img width="1918" height="1017" alt="Mengubah Data (Update)1" src="https://github.com/user-attachments/assets/101386c2-2b1a-4bc6-b8b0-ee929d301856" />
2. Setelah pengguna memilih OK pada pop-up konfirmasi, sistem memproses permintaan tersebut & Ini mengonfirmasi bahwa query DELETE telah berhasil dieksekusi di database.
<img width="1918" height="1018" alt="Mengubah Data (Update)2" src="https://github.com/user-attachments/assets/e7556844-e4f3-4298-86f1-b9c9367907f0" />
3. Halaman katalog (tabel) dimuat ulang, Data dengan ID Barang HP007 (Asus ROG Phone 9 Pro) telah hilang dari daftar & Tabel hanya menampilkan 6 data awal `(HP001 hingga HP006)`.
<img width="1918" height="956" alt="Mengubah Data (Update)3" src="https://github.com/user-attachments/assets/b4757c68-e1fb-4908-9660-3a5bb5af323c" />

### Berikut codingan keseluruhannya 
```php
<!DOCTYPE html>
<html lang="id">
<head>
  <meta charset="UTF-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1.0"/>
  <title>Pemesanan Handphone & Dashboard</title>
  <style>
    /* === STYLE LOGIN & UMUM === */
    body {
      font-family: 'Segoe UI', sans-serif;
      margin: 0;
      padding: 0;
      background: #f5f7fa;
    }

    .login-page {
      /* Latar belakang hitam */
      background: #000000;
      display: flex;
      justify-content: center;
      align-items: center;
      height: 100vh;
    }

    .container {
      background: #fff;
      border-radius: 15px;
      width: 350px;
      padding: 20px 30px;
      box-shadow: 0 4px 12px rgba(0,0,0,0.2);
      text-align: center;
      position: relative;
    }

    .container img { width: 100px; margin-bottom: 15px; }

    h2 { margin: 0; color: #2c2c2c; font-size: 22px; margin-bottom: 20px; }

    input[type="email"], input[type="password"], input[type="text"], input[type="number"], select {
      width: 90%;
      padding: 10px;
      margin: 8px 0;
      border-radius: 6px;
      border: 1px solid #ccc;
    }
    
    .form-tambah input[type="text"], .form-tambah input[type="number"], .form-tambah select {
        width: 100%; /* Override default width 90% in small form */
    }

    button {
      width: 95%;
      padding: 10px;
      background-color: #4c51bf;
      color: white;
      border: none;
      border-radius: 6px;
      font-weight: bold;
      cursor: pointer;
      margin-top: 10px;
    }

    button:hover { background-color: #434190; }

    .links { margin-top: 15px; display: flex; justify-content: space-around; }
    .links a { color: #4c51bf; cursor: pointer; text-decoration: underline; }

    .modal { display: none; position: fixed; z-index: 30; left: 0; top: 0; width: 100%; height: 100%; background: rgba(0,0,0,0.6); }
    .modal-content {
      background: #fff; margin: 5% auto; padding: 20px; width: 420px; border-radius: 10px; text-align: left;
      position: relative; overflow-y: auto; max-height: 90vh;
    }
    .close { position: absolute; top: 8px; right: 10px; cursor: pointer; color: #555; font-weight: bold; font-size: 18px; }
    .close:hover { color: red; }

    .btn-secondary { background-color: #ccc; color: black; border: none; width: 45%; border-radius: 6px; padding: 8px; cursor: pointer; }
    .btn-primary { background-color: #4c51bf; color: white; border: none; width: 45%; border-radius: 6px; padding: 8px; cursor: pointer; }
    .btn-primary:hover { background-color: #434190; }

    /* === DASHBOARD === */
    .dashboard-page { display: none; background: #f5f7fa; min-height: 100vh; color: #333; }
    header {
      background: linear-gradient(90deg, #4a90e2, #007bff);
      color: white; padding: 20px; text-align: center; border-bottom-left-radius: 20px; border-bottom-right-radius: 20px;
    }

    .container-dashboard { padding: 20px; }
    .menu { display: grid; grid-template-columns: repeat(auto-fit, minmax(160px, 1fr)); gap: 20px; margin-top: 30px; }
    .menu button {
      background: white; border: 2px solid #007bff; border-radius: 15px; padding: 20px; font-size: 16px; font-weight: 600;
      cursor: pointer; transition: 0.3s; box-shadow: 0 4px 10px rgba(0, 0, 0, 0.05);
    }
    .menu button:hover { background: #007bff; color: white; transform: scale(1.05); }

    footer { text-align: center; margin-top: 40px; color: #777; font-size: 14px; }

    /* === KATALOG & LAPORAN === */
    #katalogSection { display: none; margin-top: 30px; }
    table { width: 100%; border-collapse: collapse; background: white; margin-bottom: 20px; }
    th, td { border: 1px solid #ccc; padding: 8px; text-align: center; vertical-align: middle; }
    th { background-color: #007bff; color: white; }
    td img { max-height:100px; max-width: 120px; object-fit: contain; display:block; margin:0 auto; }
    .table-responsive { overflow-x: auto; }

    .form-tambah { background: #fff; padding: 15px; border-radius: 10px; box-shadow: 0 2px 6px rgba(0,0,0,0.1); }
    .form-tambah input { width: 100%; margin: 5px 0; padding: 8px; }

    /* === TRACKING PENGIRIMAN (Cleanup) === */
    .small-btn { padding:8px 12px; border-radius:6px; border:none; cursor:pointer; background:#4c51bf; color:white; }
    /* Perubahan warna/padding sesuai permintaan */
    .small-btn.delete-btn { background:#ef4444; color:white; padding: 6px 10px; font-size: 13px; margin-top: 4px; } /* Margin-top ditambahkan agar tombol tidak terlalu rapat */
    .small-btn.delete-btn:hover { background: #dc2626; }
    .small-btn:hover { background:#434190; }

    /* responsive */
    @media (max-width:600px){
      .modal-content { width: 92%; }
      .container { width: 92%; }
      .tracking-controls { flex-direction: column; align-items: stretch; }
      td img { max-height:70px; }
      .table-responsive table { font-size: 12px; }
      .table-responsive th, .table-responsive td { padding: 6px; }
    }
  </style>
</head>
<body>

  <div class="login-page" id="loginPage">
    <div class="container">
      <img src="Logo Toko Handphone.png" alt="Logo">
      <h2>Login Pemesanan Handphone</h2>

      <input type="email" id="email" placeholder="Email"><br>
      <input type="password" id="password" placeholder="Password"><br>
      <button onclick="login()">Login</button>

      <div class="links">
        <a onclick="openModal('forgotModal')">Lupa Password</a>
        <a onclick="openModal('registerModal')">Daftar</a>
      </div>

      <div class="footer-text">
        Baca <a onclick="openModal('syaratKetentuanModal')">Syarat & Ketentuan</a> atau <a onclick="openModal('kebijakanPrivasiModal')">Kebijakan Privasi</a>
      </div>
    </div>
  </div>

  <div id="forgotModal" class="modal">
    <div class="modal-content">
      <span class="close" onclick="closeModal('forgotModal')">&times;</span>
      <h3>Lupa Password</h3>
      <p>Masukkan email Anda untuk reset password:</p>
      <input type="email" placeholder="Email"><br><br>
      <button class="btn-primary">Kirim</button>
    </div>
  </div>

  <div id="registerModal" class="modal">
    <div class="modal-content">
      <span class="close" onclick="closeModal('registerModal')">&times;</span>
      <h3>Lengkapi Identitas Anda</h3>
      <p>Silahkan lengkapi data diri Anda.</p>
      <input type="email" placeholder="Email Anda">
      <input type="text" placeholder="Nama Lengkap">
      <input type="text" placeholder="Nomor Ponsel">
      <input type="text" placeholder="Alamat Sesuai Identitas">
      <select>
        <option value="">Kecamatan</option>
        <option value="Gambir">Gambir</option>
        <option value="Menteng">Menteng</option>
        <option value="Tebet">Tebet</option>
      </select>
      <input type="password" placeholder="Kata Sandi">
      <input type="password" placeholder="Konfirmasi Kata Sandi">

      <p class="footer-text">
        Dengan mendaftar, saya menyetujui <a onclick="openModal('syaratKetentuanModal')">Syarat & Ketentuan</a> serta <a onclick="openModal('kebijakanPrivasiModal')">Kebijakan Privasi</a>
      </p>

      <div style="display:flex; justify-content:space-around; margin-top:15px;">
        <button class="btn-secondary" onclick="closeModal('registerModal')">Sebelumnya</button>
        <button class="btn-primary">Selanjutnya</button>
      </div>
    </div>
  </div>

  <div id="syaratKetentuanModal" class="modal">
    <div class="modal-content">
      <span class="close" onclick="closeModal('syaratKetentuanModal')">&times;</span>
      <h3>Syarat & Ketentuan Toko Handphone Online</h3>
      <p>Konten Syarat & Ketentuan</p>
    </div>
  </div>

  <div id="kebijakanPrivasiModal" class="modal">
    <div class="modal-content">
      <span class="close" onclick="closeModal('kebijakanPrivasiModal')">&times;</span>
      <h3>Kebijakan Privasi Toko Handphone Online</h3>
      <p>Konten Kebijakan Privasi</p>
    </div>
  </div>

  <div class="dashboard-page" id="dashboardPage">
    <header>
      <h1 id="greeting">Selamat Datang!</h1>
      <p>Toko Handphone Online Dashboard</p>
    </header>

    <div class="container-dashboard">
      <h2>Dashboard Menu</h2>
      <div class="menu">
        <button onclick="tampilkanKatalog()">📱 Informasi Katalog</button>
      </div>

      <div id="katalogSection">
        <h2>📱 Informasi Stok / Katalog Handphone</h2>
        <div class="table-responsive">
          <table id="tabelKatalog">
            <thead>
              <tr>
                <th>Id Barang</th>
                <th>Nama Handphone</th>
                <th>Kategori</th>
                <th>Harga Beli</th>
                <th>Harga Jual</th>
                <th>Edisi</th>
                <th>Stok</th>
                <th>Foto</th>
                <th>Aksi</th> 
                </tr>
            </thead>
            <tbody></tbody>
          </table>
        </div>
        <div class="form-tambah">
          <h3>Tambah Handphone Baru</h3>
          <input type="text" id="kodeBarang" placeholder="Id Barang">
          <input type="text" id="isbnInput" placeholder="Nama Handphone">
          <input type="text" id="namaBarang" placeholder="Kategori (contoh: Flagship/Gaming)">
          <input type="text" id="hargaBeli" placeholder="Harga Beli (contoh: Rp 10.000.000)">
          <input type="text" id="hargaJual" placeholder="Harga Jual (contoh: Rp 12.000.000)">
          <input type="text" id="edisi" placeholder="Edisi/Seri">
          <input type="number" id="stok" placeholder="Jumlah Stok">
          <input type="text" id="pathFoto" placeholder="(Opsional) Nama file atau URL, contoh: samsung_s25.jpg">
          <label style="font-size:13px;color:#555;margin-top:6px;display:block;">Atau upload file foto:</label>
          <input type="file" id="fotoUpload" accept="image/*">
          <div style="display:flex; gap:8px; margin-top:8px;">
            <button onclick="tambahBuku()" class="small-btn" style="width:100%;">Tambah Handphone</button>
            </div>
          <div id="previewFoto" style="margin-top:8px; font-size:13px; color:#333;"></div>
        </div>
      </div>
    </div>

    <footer>
      © 2025 Toko Buku Online. Semua Hak Dilindungi.
    </footer>
  </div>

<script>
    /* === === DATA MODELLING (DIUBAH) === === */
    function uid() { return 'id-' + Math.random().toString(36).slice(2, 9); }

    var dataPengguna = [
      { id: 1, nama: "Rina Wulandari", email: "rina@gmail.com", password: "rina123", role: "User" },
      { id: 2, nama: "Agus Pranoto", email: "agus@gmail.com", password: "agus123", role: "User" },
      // ADMIN ACCOUNT - PASTIKAN EMAIL DAN PASSWORD SAMA PERSIS DENGAN INPUT
      { id: 3, nama: "Siti Marlina", email: "siti@gmail.com", password: "siti123", role: "Admin" }
    ];

    const KATALOG_LS_KEY = "tokoBuku_dataKatalog_v3_hp"; // Versi baru untuk data handphone
    const DEFAULT_KATALOG = [
      // MAPPING: kodeBarang=Id Barang, isbn=Nama Handphone, namaBarang=Kategori
      { kodeBarang: "HP001", isbn: "Samsung Galaxy S25", namaBarang: "Flagship", edisi: "2025", stok: 50, hargaBeli: "Rp 23000000", hargaJual: "Rp 20000000", hargaBeliNumerik: 10000000, hargaJualNumerik: 12000000, pathFoto: "Samsung.png" },
      { kodeBarang: "HP002", isbn: "Xiaomi 17 Pro Max", namaBarang: "Flagship", edisi: "2025", stok: 75, hargaBeli: "Rp 18000000", hargaJual: "Rp 15000000", hargaBeliNumerik: 8000000, hargaJualNumerik: 9500000, pathFoto: "Xiomi.png" },
      { kodeBarang: "HP003", isbn: "Oppo Find X8 Pro", namaBarang: "Mid-Range", edisi: "2025", stok: 100, hargaBeli: "Rp 19000000", hargaJual: "Rp 16000000", hargaBeliNumerik: 5500000, hargaJualNumerik: 7000000, pathFoto: "Oppo.png" },
      { kodeBarang: "HP004", isbn: "iPhone 17 Pro Max", namaBarang: "Flagship", edisi: "2025", stok: 40, hargaBeli: "Rp 25000000", hargaJual: "Rp 28000000", hargaBeliNumerik: 15000000, hargaJualNumerik: 18000000, pathFoto: "Iphone.png" },
      { kodeBarang: "HP005", isbn: "Asus ROG Phone 9 Pro", namaBarang: "Gaming", edisi: "2025", stok: 60, hargaBeli: "Rp 22000000", hargaJual: "Rp 18000000", hargaBeliNumerik: 9000000, hargaJualNumerik: 11000000, pathFoto: "Asus.png" },
      { kodeBarang: "HP006", isbn: "Vivo X Fold 3 Pro", namaBarang: "Foldable", edisi: "2025", stok: 30, hargaBeli: "Rp 24000000", hargaJual: "Rp 20000000", hargaBeliNumerik: 16000000, hargaJualNumerik: 19500000, pathFoto: "Vivo.png" } 
    ];

    let dataKatalogBuku = JSON.parse(localStorage.getItem(KATALOG_LS_KEY) || "null");
    // Menggunakan cek field baru untuk membedakan data handphone
    if (!Array.isArray(dataKatalogBuku) || dataKatalogBuku.length === 0 || !dataKatalogBuku.every(b => 'hargaBeli' in b)) {
        // Cek jika data lama masih ada atau field hargaBeli belum ada, maka gunakan default
        dataKatalogBuku = DEFAULT_KATALOG;
        localStorage.removeItem("tokoBuku_dataKatalog_v3"); // Hapus LS lama buku jika ada
    }
    saveKatalogLS(); // Simpan data terbaru


    /* === HELPER FUNCTIONS (LOOKUP) === */
    function getBukuByKode(kode) {
      return dataKatalogBuku.find(b => b.kodeBarang === kode);
    }
    
    function formatRupiah(angka) {
      if (isNaN(angka)) return '-';
      var reverse = angka.toString().split('').reverse().join(''),
      ribuan = reverse.match(/\d{1,3}/g);
      ribuan = ribuan.join('.').split('').reverse().join('');
      return 'Rp ' + ribuan;
    }

    function parseRupiah(rupiah) {
        // Menghilangkan "Rp", spasi, dan titik
        return parseInt(rupiah.replace(/[^0-9]/g, '')) || 0;
    }

    function escapeHtml(text) {
      if (text === null || text === undefined) return "";
      return String(text).replace(/[&<>"']/g, function (m) { return ({'&':'&amp;','<':'&lt;','>':'&gt;','"':'&quot;',"'":'&#39;'})[m]; });
    }
    
    /* === UTILITY === */
    function hideAllSections() {
      document.getElementById("katalogSection").style.display = "none";
    }
    
    function saveKatalogLS() {
        localStorage.setItem(KATALOG_LS_KEY, JSON.stringify(dataKatalogBuku));
    }

    function showNotification(message) {
      // Implementasi sederhana:
      alert(message);
    }


    /* === LOGIN === */
    function login() {
      const email = document.getElementById("email").value.trim();
      const password = document.getElementById("password").value.trim();
      
      const user = dataPengguna.find(u => u.email === email && u.password === password);
      
      if (user) {
        alert(`Login berhasil! Selamat datang, ${user.nama}`);
        document.getElementById("loginPage").style.display = "none";
        document.getElementById("dashboardPage").style.display = "block";
        setGreeting();
        // Memastikan tabel ter-render setelah login
        renderTabelKatalog();
      } else {
        alert("Email/Password yang anda masukkan salah!");
      }
    }

    function setGreeting() {
      const greeting = document.getElementById("greeting");
      const now = new Date();
      const hour = now.getHours();
      if (hour < 12) greeting.textContent = "Selamat Pagi!";
      else if (hour < 18) greeting.textContent = "Selamat Siang!";
      else greeting.textContent = "Selamat Sore!";
    }

    /* === MODAL UTIL === */
    function openModal(id) { document.getElementById(id).style.display = "block"; }
    function closeModal(id) { document.getElementById(id).style.display = "none"; }
    window.onclick = function(event) {
      const modals = document.getElementsByClassName("modal");
      for (let modal of modals) {
        if (event.target == modal) modal.style.display = "none";
      }
    }


    /* === KATALOG === */
    function tampilkanKatalog() {
        hideAllSections();
        document.getElementById("katalogSection").style.display = "block";
        renderTabelKatalog();
    }
    
    const PLACEHOLDER_SVG = 'data:image/svg+xml;utf8,' + encodeURIComponent(
      '<svg xmlns="http://www.w3.org/2000/svg" width="200" height="140">' +
      '<rect width="100%" height="100%" fill="#f3f4f6"/>' +
      '<text x="50%" y="50%" dominant-baseline="middle" text-anchor="middle" fill="#9ca3af" font-size="14">Tidak ada foto</text>' +
      '</svg>'
    );
    
    function renderTabelKatalog() {
      const tbody = document.querySelector("#tabelKatalog tbody");
      tbody.innerHTML = "";
      
      if (dataKatalogBuku.length === 0) {
        // Colspan adalah 9
        tbody.innerHTML = `<tr><td colspan="9">Tidak ada data katalog handphone.</td></tr>`;
        return;
      }

      dataKatalogBuku.forEach(buku => {
        const row = document.createElement("tr");

        const tdFoto = document.createElement("td");
        const img = document.createElement("img");
        img.alt = buku.isbn || "Foto Handphone"; // isbn digunakan sebagai Nama Handphone
        if (!buku.pathFoto) {
          img.src = PLACEHOLDER_SVG;
        } else {
          img.src = buku.pathFoto;
        }
        img.onerror = function(){ this.onerror = null; this.src = PLACEHOLDER_SVG; };
        tdFoto.appendChild(img);

        row.innerHTML = `
          <td>${escapeHtml(buku.kodeBarang || "")}</td> <td>${escapeHtml(buku.isbn || "-")}</td> <td style="text-align:left;">${escapeHtml(buku.namaBarang || "")}</td> <td>${escapeHtml(buku.hargaBeli || "-")}</td> <td>${escapeHtml(buku.hargaJual || "-")}</td> <td>${escapeHtml(buku.edisi || "")}</td> <td>${escapeHtml(String(buku.stok || 0))}</td> `;
        row.appendChild(tdFoto);
        
        const tdAksi = document.createElement("td");
        tdAksi.innerHTML = `<button class="small-btn delete-btn" onclick="hapusBuku('${escapeHtml(buku.kodeBarang)}')">Hapus</button>`;
        row.appendChild(tdAksi);

        tbody.appendChild(row);
      });
    }
    
    // IMPLEMENTASI FUNGSI TAMBAH BUKU (Diubah menjadi Tambah Handphone)
    function tambahBuku() { 
        const kodeBarang = document.getElementById("kodeBarang").value.trim().toUpperCase(); // Id Barang
        const isbn = document.getElementById("isbnInput").value.trim(); // Nama Handphone
        const namaBarang = document.getElementById("namaBarang").value.trim(); // Kategori
        const edisi = document.getElementById("edisi").value.trim();
        const stok = parseInt(document.getElementById("stok").value.trim());
        const hargaBeliInput = document.getElementById("hargaBeli").value.trim(); // NEW
        const hargaJualInput = document.getElementById("hargaJual").value.trim(); // NEW
        
        const fotoUpload = document.getElementById("fotoUpload").files[0];

        if (!kodeBarang || !isbn || !namaBarang || isNaN(stok) || stok < 0 || !hargaBeliInput || !hargaJualInput) {
            showNotification("Id Barang, Nama Handphone, Kategori, Stok, Harga Beli, dan Harga Jual wajib diisi dengan benar!");
            return;
        }
        
        if (dataKatalogBuku.some(b => b.kodeBarang === kodeBarang)) {
            showNotification(`Id Barang ${kodeBarang} sudah ada. Gunakan kode lain atau edit data yang sudah ada.`);
            return;
        }

        const hargaBeliNumerik = parseRupiah(hargaBeliInput);
        const hargaJualNumerik = parseRupiah(hargaJualInput);
        
        // Simulasi penyimpanan file (Hanya mengambil nama file/URL)
        let pathFoto = document.getElementById("pathFoto").value.trim();
        if (fotoUpload) {
            // Dalam implementasi nyata, ini adalah proses upload ke server
            pathFoto = fotoUpload.name;
        } else if (!pathFoto) {
            pathFoto = null; // Tidak ada foto
        }

        const newHandphone = {
            kodeBarang: kodeBarang, // Id Barang
            isbn: isbn, // Nama Handphone
            namaBarang: namaBarang, // Kategori
            edisi: edisi,
            stok: stok,
            hargaBeli: formatRupiah(hargaBeliNumerik),
            hargaJual: formatRupiah(hargaJualNumerik),
            hargaBeliNumerik: hargaBeliNumerik,
            hargaJualNumerik: hargaJualNumerik,
            pathFoto: pathFoto
        };

        dataKatalogBuku.push(newHandphone);
        saveKatalogLS();
        renderTabelKatalog();
        
        // Bersihkan form
        document.getElementById("kodeBarang").value = "";
        document.getElementById("isbnInput").value = ""; 
        document.getElementById("namaBarang").value = ""; 
        document.getElementById("edisi").value = "";
        document.getElementById("stok").value = "";
        document.getElementById("hargaBeli").value = ""; // NEW
        document.getElementById("hargaJual").value = ""; // NEW
        document.getElementById("pathFoto").value = "";
        document.getElementById("fotoUpload").value = "";

        showNotification(`Handphone "${isbn}" berhasil ditambahkan ke katalog.`);
    }

    // IMPLEMENTASI FUNGSI HAPUS BUKU (Diubah menjadi Hapus Handphone)
    function hapusBuku(kode) { 
        if (confirm(`Apakah Anda yakin ingin menghapus handphone dengan Id Barang ${kode} dari katalog?`)) {
            const initialLength = dataKatalogBuku.length;
            dataKatalogBuku = dataKatalogBuku.filter(b => b.kodeBarang !== kode);
            
            if (dataKatalogBuku.length < initialLength) {
                saveKatalogLS();
                renderTabelKatalog();
                showNotification(`Handphone dengan Id Barang ${kode} berhasil dihapus.`);
            } else {
                showNotification("Gagal menghapus data. Id Barang tidak ditemukan.");
            }
        }
    }


    /* === Inisialisasi tampilan awal === */
    document.addEventListener("DOMContentLoaded", function(){
      // Inisialisasi tabel agar terisi jika tidak melewati proses login.
      renderTabelKatalog();
    });

    // Exposed for console testing (optional)
    window.dataKatalogBuku = dataKatalogBuku;
  </script>
</body>
</html>
```
