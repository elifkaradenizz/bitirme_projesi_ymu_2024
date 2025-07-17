# Müşteri Segmentasyonu ve Aykırı Değer Tespiti (Bitirme Projesi - 2024)

Bu proje, denetimsiz öğrenme (unsupervised learning) yöntemleriyle müşteri verileri üzerinde segmentasyon (kümeleme) ve aykırı değer tespiti gerçekleştirmeyi amaçlamaktadır. Çalışmada farklı eksik veri tamamlama stratejileri, boyut indirgeme yöntemleri ve çeşitli kümeleme-algoritmaları birlikte değerlendirilmiştir.

## Proje Amacı

- Müşterileri davranışsal benzerliklerine göre kümelere ayırmak.
- Aykırı davranış sergileyen müşteri profillerini belirlemek.
- Farklı ön işleme stratejilerinin (eksik veri, normalizasyon) model performansına etkisini değerlendirmek.

 ##  Veri Seti

Bu projede kullanılan veri seti, İngiltere merkezli bir çevrimiçi perakendecinin 2010-2011 yılları arasındaki işlemlerine ait çok bilinen bir e-ticaret veri setidir. Veri setine aşağıdaki bağlantılardan erişebilirsiniz:
- [Kaggle – Online Retail Dataset](https://www.kaggle.com/datasets/vijayuv/onlineretail)
- [UCI Machine Learning Repository](https://archive.ics.uci.edu/dataset/352/online+retail)

> **Not:** Veri setinde eksik müşteri kimlikleri bulunmaktadır. Projede bu eksik değerler için farklı tamamlama stratejileri uygulanmıştır.

### Veri Seti Özellikleri

- **Toplam Gözlem Sayısı**: 541.909
- **Sütun Sayısı**: 8
- **Özellikler**:
  - `InvoiceNo`: Fatura numarası
  - `StockCode`: Ürün kodu
  - `Description`: Ürün açıklaması
  - `Quantity`: Satın alınan ürün adedi
  - `InvoiceDate`: İşlem tarihi
  - `UnitPrice`: Ürün birim fiyatı
  - `CustomerID`: Müşteri kimliği
  - `Country`: Ülke bilgisi


## Kullanılan Yöntemler ve Teknikler

- **Boyut İndirgeme**: t-SNE, PCA
- **Kümeleme Algoritmaları**: K-Means, K-Medoids, Mean Shift, DBSCAN, Hiyerarşik Kümeleme
- **Aykırı Değer Algılama**: LOF (Local Outlier Factor), Isolation Forest, SVM
- **Veri Ön İşleme**: Ortalama ile tamamlama, mod ile tamamlama, min-max normalizasyon, eksik veriyi çıkarma (dropna)

## Proje Dosyaları

- `T_SNE_K_MEANS_aykırılık_SVM.ipynb`: t-SNE + K-Means + SVM ile aykırı değer analizi.
- `T_SNE_K_MEANS_isolationForest.ipynb`: t-SNE + K-Means + Isolation Forest yöntemiyle analiz.
- `bitirme_projesi_k_medoids_kümeleme_algoritması.ipynb`: K-Medoids algoritması ile kümeleme uygulaması.
- Diğer notebook dosyaları, çeşitli eksik veri ve kümeleme kombinasyonlarını test etmektedir.

## Çalıştırma Talimatları

Notebook dosyasını Jupyter Notebook veya Google Colab üzerinden açın:

```bash
jupyter notebook
Adım adım hücreleri çalıştırarak görselleştirme ve analiz sonuçlarını gözlemleyin.

## Proje Özeti

- Eksik veriler üzerinde farklı tamamlama yöntemleri denenerek model çıktıları karşılaştırılmıştır.
- t-SNE ile boyut indirgeme, görsel olarak kümeleri daha iyi ayırt etmeyi sağlamıştır.
- Mean Shift ve K-Medoids gibi alternatif kümeleme yöntemleri, klasik K-Means algoritmasıyla karşılaştırmalı olarak değerlendirilmiştir.

---

## Gereksinimler

- Python 3.8+
- Jupyter Notebook veya Google Colab

### Gerekli Kütüphaneler

- `pandas`
- `numpy`
- `matplotlib`
- `seaborn`
- `scikit-learn`

---

## 📄 Lisans

Bu proje, 2024 yılı lisans bitirme çalışması kapsamında geliştirilmiştir.  
Tüm hakları saklıdır © Elif Karadeniz.



