#UAS

#Tugas UAS Bahasa Pemrograman

Buatlah Program Sederhana Dengan Ketentuan:

Program harus dibuat dengan konsep modular dan OOP(pisahkan class data,class view,class process)

Program harus meminta input dari pengguna

Tambahkan validasi input(dapat menggunakan konsep eksepsi)

Program menampilkan hasil(dapat berupa table view)



KODE PROGRAM


    '''class DataTiket:
    def __init__(self, asal, tujuan, tanggal, jumlah_penumpang):
        self.asal = asal
        self.tujuan = tujuan
        self.tanggal = tanggal
        self.jumlah_penumpang = jumlah_penumpang

    class View:
    def tampilan_awal():
        print("Selamat datang di sistem pemesanan tiket kereta api!")
        print("Silakan masukkan data perjalanan Anda:")

        def tampilan_hasil(data_tiket):
        print("\nRincian Pesanan:")
        print("Asal:        ", data_tiket.asal)
        print("Tujuan:      ", data_tiket.tujuan)
        print("Tanggal:     ", data_tiket.tanggal)
        print("Jumlah:     ", data_tiket.jumlah_penumpang)

    class Proses:
    def validasi_input(data):
        # Tambahkan logika validasi di sini (misal: cek tipe data, rentang nilai)
        if not isinstance(data.jumlah_penumpang, int):
            raise ValueError("Jumlah penumpang harus berupa bilangan bulat.")
        if data.jumlah_penumpang <= 0:
            raise ValueError("Jumlah penumpang harus lebih dari 0.")
        # Tambahkan validasi lainnya sesuai kebutuhan

     def hitung_harga(data_tiket):
        # Tambahkan logika perhitungan harga di sini
        # (misal: berdasarkan jarak, tanggal, dan jumlah penumpang)
        harga_per_orang = 100000  # Contoh harga per orang
        total_harga = harga_per_orang * data_tiket.jumlah_penumpang
        return total_harga

    if __name__ == "__main__":
    View.tampilan_awal()

    asal = input("Asal: ")
    tujuan = input("Tujuan: ")
    tanggal = input("Tanggal (YYYY-MM-DD): ")
    jumlah_penumpang = int(input("Jumlah penumpang: "))

    data_tiket = DataTiket(asal, tujuan, tanggal, jumlah_penumpang)
    try:
        Proses.validasi_input(data_tiket)
        total_harga = Proses.hitung_harga(data_tiket)
        print("Total harga: Rp", total_harga)
    except ValueError as e:
        print("Terjadi kesalahan:", e)

    View.tampilan_hasil(data_tiket)'''


#Penjelasan
Program ini dirancang untuk mensimulasikan sistem pemesanan tiket kereta api sederhana dengan menerapkan prinsip Pemrograman Berorientasi Objek (OOP).
Program dibangun dari tiga elemen utama (class) yang bekerja bersama untuk menangani data, interaksi pengguna, dan logika proses.

1.Class DataTiket

Class ini digunakan untuk merepresentasikan data perjalanan yang dimasukkan oleh pengguna.

(class ini bertanggung jawab untuk menyimpan data perjalanan yang diinputkan oleh pengguna)

Atribut:

asal: Kota asal perjalanan.

tujuan: Kota tujuan perjalanan.

tanggal: Tanggal perjalanan (format diharapkan YYYY-MM-DD).

jumlah_penumpang: Jumlah penumpang yang akan bepergian.

Metode:

_init_(self, asal, tujuan, tanggal, jumlah_penumpang): Konstruktor untuk menginisialisasi atribut data perjalanan.

Detail Implementasi:

Kelas ini memiliki atribut (asal, tujuan, tanggal, jumlah_penumpang) untuk merepresentasikan data perjalanan.

Konstruktor( _init_) digunakan untuk menginisialisasi data saat objek DataTiket dibuat.

Fungsi Utama:

