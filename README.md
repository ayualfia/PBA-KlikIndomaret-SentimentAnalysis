# 🛒 Amazon Shopping Reviews Sentiment Analysis

Repositori ini berisi proyek analisis review aplikasi **Amazon Shopping** dari Google Play Store. Proyek ini dilakukan menggunakan Python dan Google Colab, mulai dari scraping data, exploratory data analysis, preprocessing teks, sentiment analysis menggunakan TextBlob, hingga representasi teks menggunakan Bag of Words dan TF-IDF.

---

## 📌 Informasi Proyek

| Keterangan | Detail |
|---|---|
| Aplikasi | Amazon Shopping |
| App ID | `com.amazon.mShop.android.shopping` |
| Platform | Google Play Store |
| Bahasa Review | English |
| Negara | United States |
| Author | Ayu Alfia Putri |
| Tools | Python, Google Colab, GitHub |

---

## 🎯 Tujuan Proyek

Tujuan dari proyek ini adalah:

1. Mengambil data review aplikasi Amazon Shopping dari Google Play Store.
2. Melakukan eksplorasi awal terhadap data review.
3. Melakukan preprocessing teks agar data siap dianalisis.
4. Melakukan sentiment analysis menggunakan TextBlob.
5. Membuat representasi teks menggunakan Bag of Words dan TF-IDF.
6. Menyiapkan data untuk analisis lanjutan seperti Vector Space Model dan cosine similarity.

---

## 📁 Struktur Repository

```text
PBA-Amazon-SentimentAnalysis/
│
├── data/
│   ├── amazon_reviews.csv
│   ├── amazon_reviews_preprocessed.csv
│   ├── amazon_reviews_sentiment.csv
│   └── hasil_BoW_TF-IDF/
│       ├── amazon_bow_unigram_top_words.csv
│       ├── amazon_bow_bigram_top_words.csv
│       ├── amazon_bow_trigram_top_words.csv
│       ├── amazon_tfidf_unigram_top_words.csv
│       ├── amazon_tfidf_bigram_top_words.csv
│       ├── amazon_bow_matrix_sample.csv
│       └── amazon_bow_tfidf_summary.xlsx
│
├── notebook/
│   ├── week2_amazon_shopping_reviews_scrapping.ipynb
│   ├── week3_amazonshopping_review_preprocessing.ipynb
│   ├── week3_amazonshopping_review_sentiment.ipynb
│   ├── week4_amazonshopping_review_BoW_TF_IDF.ipynb
│   └── week5_PBA_Vector_Space_Model.ipynb
│
├── README.md
└── .gitattributes
```

---

## 🧩 Alur Pengerjaan

### 1. Scraping dan EDA

**Notebook:** `week2_amazon_shopping_reviews_scrapping.ipynb`

Tahap ini digunakan untuk mengambil review aplikasi Amazon Shopping dari Google Play Store dan melakukan exploratory data analysis awal.

Analisis yang dilakukan:

- Scraping review dari Google Play Store
- Pengecekan struktur dataset
- Missing value dan duplikat
- Distribusi rating
- Tren review berdasarkan waktu
- Panjang review
- Word frequency dan word cloud

**Output:**

```text
data/amazon_reviews.csv
```

---

### 2. Data Preprocessing

**Notebook:** `week3_amazonshopping_review_preprocessing.ipynb`

Tahap ini digunakan untuk membersihkan teks review agar siap digunakan untuk sentiment analysis dan representasi teks.

Tahapan preprocessing:

- Expand contractions
- Lowercasing
- Punctuation removal
- Spelling correction
- Tokenization
- Stopword removal
- Lemmatization
- Stemming
- Rare words removal
- Common words removal

**Output:**

```text
data/amazon_reviews_preprocessed.csv
```

Kolom utama hasil preprocessing:

```text
final_clean_text
final_stemmed_text
```

---

### 3. Sentiment Analysis

**Notebook:** `week3_amazonshopping_review_sentiment.ipynb`

