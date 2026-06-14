# 🌾 Prediksi Produksi Padi Menggunakan Regresi Linear & Sliding Window

Repositori ini berisi proyek analisis data dan peramalan (*forecasting*) produksi padi menggunakan metode **Regresi Linear Sederhana** yang dikombinasikan dengan teknik **Sliding Window (Ukuran Jendela = 3)**.

---

## 📊 Dataset Historis
Berikut adalah data aktual produksi padi yang digunakan dalam analisis (Periode 2021 - 2025):

| Tahun | X | Produksi Padi (Ton) (Y) |
|-------|---|-------------------------|
| 2021  | 1 | 900,000                 |
| 2022  | 2 | 920,000                 |
| 2023  | 3 | 915,000                 |
| 2024  | 4 | 935,000                 |
| 2025  | 5 | 950,000                 |

---

## ⚙️ Metodologi Analisis
Program ini membagi data historis ke dalam sub-jendela bergerak dengan ukuran $N=3$ untuk menghitung koefisien regresi lokal:
$$\text{Persamaan:} \quad Y = a + bX$$

Dengan metode ini, setiap jendela waktu menghasilkan persamaan unik untuk memproyeksikan tren terdekat secara dinamis.

### 📈 Hasil Perhitungan Jendela (Sliding Window):
* **Jendela 1 (Data Historis 2021 - 2023):**
  * Persamaan: $Y = 895000.00 + (7500.00)X$
  * Hasil Prediksi Tahun 2024: **925,000.00 Ton**
* **Jendela 2 (Data Historis 2022 - 2024):**
  * Persamaan: $Y = 900833.33 + (7500.00)X$
  * Hasil Prediksi Tahun 2025: **938,333.33 Ton**
* **Jendela 3 (Data Historis 2023 - 2025):**
  * Persamaan: $Y = 855000.00 + (17500.00)X$
  * Hasil Prediksi Tahun 2026: **960,000.00 Ton**

### 🎯 Kesimpulan Akhir:
> **Prediksi Total Produksi Padi untuk Tahun 2026 adalah 960,000.00 Ton.**

---

## 🚀 Cara Menjalankan Program

Ikuti langkah-langkah di bawah ini untuk menjalankan program prediksi produksi padi di komputer Anda:

### 1. Kloning Repositori
Buka terminal, Git Bash, atau Command Prompt, lalu jalankan perintah berikut untuk mengunduh proyek:
```bash
git clone [https://github.com/Imannugraha79/prediksi-produksi-padi.git](https://github.com/Imannugraha79/prediksi-produksi-padi.git)
cd prediksi-produksi-padi
```
### 2. Memasang Dependensi (Opsional)
Program ini menggunakan pustaka pandas dan matplotlib. Anda bisa memasangnya secara manual menggunakan perintah:

Bash
pip install pandas matplotlib
💡 Catatan: Script main.py sudah dilengkapi dengan fitur auto-install. Jika pustaka di atas belum terpasang di perangkat Anda, program akan mencoba mengunduhnya secara otomatis saat pertama kali dijalankan.

### 3. Memastikan File Dataset
Pastikan file data historis data_regresi_padi.csv berada di dalam folder yang sama dengan file main.py. Jika file tersebut hilang atau dipindahkan, program akan menampilkan pesan error.

### 4. Menjalankan Program Utama
Eksekusi perintah berikut di terminal Anda untuk memulai analisis regresi linear dan visualisasi data:

Windows:
Bash
python main.py

macOS / Linux:
Bash
python3 main.py

### 5. Hasil Akhir (Output)
Terminal: Akan menampilkan perhitungan manual Sliding Window (Jendela 1 hingga 3) beserta hasil akhir prediksi produksi padi untuk tahun 2026.

Visualisasi: Program akan otomatis membuka jendela baru yang menampilkan grafik perbandingan antara Data Aktual dan Hasil Prediksi.


---

### 🛠️ Tips Tambahan Sebelum Push ke GitHub:
Karena di panduan di atas disebutkan file `data_regresi_padi.csv`, pastikan file CSV tersebut **ikut ter-upload** ke repositori GitHub kamu bersama dengan `main.py`, jika tidak programnya akan langsung *force close* saat dijalankan orang lain.
