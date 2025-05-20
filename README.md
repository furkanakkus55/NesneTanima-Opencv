AI TABANLI ÇOKLU ALGILAMA SİSTEMİ

Proje Adı: Karma Kullanımlı Nesne Tanıma

Bu proje, YOLOv8, MediaPipe ve OpenCV kullanarak gerçek zamanlı olarak yüz ifadeleri, göz kırpma, el/parmak hareketleri ve çevresel nesneleri algılayan bir yapay zeka sistemidir. Kamera görüntüsünden alınan verilerle insan davranışları ve çevre analiz edilerek görselleştirilir.

Projenin Amacı:
Görüntü işleme ve yapay zeka teknolojilerini birleştirerek insan-makine etkileşimini iyileştirmeyi hedefler. Sistem şunları sağlar:
Yüz ifadesi analizi (mutlu, somurtma, normal)
Göz kırpma takibi
El/parmak hareketi tespiti
Ortamdaki nesnelerin (insan, araç vs.) tespiti

Kullanım Alanları:
Erişilebilirlik uygulamaları
Sürücü yorgunluk tespiti
Yapay zeka eğitimi
Artırılmış gerçeklik sistemleri

Hedef Kullanıcılar:
Yapay zeka ve görüntü işleme geliştiricileri
Akademisyenler, öğrenciler
Endüstriyel sistem geliştiricileri
Erişilebilirlik çözümü üreticileri
Hobi amaçlı geliştiriciler

Kullanılan Teknolojiler:
Python 3.8 ve üzeri
OpenCV 4.5+
MediaPipe
YOLOv8
NumPy
Math ve Time kütüphaneleri

Kurulum Adımları:

Python 3.8+ yüklü olmalı (https://www.python.org/downloads/)
Terminalden aşağıdaki komutları çalıştırın:
pip install opencv-python
pip install mediapipe
pip install ultralytics
pip install numpy

3.YOLOv8 modeli otomatik olarak indirilir (yolov8n.pt)

4.(Opsiyonel) QR kod oluşturmak için:
pip install qrcode pillow

Kod:

"""

import qrcode

qr = qrcode.QRCode(...)

qr.add_data("https://github.com/furkanakkus55/NesneTanima-Opencv")
...

img.save("outputs/qr_code.png") 

"""

Donanım Gereksinimleri:
Web kamerası

En az 8 GB RAM

Modern CPU (tercihen GPU)

Windows, Linux veya macOS işletim sistemi

Projeyi Çalıştırmak İçin:
git clone https://github.com/furkanakkus55/NesneTanima-Opencv

cd NesneTanima-Opencv
python main.py 

Program Başladığında:
Yüz algılanır ve gösterilir
Göz kırpma sayısı güncellenir
Yüz ifadesi tespit edilir
Parmak sayısı analiz edilir
Nesneler (insan, araç vs.) ekranda gösterilir
FPS ve analiz bilgileri sağ üst köşede görünür
Çıkmak için 'q' tuşuna basmanız yeterlidir.

Proje Dosya Yapısı:

css
Kopyala
Düzenle
face-object-detection/
├── main.py

├── README.md

├── poster.pdf

├── outputs/

│   ├── ornek_cikti.png

│   └── qr_code.png


Geliştiriciler:

Furkan Akkuş – 2405902021 – Yapay Zeka Operatörlüğü / BTMYO

Yiğit Bayram – 2405902030 – Yapay Zeka Operatörlüğü / BTMYO

GitHub Proje Linki:
https://github.com/furkanakkus55/NesneTanima-Opencv



