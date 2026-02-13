# 🏥 Sağlıkta Yapay Zeka: Hasta Yatış Süresi Tahmini

Bu proje, **Burdur Mehmet Akif Ersoy Üniversitesi** bünyesindeki **Sağlıkta Yapay Zeka** dersi uygulama çalışmaları kapsamında geliştirilmiştir. Projenin amacı, hastaneye giriş yapan hastaların çeşitli klinik ve demografik verilerini analiz ederek, hastanede kalış sürelerini (Length of Stay) tahmin eden bir model oluşturmaktır.

## 📌 Proje Özeti
Hastanelerdeki yatak kapasite yönetimi ve kaynak planlaması için hasta yatış süresinin önceden tahmin edilmesi kritik bir öneme sahiptir. Bu projede, hem regresyon hem de sınıflandırma yaklaşımları kullanılarak hastaların yatış süreleri analiz edilmiştir. 
**Veri Seti:** [Hospital Inpatient Discharges Dataset](https://www.kaggle.com/datasets/bhautikmangukiya12/hospital-inpatient-discharges-dataset)

## 🛠️ Kullanılan Teknolojiler
- **Python** (Veri Bilimi Ekosistemi)
- **Pandas & NumPy** (Veri manipülasyonu ve analizi)
- **Matplotlib & Seaborn** (Veri görselleştirme ve korelasyon analizleri)
- **Scikit-Learn** (Makine Öğrenmesi algoritmaları ve değerlendirme metrikleri)

## 🚀 Proje Uygulama Adımları

### 1. Veri Hazırlığı ve Ön İşleme
- **Label & Ordinal Encoding:** Kategorik veriler (Şehir, Hastane Tipi, Bölüm vb.) modelin işleyebileceği sayısal formatlara dönüştürülmüştür.
- **Eksik Veri Kontrolü:** Veri setindeki eksik değerler analiz edilerek temizlenmiş veya doldurulmuştur.
- **Özellik Mühendisliği:** Yatış süresini etkileyen kritik faktörler belirlenmiştir.

### 2. Modelleme Yaklaşımları
Projede iki farklı yöntem izlenmiştir:
- **Regresyon (DecisionTreeRegressor):** Yatış süresini sürekli bir sayısal değer olarak tahmin etmek için kullanılmıştır.
- **Sınıflandırma (DecisionTreeClassifier):** Yatış sürelerini belirli kategorilere (Örn: 0-10 gün, 11-20 gün vb.) ayırarak sınıflandırma yapılmıştır.

### 3. Model Optimizasyonu ve Performans
- **Overfitting Kontrolü:** Karar ağaçlarında aşırı öğrenmeyi (overfitting) engellemek için `max_depth` gibi hiperparametreler optimize edilmiştir.
- **Performans Metrikleri:** - Regresyon için **Mean Squared Error (MSE)** analizi yapılmıştır.
    - Sınıflandırma için **Accuracy**, **Recall** ve **F1-Score** metrikleri üzerinden değerlendirme yapılmıştır.

## 📊 Öne Çıkan Bulgular
- Modelin genel doğruluğu yüksek olsa da, az sayıda örneği bulunan yatış kategorilerinde (az rastlanan vakalar) "Recall" değerinin düştüğü ve modelin çoğunluk sınıfa eğilim gösterdiği saptanmıştır.
- `max_depth` parametresinin sınırlandırılmasının, test verisi üzerindeki genel performansı (genelleme yeteneğini) artırdığı gözlemlenmiştir.

## 📂 Dosya Yapısı
- `hasta_yatis_tahmini.ipynb`: Veri ön işleme, regresyon ve sınıflandırma modellerini içeren ana çalışma dosyası.
- `train_data.csv`: Modelin eğitimi için kullanılan veri seti.

