# AI Tabanlı Çoklu Algılama Sistemi

Bu projede, **YOLOv8**, **MediaPipe**, **OpenCV** ve bazı matematiksel fonksiyonlar kullanarak gerçek zamanlı olarak birden fazla insan davranışı ve nesnesi algılayan bir yapay zeka sistemi geliştirdik.

##  Projenin Amacı

Gerçek zamanlı bir kamera görüntüsü üzerinden:
- Nesne tespiti (YOLOv8 ile)
- Yüz tespiti
- Göz kırpma sayacı
- El tespiti ve parmak sayma
- Yüz ifadesi analizi (mutlu, somurtkan, normal)

özelliklerini aynı anda çalıştırabilen çok yönlü bir sistem inşa ettik.

---

##  Kullanılan Teknolojiler

- **Python 3.x**
- **OpenCV** - Görüntü işleme
- **MediaPipe** - Yüz, el ve mesh tespiti
- **Ultralytics YOLOv8** - Nesne algılama
- **Math** - Mesafe ve oran hesaplamaları

---

##  Bileşenler ve Açıklamalar

###  Göz Kırpma Takibi
- Gözlerin alt ve üst noktaları arasındaki mesafeyi ölçerek göz kırpma tespit ettik.
- Belirli bir eşik değerinin altına düşerse göz kapalı sayıldı.
- Her kapanış, göz kırpma olarak sayıldı.

###  Parmak Sayma
- El landmarks (eklem) noktalarını analiz ettik.
- Baş parmak sağa veya sola bakma yönüne göre değerlendirildi.
- Diğer parmaklar, uç noktalarının alt boğumlarına göre yukarıda mı aşağıda mı olduğu kontrol edilerek sayıldı.

###  Yüz İfadesi Analizi
- Ağız üst ve alt noktaları ile sağ ve sol köşe noktaları arasındaki oranı hesapladık.
- Bu oranlara göre:
  - `> 0.25`: Mutlu
  - `< 0.05`: Somurtkan
  - Arası: Normal

###  Nesne Tespiti (YOLOv8)
- `yolov8n.pt` modeliyle canlı görüntüdeki nesneleri sınıflandırdık.
- Tespit edilen nesnelere kutu çizip isim ve doğruluk yüzdesini yazdırdık.

---

##  Canlı Görüntü Üzerinde Gösterilen Bilgiler

- FPS (saniyedeki kare sayısı)
- Göz kırpma sayısı
- Parmak sayısı
- Yüz ifadesi (mutlu / somurtkan / normal)
- Tespit edilen nesneler

---

##  Kurulum

```bash
pip install opencv-python mediapipe ultralytics
