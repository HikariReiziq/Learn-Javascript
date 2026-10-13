# Tantangan Proyek Bab 04: Dynamic Card Generator (PR Mandiri)

Proyek ini menjadi **PR (Tugas Mandiri)** untuk menguji pemahaman Anda seputar **DOM Manipulation**: seleksi elemen, mengubah konten & gaya (`classList`), serta menciptakan dan menghapus elemen dinamis (`createElement`, `append`, `remove`).

---

## Deskripsi Proyek
Buatlah aplikasi generator kartu profil mahasiswa secara dinamis. Pengguna memasukkan data melalui formulir, dan ketika tombol ditekan, sebuah kartu profil baru akan muncul di layar lengkap dengan tombol aksi untuk mengubah tema kartu dan menghapusnya.

---

## Kriteria & Fitur yang Harus Dipenuhi

1. **Formulir Input**:
   - Kolom Nama Mahasiswa (`#input-nama`).
   - Kolom NIM (`#input-nim`).
   - Pilihan Jurusan (`<select id="input-jurusan">`).
   - Tombol "+ Buat Kartu" (`#btn-buat-kartu`).
   - Tombol "Reset Semua Kartu" (`#btn-reset-semua`).

2. **Validasi Sederhana**:
   - Jika Nama atau NIM kosong, munculkan peringatan dan jangan buat kartu.

3. **Pembuatan Elemen Dinamis (`createElement` & `append`)**:
   - Setiap kartu dibuat sebagai elemen `<div class="card-mahasiswa">`.
   - Di dalam kartu terdapat:
     - `<h3>` nama mahasiswa.
     - `<p>` NIM dan Jurusan.
     - Tombol "Ganti Tema" (`btn-tema`) untuk mengubah warna/tampilan kartu.
     - Tombol "Hapus" (`btn-hapus`) untuk menghapus kartu tersebut.

4. **Manipulasi Gaya dengan `classList`**:
   - Ketika tombol "Ganti Tema" pada kartu diklik, gunakan `.classList.toggle("tema-sorot")` untuk mengubah kartu menjadi mode tersorot/berwarna.

5. **Penghapusan Elemen (`remove` & `innerHTML = ""`)**:
   - Tombol "Hapus" pada masing-masing kartu menghapus kartu yang bersangkutan (`kartu.remove()`).
   - Tombol "Reset Semua Kartu" mengosongkan kontainer kartu (`kontainer.innerHTML = ""`).
