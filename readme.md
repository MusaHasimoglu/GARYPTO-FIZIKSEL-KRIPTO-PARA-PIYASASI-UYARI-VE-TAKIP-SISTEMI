# GARYPTO: Otonom Kripto Takip ve Somut Arayüz (Tangible UI) Sistemi

GARYPTO, finansal piyasalardaki dijital verileri (API) çevresel algıya hitap eden fiziksel hareketlere dönüştüren, ESP32-S3 tabanlı otonom bir Nesnelerin İnterneti (IoT) prototipidir. Kullanıcıların "ekran yorgunluğunu" (screen fatigue) azaltmayı hedefleyen bu sistem, bilgisayar veya akıllı telefon bağımlılığı olmadan cihaz üzerinden kontrol (On-Device Control) imkanı sunar.

Aynı zamanda Bilişimsel Düşünme (Computational Thinking) becerilerini destekleyen bir Eğitim Teknolojileri (BÖTE) ve STEM laboratuvar materyali olarak tasarlanmıştır.

![GARYPTO Cihaz Görseli](images/cihaz_genel.jpeg)

## 🌟 Temel Özellikler

* **Fiziksel Geri Bildirim (Tangible UI):** Belirlenen limitler aşıldığında servo motorlar aracılığıyla yeşil (yükseliş) ve kırmızı (düşüş) bayraklar kalkar.
* **Bağımsız Arayüz:** 4 inç Dokunmatik TFT ekran ve özel yazılmış dinamik Numpad arayüzü.
* **Asenkron API Sorgusu:** Binance Public REST API üzerinden her 5 saniyede bir güncel JSON verisi ayrıştırılır (Parsing).
* **Akıllı Çapa (Smart Anchor) Algoritması:** Yavaş fiyat sızıntılarında bile veri kaçırmayı önleyen dinamik referans güncelleme mantığı.
* **Yönden Bağımsız Filtre:** C++ `fabs()` fonksiyonu ile negatif/pozitif işaret karmaşasını ortadan kaldıran mutlak değer filtresi.
* **Soft-Sweep Motor Kontrolü:** Servo motorlarda ani tork vuruntusunu engelleyen mikro-gecikmeli PWM döngüsü.

## 🛠️ Donanım Montajı ve Prototip Tasarımı

Proje, parametrik olarak tasarlanmış 3D baskı bir kasa içerisinde, tüm elektronik bileşenlerin breadboard üzerinden beslenmesi ve ESP32-S3 kartı ile entegrasyonu prensibiyle çalışır. Tasarımda, güç darboğazlarını engellemek adına harici 5V/2A besleme hattı tercih edilmiştir. 3D tasarım dosyalarına `3D_Models/` klasöründen ulaşabilirsiniz.

## 💻 Yazılım ve Kütüphaneler

Proje **C++** dili ile Arduino IDE ortamında geliştirilmiştir.
* `TFT_eSPI` ve `SPI.h`
* `WiFi.h` ve `HTTPClient.h`
* `ArduinoJson`
* `ESP32Servo`

## ⚙️ Kurulum ve Çalıştırma

1. Bu depoyu bilgisayarınıza klonlayın: `git clone https://github.com/kullaniciadiniz/GARYPTO.git`
2. `src/` klasöründeki `.ino` dosyasını Arduino IDE ile açın.
3. Kod içerisindeki Wi-Fi ayarlarını (`ssid` ve `password`) kendi ağınıza göre güncelleyin.
4. Gerekli kütüphanelerin yüklü olduğundan emin olun ve ESP32-S3 kartınıza yükleyin.

## 👨‍💻 Geliştirici
**Musa Haşimoğlu** (Bilgisayar ve Öğretim Teknolojileri Eğitimi - STEM Projesi)

## 📄 Lisans
Bu projenin Telif Hakkı Saklıdır (All Rights Reserved)