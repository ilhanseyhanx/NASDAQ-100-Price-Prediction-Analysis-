# 📈 NASDAQ-100 Fiyat Tahmin Analizi | NASDAQ-100 Price Prediction Analysis

Geleneksel makine öğrenmesi algoritmalarını deep learning modelleriyle karşılaştıran, NASDAQ-100 15 dakikalık fiyat tahmini üzerine kapsamlı bir analiz.

*A comprehensive machine learning analysis comparing traditional ML algorithms with deep learning models for NASDAQ-100 15-minute price prediction.*

## 🎯 Proje Genel Bakış | Project Overview

Bu proje **201,676 veri noktası** içeren NASDAQ-100 15 dakikalık geçmiş fiyat verisini analiz ederek, kapanış fiyatlarını tahmin etmek için 7 farklı makine öğrenmesi modelini uygular ve karşılaştırır.

*This project analyzes **201,676 data points** of NASDAQ-100 15-minute historical price data, implementing and comparing 7 different machine learning models to predict closing prices.*

## 📊 Veri Seti Bilgileri | Dataset Information

- **Kaynak | Source:** NASDAQ-100 Geçmiş Fiyat Verisi (15 dakikalık aralıklar) | *NASDAQ-100 Historical Price Data (15-minute intervals)*
- **Özellikler | Features:** DateTime, Open, High, Low, Close, Volume, TickVolume
- **Zaman Periyodu | Time Period:** 201,676 kayıtlı güncel geçmiş veri | *Recent historical data with 201,676 records*
- **Format:** Tab ile ayrılmış CSV dosyası | *Tab-delimited CSV file*

## 🔧 Özellik Mühendisliği | Feature Engineering

### Eklenen Teknik İndikatörler | Technical Indicators Added:
- **MA20:** 20 periyotluk Hareketli Ortalama | *20-period Moving Average*
- **MA50:** 50 periyotluk Hareketli Ortalama | *50-period Moving Average*
- **Daily_Return:** Kapanış fiyatındaki yüzde değişim | *Percentage change in closing price*
- **Volatility_10:** 10 periyotluk yuvarlanma standart sapması | *10-period rolling standard deviation*
- **Zaman Özellikleri | Time Features:** Yıl, Ay, Gün, Haftanın Günü | *Year, Month, Day, DayOfWeek*

## 🤖 Uygulanan Modeller | Models Implemented

### Geleneksel Makine Öğrenmesi | Traditional Machine Learning:
1. **Doğrusal Regresyon | Linear Regression**
2. **Karar Ağacı Regresyonu | Decision Tree Regressor**
3. **Rastgele Orman Regresyonu | Random Forest Regressor**
4. **Destek Vektör Regresyonu (SVR) | Support Vector Regression (SVR)**
5. **K-En Yakın Komşu (KNN) | K-Nearest Neighbors (KNN)**

### Derin Öğrenme | Deep Learning:
6. **LSTM (Uzun Kısa Süreli Bellek) | LSTM (Long Short-Term Memory)**
7. **GRU (Kapılı Tekrarlayan Birim) | GRU (Gated Recurrent Unit)**

## 📈 Sonuç Özeti | Results Summary

| Model | R² Skoru | MSE | Performans | 
|-------|----------|-----|------------|
| **Doğrusal Regresyon \| Linear Regression** | **0.9999** | 54.59 | ⭐ En İyi \| Best |
| **Rastgele Orman \| Random Forest** | 0.9999 | 78.82 | ⭐ Mükemmel \| Excellent |
| **Karar Ağacı \| Decision Tree** | 0.9999 | 154.90 | ⭐ Mükemmel \| Excellent |
| **KNN** | 0.9988 | 27,102.48 | ✅ İyi \| Good |
| **GRU** | 0.9830 | 2.83e-05* | ✅ İyi \| Good |
| **LSTM** | 0.9096 | 50,526.34 | ⚠️ Orta \| Moderate |
| **SVR** | -0.1297 | 27,050,897 | ❌ Zayıf \| Poor |

*\*Not: GRU MSE ölçeklendirilmiş veri üzerinden hesaplandı | \*Note: GRU MSE calculated on scaled data*

