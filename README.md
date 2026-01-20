# Arçelik Markasına Ait Müşteri Şikayetlerinin Web Madenciliği ile Analizi

## Rapor ve Sunum

- **Proje Raporu**  
  [Web Madenciliği Final Raporu](WebMadenciliğiFinalRapor.docx)

- **YouTube Sunumu**  
  https://www.youtube.com/watch?v=BpofVq4QKmA

---


## 1. Proje Tanımı ve Problemin Belirlenmesi

Bu proje, beyaz eşya sektörünün lider markalarından **Arçelik** hakkında internet ortamında  
(**Şikayetvar** ve **X (Twitter)**) paylaşılan yapılandırılmamış müşteri şikayetlerini  
**web madenciliği** ve **doğal dil işleme (NLP)** yöntemleriyle analiz etmektedir.

Çalışma, satış sonrası hizmetlerde yaşanan **operasyonel gecikmeleri** ve  
**üretim kalitesinden kaynaklı sorunları** veri temelli bir bakış açısıyla ortaya koyarak  
**kurumsal karar destek süreçlerine** girdi sağlamayı amaçlamaktadır.

---

## 2. Araştırma Soruları

- Müşteri şikayetlerinin kök nedeni **üretim hataları** mı yoksa **hizmet (insan faktörü)** kaynaklı mıdır?
- Hangi departman (**Teknik Servis, Lojistik, Çağrı Merkezi**) operasyonel darboğaz oluşturmaktadır?
- Şikayetlerin ne kadarı **kritik müşteri kaybı (churn)** riski taşımaktadır?

---

## 3. Veri Tedarik Süreci ve Teknik Kaynaklar

Analiz kapsamında **19 Ocak 2026** itibarıyla son **1 yıllık dönemi** kapsayan veriler  
iki ana kaynaktan temin edilmiştir:

### Veri Kaynakları

- **Şikayetvar**
  - 10.000+ detaylı müşteri deneyimi metni

- **X (Twitter)**
  - 1.200+ anlık müşteri geri bildirimi

### Teknik Araçlar

- **Selenium WebDriver**  
  Dinamik içeriklerin kazınması ve bot engellerinin aşılması

- **BeautifulSoup & Requests**  
  HTML ayrıştırma ve veri temizleme süreçleri

- **ThreadPoolExecutor**  
  Paralel veri çekimi ile performans optimizasyonu

---

## 4. Metodoloji ve Veri Hazırlığı

Projede **CRISP-DM (Cross Industry Standard Process for Data Mining)** metodolojisi izlenmiştir.

Toplanan ham metinler aşağıdaki **NLP (Doğal Dil İşleme)** adımlarından geçirilmiştir:

- Gürültü giderimi (HTML etiketleri ve sistem mesajları)
- Tokenizasyon ve küçük harfe dönüştürme
- Türkçe stopword (etkisiz kelime) temizliği
- Markaya özel anlamsal katkısı olmayan ifadelerin filtrelenmesi

---

## 5. Sınıflandırma Mantığı ve Anahtar Kelimeler

Şikayetlerin otomatik sınıflandırılmasında **kural tabanlı (rule-based)** bir yaklaşım benimsenmiştir.

### Anahtar Kelime Grupları

- **Üretim Kaynaklı (Fabrika)**
  - motor, kart, arıza, üretim, kusurlu, fabrika hatası

- **Hizmet Kaynaklı (Servis / İnsan Faktörü)**
  - montaj, teknisyen, randevu, bayi, nezaketsiz, usta

- **Churn (Müşteri Kaybı) Riski**
  - iade, THH, avukat, dava, asla, pişman, mahkeme

---

## 6. Analiz Sonuçları ve Bulgular

### 6.1 Kök Neden Analizi

Analiz sonuçları, şikayetlerin %59,5'inin doğrudan üretim kaynaklı teknik kusurlardan oluştuğunu göstermektedir. Kelime frekans analizlerinde; motor arızaları, ana kart problemleri ve fiziksel deformasyonlar en sık tekrar eden unsurlardır. Bu durum, müşteri memnuniyetsizliğinin satış sonrası hizmetlerden ziyade fabrikadaki kalite kontrol süreçlerinde başladığını kanıtlamaktadır.

<img width="500" alt="Kök Neden Dağılımı" src="https://github.com/user-attachments/assets/5abb21ba-1d42-45c7-9aad-73ddab430cf7" />

---

### 6.2 Operasyonel Darboğaz Analizi

Müşteri memnuniyetsizliğinin %83'ü Teknik Servis süreçlerinde yoğunlaşmaktadır. Şikayetler temel olarak; randevu gecikmeleri, müdahale hızı ve yedek parça bekleme süreleri gibi zaman eksenli kısıtlarda birikmektedir. Üretimdeki yüksek hata oranı, servis ağında kontrol edilemez bir talep yığılması yaratarak bu birimi sistemin ana darboğazı haline getirmiştir.

<img width="500" alt="Departman Bazlı Darboğazlar" src="https://github.com/user-attachments/assets/3e795cf5-a2b2-441c-9a04-c8d227f2b568" />

---

### 6.3 Churn (Müşteri Kaybı) Analizi

Müşterilerin %37,9'u yüksek churn riski taşımaktadır. Metinlerde geçen "Tüketici Hakem Heyeti", "bedel iadesi" ve "avukat" gibi anahtar kelimeler, mutsuzluğun yasal sürece evrilme potansiyelini göstermektedir. Bu kitle, marka sadakati kaybının yanı sıra iade maliyetleri ve hukuki giderler nedeniyle doğrudan finansal risk oluşturmaktadır.

<img width="500" alt="Kategorilere Göre Churn" src="https://github.com/user-attachments/assets/5c568cc7-b321-4d6d-8158-b24f1f4537b5" />

---

## 7. Yönetsel Öneriler ve Sonuç

- **Dijital Servis Optimizasyonu**  
  Teknik servis üzerindeki %83'lük iş yükünü yönetmek adına, yapay zeka destekli dinamik rota optimizasyonu ve teknisyen uzmanlık eşleştirmesi yapan dijital sistemlerin devreye alınması önerilmektedir.

- **Üretimde Altı Sigma Disiplini**  
  Şikayetlerin ana kaynağı olan üretim hatalarını minimize etmek için üretim hattında Altı Sigma metodolojisi uygulanmalıdır. Hataların kaynağında yok edilmesi, servis ağındaki baskıyı çarpan etkisiyle azaltacaktır.

- **Proaktif Geri Kazanım Stratejileri**  
  Analizle tespit edilen yüksek riskli kitleye yönelik, konu Tüketici Hakem Heyeti gibi resmi mercilere taşınmadan önce müdahale edilmelidir. "Kırmızı Hat" benzeri bir mekanizma ile bu müşterilere hızlı çözüm (ürün değişimi, VIP servis) sunularak marka kaybı önlenmelidir.

---

## 8. Etik Değerlendirme ve Sınırlılıklar

- Çalışma **akademik amaçlıdır**.
- Veriler yalnızca **kamuya açık platformlardan** elde edilmiştir.
- Kişisel veriler (isim, telefon vb.) analiz dışında tutulmuştur.
- Sınıflandırma süreci **kural tabanlıdır** ve %100 doğruluk iddiası taşımamaktadır.
