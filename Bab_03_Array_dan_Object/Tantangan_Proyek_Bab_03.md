# Tantangan Proyek Bab 03: Manajemen Inventaris Toko Elektronik (Capstone Hari 1)

Proyek ini menjadi **PR (Tugas Mandiri)** untuk menguji pemahaman Anda seputar struktur data **Array**, **Object**, serta method modern **`.map()`** dan **`.filter()`**.

---

## Deskripsi Kasus
Sebuah toko elektronik membutuhkan sistem mini berbasis web untuk mengelola dan memfilter katalog produk mereka. 

Toko telah memiliki data awal berupa **Array of Objects**:
```javascript
const katalogAwal = [
  { id: 1, nama: "Laptop ASUS VivoBook", kategori: "Laptop", harga: 8500000, stok: 4 },
  { id: 2, nama: "Mouse Logitech M170", kategori: "Aksesoris", harga: 150000, stok: 15 },
  { id: 3, nama: "Keyboard Mechanical RGB", kategori: "Aksesoris", harga: 450000, stok: 0 },
  { id: 4, nama: "Monitor LG 24 Inch", kategori: "Monitor", harga: 1750000, stok: 6 },
  { id: 5, nama: "Flashdisk Sandisk 64GB", kategori: "Aksesoris", harga: 85000, stok: 20 },
  { id: 6, nama: "Laptop Lenovo ThinkPad", kategori: "Laptop", harga: 12000000, stok: 0 }
];
```

---

## Kriteria & Instruksi Pengerjaan

1. **Tampilkan Semua Produk**:
   - Ketika halaman pertama kali dimuat atau ketika tombol **"Tampilkan Semua"** diklik, tampilkan seluruh daftar produk ke elemen `#daftar-produk`.
2. **Filter Stok Tersedia**:
   - Ketika tombol **"Hanya Stok Tersedia"** diklik, gunakan method **`.filter()`** untuk menyaring produk yang `stok > 0`.
3. **Filter Berdasarkan Kategori**:
   - Ketika pengguna memilih opsi kategori dari `<select id="filter-kategori">` dan mengklik tombol **"Filter Kategori"**, saring produk sesuai kategori yang dipilih.
4. **Transformasi Diskon Flash Sale**:
   - Ketika tombol **"Terapkan Diskon 10%"** diklik, gunakan method **`.map()`** untuk menghasilkan array baru di mana setiap produk harganya dipotong 10% (`harga * 0.9`).
5. **Format Tampilan**:
   - Tampilkan informasi rapi: `[ID] Nama Barang | Kategori | Harga | Sisa Stok`.
