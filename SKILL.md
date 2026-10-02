---
name: turkce-teknik-yazim
description: Türkçe teknik metinleri, ajan talimatlarını, araç açıklamalarını ve durum raporlarını anlamı koruyarak açıklaştır. Kullanıcı Türkçe sadeleştirme istediğinde veya teknik metinde yoruma açık talimatlar bulunduğunda kullan. Yaratıcı ve pazarlama metinlerine kendiliğinden uygulama.
---

# Türkçe teknik yazım

ASD-STE100'ün açıklık ilkelerinden esinlenen Türkçe yazım becerisidir. Resmî STE çevirisi veya uygunluk denetleyicisi değildir. İngilizce sözlüğü ve dilbilgisi kısıtlarını Türkçeye taşıma.

## Kullanım biçimi

- **Talimat:** İşlem adımları, araç açıklamaları ve ajanlar arası görevlerde kullan. Faili, koşulu, işlemi ve beklenen sonucu açık yaz.
- **Açıklama:** Teknik yanıtlar, durum raporları, README ve PR açıklamalarında kullan. Ana sonucu önce ver. Gerekçeyi ve kanıtı ardından anlat.

Metnin amacına göre biçimi seç. Kullanıcı istemedikçe biçim seçimini açıklama. Kullanıcının istediği uzunluğu ve çıktı yapısını koru.

## Anlamı koruma

Yeniden yazmadan önce şu öğeleri belirle: fail, işlem, nesne, koşul, sıra, kapsam, sayı, birim, zaman ve kesinlik düzeyi.

- Olumsuzluğu, istisnayı, zorunluluğu ve izin sınırını koru.
- “Olabilir” ifadesini kesin bir olaya dönüştürme. “Yapmalı” ile “yapabilir” aynı anlamı taşımaz.
- Kanıtlanmış sonucu, çıkarımı ve kontrol edilmemiş durumu ayır. Kaynak metindeki belirsizliği silme.
- Kaynağın vermediği neden, fail, ölçüm veya sonuç ekleme.
- Anlamı etkileyen belirsizliği tahminle kapatma. Metinde koru ve kısa bir açıklama iste.
- Kod, komut, dosya yolu, API alanı, ürün adı ve hata kodunu koru. Açıkça istenmedikçe alıntıları değiştirme.

Özellikle şu dönüşümleri yapma:

| Kaynak | Anlamı bozan dönüşüm |
|---|---|
| İstek başarısız olmuş olabilir. | İstek başarısız oldu. |
| Testler geçti. Yayını kontrol etmedim. | Değişiklik sorunsuz çalışıyor. |
| Yalnızca boş klasörleri sil. | Klasörleri sil. |
| En az 10 saniye bekle. | 10 saniye bekle. |
| Kullanıcı onay verirse dosyayı gönder. | Dosyayı gönder. |

## Yazım kuralları

1. **Tek dil kullan.** Türkçe metinde açıklamaları Türkçe yaz. Kod, komut ve yerleşik adları olduğu gibi bırak.
2. **Sonucu önce ver.** “Analiz tamam” gibi boş girişler yerine bulguyu veya tamamlanan işi yaz.
3. **Faili açıklaştır.** “Dosyayı güncelledim” gibi etken cümleler kullan. Fail bilinmiyorsa fail uydurma. Fail önemsizse edilgen cümle kalabilir.
4. **Kendi işini düz cümleyle anlat.** “Kontrol ediyorum” veya “Kontrol ettim” yaz. Kullanıcının ve görev alan ajanın yapacağı işlerde emir kipini kullan.
5. **Bir cümlede tek konu anlat.** Talimatlarda 15, açıklamalarda 20 kelimeyi hedef üst sınır olarak kullan. Gerekli anlam kayboluyorsa sınırı aş.
6. **Tam cümle kur.** Kelime azaltmak için gerekli fiilleri, koşulları veya Türkçe ekleri silme. Başlıklarda ve tablo hücrelerinde kısa ifadeler kullanılabilir.
7. **Aynı kavram için aynı terimi kullan.** Kullanıcının terimini tercih et. Teknik olarak farklı işlemleri sırf benzer sözcüklerle anlatıldıkları için tek terime indirme.
8. **İsim zincirlerini kısalt.** Üç kelimeyi aşan zincirleri mümkünse cümleye dönüştür. Teknik adları ve anlamı belirleyen tamlamaları bozma.
9. **Gereksiz ifadeleri çıkar.** “Şunu belirtmek önemlidir” gibi girişleri kaldır. Ölçümsüz kalite iddialarını çıkar veya mevcut kanıtla somutlaştır.
10. **Paragrafları tek konuya ayır.** Bir paragrafta en çok altı cümle kullan. Birbirine bağlı gerekçeleri sırf metni kısaltmak için parçalama.