Mengorganisasi data pengguna dalam bentuk objek, sehingga mudah dikelola dan diolah dalam proses selanjutnya.


2.Class View

Class ini menangani interaksi dengan pengguna, khususnya menampilkan informasi.

(class ini menangani presentasi atau tampilan, bertindak sebagai penghubung antara program dan pengguna.)

Metode:

_tampilan_awal()_: Metode statis yang menampilkan ucapan selamat datang dan meminta pengguna untuk memasukkan data perjalanan mereka.

_tampilan_hasil (data_tiket)_: Metode statis yang menampilkan rincian pesanan berdasarkan

objek DataTiket.

Fungsi Utama:

Memberikan informasi kepada pengguna.

Menjaga struktur program terpisah dari proses internal yang dilakukan di kelas Proses.

2.Class Proses

Class ini berisi logika untuk memproses data perjalanan.

(class ini bertanggung jawab untuk memproses data yang dimasukkan pengguna, termasuk validasi dan perhitungan harga tiket) 

Metode:

_validasi_input(data)_: Memvalidasi data perjalanan. Contohnya:

Mengecek apakah _jumlah_penumpang_ berupa bilangan bulat.

Mengecek apakah jumlah penumpang lebih dari nol.

Validasi lainnya dapat ditambahkan sesuai kebutuhan.

_hitung_harga(data_tiket)_: Menghitung total harga berdasarkan jumlah penumpang. Dalam contoh ini, harga per penumpang ditentukan sebesar Rp10.000
Detail Implementasi:

1. Validasi Input:

Memastikan bahwa data sesuai dengan aturan bisnis.

Contoh validasi:

Jumlah penumpang harus berupa bilangan bulat.

Jumlah penumpang harus lebih dari 0.

Validasi tambahan (misal: format tanggal atau validitas kota) dapat ditambahkan.

2. Hitung Harga:

Menggunakan logika sederhana untuk menghitung total harga tiket:

Harga per penumpang ditentukan sebagai Rp10.000

Total harga _harga_per_orang x jumlah_penumpang_.


4.Bagian Utama Program

Kode utama berada di bawah blok if name adalah:_name_=="_main_": Langkah-langkah yang dilakukan

1. Menampilkan Tampilan Awal:

_View.tampilan_awal()_ memandu pengguna untuk memasukkan data.

2. Mengumpulkan Data Pengguna:

Mengambil input untuk asal, tujuan, tanggal, dan jumlah penumpang.

Membuat objek _DataTiket_ berdasarkan input tersebut.

3. Validasi Data:

Memanggil _Proses.validasi_input()_ untuk memastikan data valid.

Jika ada kesalahan, program menangkap dan menampilkan pesan kesalahan.

4. Menghitung Harga:

Menggunakan _Proses.hitung_harga()_ untuk menghitung total harga tiket.

Hasilnya ditampilkan di konsol.

5. Menampilkan Rincian Pesanan:

Menggunakan _View.tampilan_hasil (data_tiket)_ untuk menampilkan data pesanan yang telah dimasukkan.

Keunggulan Program

1.Pemisahan Tanggung Jawab:

Setiap kelas memiliki tugas spesifik (Data, Tampilan, dan Logika), sehingga program lebih modular dan mudah dikembangkan.

2.Kemudahan Pemeliharaan:

Perubahan pada salah satu kelas (misalnya, logika perhitungan harga di kelas Proses) tidak memengaruhi kelas lain.

3.Penerapan OOP

Pendekatan ini menciptakan struktur kode yang terorganisasi, memanfaatkan abstraksi melalui objek.

Kesimpulan:

Kode ini merupakan contoh sederhana penerapan konsep OOP untuk pemesanan tiket. Dengan pendekatan ini:

Program mudah dikelola, ditingkatkan, dan diperbaiki.

Setiap bagian kode memiliki tanggung jawab yang jelas.

Menyediakan landasan untuk sistem yang lebih kompleks.



