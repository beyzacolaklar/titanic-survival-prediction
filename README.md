# titanic-survival-prediction

# 🚢 Titanic Survival Prediction

> Makine öğrenmesi algoritmaları kullanarak Titanic kazasındaki yolcuların hayatta kalma durumlarını tahmin eden uçtan uca bir veri bilimi projesi.

---

## 📌 Proje Özeti
Bu çalışmada, Titanic veri seti üzerindeki eksik veriler temizlenmiş, yeni öznitelikler türetilmiş (Özellik Mühendisliği) ve farklı sınıflandırma modelleri karşılaştırılarak en yüksek doğruluk oranına ulaşılmıştır.

* **Problem Türü:** İkili Sınıflandırma (Binary Classification - 0 veya 1)
* **En İyi Model:** En Uygun Sınıflandırma Modeli (%80.22 Doğruluk)

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

| Model | Doğruluk (Accuracy) |
| :--- | :---: |
| **Başlangıç (Referanslar)** | ~%63,00 |
| **Karar Ağacı** | %74,63 |
| **Lojistik Regresyon** | %79,85 |
| **En İyi Model ⭐** | **%80,22** |

---

## 🧭 Özet Mimari Akış
`Ham Veri (CSV)` ➔ `Ön İşleme & EDA` ➔ `Özellik Mühendisliği` ➔ `En Uygun Model (%80.22)` ➔ `Hata & Önem Analizi`

---

## 💡 Kritik Bulgular
* **Özelliğin Önemi:** Modelin kararlarını veren en baskın özellikler **Cinsiyet (`Sex` - %24.2)** ve **Bilet Ücreti (`Fare` - %22.0)** olmuştur.
* **Hata Analizi:** Modeller vefat edenleri yüksek başarıyla tahmin ederken, en çok **Yanlış Negatif (Kaçırılan Kurtulanlar)** grubunda zorlanmıştır.

---

## 🧰 Technologies Used
* Python
* Pandas
* NumPy
* Matplotlib
* Seaborn
* Scikit-learn

---

## 📁 Project Structure
```text
Titanic-Survival-Prediction/


🚀 Installation
Bash
git clone [https://github.com/ilaydaylcnz/titanic-machine-learning-project.git](https://github.com/ilaydaylcnz/titanic-machine-learning-project.git)
Bash
pip install pandas numpy matplotlib seaborn scikit-learn
Run the notebook using Jupyter Notebook or Kaggle.
│
├── data-science-titanic-project.ipynb
├── README.md
└── images/ (optional)
