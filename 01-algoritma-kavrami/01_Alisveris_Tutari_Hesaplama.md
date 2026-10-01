# Alışveriş Tutarını Hesaplama

## 1. Çalışmanın Amacı

Bu çalışma, algoritma kavramını günlük hayattan bir örnek üzerinden anlamak ve temel problem çözme adımlarını uygulamak amacıyla hazırlanmıştır.

## 2. Problem Tanımı

Bir müşterinin satın almak istediği ürünün birim fiyatı ve ürün adedi kullanılarak toplam alışveriş tutarının hesaplanması hedeflenmektedir.

**Örnek veriler:**

| Değişken     |  Değer |
| ------------ | -----: |
| Ürün fiyatı  | 250 TL |
| Ürün adedi   |      3 |
| Toplam tutar | 750 TL |

## 3. Girdi, İşlem ve Çıktı

| Aşama           | Açıklama                  |
| --------------- | ------------------------- |
| Girdi (Input)   | Ürün fiyatı ve ürün adedi |
| İşlem (Process) | Ürün fiyatı × ürün adedi  |
| Çıktı (Output)  | Hesaplanan toplam tutar   |

## 4. Algoritma Adımları

1. Başla.
2. Ürün fiyatını belirle.
3. Ürün adedini belirle.
4. Ürün fiyatını ürün adediyle çarp.
5. Hesaplanan toplam tutarı ekrana yazdır.
6. Bitir.

## 5. Sözde Kod

```text
BAŞLA
    ürün_fiyatı = 250
    ürün_adedi = 3
    toplam_tutar = ürün_fiyatı * ürün_adedi
    YAZDIR toplam_tutar
BİTİR
```

## 6. Örnek Çalıştırma

**Girdiler:**

* Ürün fiyatı: 250 TL
* Ürün adedi: 3

**Hesaplama:**

250 × 3 = 750 TL

**Beklenen çıktı:**

```text
Toplam tutar: 750 TL
```

## 7. İş Analizi Açısından Değerlendirme

Bu örnek, bir iş sürecinin temel girdilerinin, işlemlerinin ve çıktılarının belirlenmesini göstermektedir.

Gerçek bir e-ticaret uygulamasında aşağıdaki iş kuralları da değerlendirilmelidir:

* Ürün adedi sıfırdan büyük olmalıdır.
* Ürün fiyatı geçerli bir değer olmalıdır.
* İndirim uygulanıyorsa indirim tutarı hesaplamaya dâhil edilmelidir.
* Hesaplanan toplam tutar kullanıcıya gösterilmelidir.

## 8. Sonuç

Bu uygulama ile basit bir problemin sıralı işlem adımlarıyla nasıl çözülebileceği incelenmiştir. Girdi, işlem ve çıktı kavramları kullanılarak temel bir algoritma oluşturulmuştur.
