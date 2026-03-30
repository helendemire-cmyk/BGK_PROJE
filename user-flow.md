# user-flow.md — ClearRead AI

## Kullanıcı Akışı

1. **Kullanıcı uygulamayı açar**
   Tek sayfalık sade bir arayüz görür.

   * Sol panel: metin giriş alanı
   * Sağ panel: dönüştürülmüş metnin gösterileceği alan

2. **Kullanıcı metni yapıştırır**
   Okumakta zorlandığı metni sol paneldeki kutuya yapıştırır.

3. **Kullanıcı “Transform” butonuna basar**
   Sistem metni sağ panelde disleksi dostu görsel stile dönüştürür:

   * Daha okunabilir font
   * Daha geniş satır aralığı
   * Daha yumuşak arka plan
   * Daha net kontrast

4. **Kullanıcı Bionic Reading’i açıp kapatabilir**
   Toggle açık olduğunda kelimelerin ilk kısmı kalınlaştırılır.
   Toggle kapalı olduğunda metin normal görünümde kalır.

5. **Kullanıcı “Simplify” butonuna basar**
   Eğer metin hâlâ karmaşıksa, kullanıcı AI destekli sadeleştirme ister.

6. **Sistem metni sadeleştirir**
   AI:

   * Uzun cümleleri böler
   * Zor kelimeleri basitleştirir
   * Anlamı koruyarak daha anlaşılır bir versiyon üretir

7. **Kullanıcı sonucu okur ve karşılaştırır**
   Kullanıcı sol taraftaki orijinal metin ile sağ taraftaki dönüştürülmüş metin arasındaki farkı görür.

8. **Kullanıcı metni kopyalayabilir**
   İsterse sadeleştirilmiş metni tek tıkla kopyalar ve başka yerde kullanır.

9. **Kullanıcı “Clear” butonu ile sıfırlar**
   Her iki panel temizlenir ve kullanıcı yeni bir metinle tekrar başlayabilir.

---

## Akışın Özeti

**Metni yapıştır → Transform → Bionic Reading (opsiyonel) → Simplify → Karşılaştır → Kopyala / Temizle**
