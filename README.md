# 🚢 Titanic Survival Analysis - Machine Learning Case Study

Bu proje, veri bilimi ve analitiği eğitimim kapsamında **uçtan uca bir makine öğrenmesi sürecini** (End-to-End ML Pipeline) deneyimlemek amacıyla geliştirilmiştir. Veri temizliğinden başlayarak, hiperparametre optimizasyonuna kadar tüm süreçler adım adım kurgulanmıştır.

## 🎯 Projenin Amacı
Sadece yüksek skor almak değil; veriyi doğru yorumlamak, gerçekçi analiz süreçleri kurmak ve algoritmaların arka planındaki mantığı (özellikle Pipeline ve GridSearchCV mimarisini) kavramaktır. Kaggle'da elde edilen **[0.77272]** skoru, modelin veri içindeki kalıpları ezberlemeden öğrendiğini göstermektedir.

## 🛠️ Kullanılan Teknolojiler ve Yöntemler
* **Veri Manipülasyonu:** `Pandas`, `NumPy`
* **Makine Öğrenmesi (Scikit-Learn):**
    * **Modeller:** Random Forest, Support Vector Classifier (SVC), AdaBoost
    * **Veri Ön İşleme:** `SimpleImputer`, `OrdinalEncoder`, `OneHotEncoder`
    * **Mimari:** `Pipeline`, `ColumnTransformer` (Veri sızıntısını (Data Leakage) önlemek için)
    * **Optimizasyon:** `GridSearchCV` (Çapraz doğrulama ile en iyi hiperparametrelerin bulunması)
* **Görselleştirme:** `Seaborn`, `Matplotlib`

## 📊 Kilit Bulgular ve Feature Engineering
*(Buraya daha önce çizdiğin Seaborn grafiğinin ekran görüntüsünü ekleyebilirsin veya aşağıdaki gibi notlar düşebilirsin)*
* Yaş gruplarının (binning) doğrudan modele verilmesinden ziyade, anlamlı kategorilere ayrılması model başarısını artırdı.
* Bilet fiyatı (`Fare`) ve yolcu sınıfı (`Pclass`) ile hayatta kalma oranı arasındaki güçlü korelasyon, kurulan farklı modeller (RF, SVC) tarafından da doğrulandı.

## 💡 Neler Öğrendim?
Bu projede, veriyi modele vermeden önceki ön hazırlığın (preprocessing) kod yazmaktan çok daha kritik olduğunu yaşayarak tecrübe ettim. Özellikle `ColumnTransformer` ile farklı sütunlara farklı dönüşüm kuralları atamak ve bunları `GridSearchCV` ile test etmek en büyük teknik kazanımım oldu.
