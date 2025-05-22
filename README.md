```markdown
# 📰 Fake News Detector Indonesia 🇮🇩
Deteksi berita palsu dan fakta berbahasa Indonesia menggunakan Machine Learning.

## 📌 Deskripsi
Proyek ini bertujuan untuk membangun model machine learning yang mampu mengklasifikasikan apakah suatu berita merupakan fakta atau hoaks. Model dilatih menggunakan dataset berita Indonesia yang mencakup berita dari media terpercaya serta berita palsu/hoaks dari sumber seperti TurnBackHoax.

## 🧠 Teknologi & Tools
- Python 3.x
- Scikit-learn
- Pandas & Numpy
- Sastrawi (untuk preprocessing bahasa Indonesia)
- TF-IDF Vectorizer
- Logistic Regression (dapat ditingkatkan ke BERT)

## 📁 Struktur Proyek
```

📦 fake-news-detector
├── data/
│   ├── hoax.csv
│   ├── real.csv
├── model/
│   ├── model.pkl
│   ├── tfidf\_vectorizer.pkl
├── notebooks/
│   └── FakeNewsDetector.ipynb
├── predict.py
├── train.py
└── README.md

````

## 📝 Dataset
Dataset yang digunakan:
- [Indonesian Fact and Hoax Political News - Kaggle](https://www.kaggle.com/datasets/linkgish/indonesian-fact-and-hoax-political-news)
- [Hoax News Indonesia - Kaggle](https://www.kaggle.com/datasets/vijayandika/hoax-news-indonesia)

Dataset berisi kolom `content` dan `label` (`hoax` atau `fact`).

## ⚙️ Instalasi

1. Clone repositori:
```bash
git clone https://github.com/username/fake-news-detector-id.git
cd fake-news-detector-id
````

2. Buat virtual environment (opsional):

```bash
python -m venv venv
source venv/bin/activate  # Linux/Mac
venv\Scripts\activate     # Windows
```

3. Install dependencies:

```bash
pip install -r requirements.txt
```

4. Jalankan notebook atau script pelatihan:

```bash
jupyter notebook notebooks/FakeNewsDetector.ipynb
```

## 🚀 Cara Prediksi

Setelah model dilatih, kamu bisa gunakan fungsi prediksi seperti berikut:

```python
from predict import predict_news

news = "Vaksin Covid-19 menyebabkan autisme menurut pesan berantai di WhatsApp."
print(predict_news(news))  # Output: FAKE 🚫
```

## 📊 Contoh Output

| Berita                                                                    | Prediksi |
| ------------------------------------------------------------------------- | -------- |
| "Pemerintah resmi menaikkan subsidi BBM untuk masyarakat tidak mampu."    | REAL ✅   |
| "Minum air panas setiap 15 menit bisa membunuh virus corona dalam tubuh." | FAKE 🚫  |

## 🔒 License

Proyek ini menggunakan lisensi [MIT](LICENSE).

## 🙋‍♂️ Kontribusi

Pull request sangat terbuka. Untuk perubahan besar, silakan buka issue terlebih dahulu.

---

Dibuat oleh Ahmad Syahreza.

```


