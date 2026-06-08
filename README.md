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

1. **Clone Repositori Ini**
   ```bash
   git clone [https://github.com/USERNAME_ANDA/prediksi-produksi-padi.git](https://github.com/USERNAME_ANDA/prediksi-produksi-padi.git)
   cd prediksi-produksi-padi