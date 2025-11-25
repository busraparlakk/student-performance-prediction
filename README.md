# student-performance-prediction
Student Performance Analysis

Makine Öğrenmesi ile Öğrenci Başarı Tahmini

Bu proje, UCI Student Performance veri seti (özellikle student-mat.csv) kullanılarak öğrencilerin final notunun (G3) tahmin edilmesini amaçlayan bir veri analizi ve makine öğrenmesi çalışmasıdır.
Proje Google Colab üzerinde gerçekleştirilmiştir ve GitHub’a yüklenebilir yapıdadır.

1. Proje Yapısı
├── student_data/
│   ├── student-mat.csv
│   ├── student-por.csv
│   ├── student.txt
│   └── student-merge.R
├── prediction_results.csv
├── student_grade_model.pkl
└── Student_Performance_Analysis.ipynb

2. Projenin Amacı

Veri setini incelemek

Temel istatistikleri çıkarmak

Kategorik değişkenleri işlemek

Öğrencilerin final notunu tahmin eden bir model oluşturmak

Tahmin sonuçlarını değerlendirmek

Modeli kaydetmek ve çıktı dosyaları üretmek

3. Kullanılan Kütüphaneler

pandas

numpy

matplotlib

seaborn

scikit-learn

joblib

4. Veri Seti Hakkında

Kullanılan veri seti UCI Student Performance veri setidir.
Öğrencilerin demografik bilgileri, aile bilgileri, eğitim geçmişi, devamsızlık durumu ve dönem içi notları gibi çeşitli değişkenler içerir.

Özellikle kullanılan dosya:

student-mat.csv (Matematik dersi)

Hedef değişken:

G3 (Final Grade)

5. Yapılan İşlemler
5.1 Veri Yükleme

CSV dosyaları pandas ile yüklenmiştir.

5.2 Temel Analiz

İlk satırlar

Veri tipleri

Eksik değer kontrolü

İstatistiksel özet

5.3 Ön İşleme

Kategorik değişkenler get_dummies() ile sayısal hale dönüştürülmüştür.

5.4 Eğitim/Test Ayrımı

Veri %80 eğitim, %20 test olacak şekilde bölünmüştür.

5.5 Model Eğitimi

RandomForestRegressor kullanılarak bir tahmin modeli oluşturulmuştur.

5.6 Değerlendirme

Model, MSE (Mean Squared Error) ve R² skorları ile değerlendirilmiştir.

5.7 Özellik Önemi

En önemli özellikler görselleştirilmiştir.

5.8 Model ve Sonuçların Kaydedilmesi

Kaydedilmiş model: student_grade_model.pkl

Gerçek ve tahmin değerleri: prediction_results.csv

6. Sonuçlar

Model, öğrencilerin final notunu tahmin etmede başarılı performans göstermiştir.
Özellikle geçmiş dönem notları (G1 ve G2), çalışma süresi ve devamsızlık değişkenleri tahmin üzerinde önemli etkiye sahiptir.

7. Çalıştırma

Dosyaları bu yapıda tutun

Colab veya Jupyter Notebook ortamında .ipynb dosyasını açın

Hücreleri sırayla çalıştırın

8. Not

Proje eğitim amaçlı hazırlanmıştır.
İstenirse Portekizce dosyası (student-por.csv) için ayrı bir model veya karşılaştırmalı analiz yapılabilir.
