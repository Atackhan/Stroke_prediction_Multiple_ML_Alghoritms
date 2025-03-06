# 🏡 Costa Rican Household Poverty Level Prediction

Bu proje, **Costa Rica'daki hanelerin sosyoekonomik durumunu sınıflandırmak** amacıyla makine öğrenimi modelleri geliştirmeyi hedeflemektedir. Veri analizi, veri temizleme, özellik mühendisliği ve modelleme adımlarını içerir.

---

## 📁 Veri Seti

Veri seti, [Kaggle Costa Rican Household Poverty Level Prediction](https://www.kaggle.com/c/costa-rican-household-poverty-prediction) yarışmasından alınmıştır.

**Dosyalar:**
- `train.csv` (Eğitim verisi)
- `codebook.csv` (Veri açıklamaları içeren sözlük dosyası)

---

## 🔍 Kullanılan Kütüphaneler
- `pandas`
- `numpy`
- `matplotlib`
- `scikit-learn`

Kurulum için:
```
pip install pandas numpy matplotlib scikit-learn
```

---

## 🛠️ Proje Adımları

### 1. Veri Yükleme ve Temel Analiz
- Verinin yüklenmesi ve genel bilgilerinin incelenmesi.

### 2. Veri Temizleme ve Ön İşleme
- Eksik değerlerin tespiti ve median değerlerle doldurulması.
- Kategorik verilerin sayısal değerlere dönüştürülmesi.

### 3. Özellik Mühendisliği (Feature Engineering)
Yeni özelliklerin oluşturulması:
- Kişi başına düşen kira miktarları
- Yatak odası ve oda başına düşen kişi sayısı
- Elektronik cihaz sayıları
- Demografik oranlar (çocuk, yetişkin ve yaşlı oranları vb.)

### 4. Makine Öğrenmesi Modelleri
- Eğitim ve test verilerinin oluşturulması.
- Kullanılan modeller:
  - **Support Vector Machine (SVM)**
  - **Stochastic Gradient Descent (SGDClassifier)**

### 5. Model Değerlendirmesi
Modellerin performansları aşağıdaki metriklerle ölçülmüştür:
- Accuracy
- Precision
- Recall
- F1 Score

---

## 📊 Model Sonuçları

| Model             | Accuracy | Precision | Recall | F1 Score |
|-------------------|----------|-----------|--------|----------|
| **SVM**           | 0.63     | 0.40      | 0.63   | 0.49     |
| **SGD Classifier**| 0.61     | 0.49      | 0.61   | 0.52     |

> ⚠️ **Not:** Modellerin performansını artırmak için daha ileri seviye modeller (XGBoost, LightGBM vb.) kullanılabilir ve hiperparametre optimizasyonu yapılabilir.

---

## 🚀 Gelecek Planları
- XGBoost ve LightGBM gibi ileri seviye algoritmaların eklenmesi.
- SMOTE yöntemi ile sınıf dengesizliğinin giderilmesi.
- Hiperparametre optimizasyonu (GridSearchCV, RandomizedSearchCV).

---

## 📌 Nasıl Kullanılır?
1. Bu repository'i klonlayın:
```
git clone https://github.com/kullanici-adiniz/proje-adiniz.git
```

2. Gerekli kütüphaneleri yükleyin:
```
pip install -r requirements.txt
```

3. Notebook'u çalıştırmak için:
```
jupyter notebook costa-rican.ipynb
```

---
