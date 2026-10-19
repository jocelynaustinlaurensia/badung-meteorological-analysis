# Analisis Meteorologi & Pemodelan Suhu Kabupaten Badung (2010–2025)

Repositori ini memuat proyek analisis data meteorologi dan implementasi model regresi linier untuk memprediksi suhu rata-rata harian (`temperature_2m_mean`) di wilayah Kabupaten Badung berdasarkan data iklim historis periode 2010 hingga 2025.

Ringkasan Dataset
- Sumber Data: Data Koordinat Badung (`.xlsx`)
- Total Observasi: 5.844 baris (rentang waktu: 01 Januari 2010 – 31 Desember 2025)
- Status Integritas: 100% data valid dan tidak memiliki nilai yang hilang (zero missing values).

Fitur & Variabel Analisis
- Variabel Target ($Y$): `temperature_2m_mean` (Suhu rata-rata harian, °C)
- Variabel Prediktor ($X$):
  - `temperature_2m_max` (°C) — Suhu harian maksimum
  - `temperature_2m_min` (°C) — Suhu harian minimum
  - `daylight_duration` (detik) — Durasi penyinaran matahari
  - `rain_sum` (mm) — Akumulasi curah hujan harian
  - `wind_speed_10m_max` (km/jam) — Kecepatan angin maksimum

Alur Analisis & Metodologi
1. Data Ingestion & Integrity Audit: Pemeriksaan struktur data, sanitasi duplikasi baris/waktu, dan penataan format datetime.
2. Exploratory Data Analysis (EDA): Analisis statistik deskriptif, histogram distribusi suhu, dan deteksi anomali (*boxplot*).
3. Model Preparation: Pemisahan fitur prediktor dan variabel target untuk pemodelan `LinearRegression` menggunakan pustaka `scikit-learn`.

Pustaka yang Digunakan
- Data Manipulation: `pandas`, `numpy`
- Machine Learning & Evaluasi: `scikit-learn`
- Visualisasi Data: `matplotlib`, `seaborn`
