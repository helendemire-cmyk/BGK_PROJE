# tech-stack.md — ClearRead AI

## Proje Adı

ClearRead AI

## Amaç

ClearRead AI, disleksi ve okuma güçlüğü çeken bireyler için metinleri daha okunabilir hale getiren basit bir web uygulamasıdır.

Bu uygulama iki temel katmandan oluşur:

1. **Görsel Okuma Desteği (Kod ile)**

   * Disleksi dostu font
   * Satır aralığı ve boşluk düzeni
   * Kontrast ayarları
   * Bionic Reading

2. **AI Destekli Sadeleştirme**

   * Uzun cümleleri bölme
   * Zor kelimeleri basitleştirme
   * Anlamı koruyarak metni kolaylaştırma

Amaç: 2-3 gün içinde çalışan, stabil ve sade bir MVP üretmek.

---

## Kullanılan Teknolojiler

### 1. Frontend

**React + Vite**

#### Neden?

* Hızlı kurulum
* Cursor ile çok iyi çalışır
* Tek sayfalık uygulama için ideal
* Vercel ile kolay deploy edilir

---

### 2. Stil (UI)

**Basit CSS (veya mümkünse Tailwind)**

#### Neden?

* Karmaşık tasarım sistemine ihtiyaç yok
* Odak: okunabilirlik
* Gerekli olanlar:

  * font
  * spacing
  * contrast
  * split layout

Eğer Tailwind kurulumda sorun çıkarırsa, direkt CSS kullanılabilir.

---

### 3. Yapay Zeka

**Gemini API (Google AI Studio)**

#### Neden?

* Metin sadeleştirme için uygun
* Prompt ile kolay kontrol edilir
* MVP için yeterli

⚠️ Not:
AI sadece “Simplify” özelliğinde kullanılacak.
Uygulama AI olmadan da çalışmalıdır.

---

### 4. Güvenlik Katmanı

**Vercel Serverless Function (api/simplify.js)**

#### Neden?

API anahtarını frontend’de kullanmak güvenli değildir.

Bu yüzden:

* frontend → `/api/simplify` endpoint’ine gider
* backend (serverless) → Gemini’a gider
* sonuç frontend’e döner

Bu sayede API key gizli kalır.

---

### 5. Geliştirme Ortamı

**Cursor**

#### Neden?

* Kod bilmeyen biri için en güçlü araç
* AI ile kod yazdırma imkanı
* Hataları anlamayı kolaylaştırır

---

### 6. Versiyon Kontrol

**GitHub**

#### Neden?

* Proje teslimi için gerekli
* Kodun yedeği olur
* Dokümantasyon gösterilir

---

### 7. Yayınlama (Deploy)

**Vercel**

#### Neden?

* GitHub ile otomatik bağlantı
* React projeleri için ideal
* Serverless API destekler

---

## Dosya Yapısı

```
clearread-ai/
├── api/
│   └── simplify.js
├── src/
│   ├── App.jsx
│   ├── index.css
│   └── main.jsx
├── .env
├── vercel.json
├── package.json
└── README.md
```

---

## Geliştirme Stratejisi

### 1. Aşama — Temel UI

* Metin input
* Output panel
* Split screen

### 2. Aşama — Görsel Okuma

* Font değişimi
* Satır aralığı
* Kontrast
* Bionic Reading

### 3. Aşama — AI Simplify

* API bağlantısı
* Loading durumu
* Hata yönetimi

---

## En Kritik İlke

👉 **Uygulama AI olmasa bile çalışmalı**

Bu yüzden:

* Visual reading her zaman çalışır
* Bionic reading her zaman çalışır
* AI sadece ekstra katmandır

---

## Riskler

1. API bağlantı hataları
2. Vercel deploy sorunları
3. Fazla özellik ekleme (scope creep)

---

## Risk Azaltma

* Önce UI çalıştır
* Sonra visual features ekle
* En son AI bağla
* Deploy’u en sona bırak

---

## Final Karar

Bu teknoloji seçimi:

* Basit
* Güvenli
* Yapılabilir
* Demo için güçlü

ve 2-3 gün içinde tamamlanabilecek en doğru yaklaşımdır.
