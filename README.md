<!DOCTYPE html>
<html lang="id">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>Ujian SMK - Soal Pilihan Ganda A-E</title>
<style>
  * {
    box-sizing: border-box;
    margin: 0;
    padding: 0;
    font-family: 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif;
  }

  body {
    background: linear-gradient(135deg, #1e3c72 0%, #2a5298 100%);
    min-height: 100vh;
    display: flex;
    justify-content: center;
    align-items: center;
    padding: 20px;
  }

  .container {
    background: #ffffff;
    width: 100%;
    max-width: 820px;
    border-radius: 16px;
    box-shadow: 0 20px 40px rgba(0,0,0,0.3);
    overflow: hidden;
  }

  /* ===== HEADER ===== */
  .header {
    background: #f8f9fa;
    padding: 20px 25px;
    border-bottom: 3px solid #1e3c72;
    display: flex;
    align-items: center;
    gap: 20px;
    flex-wrap: wrap;
  }

  .logo-box {
    width: 75px;
    height: 75px;
    background: #1e3c72;
    border-radius: 12px;
    display: flex;
    justify-content: center;
    align-items: center;
    color: #fff;
    font-size: 11px;
    font-weight: bold;
    text-align: center;
    flex-shrink: 0;
    overflow: hidden;
    border: 2px solid #2a5298;
  }

  .logo-box img {
    width: 100%;
    height: 100%;
    object-fit: contain;
  }

  .identitas {
    flex: 1;
    min-width: 250px;
  }

  .identitas .row {
    display: flex;
    margin-bottom: 5px;
    font-size: 14px;
  }

  .identitas .row .label {
    width: 110px;
    font-weight: 600;
    color: #555;
  }

  .identitas .row .value {
    color: #1e3c72;
    font-weight: 600;
    flex: 1;
  }

  /* ===== KONTEN SOAL ===== */
  .content {
    padding: 28px 25px;
  }

  .info-bar {
    display: flex;
    justify-content: space-between;
    align-items: center;
    margin-bottom: 18px;
    padding-bottom: 14px;
    border-bottom: 1px solid #e0e0e0;
    flex-wrap: wrap;
    gap: 10px;
  }

  .info-bar .soal-ke {
    background: #1e3c72;
    color: #fff;
    padding: 6px 18px;
    border-radius: 20px;
    font-size: 14px;
    font-weight: 600;
  }

  .info-bar .terjawab {
    color: #27ae60;
    font-weight: 600;
    font-size: 14px;
  }

  .perintah {
    font-size: 14.5px;
    color: #444;
    margin-bottom: 18px;
    font-style: italic;
    background: #fff8e1;
    padding: 12px 16px;
    border-left: 4px solid #f39c12;
    border-radius: 4px;
  }

  .soal-teks {
    font-size: 17px;
    color: #222;
    margin-bottom: 16px;
    line-height: 1.55;
    font-weight: 500;
  }

  .soal-gambar {
    max-width: 100%;
    max-height: 240px;
    border-radius: 8px;
    border: 1px solid #ddd;
    margin-bottom: 18px;
    display: none;
  }

  /* ===== OPSI A-E ===== */
  .opsi {
    display: flex;
    flex-direction: column;
    gap: 10px;
    margin-top: 18px;
  }

  .opsi label {
    display: flex;
    align-items: flex-start;
    gap: 12px;
    padding: 13px 18px;
    border: 2px solid #e0e0e0;
    border-radius: 10px;
    cursor: pointer;
    transition: all 0.18s;
    font-size: 15.5px;
    line-height: 1.4;
  }

  .opsi label:hover {
    border-color: #1e3c72;
    background: #f5f8ff;
  }

  .opsi input[type="radio"] {
    accent-color: #1e3c72;
    width: 18px;
    height: 18px;
    margin-top: 3px;
    flex-shrink: 0;
  }

  .opsi label.selected {
    border-color: #1e3c72;
    background: #e8f0fe;
    box-shadow: 0 2px 8px rgba(30,60,114,0.18);
  }

  .opsi .kode-opsi {
    display: inline-block;
    width: 26px;
    height: 26px;
    background: #e9ecef;
    color: #495057;
    border-radius: 50%;
    text-align: center;
    line-height: 26px;
    font-weight: 700;
    font-size: 13px;
    flex-shrink: 0;
  }

  .opsi label.selected .kode-opsi {
    background: #1e3c72;
    color: #fff;
  }

  /* ===== UPLOAD ===== */
  .upload-section {
    margin-top: 22px;
    padding: 14px 16px;
    background: #f8f9fa;
    border-radius: 10px;
    border: 1px dashed #adb5bd;
  }

  .upload-section h4 {
    font-size: 13px;
    color: #6c757d;
    margin-bottom: 8px;
  }

  .upload-section input[type="file"] {
    font-size: 13px;
    color: #555;
    width: 100%;
  }

  .upload-info {
    font-size: 12px;
    color: #888;
    margin-top: 6px;
  }

  /* ===== NAVIGASI ===== */
  .nav-buttons {
    display: flex;
    justify-content: space-between;
    gap: 12px;
    padding: 18px 25px;
    background: #f8f9fa;
    border-top: 1px solid #e0e0e0;
    flex-wrap: wrap;
  }

  .nav-buttons button {
    padding: 12px 26px;
    border: none;
    border-radius: 8px;
    font-size: 15px;
    font-weight: 600;
    cursor: pointer;
    transition: all 0.2s;
    flex: 1;
    min-width: 120px;
  }

  .btn-prev {
    background: #e9ecef;
    color: #495057;
  }

  .btn-prev:hover:not(:disabled) {
    background: #dee2e6;
  }

  .btn-next {
    background: #1e3c72;
    color: #fff;
  }

  .btn-next:hover:not(:disabled) {
    background: #2a5298;
  }

  .btn-submit {
    background: #27ae60;
    color: #fff;
  }

  .btn-submit:hover {
    background: #219150;
  }

  button:disabled {
    opacity: 0.45;
    cursor: not-allowed;
  }

  /* ===== PROGRESS DOTS ===== */
  .progress-dots {
    display: flex;
    gap: 6px;
    justify-content: center;
    padding: 0 25px 18px;
    flex-wrap: wrap;
    background: #f8f9fa;
  }

  .dot {
    width: 11px;
    height: 11px;
    border-radius: 50%;
    background: #d0d7de;
  }

  .dot.aktif { background: #1e3c72; transform: scale(1.25); }
  .dot.terjawab { background: #27ae60; }

  /* ===== HASIL ===== */
  .hasil-box {
    display: none;
    padding: 40px 25px;
    text-align: center;
  }

  .hasil-box .skor-besar {
    font-size: 68px;
    font-weight: 800;
    color: #1e3c72;
    margin: 10px 0;
    line-height: 1;
  }

  .hasil-box .skor-label {
    font-size: 15px;
    color: #666;
    letter-spacing: 1px;
  }

  .hasil-box .detail {
    margin: 25px auto;
    max-width: 420px;
    background: #f8f9fa;
    padding: 18px 24px;
    border-radius: 12px;
    text-align: left;
    font-size: 15px;
    line-height: 2.1;
  }

  .hasil-box .detail span {
    font-weight: 700;
    color: #1e3c72;
    float: right;
  }

  .predikat {
    display: inline-block;
    padding: 8px 32px;
    border-radius: 30px;
    font-size: 19px;
    font-weight: 700;
    color: #fff;
    margin: 8px 0 4px;
  }

  .predikat.lulus { background: #27ae60; }
  .predikat.cukup { background: #f39c12; }
  .predikat.gagal { background: #e74c3c; }

  .btn-restart {
    margin-top: 20px;
    padding: 12px 35px;
    background: #1e3c72;
    color: #fff;
    border: none;
    border-radius: 8px;
    font-size: 15px;
    font-weight: 600;
    cursor: pointer;
  }

  .btn-restart:hover { background: #2a5298; }

  @media (max-width: 500px) {
    .header { flex-direction: column; align-items: flex-start; }
    .identitas .row .label { width: 90px; font-size: 13px; }
    .nav-buttons button { padding: 12px 12px; font-size: 14px; }
    .soal-teks { font-size: 16px; }
  }
</style>
</head>
<body>

<div class="container">
  <!-- ============ HEADER ============ -->
  <div class="header">
    <div class="logo-box" id="logoBox">
      LOGO<br>SMK
    </div>
    <div class="identitas">
      <div class="row"><span class="label">Nama Siswa</span><span class="value">: Andi Pratama</span></div>
      <div class="row"><span class="label">NISN</span><span class="value">: 0071234567</span></div>
      <div class="row"><span class="label">Nama Sekolah</span><span class="value">: SMK Negeri 1 Jakarta</span></div>
    </div>
  </div>

  <!-- ============ AREA SOAL ============ -->
  <div id="areaSoal">
    <div class="content">
      <div class="info-bar">
        <span class="soal-ke" id="labelSoal">Soal 1 / 5</span>
        <span class="terjawab" id="labelTerjawab">Terjawab: 0</span>
      </div>

      <div class="perintah" id="perintahSoal">
        Perintah: Pilihlah salah satu jawaban yang paling benar (A, B, C, D, atau E).
      </div>

      <div class="soal-teks" id="teksSoal"></div>

      <img id="gambarSoal" class="soal-gambar" alt="Gambar Soal">

      <div class="opsi" id="opsiContainer"></div>

      <div class="upload-section">
        <h4>📎 Upload soal (screenshot / gambar) — opsional</h4>
        <input type="file" id="uploadSoal" accept="image/*">
        <div class="upload-info">File gambar akan ditampilkan sebagai visual soal saat ini.</div>
      </div>
    </div>

    <div class="nav-buttons">
      <button class="btn-prev" id="btnPrev" disabled>‹ Sebelumnya</button>
      <button class="btn-next" id="btnNext">Selanjutnya ›</button>
      <button class="btn-submit" id="btnSubmit" style="display:none;">✅ Submit & Lihat Nilai</button>
    </div>

    <div class="progress-dots" id="progressDots"></div>
  </div>

  <!-- ============ AREA HASIL ============ -->
  <div class="hasil-box" id="areaHasil">
    <div class="skor-label">NILAI AKHIR ANDA</div>
    <div class="skor-besar" id="skorAkhir">0</div>
    <div id="predikatBox"></div>
    <div class="detail">
      <div>Jumlah Soal <span id="totalSoal">5</span></div>
      <div>Jawaban Benar <span id="jumlahBenar">0</span></div>
      <div>Jawaban Salah <span id="jumlahSalah">0</span></div>
      <div>Tidak Dijawab <span id="jumlahKosong">0</span></div>
    </div>
    <button class="btn-restart" id="btnRestart">🔄 Ulangi Ujian</button>
  </div>
</div>

<script>
/* =========================================================
   DATA SOAL (5 OPSI A-E)
   ========================================================= */
const HURUF = ['A', 'B', 'C', 'D', 'E'];

const soalData = [
  {
    perintah: "Pilihlah salah satu jawaban yang paling benar (A, B, C, D, atau E).",
    teks: "1. Perangkat keras komputer yang berfungsi sebagai otak pemrosesan utama adalah...",
    gambar: "",
    opsi: [
      "Monitor",
      "CPU (Processor)",
      "Keyboard",
      "Printer",
      "Speaker"
    ],
    jawaban: 1
  },
  {
    perintah: "Pilihlah salah satu jawaban yang paling benar (A, B, C, D, atau E).",
    teks: "2. Bahasa pemrograman yang paling banyak digunakan untuk membangun website dinamis adalah...",
    gambar: "",
    opsi: [
      "Pascal",
      "Assembly",
      "PHP & JavaScript",
      "Fortran",
      "COBOL"
    ],
    jawaban: 2
  },
  {
    perintah: "Perhatikan pernyataan berikut, pilih jawaban yang benar.",
    teks: "3. Rumus kimia untuk air adalah...",
    gambar: "",
    opsi: [
      "CO₂",
      "O₂",
      "NaCl",
      "H₂O",
      "CH₄"
    ],
    jawaban: 3
  },
  {
    perintah: "Pilihlah salah satu jawaban yang paling benar (A, B, C, D, atau E).",
    teks: "4. Alat ukur yang digunakan untuk mengukur besarnya arus listrik adalah...",
    gambar: "",
    opsi: [
      "Voltmeter",
      "Ohmmeter",
      "Barometer",
      "Higrometer",
      "Amperemeter"
    ],
    jawaban: 4
  },
  {
    perintah: "Pilihlah salah satu jawaban yang paling benar (A, B, C, D, atau E).",
    teks: "5. Dalam jaringan komputer, perangkat yang berfungsi mengarahkan paket data antar jaringan yang berbeda disebut...",
    gambar: "",
    opsi: [
      "Switch",
      "Router",
      "Hub",
      "Repeater",
      "Bridge"
    ],
    jawaban: 1
  }
];

/* =========================================================
   STATE
   ========================================================= */
let currentIndex = 0;
let jawabanUser = new Array(soalData.length).fill(null);

/* =========================================================
   ELEMEN
   ========================================================= */
const teksSoalEl = document.getElementById('teksSoal');
const gambarSoalEl = document.getElementById('gambarSoal');
const opsiContainer = document.getElementById('opsiContainer');
const perintahSoalEl = document.getElementById('perintahSoal');
const labelSoalEl = document.getElementById('labelSoal');
const labelTerjawabEl = document.getElementById('labelTerjawab');
const btnPrev = document.getElementById('btnPrev');
const btnNext = document.getElementById('btnNext');
const btnSubmit = document.getElementById('btnSubmit');
const progressDots = document.getElementById('progressDots');
const uploadSoal = document.getElementById('uploadSoal');

/* =========================================================
   RENDER SOAL
   ========================================================= */
function renderSoal() {
  const soal = soalData[currentIndex];

  // Label & perintah
  labelSoalEl.textContent = `Soal ${currentIndex + 1} / ${soalData.length}`;
  perintahSoalEl.textContent = "Perintah: " + soal.perintah;
  updateTerjawab();

  // Teks soal
  teksSoalEl.textContent = soal.teks;

  // Gambar bawaan soal
  if (soal.gambar) {
    gambarSoalEl.src = soal.gambar;
    gambarSoalEl.style.display = 'block';
  } else {
    gambarSoalEl.style.display = 'none';
    gambarSoalEl.removeAttribute('src');
  }

  // Reset input upload karena pindah soal
  uploadSoal.value = '';

  // Render opsi A-E
  opsiContainer.innerHTML = '';
  soal.opsi.forEach((opsiTeks, idx) => {
    const label = document.createElement('label');
    label.className = 'opsi-item';
    if (jawabanUser[currentIndex] === idx) label.classList.add('selected');

    const radio = document.createElement('input');
    radio.type = 'radio';
    radio.name = 'opsi_' + currentIndex;
    radio.value = idx;
    radio.checked = jawabanUser[currentIndex] === idx;

    radio.addEventListener('change', () => {
      jawabanUser[currentIndex] = idx;
      document.querySelectorAll('#opsiContainer label').forEach(l => l.classList.remove('selected'));
      label.classList.add('selected');
      updateTerjawab();
      renderProgressDots();
    });

    const kode = document.createElement('span');
    kode.className = 'kode-opsi';
    kode.textContent = HURUF[idx];

    const span = document.createElement('span');
    span.textContent = opsiTeks;

    label.appendChild(radio);
    label.appendChild(kode);
    label.appendChild(span);
    opsiContainer.appendChild(label);
  });

  // Tombol navigasi
  btnPrev.disabled = currentIndex === 0;

  if (currentIndex === soalData.length - 1) {
    btnNext.style.display = 'none';
    btnSubmit.style.display = 'block';
  } else {
    btnNext.style.display = 'block';
    btnSubmit.style.display = 'none';
  }

  renderProgressDots();
}

/* =========================================================
   PROGRESS
   ========================================================= */
function updateTerjawab() {
  const terjawab = jawabanUser.filter(j => j !== null).length;
  labelTerjawabEl.textContent = `Terjawab: ${terjawab} / ${soalData.length}`;
}

function renderProgressDots() {
  progressDots.innerHTML = '';
  soalData.forEach((_, i) => {
    const d = document.createElement('div');
    d.className = 'dot';
    if (i === currentIndex) d.classList.add('aktif');
    else if (jawabanUser[i] !== null) d.classList.add('terjawab');
    progressDots.appendChild(d);
  });
}

/* =========================================================
   NAVIGASI
   ========================================================= */
btnPrev.addEventListener('click', () => {
  if (currentIndex > 0) {
    currentIndex--;
    renderSoal();
  }
});

btnNext.addEventListener('click', () => {
  if (currentIndex < soalData.length - 1) {
    currentIndex++;
    renderSoal();
  }
});

/* =========================================================
   SUBMIT & HITUNG NILAI
   ========================================================= */
btnSubmit.addEventListener('click', () => {
  let benar = 0, salah = 0, kosong = 0;

  soalData.forEach((soal, i) => {
    if (jawabanUser[i] === null) kosong++;
    else if (jawabanUser[i] === soal.jawaban) benar++;
    else salah++;
  });

  const nilai = Math.round((benar / soalData.length) * 100);

  // Sembunyikan area soal, tampilkan hasil
  document.getElementById('areaSoal').style.display = 'none';
  const areaHasil = document.getElementById('areaHasil');
  areaHasil.style.display = 'block';

  document.getElementById('skorAkhir').textContent = nilai;
  document.getElementById('totalSoal').textContent = soalData.length;
  document.getElementById('jumlahBenar').textContent = benar;
  document.getElementById('jumlahSalah').textContent = salah;
  document.getElementById('jumlahKosong').textContent = kosong;

  // Predikat
  const predikatBox = document.getElementById('predikatBox');
  let predikat = '', kelas = '';
  if (nilai >= 75) { predikat = 'LULUS ✔'; kelas = 'lulus'; }
  else if (nilai >= 60) { predikat = 'CUKUP'; kelas = 'cukup'; }
  else { predikat = 'BELUM LULUS'; kelas = 'gagal'; }

  predikatBox.innerHTML = `<span class="predikat ${kelas}">${predikat}</span>`;

  window.scrollTo({ top: 0, behavior: 'smooth' });
});

/* =========================================================
   UPLOAD GAMBAR SOAL
   ========================================================= */
uploadSoal.addEventListener('change', (e) => {
  const file = e.target.files[0];
  if (!file) return;

  const reader = new FileReader();
  reader.onload = (ev) => {
    gambarSoalEl.src = ev.target.result;
    gambarSoalEl.style.display = 'block';
  };
  reader.readAsDataURL(file);
});

/* =========================================================
   RESTART
   ========================================================= */
document.getElementById('btnRestart').addEventListener('click', () => {
  jawabanUser = new Array(soalData.length).fill(null);
  currentIndex = 0;

  document.getElementById('areaHasil').style.display = 'none';
  document.getElementById('areaSoal').style.display = 'block';

  renderSoal();
  window.scrollTo({ top: 0, behavior: 'smooth' });
});

/* =========================================================
   INIT
   ========================================================= */
renderSoal();
</script>
</body>
</html>
