|                |                    |
| -------------- | ------------------ |
|      Nama    | Friska Pebriana Lestari |
|      NIM     |      312410160     |
|     Kelas    |      TI.24.A1      |
|  Mata Kuliah | Bahasa Pemrograman Web 1 |

## Input
```` html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>HTML Lanjutan</title>
</head>
<body>
    <header>
        <h1>Membuat List</h1>
    </header>

    <section id="order-list">
        <h2>Ordered List</h2>
        <ol>
            <li>Pemrograman Web</li>
            <li>Sistem Informasi</li>
            <li>Basis Data 2</li>
        </ol>
    </section>

    <section id="unorder-list">
        <h2>Unordered List</h2>
        <ul type="square">
            <li>Jaringan Komputer</li>
            <li>Struktur Data</li>
            <li>Algoritma &amp; Pemrograman</li>
        </ul>
    </section>

    <section id="unorder-list">
        <h2>Description List</h2>
        <dl>
            <dt>Fakultas Teknik</dt>
            <dd>Teknik Industri</dd>
            <dd>Teknik Informatika</dd>
            <dd>Teknik Lingkungan</dd>
            <dt>Fakultas Ekonomi dan Bisnis</dt>
            <dd>Akuntansi</dd>
            <dd>Manajemen</dd>
            <dd>Bisnis Digital</dd>
        </dl>
    </section>
</body>
</html>
````
## output
<img width="954" height="1123" alt="foto1" src="https://github.com/user-attachments/assets/efde3231-2c46-4f60-b77a-d657249f1bf8" />
## Input
```` html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>HTML Lanjutan</title>
</head>
<body>
    <header>
        <h1>Membuat Table</h1>
    </header>
    <table border="1" cellpadding="4" cellspacing="0">
        <thead>
            <tr>
                <th>No.</th>
                <th>Fakultas</th>
                <th>Program Studi</th>
            </tr>
        </thead>
        <tbody>
            <tr>
                <td>1.</td>
                <td>Teknik</td>
                <td>Teknik Informatika</td>
            </tr>
            <tr>
                <td>2.</td>
                <td>Teknik</td>
                <td>Teknik Industri</td>
            </tr>
            <tr>
                <td>3.</td>
                <td>Teknik</td>
                <td>Teknik Lingkungan</td>
            </tr>
        </tbody>
    </table>
    <br>
    <table border="1" cellpadding="6" cellspacing="0">
        <thead>
            <tr>
                <th>No.</th>
                <th>Fakultas</th>
                <th>Program Studi</th>
            </tr>
        </thead>
        <tbody>
            <tr>
                <td>1.</td>
                <td rowspan="3">Teknik</td>
                <td>Teknik Informatika</td>
            </tr>
            <tr>
                <td>2.</td>
                <td>Teknik Industri</td>
            </tr>
            <tr>
                <td>3.</td>
                <td>Teknik Lingkungan</td>
            </tr>
        </tbody>
    </table>
</body>
</html>
````

## Output
<img width="1177" height="835" alt="foto2" src="https://github.com/user-attachments/assets/40389f87-4cfa-4a0a-9d50-e89db41ebb68" />

## Input
```` html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>HTML Lanjutan</title>

    <!-- taruh di <head> -->
<link href="https://fonts.googleapis.com/css2?family=Press+Start+2P&display=swap"  rel="stylesheet">

<!-- CSS -->
<style>
/* ---------- background pixel pink ---------- */
:root{
  --pink-1:#ffd6e8;
  --pink-2:#ff93c2;
  --accent:#d95b9b;
  --shadow:#f8b0d7;
}

/* pixel grid with soft pinks */
body{
  font-family: "Inter", system-ui, sans-serif;
  margin:0;
  min-height:100vh;
  background-color:#fbeae7;
  padding:40px;
  box-sizing:border-box;
}

