# TUGAS-BESAR
pbo per kelompok

# PANDUAN INSTALASI FINAL
# Aplikasi Absensi Face Recognition
# ====================================

## PRASYARAT
- Python 3.13 (sudah terinstall)
- VS Code

---

## LANGKAH 1 - Buat & Aktifkan Virtual Environment

Buka terminal di folder project, lalu jalankan:

    cd D:\project_absensi
    python -m venv venv
    venv\Scripts\activate

Pastikan muncul (venv) di depan prompt.

---

## LANGKAH 2 - Download File Manual (lewat browser)

Download file ini dan simpan di folder Downloads:

    https://github.com/z-mahmud22/Dlib_Windows_Python3.x/raw/main/dlib-20.0.99-cp313-cp313-win_amd64.whl

Download file ini dan extract (klik kanan > Extract All):

    https://github.com/ageitgey/face_recognition_models/archive/refs/heads/master.zip

---

## LANGKAH 3 - Install Semua Library (urutan wajib diikuti)

Jalankan satu per satu di terminal:

    python -m pip install C:\Users\user\Downloads\dlib-20.0.99-cp313-cp313-win_amd64.whl

    python -m pip install C:\Users\user\Downloads\face_recognition_models-master\face_recognition_models-master

    python -m pip install opencv-python face_recognition pandas

    python -m pip install "setuptools<72"

---

## LANGKAH 4 - Verifikasi Instalasi

    python -c "import cv2; import face_recognition; print('Semua OK!')"

Harus muncul: Semua OK!

---

## LANGKAH 5 - Jalankan Aplikasi

    python main.py

---

## URUTAN PEMAKAIAN PERTAMA KALI

    1. Pilih Menu 1 -> Registrasi semua mahasiswa (satu per satu)
    2. Pilih Menu 3 -> Inisialisasi tabel kehadiran (cukup sekali)
    3. Pilih Menu 2 -> Mulai absensi, pilih pertemuan ke berapa
    4. Pilih Menu 4 -> Lihat rekap kehadiran

---

## FILE YANG DIHASILKAN OTOMATIS

    data_foto/          -> Foto wajah setiap mahasiswa
    data_mahasiswa.pkl  -> Database mahasiswa + vektor wajah
    data_kehadiran.csv  -> Tabel kehadiran (bisa dibuka di Excel)

---

## CATATAN PENTING

- Wajib pakai venv agar tidak konflik dengan Python global
- setuptools<72 wajib diinstall, versi lebih baru tidak kompatibel
- Urutan install wajib diikuti (dlib dulu, baru face_recognition)
- Jika ganti PC, ulangi semua langkah dari awal
