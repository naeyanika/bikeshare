# Capital Bikeshare - Demand Prediction System

Aplikasi prediksi permintaan sepeda Capital Bikeshare menggunakan Machine Learning (XGBoost Regressor) yang dibangun dengan Streamlit.

## Deskripsi

Aplikasi ini memprediksi jumlah permintaan sepeda berdasarkan berbagai faktor seperti:

- Waktu (jam dalam sehari)
- Musim
- Cuaca
- Temperatur
- Kelembaban
- Hari libur

## Fitur

- **Prediksi Real-time**: Input parameter dan dapatkan prediksi langsung
- **Visualisasi Data**: Grafik interaktif untuk feature importance
- **Analisis Insights**: Informasi tentang peak hours dan weather impact
- **UI Modern**: Desain menggunakan Material Design dengan Capital Bikeshare branding
- **Model Performance Metrics**: Menampilkan R² Score dan RMSE

## Teknologi yang Digunakan

- Python 3.8+
- Streamlit
- XGBoost
- Pandas
- NumPy
- Plotly
- Pickle

## Instalasi

### 1. Clone Repository

```bash
git clone https://github.com/naeyanika/bikeshare.git
cd bikeshare
```

### 2. Install Dependencies

```bash
pip install -r requirements.txt
```

### 3. Jalankan Aplikasi

```bash
streamlit run app.py
```

Aplikasi akan berjalan di `http://localhost:8501`

## Struktur File

```
bikeshare/
├── app.py                      # Main application file
├── bike_sharing_model.pkl      # Trained XGBoost model
├── requirements.txt            # Python dependencies
└── README.md                   # Documentation (this file)
```

## Deploy ke Streamlit Cloud

### Persiapan

1. Pastikan semua file sudah di-push ke GitHub repository Anda
2. File yang dibutuhkan:
   - `app.py`
   - `bike_sharing_model.pkl`
   - `requirements.txt`

### Langkah Deploy

1. Buka [Streamlit Cloud](https://streamlit.io/cloud)
2. Login dengan akun GitHub Anda
3. Klik "New app"
4. Pilih repository: `naeyanika/bikeshare`
5. Branch: `master` (atau branch yang Anda gunakan)
6. Main file path: `app.py`
7. Klik "Deploy!"

### URL Aplikasi

Setelah deploy berhasil, aplikasi akan tersedia di:

```
[https://bikeshare-pwdk.streamlit.app](https://bikeshare-pwdk.streamlit.app/)
```

## Model Information

- **Model Type**: XGBoost Regressor
- **R² Score**: 69.76%
- **RMSE**: 97.08
- **Dataset**: Capital Bikeshare (2011-2012)
- **Features**: 7 features (hr, temp, atemp, hum, weathersit, season, holiday)

### Feature Importance

1. **Hour of Day** (45%) - Faktor paling berpengaruh
2. **Temperature** (18%)
3. **Season** (11%)
4. **Weather Situation** (9%)
5. **Feels Like Temperature** (7%)
6. **Holiday** (4%)
7. **Humidity** (3%)

## Cara Menggunakan

1. **Atur Parameter di Sidebar**:

   - Pilih musim (Spring, Summer, Fall, Winter)
   - Atur jam (0-23)
   - Pilih apakah hari libur atau tidak
   - Pilih kondisi cuaca
   - Atur temperatur (°C)
   - Atur feels like temperature (°C)
   - Atur kelembaban (%)

2. **Lihat Hasil Prediksi**:

   - Jumlah sepeda yang diprediksi
   - Level demand (Low, Moderate, High, Very High)
   - Rekomendasi operasional

3. **Analisis Insights**:
   - Peak demand hours
   - Weather impact analysis
   - Feature importance chart

## Branding

Aplikasi menggunakan warna official Capital Bikeshare:

- Primary Red: `#DA2128`
- Dark Red: `#B71C1C`
- White: `#FFFFFF`

## Author

**Dede Yudha N (Joey)**

- Purwadhika Capstone Project Module 3
- GitHub: [@naeyanika](https://github.com/naeyanika)

## License

This project is part of Purwadhika Capstone Project Module 3.

## Acknowledgments

- Capital Bikeshare untuk dataset
- Purwadhika Digital Technology School
- Streamlit untuk platform deployment

## Contact

Untuk pertanyaan atau feedback, silakan hubungi melalui GitHub issues.

---

**Note**: Pastikan file `bike_sharing_model.pkl` sudah tersedia di repository sebelum deploy ke Streamlit Cloud.