/* container: retro pixel card */
.card {
  width: 480px;
  max-width: calc(100% - 48px);
  background: linear-gradient(180deg, rgba(255,255,255,0.95), rgba(255,245,250,0.95));
  border: 3px solid var(--accent);
  padding:20px 26px;
  position:relative;
  border-radius:6px;
  /* stepped pixel shadow (8-bit vibe) */
  box-shadow:
    6px 6px 0 0 var(--shadow),
    12px 12px 0 0 rgba(217,91,155,0.12);
  font-size:14px;
}

/* pixel header */
.card h1{
  font-family: "Press Start 2P", monospace;
  font-size:18px;
  margin:6px 0 16px 0;
  color:var(--accent);
  letter-spacing:1px;
}

/* labels left column look */
.form-row{
  display:flex;
  align-items:flex-start;
  gap:20px;
  margin-bottom:14px;
}
.form-row label{
  width:110px;
  color:#6b5163;
  padding-top:6px;
}

/* inputs with pixel border */
input[type="text"],
textarea{
  font-family:inherit;
  font-size:13px;
  padding:8px 10px;
  border:2px solid #c76a9a;
  border-radius:2px;
  background: #fff;
  box-shadow: inset 0 -4px 0 rgba(0,0,0,0.03);
  outline:none;
  transition: transform .08s ease;
}
input[type="text"]:focus,
textarea:focus{
  transform: translateY(-1px);
  box-shadow: 0 0 0 3px rgba(217,91,155,0.08);
}

/* make textarea look pixel-blocky */
textarea{
  min-height:60px;
  resize:vertical;
}

/* pixel radio group */
.radio-group{
  display:flex;
  gap:18px;
  align-items:center;
  color:#5b4150;
}

