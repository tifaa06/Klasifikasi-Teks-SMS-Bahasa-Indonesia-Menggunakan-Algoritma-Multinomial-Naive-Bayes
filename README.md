# Klasifikasi SMS Teks Bahasa Indonesia Menggunakan Multinomial Naive Bayes & TF-IDF

Proyek ini merupakan Tugas Akhir mata kuliah Kecerdasan Buatan yang bertujuan untuk mendeteksi dan mengklasifikasikan pesan SMS ke dalam tiga kategori: **Normal**, **Penipuan (Spam/Scam)**, dan **Promo**.

* [Nur lathifatur Rabbani] - [245060300111028]

## Repositori & Akses Demo
* **Google Colab Notebook:** [https://colab.research.google.com/drive/1bOlOxwR0wrMNT-DgNtz13YCeB5xgnAUK?usp=sharing]
* **Dataset:** 1.143 baris data SMS (https://gist.github.com/agtbaskara/614d62adbcd41408ee956ca70345f75f)

## Ringkasan Performa Model
Model ini diuji menggunakan proporsi data latih 80% dan data uji 20% (229 data uji) dengan hasil sebagai berikut:
* **Akurasi Global:** 91.70%
* **Precision (Penipuan):** 97% (Sangat baik dalam menekan *False Positive*)
* **Recall (Promo):** 94% (Sangat sensitif dalam menjaring pesan iklan)

## Alur Program & Teknologi
Proyek ini dibangun menggunakan Python dengan pustaka utama `scikit-learn`, `pandas`, dan `NLTK`/`Sastrawi` (jika menggunakan text preprocessing). Alur utamanya meliputi:
1. **Text Preprocessing:** Case folding, Filtering/Cleansing, Tokenizing, Stemming/Lemmatization.
2. **Feature Extraction:** Mengubah teks menjadi vektor numerik menggunakan *TF-IDF Vectorizer*.
3. **Classification:** Klasifikasi probabilitas menggunakan *Multinomial Naive Bayes*.
4. **Evaluation:** Pengujian performa menggunakan *Classification Report* dan *Confusion Matrix*.

## Cara Menjalankan Proyek
Karena proyek ini berbasis Google Colab, maka tidak perlu melakukan instalasi lokal. berikut langkah-langkah menjalankann proyek:
1. Buka link **Google Colab** yang tertera di atas.
2. Pastikan file dataset sudah diunggah ke Google Drive atau di-*upload* langsung ke sesi penyimpanan Colab jika diminta oleh *script*.
3. Pilih menu **Runtime** > **Run all** (atau tekan `Ctrl + F9`) untuk menjalankan seluruh blok kode dari awal hingga evaluasi model selesai.