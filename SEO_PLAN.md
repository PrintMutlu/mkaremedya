# M² Medya - Kapsamlı SEO Optimizasyon Planı

Bu belge, M² Medya web sitesinin arama motorlarında (Google, Yandex, Bing) en üst sıralarda yer alması ve sosyal medyada profesyonel görünmesi için gereken **eksiksiz** yol haritasıdır.

## 1. Mevcut Durum Analizi
*   **Eksikler:** Open Graph (Sosyal Medya) etiketleri yok, Canonical URL'ler yok, `robots.txt` ve `sitemap.xml` eksik, bazı sayfalarda dil `en` olarak kalmış, görsel `alt` etiketleri yetersiz ("img" gibi).
*   **İyi Yönler:** HTML5 yapısı temiz, başlık etiketleri (H1) mevcut.

## 2. Teknik SEO Gereksinimleri (Altyapı)

Bu maddeler sitenin "iskeletini" oluşturur ve arama motorlarının siteyi doğru okumasını sağlar.

### A. Meta Etiketler (Her Sayfa İçin)
Her `.html` dosyasının `<head>` bölümüne eklenecek standart yapı:
```html
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<meta name="description" content="[Sayfaya Özel Açıklama]">
<meta name="keywords" content="[Sayfaya Özel Anahtar Kelimeler]">
<meta name="author" content="M² Medya">
<meta name="robots" content="index, follow">
<link rel="canonical" href="https://mkaremedya.com/[sayfa-adi].html">
```

### B. Sosyal Medya Entegrasyonu (Open Graph & Twitter Cards)
Link paylaşıldığında (WhatsApp, LinkedIn, Instagram DM) profesyonel bir önizleme kartı çıkması için şarttır.
```html
<!-- Open Graph / Facebook & WhatsApp -->
<meta property="og:type" content="website">
<meta property="og:url" content="https://mkaremedya.com/[sayfa-adi].html">
<meta property="og:title" content="[Sayfa Başlığı] | M² Medya">
<meta property="og:description" content="[Sayfa Açıklaması]">
<meta property="og:image" content="https://mkaremedya.com/assets/img/og-image.jpg"> <!-- 1200x630px özel görsel -->

<!-- Twitter -->
<meta name="twitter:card" content="summary_large_image">
<meta name="twitter:url" content="https://mkaremedya.com/[sayfa-adi].html">
<meta name="twitter:title" content="[Sayfa Başlığı] | M² Medya">
<meta name="twitter:description" content="[Sayfa Açıklaması]">
<meta name="twitter:image" content="https://mkaremedya.com/assets/img/og-image.jpg">
```

### C. Yapısal Veri (Schema.org JSON-LD)
Google'ın işletmeyi "Dijital Ajans" olarak tanıması için `index.html` ve `contact.html` sayfalarına eklenecek kod.
```html
<script type="application/ld+json">
{
  "@context": "https://schema.org",
  "@type": "LocalBusiness",
  "name": "M² Medya",
  "image": "https://mkaremedya.com/assets/img/logo/logo.png",
  "@id": "",
  "url": "https://mkaremedya.com",
  "telephone": "+905555555555",
  "address": {
    "@type": "PostalAddress",
    "streetAddress": "Konyaaltı",
    "addressLocality": "Antalya",
    "postalCode": "07000",
    "addressCountry": "TR"
  },
  "geo": {
    "@type": "GeoCoordinates",
    "latitude": "36.8841",
    "longitude": "30.7056"
  },
  "openingHoursSpecification": {
    "@type": "OpeningHoursSpecification",
    "dayOfWeek": [
      "Monday",
      "Tuesday",
      "Wednesday",
      "Thursday",
      "Friday"
    ],
    "opens": "09:00",
    "closes": "18:00"
  }
}
</script>
```

### D. Dosya Düzeltmeleri
*   **Dil Tanımı:** Tüm sayfalarda `<html lang="en">` -> `<html lang="tr">` olarak değiştirilecek.
*   **Robots.txt:** Ana dizine eklenecek.
*   **Sitemap.xml:** Tüm sayfaları listeleyen harita oluşturulacak.

---

## 3. Sayfa Bazlı İçerik ve Meta Stratejisi

Her sayfa belirli anahtar kelimelere odaklanmalıdır.

