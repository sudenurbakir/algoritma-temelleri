# İndirimli Ürün Fiyatı Hesaplama

## 1. Çalışmanın Amacı

Bu çalışma, algoritmik düşünme becerisini geliştirmek ve bir problemin daha küçük işlem adımlarına ayrılarak nasıl çözülebileceğini incelemek amacıyla hazırlanmıştır.

Örnek uygulamada bir ürünün indirimli satış fiyatı hesaplanmaktadır.

## 2. Problem Tanımı

Bir e-ticaret sitesinde ürünün normal fiyatı ve indirim oranı kullanılarak indirimli satış fiyatının hesaplanması hedeflenmektedir.

**Örnek veriler:**

| Değişken        |    Değer |
| --------------- | -------: |
| Ürün fiyatı     | 1.000 TL |
| İndirim oranı   |      %20 |
| İndirim tutarı  |   200 TL |
| İndirimli fiyat |   800 TL |

## 3. Problemin Analizi

Problem, iki temel işleme ayrılmıştır:

1. İndirim tutarının hesaplanması.
2. İndirim tutarının ürünün normal fiyatından çıkarılması.

## 4. Girdi, İşlem ve Çıktı

| Aşama           | Açıklama                                                      |
| --------------- | ------------------------------------------------------------- |
| Girdi (Input)   | Ürün fiyatı ve indirim oranı                                  |
| İşlem (Process) | İndirim tutarının hesaplanması ve normal fiyattan çıkarılması |
| Çıktı (Output)  | İndirim tutarı ve indirimli ürün fiyatı                       |

## 5. Algoritma Adımları

1. Başla.
2. Ürün fiyatını belirle.
3. İndirim oranını belirle.
4. Ürün fiyatı ile indirim oranını çarp.
5. Elde edilen sonucu 100'e bölerek indirim tutarını hesapla.
6. İndirim tutarını ürün fiyatından çıkar.
7. İndirimli fiyatı ekrana yazdır.
8. Bitir.

## 6. Sözde Kod

```text
BAŞLA
    ürün_fiyatı = 1000
    indirim_oranı = 20

    indirim_tutarı = ürün_fiyatı * indirim_oranı / 100
    indirimli_fiyat = ürün_fiyatı - indirim_tutarı

    YAZDIR indirim_tutarı
    YAZDIR indirimli_fiyat
BİTİR
```

## 7. Örnek Çalıştırma

**Girdiler:**

* Ürün fiyatı: 1.000 TL
* İndirim oranı: %20

**Hesaplama:**

İndirim tutarı:

1.000 × 20 / 100 = 200 TL

İndirimli fiyat:

1.000 - 200 = 800 TL

**Beklenen çıktı:**

```text
İndirim tutarı: 200 TL
İndirimli fiyat: 800 TL
```

## 8. İş Analizi Açısından Değerlendirme

Bu çalışma kapsamında problem, girdi, işlem ve çıktı aşamalarına ayrılarak analiz edilmiştir.

Gerçek bir e-ticaret uygulamasında aşağıdaki iş kurallarının da belirlenmesi gerekir:

* İndirim oranının geçerli aralıkta olması.
* İndirim uygulanmayan ürünlerin nasıl işleneceği.
* Ondalıklı tutarların nasıl yuvarlanacağı.
* Birden fazla indirimin birlikte uygulanıp uygulanamayacağı.

Bu kuralların netleştirilmesi, gereksinimlerin doğru tanımlanmasına ve geliştirme sürecinde oluşabilecek belirsizliklerin azaltılmasına yardımcı olur.

## 9. Sonuç

Bu uygulama ile algoritmik düşünmenin temel aşamaları incelenmiştir. Bir problemin küçük parçalara ayrılması, çözüm adımlarının oluşturulması ve elde edilen sonucun kontrol edilmesi uygulanmıştır.