/* pixel button */
.btn-pixel{
  display:inline-block;
  font-family: "Press Start 2P", monospace;
  padding:8px 14px;
  background: linear-gradient(180deg, var(--accent), #b94a7f);
  color: #fff;
  border:3px solid #7f2f52;
  border-bottom-width:6px;
  border-radius:3px;
  cursor:pointer;
  box-shadow: 6px 6px 0 rgba(0,0,0,0.06);
  text-decoration:none;
  font-size:12px;
}

/* floating pixel sticker (use <img class="sticker">) */
.sticker{
  position:absolute;
  width:72px;
  height:72px;
  object-fit:contain;
  image-rendering: pixelated; /* jika sticker resolusi kecil, jadi pixel look */
  transform: rotate(-10deg);
  top: -20px;
  right: -20px;
  pointer-events:none;
  filter: drop-shadow(4px 4px 0 rgba(217,91,155,0.18));
}

/* small responsive tweak */
@media (max-width:520px){
  .card{ padding:16px; }
  .form-row{ flex-direction:column; gap:8px; }
  .form-row label{ width:100%; }
  .sticker{ width:56px; height:56px; top:-14px; right:-12px; }
}
.judul-pixel {
      font-family: "Press Start 2P", monospace;
      font-size: 36px;
      color: var(--accent);
      letter-spacing: 1px;
      text-shadow: 2px 2px var(--shadow);
      
    }
</style>

</head>
<body>
    <header>
        <div class="card">
            <img class="sticker" src="stiker-heart pixel.png" alt="sticker">
        <h1> MEMBUAT FORM!!</h1>
    </header>

    <form action="proses.php" method="post">
        <fieldset>
            <legend>Data Pelanggan</legend>
            <p>
                <label for="nama">Nama</label>
                <input type="text" id="nama" name="nama">
            </p>
            <p>
                <label for="alamat">Alamat</label>
                <textarea id="alamat" name="alamat" cols="20" rows="3"></textarea>
            </p>
            <p>
                <label>Jenis Kelamin</label>
                <input id="jk_l" type="radio" name="kelamin" value="L" /><label
    for="jk_l">Laki-laki</label>
                <input id="jk_p" type="radio" name="kelamin" value="P" /><label
    for="jk_p">Perempuan</label>
            </p>
            <p><input type="submit" value="Login"></p>
        </fieldset>
    </form>

    <style>
        form p > label {
            display: inline-block;
            width: 100px;
        }
        form input[type="text"], form textarea {
            border: 1px solid #b5316e;
        }
        form input[type="submit"] {
            border: 1px solid #b5316e;
            background-color: #b5316e;
            color: #ffffff;
            font-weight: bold;
            padding: 5px 15px;
        }
    </style>
</body>
</html>
````
## Output
<img width="2559" height="902" alt="foto3" src="https://github.com/user-attachments/assets/53cf54b3-4f59-4413-8eef-2e44329195da" />

## Input
````html
<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>Form Jurusan & Minat</title>
  <style>
    @import url('https://fonts.googleapis.com/css2?family=Press+Start+2P&display=swap');

    body {
      font-family: 'Press Start 2P', cursive;
      background-color: #fbeefc;
      display: flex;
      justify-content: center;
      align-items: center;
      height: 100vh;
    }

    .form-box {
      background-color: #fff;
      border: 3px solid #000;
      box-shadow: 6px 6px 0px #000;
      padding: 25px;
      width: 360px;
      transition: all 0.2s ease;
    }

    .form-box:hover {
      transform: scale(1.02);
      box-shadow: 8px 8px 0px #000;
    }

    h2 {
      text-align: center;
      color: #ff55aa;
      font-size: 14px;
      margin-bottom: 25px;
      text-shadow: 2px 2px 0 #000;
    }

    label {
      display: block;
      margin-top: 18px;
      font-size: 10px;
      color: #333;
    }

    select {
      width: 100%;
      padding: 8px;
      border: 2px solid #000;
      background-color: #ffeaf6;
      font-family: inherit;
      font-size: 10px;
      color: #333;
      transition: all 0.2s ease;
    }

    select:hover {
      background-color: #ffd9f2;
      transform: scale(1.02);
    }

    .listbox {
      height: 110px;
    }

    input[type="submit"] {
      margin-top: 25px;
      width: 100%;
      padding: 10px;
      background-color: #ff55aa;
      color: #fff;
      border: 2px solid #000;
      cursor: pointer;
      font-size: 10px;
      box-shadow: 3px 3px 0px #000;
      transition: all 0.1s ease;
    }

    input[type="submit"]:hover {
      background-color: #ff85c2;
      transform: scale(1.05);
    }

    input[type="submit"]:active {
      box-shadow: none;
      transform: translate(3px, 3px);
    }
  </style>
</head>
<body>
  <form class="form-box" action="#" method="post">
    <h2>🎓 FORM JURUSAN & MINAT 🎮</h2>

    <label for="jurusan">Pilih Jurusan:</label>
    <select id="jurusan" name="jurusan">
      <option value="">-- Pilih Jurusan --</option>
      <option value="TI">Teknik Informatika</option>
      <option value="SI">Sistem Informasi</option>
      <option value="DKV">Desain Komunikasi Visual</option>
      <option value="AK">Akuntansi</option>
      <option value="MI">Manajemen Informatika</option>
    </select>

    <label for="minat">Pilih Minat Tambahan:</label>
    <select id="minat" name="minat" class="listbox" multiple>
      <option value="ai">Kecerdasan Buatan</option>
      <option value="web">Web Development</option>
      <option value="game">Game Design</option>
      <option value="uiux">UI/UX Design</option>
      <option value="data">Data Science</option>
      <option value="network">Networking</option>
    </select>

    <input type="submit" value="KIRIM 🔥">
  </form>
</body>
</html>
````

## Output
<img width="1095" height="971" alt="Cuplikan layar 2025-10-06 193918" src="https://github.com/user-attachments/assets/610fd8a2-cfba-4a3d-8732-1e69351b8ba4" />
