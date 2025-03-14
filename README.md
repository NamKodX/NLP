# 🧠 NLP Toolkit

Bu proje, doğal dil işleme (NLP) görevlerini kolaylaştıran geniş kapsamlı bir Python araç takımıdır. İçinde metin analizinden duygu analizine, kelime vektörleştirmeden çeviri işlemlerine kadar birçok faydalı özellik barındırmaktadır.

## 🚀 Özellikler

- **Duygu Analizi**: Metinlerin olumlu, olumsuz veya nötr olarak sınıflandırılması.
- **Kelime Vektörleştirme**: TF-IDF, Word2Vec, FastText ve BERT ile kelime temsilcileri.
- **Dil Algılama**: Metnin hangi dilde olduğunu belirleme.
- **Çeviri Desteği**: Otomatik dil çevirisi (Google Translate API entegrasyonu opsiyonel).
- **Metin Temizleme**: Stopword kaldırma, lemmatization ve stemming işlemleri.
- **Adlandırılmış Varlık Tanıma (NER)**: Metindeki kişi, yer ve organizasyon adlarını çıkarma.
- **Kelime Frekans Analizi**: Metinde en sık geçen kelimeleri analiz etme.
- **Özetleme**: Uzun metinleri kısa özetlere dönüştürme.

---

## 🛠️ Kurulum

Projeyi sisteminize indirmek için:

```bash
git clone https://github.com/kullaniciadi/nlp-toolkit.git
cd nlp-toolkit
pip install -r requirements.txt
```

Eğer ek bağımlılıklar gerekirse:

```bash
pip install nltk spacy textblob transformers torch scikit-learn
python -m nltk.downloader punkt stopwords
python -m spacy download en_core_web_sm
```

---

## 📌 Kullanım

### **1️⃣ Duygu Analizi**

```python
from toolkit.sentiment import analyze_sentiment

text = "Bu film harikaydı! Bayıldım."
print(analyze_sentiment(text))
# Çıktı: Pozitif
```

### **2️⃣ Kelime Vektörleştirme**

```python
from toolkit.vectorizer import tfidf_vectorize

corpus = ["Bu bir test cümlesidir.", "NLP araçları çok faydalıdır."]
vectors = tfidf_vectorize(corpus)
print(vectors)
```

### **3️⃣ Adlandırılmış Varlık Tanıma (NER)**

```python
from toolkit.ner import extract_entities

text = "Elon Musk, Tesla ve SpaceX'in CEO'sudur."
print(extract_entities(text))
# Çıktı: [('Elon Musk', 'PERSON'), ('Tesla', 'ORG'), ('SpaceX', 'ORG')]
```

---

## 🤝 Katkıda Bulunma

Eğer projeye katkıda bulunmak isterseniz:

1. Depoyu çatallayın (fork).
2. Yeni bir dal (branch) oluşturun (`git checkout -b yeni-ozellik`).
3. Geliştirmelerinizi yapın ve değişiklikleri işleyin (`git commit -m 'Yeni özellik eklendi'`).
4. Deponuza gönderin (`git push origin yeni-ozellik`).
5. Bir çekme isteği (pull request) oluşturun.

---

## 📜 Lisans

Bu proje MIT Lisansı ile lisanslanmıştır. Daha fazla bilgi için `LICENSE` dosyasına göz atabilirsiniz.

---

## 📬 İletişim

Herhangi bir sorunuz olursa, GitHub üzerinden issue açabilir veya benimle iletişime geçebilirsiniz! 🚀