Türkçede kişi ekleri faili gösterebilir. Her cümlede “ben” veya “sen” yazmak gerekmez. Zaman ve görünüş eklerini yalnızca cümleyi kısaltmak için değiştirme.

## Adımlar ve uyarılar

- Kullanıcının sıralı işlemlerini numaralı liste yap. Her adımda tek talimat ver.
- Koşulu ilgili işlemden önce yaz: “Klasör boşsa, klasörü sil.”
- Bağımsız talimatları noktalı virgülle bağlama. Noktalı virgülü düzyazıda ayrı cümlelerle değiştir.
- Komutu ayrı kod bloğunda ver. Tek satırlı komutu görsel amaçla bölme. Anlamlı çok satırlı betikleri koru.
- Kaynakta bir risk varsa uyarıyı riskli adımdan önce ver. Uyarıya yapılacak işlemle başla. Riski tek cümlede açıkla.
- Kaynakta olmayan bir risk, onay gereksinimi veya dış işlem yetkisi ekleme.
- Kullanıcı riski zaten kabul ettiyse aynı uyarıyı tekrarlama.

## Örnekler

| Önce | Sonra |
|---|---|
| Dosya güncellendi ve kontrol edildi. | Dosyayı güncelledim. Dosyayı kontrol ettim. |
| Öncelikle logların bir analizini gerçekleştireceğim. | Önce logları analiz edeceğim. |
| Testler yeşil görünüyor. | Testler geçti. |
| Sistem güçlü ve sorunsuz bir deneyim sunar. | Ölçüm yoksa kalite iddiasını çıkar. |
| AI bot tarama izleme sistemi | AI botlarının taramasını izleyen sistem |

Bu örneklerde fail ve test sonucu biliniyor. Kaynak bunları doğrulamıyorsa örnekteki kesin ifadeyi kullanma.

## Kontrol ve çıktı

Yeniden yazdıktan sonra kaynakla karşılaştır. Sayıların, birimlerin, olumsuzlukların, koşulların, işlem sırasının ve kesinlik düzeyinin korunduğunu kontrol et.

Deterministik kontrolleri anlam denetiminden ayır. Kelime sayısı ve noktalama otomatik kontrol edilebilir. Bu kontroller anlamın korunduğunu kanıtlamaz. Türkçe ekleri, faili ve terim eşdeğerliğini yalnızca basit sözcük eşleştirmeleriyle doğrulanmış sayma.

- **Yeniden yazma isteği:** Yalnızca düzenlenmiş metni ver. Anlamı etkileyen çözümsüz belirsizlik varsa metnin ardından kısa bir “Belirsizlik:” notu ekle.
- **Gerekçe isteği:** “Kural / Önce / Sonra” tablosu ver. Bilerek koruduğun uzun ifadeyi ve nedenini açıkla.
- **Yeni metin üretme:** İstenen içeriği doğrudan yaz. Beceri adı veya kural raporu ekleme.
- **Zaten açık metin:** Sırf beceriyi uygulamak için değişiklik yapma. Yeniden yazma isteğinde metni olduğu gibi döndür.

Kelime sınırı anlamı bozuyorsa anlamı koru. Amaç en kısa metni yazmak değil, yanlış anlaşılmayı azaltmaktır.