## 🔍 Temel Bulgular | Key Findings

### 🎯 **Şaşırtıcı Sonuçlar | Surprising Results:**
- **Doğrusal Regresyon** en yüksek R² skorunu (0.9999) elde etti | ***Linear Regression** achieved the highest R² score (0.9999)*
- Geleneksel ML modelleri derin öğrenme modellerinden daha iyi performans gösterdi | *Traditional ML models outperformed deep learning models*
- **GRU, LSTM'den daha hızlı eğitim süresiyle daha iyi performans** gösterdi | ***GRU performed better than LSTM** with faster training time*

### 📊 **Teknik İçgörüler | Technical Insights:**
- Hareketli ortalamalarla özellik mühendisliği kritikti | *Feature engineering with moving averages was crucial*
- SVR finansal zaman serisi verileriyle zorlandı | *SVR struggled with financial time series data*
- LSTM/GRU için 60'lık pencere boyutu optimize edilebilir | *Window size of 60 for LSTM/GRU might be optimizable*

### 💡 **Piyasa Çıkarımları | Market Implications:**
- Kısa vadeli fiyat hareketleri yüksek tahmin edilebilirlik gösteriyor | *Short-term price movements show high predictability*
- 15 dakikalık aralıklarda basit doğrusal ilişkiler mevcut | *Simple linear relationships exist in 15-minute intervals*
- Teknik indikatörler model performansını önemli ölçüde artırıyor | *Technical indicators significantly improve model performance*

## 🛠️ Kullanılan Teknolojiler | Technologies Used

```python
# Temel Kütüphaneler | Core Libraries
pandas, numpy, matplotlib, seaborn

# Makine Öğrenmesi | Machine Learning
scikit-learn (LinearRegression, DecisionTree, RandomForest, SVR, KNN)
StandardScaler, train_test_split

# Derin Öğrenme | Deep Learning  
tensorflow, keras (LSTM, GRU, Sequential, Dense, Dropout)

# Ön İşleme | Preprocessing
MinMaxScaler for neural networks
```

## 📊 Görselleştirmeler | Visualizations

Proje kapsamlı görselleştirmeler içeriyor | *The project includes comprehensive visualizations:*

- 📈 Hareketli ortalamalarla fiyat trendleri | *Price trends with moving averages*
- 🎯 Her model için Gerçek vs Tahmin karşılaştırmaları | *Actual vs Predicted comparisons for each model*
- 📊 Model performans metrikleri karşılaştırması | *Model performance metrics comparison*
- 🔄 LSTM/GRU eğitim kaybı eğrileri | *LSTM/GRU training loss curves*


## 🔮 Gelecek İyileştirmeler | Future Improvements

- [ ] **GridSearchCV kullanarak hiperparametre optimizasyonu** | ***Hyperparameter optimization** using GridSearchCV*
- [ ] **Sağlam model değerlendirmesi için çapraz doğrulama** | ***Cross-validation** for robust model evaluation*
- [ ] **Özellik seçimi teknikleri** | ***Feature selection** techniques*
- [ ] **En iyi modelleri birleştiren topluluk yöntemleri** | ***Ensemble methods** combining best models*
- [ ] **Gerçek zamanlı tahmin** pipeline'ı | ***Real-time prediction** pipeline*
- [ ] **Risk yönetimi** metrikleri | ***Risk management** metrics*

## 🤝 Katkıda Bulunma | Contributing

Katkılar memnuniyetle karşılanır! Lütfen Pull Request göndermekten çekinmeyin.

*Contributions are welcome! Please feel free to submit a Pull Request.*

## 📧 İletişim | Contact

- **LinkedIn:** [linkedin.com/in/ilhanseyhan](https://www.linkedin.com/in/ilhanseyhan/)
- **GitHub:** [github.com/ilhanseyhanx](https://github.com/ilhanseyhanx)
- **Email:** [ilhanseyhan5@gmail.com](mailto:ilhanseyhan5@gmail.com)

---

⭐ **Bu projeyi faydalı bulduysanız, lütfen yıldız verin! | If you found this project helpful, please give it a star!**