### 🏠 Ana Sayfa (`index.html`)
*   **Odak:** Genel Marka Bilinirliği, Dijital Ajans, 360 Derece Pazarlama.
*   **Title:** M² Medya | Dijital Pazarlama, Web Tasarım ve SEO Ajansı
*   **Description:** M² Medya ile markanızı dijital dünyada büyütün. Profesyonel web tasarım, SEO, sosyal medya yönetimi ve dijital reklam hizmetleri sunuyoruz. Teklif alın!
*   **Keywords:** dijital ajans, web tasarım ajansı, seo hizmeti, sosyal medya yönetimi, kurumsal kimlik, m2 medya.
*   **H1:** Dijital Dünyada Markanızı Büyüten Çözümler (Mevcut H1 revize edilecek).

### 🏢 Hakkımızda (`about.html`)
*   **Odak:** Güven, Tecrübe, Ekip.
*   **Title:** Hakkımızda | M² Medya - Dijital Çözüm Ortağınız
*   **Description:** M² Medya olarak yenilikçi ve sonuç odaklı dijital pazarlama çözümleri sunuyoruz. Ekibimiz ve vizyonumuz hakkında bilgi alın.
*   **Keywords:** m2 medya kimdir, dijital ajans ekibi, kurumsal çözüm ortağı.

### 🛠 Hizmetler (`service.html`)
*   **Odak:** Hizmet Çeşitliliği.
*   **Title:** Hizmetlerimiz | Web Tasarım, SEO, Sosyal Medya ve Reklam
*   **Description:** İşletmeniz için sunduğumuz profesyonel hizmetler: Web geliştirme, arama motoru optimizasyonu (SEO), Google Ads yönetimi ve daha fazlası.
*   **Keywords:** web tasarım fiyatları, seo danışmanlığı, google reklam yönetimi, sosyal medya ajansı.

### 📞 İletişim (`contact.html`)
*   **Odak:** Erişim, Lokasyon.
*   **Title:** İletişim | M² Medya - Hemen Teklif Alın
*   **Description:** Projeniz için bizimle iletişime geçin. Adres, telefon ve e-posta bilgilerimiz. Ücretsiz ön analiz ve teklif için formu doldurun.
*   **Keywords:** dijital ajans iletişim, web tasarım teklif al, m2 medya adres.

---

## 4. Görsel Optimizasyonu (Image SEO)
Arama görsellerinde çıkmak için kritik.
*   **Kural:** Asla `alt="img"` veya `alt="logo"` kullanma.
*   **Uygulama:**
    *   Logo: `alt="M² Medya Dijital Pazarlama Ajansı Logosu"`
    *   Hero Görseli: `alt="M² Medya Web Tasarım ve Yazılım Ekibi Çalışırken"`
    *   Hizmet İkonları: `alt="SEO ve Arama Motoru Optimizasyonu İkonu"`, `alt="Sosyal Medya Yönetimi İkonu"`

---

## 5. Uygulama Kontrol Listesi (Todo List)

### Aşama 1: Temel Yapılandırma
- [ ] `robots.txt` dosyasını oluştur.
- [ ] `sitemap.xml` dosyasını oluştur.
- [ ] Tüm HTML dosyalarında `lang="tr"` düzeltmesi yap.
- [ ] `assets/img/` klasörüne `og-image.jpg` (1200x630px) ekle (Sosyal medya paylaşım görseli).

### Aşama 2: Sayfa İçi SEO (On-Page)
- [ ] **index.html:** Title, Description, Keywords, Canonical, OG Tags, JSON-LD Schema ekle.
- [ ] **about.html:** Title, Description, Keywords, Canonical, OG Tags ekle.
- [ ] **service.html:** Title, Description, Keywords, Canonical, OG Tags ekle.
- [ ] **contact.html:** Title, Description, Keywords, Canonical, OG Tags, LocalBusiness Schema ekle.
- [ ] **Diğer Sayfalar:** (pricing, faq vb.) Standart meta etiketlerini uygula.

### Aşama 3: İçerik ve Görsel İyileştirme
- [ ] Tüm `<img>` etiketlerini tara ve açıklayıcı `alt` metinleri yaz.
- [ ] `index.html` içindeki İngilizce kalan başlıkları (varsa) Türkçeleştir.
- [ ] H1, H2, H3 başlık hiyerarşisini kontrol et (H1'den sonra H2 gelmeli, H5 değil).

### Aşama 4: Test
- [ ] Google Rich Results Test aracı ile Schema yapısını test et.
- [ ] Meta etiketlerin uzunluklarını kontrol et (Title: max 60, Desc: max 160 karakter).
- [ ] Kırık link kontrolü yap.
