# Derin Öğrenme Tabanlı İşaret Dili Sınıflandırıcı (Sign Language MNIST — CNN)

## 🌟 Amaç  
Bu proje, **Sign Language MNIST** veri setini kullanarak işaret dili alfabesindeki harfleri **Convolutional Neural Network (CNN)** ile sınıflandırmayı hedefler.  
Bu sayede, işaret dili harflerinin görsel olarak tanınması, işaret dili ile arayüzler kurma, erişilebilirlik artırma gibi amaçlara yönelik bir temel altyapı sunar.

---

## 📌 İçerikler & Özellikler  

- **Veri Önişleme ve Augmentasyon**  
  - Görüntü normalizasyonu  
  - Veri genişletme (rotation, shift, zoom, flip vs.)  
  - Gri tonlamadan uygun boyutlara yeniden şekillendirme (28×28×1)  

- **Model Mimarisi**  
  - İki adet `Conv2D + BatchNormalization + MaxPooling + Dropout` bloğu  
  - Tam bağlı katman (Dense) + Softmax çıkışı  
  - Modelin aşırı öğrenmesini önlemek için Dropout ve Regularization stratejileri  

- **Eğitim Süreci & Hiperparametreler**  
  - Optimizer: Adam  
  - Erken durdurma (EarlyStopping), öğrenme oranı azaltma (ReduceLROnPlateau), en iyi modeli saklama (ModelCheckpoint)  
  - Epoch sayısı, batch size gibi ayarlar  

- **Değerlendirme & Görselleştirme**  
  - Eğitim / doğrulama / test için doğruluk ve loss grafiklerinin çizimi  
  - Confusion matrix, classification report (precision, recall, f1-score)  
  - **Grad-CAM** (Gradient-weighted Class Activation Mapping) ile modelin dikkate aldığı bölgelerin görselleştirilmesi  

---

## 📊 Sonuçlar (Özet)

| Ölçüt | Değer |
|-------|-------|
| Test Doğruluğu | ~ %94,81 |
| Gözlemler | Bazı harfler kolay ayırt edilirken, görsel olarak benzer harflerde karışıklık yaşanmıştır. |

---

## 📂 Veri Seti & Kaynaklar

- Veriset: **Sign Language MNIST** (Kaggle)  
  🔗 [https://www.kaggle.com/datamunge/sign-language-mnist](https://www.kaggle.com/datamunge/sign-language-mnist)  
  > Not: Bu repo veriyi içermez, veriyi Kaggle’dan indirip uygun dizine koymalısınız.  

- Projenin Kaggle Notebook versiyonu:  
  🔗 [https://www.kaggle.com/code/gokcebaykal/derin-ogrenme-tabanli-isaret-dili-siniflandirici](https://www.kaggle.com/code/gokcebaykal/derin-ogrenme-tabanli-isaret-dili-siniflandirici)

---

## 🛠️ Kurulum & Çalıştırma

# Repoyu klonla
git clone https://github.com/gokcebaykaal/derin-ogrenme-tabanli-isaret-dili-siniflandirici-sign-language-mnist-cnn.git
cd derin-ogrenme-tabanli-isaret-dili-siniflandirici-sign-language-mnist-cnn

# Gerekli kütüphaneleri yükle
pip install -r requirements.txt

# Notebook'u çalıştır
jupyter notebook

---

## 🧩 Dosya Yapısı

├── notebooks/
│   └── main.ipynb
├── requirements.txt
├── README.md
├── LICENSE
└── (opsiyonel yardımcı scriptler)
