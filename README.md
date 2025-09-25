# Derin Öğrenme Tabanlı İşaret Dili Sınıflandırıcı (Sign Language MNIST - CNN)

Bu proje, **Sign Language MNIST** veri seti ile işaret dili harflerini
**Convolutional Neural Network (CNN)** kullanarak sınıflandırmayı amaçlar.

## 🎯 Amaç
Bu proje işaret dili harflerini bilgisayara tanıtmak için derin öğrenme yöntemleri kullanır.

## 🧰 Yöntemler
- Önişleme: normalizasyon, 28×28×1 şekillendirme
- Model: 2×(Conv2D+BN+MaxPool+Dropout) + Dense(256) + Softmax
- Eğitim: Adam optimizer, EarlyStopping, ReduceLROnPlateau, ModelCheckpoint
- Değerlendirme: accuracy/loss grafik, confusion matrix, classification report
- Görselleştirme: Grad-CAM

## 📊 Sonuçlar (Özet)
- Test Accuracy: **%XX.XX**
- Önemli gözlem: Model bazı harflerde yüksek doğruluk, bazı benzer harflerde hata yapmıştır.

## 💾 Veri Seti
- Kaggle: Sign Language MNIST  
- Bağlantı: https://www.kaggle.com/datamunge/sign-language-mnist  
> Bu repo veriyi içermez. Veriyi Kaggle’dan indiriniz.

## 🔗 Kaggle Notebook Linki
Proje defteri: https://www.kaggle.com/code/gokcebaykal/derin-ogrenme-tabanli-isaret-dili-siniflandirici

##📜 Lisans
MIT

## ▶️ Nasıl Çalıştırılır?
```bash
pip install -r requirements.txt
jupyter notebook  # notebooks/main.ipynb'yi aç
