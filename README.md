# EduInformatika — Cloud Computing Project

**EduInformatika** adalah platform *e-learning* berbasis website yang dirancang untuk membantu siswa SMA mempelajari mata pelajaran Informatika secara online. Website ini menyediakan materi pembelajaran interaktif dan kuis evaluasi mandiri.

---

## Tujuan Proyek
Menyediakan sarana pembelajaran Informatika berbasis web yang memudahkan siswa SMA mengakses materi dan latihan soal secara online, serta membantu pengajar dalam mengelola materi dan evaluasi pembelajaran.

---

## Target Pengguna
1. **Siswa SMA:** Mempelajari materi pembelajaran dan mengerjakan kuis evaluasi.
2. **Pengajar Informatika SMA:** Mengelola/menyediakan materi dan membuat kuis interaktif.

---

## Fitur Utama
* **Materi Pembelajaran:** Akses materi berbasis teks maupun dokumen PDF.
* **Pencarian Topik:** Kemudahan mencari dan memilih materi berdasarkan topik Informatika.
* **AI Tutor Interaktif**: Asisten cerdas berbasis AI untuk membantu siswa memahami konsep sulit dan menjawab pertanyaan materi secara mandiri.
* **Kuis & Evaluasi:** Kuis pilihan ganda dengan sistem penilaian otomatis.
* **Riwayat Nilai:** Catatan hasil kuis siswa untuk memantau perkembangan belajar.
* **Manajemen Pengajar:** Panel khusus pengajar untuk mengunggah materi dan mengelola kuis.

---

## Contoh Topik Materi
* Berpikir Komputasional
* Algoritma dan Pemrograman
* Sistem Komputer
* Jaringan Komputer dan Internet
* Analisis Data

---

## Production-like Development Endpoint
- **URL Utama:** `https://25832072003.103.59.95.198.sslip.io/`
- **Health Endpoint:** `https://25832072003.103.59.95.198.sslip.io/health`

---

## Network Architecture
Public entry points:
- **TCP/80** → Caddy HTTP redirect / ACME challenge
- **TCP/443** → Caddy HTTPS

Internal application:
- `127.0.0.1:8000` → Gunicorn (Flask App)

---

## DNS
`25832072003.103.59.95.198.sslip.io` resolves via A Record to `103.59.95.198`.

---

## Security Baseline
- SSH Key authentication
- Active UFW (Ports 22, 80, 443)
- Loopback-only Flask/Gunicorn backend
- Caddy Automatic HTTPS
