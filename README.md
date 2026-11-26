# Analisis Sentimen Translokasi Badak Jawa

Analisis sentimen publik terhadap isu translokasi Badak Jawa (*Rhinoceros sondaicus*) menggunakan Natural Language Processing (NLP).

## Dataset
- **Sumber**: Komentar YouTube (video: f9k1WOIvahE)
- **Jumlah**: 100 komentar
- **Label**: Negatif / Netral / Positif (anotasi manual)

## Metodologi
1. **Scraping** - YouTube Data API v3
2. **Preprocessing** - case folding, HTML cleaning, filter non-alfabet
3. **Ekstraksi fitur** - TF-IDF
4. **Klasifikasi** - Naive Bayes dan SVM
5. **Evaluasi** - Confusion Matrix dan Classification Report

## Cara Menjalankan

pip install -r requirements.txt
cp .env.example .env
# edit .env, isi YOUTUBE_API_KEY
jupyter notebook

## Struktur Notebook
- 00_install.ipynb - instalasi dependency
- 01_scraping.ipynb - scraping komentar YouTube
- 02_eda.ipynb - exploratory data analysis
- 03_preprocessing.ipynb - cleaning teks
- 04_modeling.ipynb - training dan evaluasi model
- 05_visualization.ipynb - visualisasi hasil

## Hasil
- **Akurasi SVM**: 85 persen
- **Catatan**: model masih lemah pada kelas minoritas karena keterbatasan data (3 sampel Positif, 12 Netral)

## Author
Dayona Zain - https://github.com/dayonazain-cmd
