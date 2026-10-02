# Türkçe Teknik Yazım — ASD-STE100_TR

Türkçe teknik metinleri, ajan talimatlarını, araç açıklamalarını ve durum raporlarını anlamı koruyarak açıklaştıran bir beceri.

ASD-STE100'ün açıklık ilkelerinden esinlenir. Resmî STE çevirisi veya uygunluk denetleyicisi değildir. İngilizce onaylı sözlük ve dilbilgisi kısıtlarını Türkçeye taşımaz.

## Kurallar

- Bir cümlede tek konu veya işlem anlat.
- Faili ve koşulları açık yaz.
- Aynı kavram için aynı terimi kullan.
- Sayıları, birimleri, olumsuzlukları ve belirsizlik düzeyini koru.
- Kullanıcının sıralı işlemlerini numaralandır.
- Kısa yazarken gerekli anlamı silme.

Talimatlarda 15, açıklamalarda 20 kelime hedef üst sınırdır. Anlamı korumak için sınır aşılabilir. Bunlar resmî STE eşikleri değildir.

## Kurulum

Skills CLI ile:

```bash
npx skills add cenktk/ASD-STE100_TR
```

## Kullanım

Beceri adı: `turkce-teknik-yazim`.

Örnek istekler:

```text
$turkce-teknik-yazim Bu araç açıklamasını anlamı koruyarak sadeleştir.
```

```text
$turkce-teknik-yazim Bu yanıtı önce/sonra tablosuyla değerlendir.
```

Yeniden yazma isteğinde yalnızca düzenlenmiş metni verir. Gerekçe istendiğinde kural, önce ve sonra tablosu üretir. Zaten açık metni zorunlu olarak değiştirmez.

## Sınırlar

- Yaratıcı veya pazarlama metinlerine kendiliğinden uygulanmaz.
- Kod, komut, dosya yolu ve API alanları korunur.
- “Olabilir” ifadesi kanıt olmadan kesinleştirilmez.
- Yapısal uygunluk, anlamın korunduğunu veya içeriğin doğru olduğunu kanıtlamaz.
- Bu paket otomatik bir Türkçe denetleyici içermez.

Tam kurallar [SKILL.md](SKILL.md) dosyasındadır.

## Esin kaynağı

- [ASD-STE100](https://www.asd-ste100.org/)
- [danyuchn/asd-ste100-skill](https://github.com/danyuchn/asd-ste100-skill)
