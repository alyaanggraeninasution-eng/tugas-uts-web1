# Aplikasi Pemesanan Buku - UTS Pemrograman Web 1

Project ini merupakan aplikasi front-end sederhana untuk simulasi toko/pemesanan buku. Data contoh disimpan pada file JavaScript (`js/data.js`), sehingga aplikasi tidak membutuhkan server atau database.

## 1. Teknologi yang digunakan

- HTML untuk struktur halaman.
- CSS untuk mengatur tampilan.
- JavaScript untuk membaca data, manipulasi DOM, dan interaksi halaman.
- Live Server (ekstensi Visual Studio Code) untuk menjalankan project secara lokal.

## 2. Struktur folder

```text
tugas_uts_web1/
├── css/
│   └── style.css
├── img/
│   ├── pengantar_komunikasi.jpg
│   ├── manajemen_keuangan.jpg
│   ├── kepemimpinan.jpg
│   ├── mikrobiologi.jpg
│   └── paud_perkembangan.jpg
├── images/                 # Salinan aset gambar yang sudah ada di project awal
├── js/
│   ├── data.js
│   └── script.js
├── index.html
├── login.html
├── dashboard.html
├── stok.html
├── checkout.html
├── tracking.html
└── README.md
```

Folder `img/` digunakan oleh alamat foto sampul pada data katalog di `js/data.js`.

## 3. Cara menjalankan project

1. Ekstrak file ZIP project ke folder di komputer.
2. Buka Visual Studio Code.
3. Pilih **File > Open Folder**, lalu pilih folder `tugas_uts_web1`.
4. Pastikan folder `css`, `js`, dan `img` berada di dalam folder project yang sama dengan file HTML.
5. Jika belum ada, pasang ekstensi **Live Server** di Visual Studio Code.
6. Klik kanan `login.html`, lalu pilih **Open with Live Server**.
7. Browser akan membuka halaman login. Ikuti menu navigasi untuk mencoba halaman lainnya.

> Jangan memindahkan file HTML keluar dari folder project karena alamat relatif ke CSS, JavaScript, dan gambar bergantung pada struktur folder tersebut.

## 4. Akun contoh untuk login

Data akun contoh tersimpan di `dataPengguna` dalam `js/data.js`.

| Peran | Email | Password |
|---|---|---|
| User | rina@gmail.com | rina123 |
| User | agus@gmail.com | agus123 |
| Admin | siti@gmail.com | siti123 |

Akun tersebut hanya data dummy untuk pengujian lokal, bukan akun sungguhan.

## 5. Data katalog dan foto buku

Data katalog berada pada variabel `dataKatalogBuku` di `js/data.js`. Setiap objek buku memiliki properti berikut:

- `kodeBarang`: kode unik buku.
- `namaBarang`: judul buku.
- `jenisBarang`: kategori/jenis buku.
- `edisi`: edisi buku.
- `stok`: jumlah stok.
- `harga`: harga dalam bentuk teks.
- `cover`: alamat relatif file foto sampul.

Contoh:

```javascript
{
    kodeBarang: "ASIP4301",
    namaBarang: "Pengantar Ilmu Komunikasi",
    jenisBarang: "Buku Ajar",
    edisi: "2",
    stok: 548,
    harga: "Rp 180.000",
    cover: "img/pengantar_komunikasi.jpg"
}
```

Pastikan nama file pada properti `cover` sama persis dengan nama file di folder `img/`. Penulisan huruf besar/kecil dan ekstensi `.jpg` atau `.jpeg` harus sesuai.

## 6. Halaman aplikasi

- `login.html`: halaman login dengan data pengguna dummy.
- `dashboard.html`: menu utama/navigasi aplikasi.
- `stok.html`: daftar katalog dan formulir penambahan stok buku.
- `checkout.html`: halaman pemesanan/checkout.
- `tracking.html`: halaman pencarian informasi pengiriman.
- `index.html`: halaman awal/pengarah aplikasi.

## 7. Jika foto katalog tidak muncul

Periksa hal-hal berikut:

1. Pastikan kelima foto berada di folder `img/`.
2. Pastikan alamat `cover` di `js/data.js` diawali `img/`.
3. Cocokkan nama dan ekstensi file dengan nama yang tertulis di `data.js`.
4. Pastikan `stok.html` memanggil `js/data.js` sebelum `js/script.js`.
5. Muat ulang halaman browser. Jika perlu, tekan `Ctrl + F5`.

## 8. Catatan

- Project ini menggunakan data dummy JavaScript dan berjalan di sisi front-end.
- Perubahan data yang hanya disimpan dalam variabel JavaScript dapat kembali ke data awal ketika halaman dimuat ulang, kecuali ada mekanisme penyimpanan tambahan.
- Kolom penulis tidak tersedia pada data katalog awal, sehingga README dan tampilan katalog menggunakan properti yang memang tersedia (`namaBarang`, `jenisBarang`, dan `edisi`).
