# onlinealisveris-sitesi
OOP mantığını kullanarak mini alışveriş sitesi oluşturduk
# 🛒 Online Alışveriş Sistemi (Python OOP Projesi)

Bu proje, Python kullanılarak geliştirilmiş terminal tabanlı bir e-ticaret ve sipariş yönetimi simülasyonudur. Projenin temel amacı, **Nesne Yönelimli Programlama (OOP)** prensiplerinin (Abstraction, Encapsulation, Inheritance, Polymorphism) gerçek hayat senaryolarında nasıl uygulanacağını pratik ve anlaşılır bir şekilde göstermektir.

---

## 🚀 Özellikler

* **Ürün Yönetimi:** Yeni ürün ekleme, listeleme, fiyat ve stok takibi.
* **Kullanıcı Yönetimi:** Standart ve Premium olmak üzere iki farklı üyelik tipi.
* **Sepet İşlemleri:** Sepete ürün ekleme/çıkarma, anlık tutar hesaplama.
* **Sipariş Motoru:** Stok kontrolü yaparak sipariş oluşturma ve kargo ücreti hesaplama (Premium üyelere ücretsiz kargo, Standart üyelere limite göre ücretlendirme).
* **Veri Kalıcılığı:** Sistemdeki tüm ürün, kullanıcı ve sipariş verilerini `JSON` formatında dosyaya kaydetme ve geri yükleme.
* **Hata Yönetimi:** Geçersiz girişlere ve stok yetersizliği gibi durumlara karşı `try-except` blokları ile güvenli akış.

---

## 🧠 Uygulanan OOP Prensipleri

Proje kodları incelendiğinde aşağıdaki kavramların aktif olarak kullanıldığı görülebilir:

1. **Soyutlama (Abstraction):** `TemelSistemElemani` sınıfı `ABC` (Abstract Base Class) kullanılarak oluşturulmuş ve ortak özellikler bu çatı altında toplanmıştır.
2. **Kapsülleme (Encapsulation):** `Urun` sınıfındaki `__ad`, `__fiyat`, `__stok` gibi özellikler private (gizli) yapılmış, bu verilere erişim ve müdahale `getter` ve `setter` metotları ile kontrol altına alınmıştır.
3. **Kalıtım (Inheritance):** `PremiumKullanici` sınıfı, temel `Kullanici` sınıfından türetilerek kod tekrarı önlenmiştir.
4. **Çok Biçimlilik (Polymorphism):** `bilgi_goster()` ve `kargo_ucreti_hesapla()` metotları farklı sınıflarda kendi yapılarına uygun şekilde (Method Overriding) yeniden yazılmıştır.
5. **Bileşim (Composition):** Her kullanıcının kendisine ait bir `Sepet` nesnesi barındırması sağlanmıştır.

---

## 🛠️ Sistem Gereksinimleri ve Kurulum

Proje tamamen Python'ın standart kütüphaneleri (`json`, `abc`) kullanılarak yazılmıştır. Herhangi bir harici paket yüklemesine gerek yoktur.

* **Gereksinim:** Python 3.x

### Çalıştırma Adımları

1. Proje dosyalarını bilgisayarınıza indirin.
2. Terminal veya komut satırını açarak dosyanın bulunduğu dizine gidin.
3. Aşağıdaki komutu çalıştırın:

```bash
python main.py
