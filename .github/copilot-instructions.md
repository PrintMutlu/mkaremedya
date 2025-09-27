# M² Medya Statik Web Sitesi için Copilot Talimatları

Bu proje, bir dijital pazarlama ajansı olan M² Medya'nın statik HTML web sitesidir. Temel amaç, "Boostly" adlı orijinal şablonu M² Medya markası ve hizmetleri için tamamen özelleştirmektir.

## Mimarinin "Büyük Resmi"

- **Statik HTML Yapısı:** Bu bir sunucu tarafı dil (PHP, Node.js vb.) veya modern bir frontend framework (React, Vue) kullanmayan, tamamen statik bir projedir. Tüm sayfalar `buyer-file/` klasöründe bulunan bağımsız `.html` dosyalarıdır.
- **Paylaşılan Bileşen Yok:** En kritik nokta budur. `<header>` (navigasyon menüsü) ve `<footer>` (alt bilgi) gibi ortak bileşenler için bir şablon sistemi **yoktur**. Bu bileşenlerin kodları her bir `.html` dosyası içinde (`about.html`, `service.html` vb.) kopyalanıp yapıştırılmıştır.
- **Önemli Kural:** Navigasyon menüsü veya alt bilgi gibi genel bir alanda değişiklik yaparken, bu değişikliği `buyer-file/` içindeki **tüm** `.html` dosyalarına manuel olarak uygulamanız gerekir. Genellikle `index.html` dosyasını ana şablon olarak kullanır, değişikliği önce orada yapar ve sonra diğer dosyalara kopyalarız.

## Geliştirici İş Akışları

- **Yerel Sunucuda Çalıştırma:** Projeyi yerel olarak görüntülemenin en basit yolu, `buyer-file` dizini içindeyken bir HTTP sunucusu başlatmaktır.
  ```bash
  cd buyer-file
  python3 -m http.server 8000
  ```
  Alternatif olarak, VS Code'daki "Live Server" uzantısı şiddetle tavsiye edilir.
- **Build/Test Süreci Yok:** Bu statik bir site olduğu için herhangi bir derleme (build) veya test komutu yoktur. Değişiklikler doğrudan dosyalara yapılır ve tarayıcıda anında görülebilir.

## Projeye Özgü Kurallar ve Desenler

- **Tasarım Bütünlüğü:** En önemli kuraldır. Yapılan tüm metin ve yapısal değişiklikler, mevcut CSS sınıflarını ve HTML yapısını koruyarak sitenin görsel tasarımını **asla bozmamalıdır**. Yeni bir bileşen eklenmiyorsa, `assets/css/main.css` gibi ana stil dosyalarında değişiklik yapmaktan kaçının.
- **Marka ve Dil:** Ana marka "M² Medya"dır. Tüm içerik ve metinler **Türkçe** olmalıdır. "Boostly", "Company", "Services" gibi İngilizce kalıntıları gördüğünüzde bunları Türkçeleştirin.
- **Dosya Yapısı:**
  - `buyer-file/`: Kullanıcıların gördüğü canlı web sitesi dosyalarının bulunduğu ana klasördür. Tüm düzenlemeler bu klasör içinde yapılmalıdır.
  - `buyer-file/assets/`: CSS, JavaScript, resimler ve fontlar gibi tüm statik varlıkların bulunduğu yerdir.
  - `documentation/`: Orijinal şablonun dokümantasyonudur, projenin kendisiyle doğrudan bir ilgisi yoktur.
- **Hizmetler:** Ana hizmetler şunlardır: Web Tasarımı, SaaS Yazılımlar, Sosyal Medya Yönetimi, Reklam Yönetimi (Google & Meta Ads), SEO. İçerik bu hizmetler etrafında şekillendirilmelidir.
- **Örnek Değişiklik Senaryosu:**
  1. `buyer-file/index.html` dosyasındaki `<header>` bölümünde yeni bir menü öğesi ekleyin.
  2. Güncellenmiş `<header>...</header>` kod bloğunu kopyalayın.
  3. `buyer-file/about.html`, `buyer-file/service.html`, `buyer-file/contact.html` ve diğer tüm `.html` dosyalarını açın, mevcut `<header>` bloklarını silin ve yenisiyle değiştirin.
