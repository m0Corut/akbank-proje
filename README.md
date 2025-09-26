kaggle linki: https://www.kaggle.com/code/muhammetcorut/akbank-cnn

Sınıflandırma Projesi

> Görsellerden sınıflandırma yapan, açıklanabilir yapay zeka destekli bir model.

---

## Projenin Amacı

Bu projede amaç, görüntülerdeki sınıfları doğru tanıyacak bir derin öğrenme modeli geliştirmektir.  
Geçmişte “kara-kaya”, “bina”, “orman” gibi görselleri ayırt etmek zor olurdu; bu model bunu öğreniyor ve kararlarını görselleştirilebilir hale getiriyor.

---

## Veri Seti Hakkında

- Veri seti, farklı sınıflardan (örneğin binalar, orman, dağ, buz, vs.) görseller içeriyor.  
- Eğitim, doğrulama ve test bölümlerine ayrılmış durumda.  
- Her sınıftan dengeli sayıda örnek kullanıldı (ne çok az ne çok fazla).  
- Görseller **150×150** boyuta küçültülüp `1/255` ile normalize edildi.  

---

## Kullanılan Yöntemler

- **CNN (Convolutional Neural Network):** Görsellerden öznitelik çıkarımı için.  
- **Dropout & L2 Regularizasyon:** Overfitting’i engellemek için.  
- **EarlyStopping & ReduceLROnPlateau:** Eğitim sırasında performansı optimize etmek için callback’ler.  
- **ModelCheckpoint:** En iyi modeli kaydetmek için.  
- **Grad-CAM / Eigen-CAM:** Modelin karar verirken hangi görsel bölgelere dikkat ettiğini göstermek için.  
- **Fine-Tuning / Hiperparametre Araması:** Öğrenme oranı, optimizer, dropout oranı gibi ayarlamalarla modelin performansını iyileştirme.

---

## Elde Edilen Sonuçlar

- Test doğruluğu: **%81–82** civarında.  
- Baseline model üzerinden yapılan fine-tuning ile **%82–83**’e kadar çıktı.  
- Grad-CAM/Eigen-CAM görselleri, modelin özellikle kenar, doku geçişleri, ufuk çizgisi gibi bölgelere odaklandığını gösteriyor.  
- Hiperparametre optimizasyonu, modelin validation doğruluğunu artırdı ve overfitting seviyesini düşürdü.

---

##  Performans Grafikleri

**Training & Validation Accuracy / Loss**

<img width="705" height="661" alt="image" src="https://github.com/user-attachments/assets/c585e7b2-5325-47d3-9ef8-1b52543a8e91" />

<img width="536" height="393" alt="download" src="https://github.com/user-attachments/assets/00acd298-cc07-4b8d-bd3c-71e0dd060895" />

<img width="536" height="393" alt="download" src="https://github.com/user-attachments/assets/59954397-df85-45bd-b480-8e741605746d" />