Tahap ini digunakan untuk menganalisis sentimen review menggunakan **TextBlob**.

Hasil yang diperoleh:

- `polarity`
- `subjectivity`
- `sentiment_textblob`
- `sentiment_rating`

Kategori sentimen:

```text
Positive
Neutral
Negative
```

Visualisasi yang digunakan:

- Distribusi sentimen
- Pie chart sentimen
- Distribusi polarity dan subjectivity
- Scatter plot polarity dan subjectivity
- Heatmap perbandingan rating dan sentimen
- Word cloud berdasarkan sentimen

**Output:**

```text
data/amazon_reviews_sentiment.csv
```

---

### 4. Bag of Words dan TF-IDF

**Notebook:** `week4_amazonshopping_review_BoW_TF_IDF.ipynb`

Tahap ini digunakan untuk membuat representasi teks menggunakan **Bag of Words** dan **TF-IDF**.

Pada tahap ini tidak dilakukan preprocessing ulang karena data sudah dibersihkan pada tahap sebelumnya. Kolom utama yang digunakan adalah:

```text
final_clean_text
```

Analisis yang dilakukan:

- Bag of Words unigram, bigram, dan trigram
- TF-IDF unigram dan bigram
- BoW matrix sample
- Top words dan top n-grams
- Visualisasi word frequency dan word cloud
- Export hasil ke CSV dan Excel

**Output:**

```text
data/hasil_BoW_TF-IDF/
```

---

### 5. Vector Space Model

**Notebook:** `week5_PBA_Vector_Space_Model.ipynb`

Tahap ini digunakan untuk menghitung kemiripan antar review menggunakan representasi vektor dan cosine similarity.

---

## 📊 Dataset Utama

| File | Keterangan |
|---|---|
| `amazon_reviews.csv` | Dataset raw hasil scraping |
| `amazon_reviews_preprocessed.csv` | Dataset hasil preprocessing |
| `amazon_reviews_sentiment.csv` | Dataset hasil sentiment analysis |
| `amazon_bow_tfidf_summary.xlsx` | Ringkasan hasil BoW dan TF-IDF |

---

## 🛠️ Library yang Digunakan

Library utama yang digunakan dalam proyek ini:

```text
pandas
numpy
matplotlib
seaborn
google-play-scraper
nltk
contractions
textblob
wordcloud
scikit-learn
openpyxl
tqdm
```

---

## ⚙️ Cara Menjalankan

Clone repository:

```bash
git clone https://github.com/ayualfia/PBA-Amazon-SentimentAnalysis.git
cd PBA-Amazon-SentimentAnalysis
```

Install library melalui Google Colab:

```python
!pip install google-play-scraper wordcloud nltk contractions textblob scikit-learn openpyxl tqdm -q
```

Jalankan notebook secara berurutan:

```text
1. week2_amazon_shopping_reviews_scrapping.ipynb
2. week3_amazonshopping_review_preprocessing.ipynb
3. week3_amazonshopping_review_sentiment.ipynb
4. week4_amazonshopping_review_BoW_TF_IDF.ipynb
```

---

## 📈 Visualisasi

Beberapa visualisasi yang digunakan dalam proyek ini:

- Distribusi rating review
- Tren jumlah review
- Missing value chart
- Word frequency
- Word cloud
- Distribusi sentimen
- Scatter plot polarity dan subjectivity
- Heatmap rating dan sentimen
- Top words BoW
- Top words TF-IDF

---


## ✅ Kesimpulan Singkat

Proyek ini menunjukkan proses analisis teks pada review aplikasi Amazon Shopping, mulai dari pengambilan data, eksplorasi, preprocessing, sentiment analysis, Bag of Words, TF-IDF, hingga Vector Space Model. Hasil analisis membantu memahami kecenderungan opini pengguna terhadap aplikasi Amazon Shopping berdasarkan review yang diberikan.

---

## 👩‍💻 Author

**Ayu Alfia Putri**  
Project: Amazon Shopping Reviews Sentiment Analysis
