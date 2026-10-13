# Tantangan Proyek Bab 05: Persistent To-Do List App (PR Mandiri)

Proyek ini menjadi **PR (Tugas Mandiri)** untuk menguji pemahaman Anda seputar **Event Handling** dan **Web Storage**: menangani form tanpa reload (`e.preventDefault()`), mengelola aksi elemen dinamis dengan **Event Delegation**, serta menyimpan dan memuat data secara abadi menggunakan **`localStorage`** dan format **JSON**.

---

## 📌 Deskripsi Proyek
Buatlah aplikasi To-Do List interaktif di mana daftar tugas yang dibuat pengguna **tidak akan hilang meskipun halaman di-refresh atau browser ditutup**. Pengguna dapat menambahkan tugas baru, menandai tugas yang selesai (dicoret), dan menghapus tugas tertentu.

---

## 🎯 Spesifikasi & Fitur yang Harus Dipenuhi

1. **Penanganan Formulir Tanpa Reload**:
   - Pasang event `'submit'` pada tag `<form id="form-tugas">`.
   - Gunakan `e.preventDefault()` agar halaman web tidak me-refresh saat pengguna menekan tombol Tambah atau menekan tombol **Enter**.
   - Validasi: jangan izinkan penambahan tugas jika kolom input kosong atau hanya berisi spasi.

2. **Penyimpanan Abadi (`localStorage` & JSON)**:
   - Simpan daftar tugas dalam bentuk **Array of Objects**:
     ```javascript
     [
       { id: 1711001, teks: "Belajar JavaScript DOM", selesai: false }
     ]
     ```
   - Setiap kali ada tugas **ditambah**, **statusnya diubah**, atau **dihapus**, sinkronkan array tersebut ke `localStorage` menggunakan `JSON.stringify()`.
   - Ketika halaman pertama kali dibuka, baca data dari `localStorage` menggunakan `JSON.parse()` dan render seluruh tugas yang tersimpan ke layar.

3. **Event Delegation pada Elemen Dinamis**:
   - **JANGAN** memasang event listener ke setiap tombol baru satu per satu.
   - Pasang **HANYA SATU event listener `'click'`** pada elemen induk `<ul id="daftar-tugas">`.
   - Manfaatkan `e.target` dan `e.target.closest()`:
     - Jika tombol centang/selesai diklik: ubah status `selesai` pada data tugas, beri efek coret (`line-through`), dan perbarui `localStorage`.
     - Jika tombol hapus diklik: hapus elemen dari layar dan buang data tersebut dari array di `localStorage`.

4. **Tombol "Hapus Semua" (Clear All)**:
   - Menyediakan tombol untuk mengosongkan seluruh tugas di layar dan menghapus data dari `localStorage` (`localStorage.removeItem()` atau `clear()`).

---

## 📋 Checklist Kriteria Kelulusan Proyek
- [ ] Formulir menggunakan event `submit` dan `e.preventDefault()`.
- [ ] Tugas baru berhasil ditambahkan dan langsung terlihat di layar.
- [ ] Data tugas tersimpan abadi di `localStorage` dalam format JSON.
- [ ] Saat halaman di-refresh (F5), seluruh tugas yang tersimpan tetap muncul utuh.
- [ ] Fitur ubah status (selesai) dan hapus tugas bekerja menggunakan teknik **Event Delegation**.
- [ ] Perubahan status selesai dan penghapusan tugas ikut tersinkronisasi ke `localStorage`.

---

## ⚠️ Petunjuk Pengerjaan:
Kerjakan secara mandiri di berkas [Template_Proyek_Bab_05.html](Template_Proyek_Bab_05.html).
