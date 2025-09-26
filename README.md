# Sign Language Digits Classification

## 📖 Giriş  
Bu proje, **Sign Language Digits Dataset** kullanılarak işaret dili ile gösterilen rakamların (0–9) sınıflandırılmasını amaçlamaktadır.  
Projede temel CNN mimarisi, veri artırma (augmentation), Batch Normalization, Dropout ve transfer learning (VGG16) yöntemleri uygulanmış, farklı optimizatörler (Adam, SGD, RMSprop) test edilmiştir.  

Notebook dosyasında, veri keşfi (EDA), model oluşturma, eğitim süreci ve değerlendirme aşamaları ayrıntılı olarak Markdown hücreleri ile anlatılmıştır.  

---

## 📊 Metrikler  
Çalışma sonucunda elde edilen doğruluk değerleri:  

| Model                        | Test Doğruluğu |
|-------------------------------|----------------|
| Temel CNN                    | %96.1 |
| Transfer Learning (VGG16)     | %96.1 |
| Fine-Tuning (VGG16 block5)    | %96+ |
| En iyi optimizatör (RMSprop)  | **%97.8** |

**Yorum:**  
- Küçük ve dengeli bir veri setinde hem temel CNN hem de transfer learning modelleri benzer performans göstermiştir.  
- Optimizer seçiminin etkisi belirgin olmuş, RMSprop ile en yüksek doğruluk elde edilmiştir.  

---

## 🛠 Ekler  
- **Data Augmentation**: Rotation, Translation, Zoom, Contrast artırma uygulanmıştır.  
- **Fine-Tuning**: VGG16’nın `block5` katmanları eğitime açılarak daha yüksek uyum sağlanmıştır.  
- **Aktivasyon Görselleştirmesi**: VGG16’nın erken katmanlarında feature map’ler incelenmiştir.  


---

## 🚀 Sonuç ve Gelecek Çalışmalar  
Bu çalışma ile işaret dili rakamlarını sınıflandırmada yüksek doğruluk elde edilmiştir.  
Gelecekte:  
- Daha büyük ve çeşitlendirilmiş veri setleriyle eğitim yapılabilir.  
- Gerçek zamanlı kamera verisiyle test edilerek pratik uygulama sağlanabilir.  
- Kullanıcı dostu bir arayüz (ör. Streamlit) geliştirilerek yaygın kullanım için kullanılabilir hale getirilebilir.  

---

## 🔗 Linkler  
- Kaggle Notebook: [Sign Language Digits Project](https://www.kaggle.com/code/sudednmez/signlanguagedigits)  
- Veri Seti: [Sign Language Digits Dataset](https://www.kaggle.com/datasets/ardamavi/sign-language-digits-dataset)  
