
# Sistem Analisis Nilai Mahasiswa Menggunakan Array

## Deskripsi Program

Program ini dibuat menggunakan bahasa pemrograman **Python** untuk mengolah dan menganalisis data nilai mahasiswa. Dalam program ini, nilai mahasiswa disimpan menggunakan **struktur data array (list)** sehingga data dapat diproses secara sistematis.

Pengguna diminta untuk memasukkan **10 nilai mahasiswa**, kemudian program akan melakukan beberapa proses perhitungan untuk mendapatkan informasi penting dari data tersebut, seperti:

* Menentukan **nilai tertinggi**
* Menentukan **nilai terendah**
* Menghitung **rata-rata nilai**
* Menghitung **jumlah mahasiswa yang lulus**

Mahasiswa dinyatakan **lulus apabila nilai ≥ 60**.

Selain menampilkan hasil dalam bentuk teks, program juga menampilkan **visualisasi data menggunakan grafik batang** untuk memperjelas hasil analisis nilai mahasiswa.

---

# 1 Penjelasan Konsep Array

Array merupakan salah satu **struktur data** yang digunakan untuk menyimpan beberapa data dalam satu variabel yang sama. Dengan menggunakan array, kita dapat mengelola banyak data sekaligus tanpa harus membuat banyak variabel.

Pada program ini, array digunakan untuk menyimpan nilai mahasiswa yang dimasukkan oleh pengguna.

Program terlebih dahulu membuat **list kosong** untuk menampung data nilai.

```python
nilai_mahasiswa = []
```

Selanjutnya program menggunakan **perulangan (loop)** untuk meminta pengguna memasukkan nilai sebanyak 10 kali.

```python
for i in range(10):
    nilai = int(input(f"Input nilai ke-{i+1}: "))
    nilai_mahasiswa.append(nilai)
```

Penjelasan kode tersebut:

* `range(10)` digunakan untuk melakukan perulangan sebanyak 10 kali
* `input()` digunakan untuk menerima nilai dari pengguna
* `int()` digunakan untuk mengubah input menjadi bilangan bulat
* `append()` digunakan untuk menambahkan nilai ke dalam array

Setelah semua nilai dimasukkan, data tersebut tersimpan dalam array `nilai_mahasiswa` dan siap untuk diproses lebih lanjut.

Contoh isi array:

```
[78, 55, 54, 90, 88, 75, 60, 67, 80, 72]
```

Array ini kemudian digunakan untuk melakukan berbagai proses analisis nilai mahasiswa.

---

# 2 Proses Analisis Data

![](https://github.com/galang-ajus/tugas-struktur-data/blob/main/Foto/Cuplikan%20layar%202026-03-14%20115636.jpg?raw=true)

ini adalah output dari tambah nilai



![](https://github.com/galang-ajus/tugas-struktur-data/blob/main/Foto/Cuplikan%20layar%202026-03-14%20115724.jpg?raw=true)

ini adalah output dari grafik batang nilai



![](https://github.com/galang-ajus/tugas-struktur-data/blob/main/Foto/Cuplikan%20layar%202026-03-14%20115757.jpg?raw=true)

ini adalah output dari grafik batang nilai kelulusan


# 3 Visualisasi Grafik

Program juga menampilkan hasil analisis dalam bentuk **grafik batang menggunakan library matplotlib**.

### Grafik Nilai Tertinggi dan Terendah

Grafik ini digunakan untuk menampilkan perbandingan antara nilai tertinggi dan nilai terendah.

```python
kategori_nilai = ["Nilai Tertinggi", "Nilai Terendah"]
data_nilai_grafik = [nilai_tertinggi, nilai_terendah]

plt.bar(kategori_nilai, data_nilai_grafik)
```

Grafik ini memudahkan pengguna untuk melihat perbedaan nilai secara visual.

---

### Grafik Kelulusan Mahasiswa

Grafik ini menampilkan jumlah mahasiswa yang **lulus dan tidak lulus**.

```python
status = ["Lulus", "Tidak Lulus"]
jumlah = [jumlah_lulus, len(nilai_mahasiswa) - jumlah_lulus]

plt.bar(status, jumlah)
```

Grafik ini memberikan gambaran mengenai distribusi kelulusan mahasiswa.

---

# 4 Analisis Kompleksitas

Analisis kompleksitas digunakan untuk mengetahui seberapa besar waktu yang dibutuhkan program untuk memproses data berdasarkan jumlah input.

### Input Data

Proses memasukkan nilai menggunakan perulangan sebanyak **n data**.

Kompleksitas waktu:

**O(n)**

---

### Pencarian Nilai Tertinggi dan Terendah

Fungsi `max()` dan `min()` akan memeriksa semua data dalam array.

Kompleksitas waktu:

**O(n)**

---

### Perhitungan Rata-rata

Fungsi `sum()` menjumlahkan seluruh nilai dalam array.

Kompleksitas waktu:

**O(n)**

---

### Perhitungan Jumlah Lulus

Program memeriksa setiap nilai menggunakan perulangan.

Kompleksitas waktu:

**O(n)**

---

### Kesimpulan Kompleksitas

Karena hampir semua proses harus membaca seluruh data dalam array, maka kompleksitas keseluruhan program adalah:

**O(n)**

Artinya waktu eksekusi program akan meningkat secara **linear** seiring bertambahnya jumlah data nilai yang diproses.

---

# 5 Refleksi Pembelajaran

Melalui pembuatan program ini saya mempelajari bagaimana menggunakan **struktur data array (list)** untuk menyimpan dan mengelola data dalam jumlah banyak. Penggunaan array mempermudah proses pengolahan data karena setiap nilai dapat diproses menggunakan perulangan.

Saya juga belajar menggunakan berbagai **fungsi bawaan Python** seperti `max()`, `min()`, `sum()`, dan `len()` untuk melakukan perhitungan data dengan lebih efisien.

Selain itu, saya mendapatkan pengalaman dalam membuat **visualisasi data menggunakan library matplotlib**, sehingga hasil analisis dapat ditampilkan dalam bentuk grafik yang lebih mudah dipahami.

Dari sisi algoritma, saya juga memahami bahwa sebagian besar operasi pada array memiliki kompleksitas waktu **O(n)** karena setiap elemen data harus diproses satu per satu.

Melalui program ini, saya menjadi lebih memahami penerapan struktur data array dalam pengolahan data serta bagaimana membuat program analisis data sederhana menggunakan Python.

