# 📖 ClearRead AI

**ClearRead AI**, disleksi ve okuma güçlüğü çeken bireylerin dijital içerikleri daha rahat okuyabilmesi için geliştirilmiş, erişilebilirlik odaklı bir web uygulamasıdır. Metni sadece "kısaltmak" yerine, hem görsel olarak okunabilir hale getirir hem de anlamsal olarak sadeleştirir.

## 🎯 Problem
Dijital dünyadaki içeriklerin büyük çoğunluğu:
* Uzun ve karmaşık cümlelerden oluşur.
* Okunması zor fontlar kullanır.
* Görsel olarak yorucudur.

Bu durum, toplumun yaklaşık %10'unu oluşturan disleksiye sahip bireyler için ciddi bir bilgiye erişim problemidir.

## 💡 Çözüm (Çift Katmanlı Yaklaşım)

**1. Görsel Okuma Katmanı (Kod ile - Her Zaman Aktif)**
* Disleksi dostu font kullanımı (`OpenDyslexic`)
* Artırılmış satır aralığı ve göz yormayan arka plan (#F5F5DC)
* **Bionic Reading:** Gözün taramasını kolaylaştırmak için kelime başlarını kalınlaştırma.

**2. AI Destekli Sadeleştirme (İsteğe Bağlı)**
* Gemini AI API kullanılarak uzun cümlelerin bölünmesi.
* Zor kelimelerin basitleştirilmesi.
* Anlam bütünlüğünün korunarak bilişsel yükün azaltılması.

## ⚙️ Nasıl Çalışır?
1. Kullanıcı metni sol panele yapıştırır.
2. "Okuma Modu" ile metin sağ panelde anında görsel olarak optimize edilir.
3. İhtiyaç duyulursa "Simplify" (Sadeleştir) butonuna basılır.
4. Gemini AI, metni 5. sınıf okuma seviyesinde daha sade bir hale getirir.

## 🧠 Önemli Tasarım Kararı: Fallback Mimarisi
Bu proje şu sarsılmaz prensiple geliştirildi: **AI olmasa bile uygulama çalışmalıdır.** Görsel erişilebilirlik (font, satır aralığı, Bionic Reading) her zaman aktiftir. AI (Gemini), sadece ek bir bilişsel destek katmanıdır.

## 🛠️ Kullanılan Teknolojiler
* **Frontend:** React + Vite
* **Stil:** CSS / Tailwind
* **Yapay Zeka:** Gemini API (Google AI Studio)
* **Güvenlik:** Vercel Serverless Functions (`api/simplify.js`)
* **Geliştirme:** Cursor

## 🚀 Kurulum

Projeyi yerel ortamınızda çalıştırmak için:

```bash
# Bağımlılıkları yükleyin
npm install

# Geliştirme sunucusunu başlatın
npm run dev
