# titanic-survival-prediction

# 🚢 Titanic Survival Prediction

> Makine öğrenmesi algoritmaları kullanarak Titanic kazasındaki yolcuların hayatta kalma durumlarını tahmin eden uçtan uca bir veri bilimi projesi.

---

## 📌 Proje Özeti
Bu çalışmada, Titanic veri seti üzerindeki eksik veriler temizlenmiş, yeni öznitelikler türetilmiş (Feature Engineering) ve farklı sınıflandırma modelleri karşılaştırılarak en yüksek doğruluk oranına ulaşılmıştır.

* **Problem Türü:** İkili Sınıflandırma (Binary Classification - 0 veya 1)
* **En İyi Model:** Random Forest (%80.22 Accuracy)

---

## 🔄 Proje İş Akışı
1. **Keşifsel Veri Analizi (EDA):** Verinin yapısının incelenmesi ve görselleştirilmesi.
2. **Veri Ön İşleme:** Eksik verilerin doldurulması (`Age` -> Medyan) ve IQR yöntemiyle aykırı değerlerin baskılanması.
3. **Özellik Mühendisliği (Feature Engineering):** 
   - `FamilySize` ve `IsAlone` türetilmesi
   - `Name` sütunundan unvanların (`Title`) çekilmesi
   - One-Hot Encoding işlemleri
4. **Modelleme:** Baseline, Decision Tree, Logistic Regression ve Random Forest algoritmalarının koşturulması.

---

## 🏆 Model Performans Sonuçları

| Model | Doğruluk (Accuracy) | Durum |
| :--- | :---: | :--- |
| **Baseline (Referans)** | ~63.00% | Başlangıç Çizgisi |
| **Decision Tree** | 74.63% | Overfitting Eğilimli |
| **Logistic Regression** | 79.85% | Kararlı Model |
| **Random Forest ⭐** | **80.22%** | **Şampiyon Model** |


---

## 🧭 Özet Mimari Akış
`Ham Veri (CSV)` ➔ `Ön İşleme & EDA` ➔ `Özellik Mühendisliği` ➔ `Random Forest (%80.22)` ➔ `Hata & Önem Analizi`

---

## 💡 Kritik Bulgular
* **Feature Importance:** Modelin kararlarını veren en baskın özellikler **Cinsiyet (`Sex` - %24.2)** ve **Bilet Ücreti (`Fare` - %22.0)** olmuştur.
* **Hata Analizi:** Modeller vefat edenleri yüksek başarıyla tahmin ederken, en çok **False Negative (Kaçırılan Kurtulanlar)** grubunda zorlanmıştır.
