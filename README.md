# ERD-POS
ERD for interview. thanks to Angga Rahagiyanto

salah satu contoh ERD, berikut penjabarannya :

User mengkodekan produk (hubungan 1 ke banyak).
User dapat memproses beberapa invoice (hubungan 1 ke banyak).
User dapat memproses transaksi penerimaan (hubungan 1 ke banyak).
User dapat memproses transaksi pesanan pembelian (hubungan 1 ke banyak).
produk termasuk dalam kategori tertentu (hubungan 1 ke 1).
produk memiliki beberapa unit produk (hubungan 1 ke banyak).
produk memiliki beberapa transaksi penerimaan (hubungan 1 ke banyak).
produk juga termasuk dalam transaksi pesanan pembelian (hubungan 1 ke banyak).
pesanan pembelian akan diteruskan ke pemasok (hubungan 1 ke banyak).
Pemasok akan memasok produk yang diminta (hubungan 1 ke banyak).
produk termasuk dalam beberapa transaksi penjualan (hubungan 1 ke banyak).
penjualan menghasilkan Invoice (hubungan 1 ke banyak).
Invoice diberikan kepada pelanggan (hubungan 1 ke banyak). 


=========================================


Entitas Produk memiliki atribut berikut:
    ID Produk - primary key diwakili dengan garis bawah
    Kode
    Nama
    Patokan harga
    Unit dalam Persediaan
    Persentase Diskon
    Re Order Level
    ID Kategori - foreign key
    ID Unit - foreign key
    ID Pengguna - foreign key

Entitas Kategori Produk memiliki atribut berikut:

    ID Kategori - primary key diwakili dengan garis bawah
    Nama

Entitas Unit Produk memiliki atribut berikut:

    ID Unit - primary key diwakili dengan garis bawah
    Nama

Entitas Sales memiliki atribut berikut:

    ID Penjualan - primary key diwakili dengan garis bawah
    ID Faktur - foreign key
    ID Produk - foreign key
    Kuantitas
    Patokan harga
    Sub Total

Entitas Invoice memiliki atribut berikut:

    ID Invoice - primary key diwakili dengan garis bawah
    ID Pelanggan - foreign key
    Jumlah total
    Jumlah yang Ditenderkan
    Tipe pembayaran
    Nama akun bank
    Nomor rekening bank
    Tanggal Direkam
    ID Pengguna - kunci asing

Entitas Receive Produk memiliki atribut berikut:

    ID Receive Produk - primary key diwakili dengan garis bawah
    ID Produk - foreign key
    Kuantitas
    Patokan harga
    Sub Total
    Tanggal diterima
    ID Pemasok - foreign key
    ID Pengguna - foreign key

Entitas Pelanggan memiliki atribut berikut:

    ID Pelanggan - primary key diwakili dengan garis bawah
    Kode
    Nama
    Kontak Alamat

Entitas supplier memiliki atribut berikut:

    ID supplier - primary key diwakili dengan garis bawah
    Kode
    Nama
    Kontak
    email
    Alamat 

Entitas Purchase order memiliki atribut berikut:

     ID Purchase order - primary key diwakili dengan garis bawah
     ID Produk - foreign key
     Kuantitas
     Patokan harga
     Sub Total
     Tanggal pemesanan
     ID Pemasok - foreign key
     ID Pengguna - foreign key

Entitas user memiliki atribut berikut:

     ID user - primary key diwakili dengan garis bawah
     Nama lengkap
     Kontak
     Penunjukan
     Jenis akun
     Nama pengguna
     Kata sandi 
