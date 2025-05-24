
# ✈️ Uçuş Verileri Analizi ve Gecikme Tahmini

Bu proje, **uçuşlara ait zaman serisi verileri** üzerinde analiz ve **2013 yılı sonuna kadar uçuş gecikmelerini tahmin etme** amaçlı bir çalışma gerçekleştirmektedir. Veri kümesi, her bir uçuşa dair zaman, yön, havayolu, mesafe gibi çeşitli öznitelikleri içermektedir. Bu çalışma, uçuşlardaki gecikmeleri anlamak, öznitelik mühendisliği uygulamaları yapmak ve gecikmeleri tahmin etmek için bir model geliştirmek üzere yapılandırılmıştır.

## 🎯 Projenin Amacı

- Uçuş gecikmelerine neden olabilecek faktörleri analiz etmek
- Tarih/zaman verilerinden yeni öznitelikler üretmek (örneğin: hafta sonu olup olmaması, ay dönüşümleri)
- 2013 yılı verilerine dayanarak uçuşlardaki **kalkış gecikmesini tahmin eden** bir model geliştirmek
- İstatistiksel analiz, görselleştirme ve makine öğrenmesi tekniklerini bir arada uygulamak

## 🗂️ Kullanılan Veri

Veri, `flights.csv` adlı dosyadan alınmıştır. Öne çıkan sütunlar:

- `year`, `month`, `day`
- `dep_delay`, `arr_delay` (kalkış ve varış gecikmeleri)
- `origin`, `dest`
- `air_time`, `distance`
- `sched_dep_time` (planlanan kalkış zamanı)

## 🛠️ Yöntemler

### Öznitelik Mühendisliği

- Tarihsel özniteliklerin çıkarılması (gün, ay, hafta sonu, vs.)
- Döngüsel veri dönüşümü (`month_sin`, `month_cos`)
- Ortalama hız ve taşıyıcı gecikmesi gibi türetilmiş öznitelikler

### Makine Öğrenmesi

- **Amaç**: `dep_delay` (kalkış gecikmesi) değerini tahmin etmek
- **Kullanılan Modeller**:
  - Doğrusal Regresyon (Linear Regression)
  - Karar Ağaçları (Decision Tree)
  - Rastgele Orman (Random Forest)

### Değerlendirme

- Eğitim ve test verisi ayrımı ile model değerlendirmesi
- Hata metrikleri: MAE, RMSE, R² gibi ölçütler kullanılmıştır

## 📊 Görselleştirmeler

- `matplotlib` ve `seaborn` ile veri dağılımı ve ilişki görselleştirmeleri

## 📚 Kullanılan Kütüphaneler

- `pandas`, `numpy`
- `matplotlib`, `seaborn`
- `sklearn` (Scikit-learn)

## 🔮 Gelecekteki Geliştirmeler

- Uçuş iptalleri ve hava durumu etkileri üzerine daha fazla öznitelik ekleme
- Derin öğrenme modelleri ile tahmin performansının artırılması
- Web tabanlı arayüzle tahmin modeli sunumu
