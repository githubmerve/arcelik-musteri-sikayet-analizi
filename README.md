# Arçelik Müşteri Şikayetlerinin Web Madenciliği ve NLP ile Analizi

Bu proje, Arçelik markasına ait müşteri şikayetlerini web madenciliği ve doğal dil işleme (NLP) teknikleri kullanarak analiz etmeyi amaçlamaktadır.  
Çalışma kapsamında müşteri memnuniyetsizliğine yol açan kök nedenler, operasyonel darboğazlar ve müşteri kaybı (churn) riski sınıflandırma yaklaşımıyla incelenmiştir.

---

## Proje Amacı

Bu projenin temel amacı, yapılandırılmamış müşteri şikayet metinlerinden anlamlı içgörüler elde ederek aşağıdaki sorulara yanıt aramaktır:

- Şikayetlerin kök nedeni üretim kaynaklı mı yoksa hizmet/personel kaynaklı mıdır?
- Hangi departmanlar müşteri memnuniyetsizliğinde temel darboğaz konumundadır?
- Hangi şikayetler acil müdahale edilmediği takdirde müşteri kaybına (churn) yol açacak seviyededir?

Bu yönüyle proje, müşteri ilişkileri ve kriz yönetimi perspektifinden bir **sınıflandırma (classification)** problemidir.

---

## Veri Kaynakları

Projede kullanılan veri kaynakları aşağıda listelenmiştir:

### Şikayetvar
- Kaynak: https://www.sikayetvar.com/arcelik  
- Kapsam: 10.000+ detaylı müşteri şikayeti  
- Kullanım Amacı: Ana analiz kaynağı

### X (Twitter)
- Kaynak: [https://twitter.com/ArcelikDestek](https://x.com/ArcelikDestek/with_replies)  
- Kapsam: 1.200+ anlık müşteri geri bildirimi  
- Kullanım Amacı: Kriz potansiyeli yüksek geri bildirimlerin analizi

---

## Metodoloji

Bu çalışmada **CRISP-DM (Cross Industry Standard Process for Data Mining)** metodolojisi benimsenmiştir.

### Veri Hazırlığı ve NLP Pipeline

- HTML ve gürültü temizleme
- Tokenizasyon
- Sayı ve özel karakter temizliği
- Türkçe stopword çıkarımı
- Sözcük normalizasyonu

### Sınıflandırma Yapısı

Şikayetler aşağıdaki kriterlere göre etiketlenmiştir:

- **Kök Neden:** Üretim / Hizmet  
- **Darboğaz Departman:** Teknik Servis / Lojistik / Çağrı Merkezi  
- **Churn Riski:** Yüksek / Düşük  

---

## Analizler ve Görselleştirmeler

Proje kapsamında aşağıdaki analizler gerçekleştirilmiştir:

1. Şikayetlerin kök neden dağılımı (Pasta Grafik)  
2. Departman bazlı operasyonel darboğaz analizi (Bar Grafik)  
3. Ürün kategorilerine göre müşteri kaybı (Churn) riski analizi  

---

## Elde Edilen Bulgular

- Üretim kaynaklı şikayet oranı: %59,5  
- En kritik operasyonel darboğaz: Teknik Servis (%83)  
- Yüksek churn riski taşıyan müşteri oranı: %37,9  

Bu bulgular, müşteri memnuniyetsizliğinin temel nedeninin pazarlama değil; üretim kalitesi ve satış sonrası operasyonlar olduğunu göstermektedir.

---

## Rapor ve Sunum

- **Final Raporu:**  
  [Web Madenciliği Final Raporu](WebMadenciliğiFinalRapor.docx)

- **YouTube Sunumu:**  
  https://www.youtube.com/watch?v=BpofVq4QKmA

---

## Kullanılan Teknolojiler

- Python  
- Selenium  
- BeautifulSoup  
- Pandas  
- Scikit-learn  
- NLTK  
- Matplotlib  
- Seaborn  

---

## Akademik Bilgi

Bu proje,  
**Bursa Uludağ Üniversitesi – İnegöl İşletme Fakültesi**  
**Yönetim Bilişim Sistemleri Bölümü**  
**Web Madenciliği Dersi Final Projesi** kapsamında hazırlanmıştır.

---

## 

Bu proje yalnızca akademik amaçlarla geliştirilmiştir.
