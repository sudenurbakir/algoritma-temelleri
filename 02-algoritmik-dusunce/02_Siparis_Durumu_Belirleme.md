# Sipariş Durumu Belirleme

## 1. Problem

Bir siparişin durumuna göre ekrana uygun bir mesaj yazdıran algoritma oluşturulacaktır.

Sipariş durumu:

* `Hazırlanıyor`
* `Kargoya Verildi`
* `Teslim Edildi`

değerlerinden biri olabilir.

Algoritma, siparişin mevcut durumunu kontrol ederek uygun mesajı göstermelidir.

---

## 2. Girdi

Algoritmanın ihtiyaç duyduğu bilgi:

* Sipariş durumu

Örneğin:

```text
Sipariş durumu = "Kargoya Verildi"
```

---

## 3. İşlem

Sipariş durumunun hangi değer olduğu kontrol edilir.

```text
Eğer sipariş durumu "Hazırlanıyor" ise
    "Siparişiniz hazırlanıyor." mesajını göster

Eğer sipariş durumu "Kargoya Verildi" ise
    "Siparişiniz kargoya verildi." mesajını göster

Eğer sipariş durumu "Teslim Edildi" ise
    "Siparişiniz teslim edildi." mesajını göster
```

Burada **koşul** kullanıyoruz.

---

## 4. Örnek

Kullanıcının sipariş durumu:

```text
Kargoya Verildi
```

Algoritma bu değeri kontrol eder.

```text
Sipariş durumu = "Hazırlanıyor"?
Hayır

Sipariş durumu = "Kargoya Verildi"?
Evet
```

Bu nedenle ekrana:

```text
Siparişiniz kargoya verildi.
```

yazdırılır.

---

## 5. Algoritma

```text
1. Başla
2. Sipariş durumunu al
3. Sipariş durumu "Hazırlanıyor" ise "Siparişiniz hazırlanıyor." yazdır
4. Sipariş durumu "Kargoya Verildi" ise "Siparişiniz kargoya verildi." yazdır
5. Sipariş durumu "Teslim Edildi" ise "Siparişiniz teslim edildi." yazdır
6. Bitir
```

---

## 6. Sözde Kod 

```text
BAŞLA

siparis_durumu değerini al

EĞER siparis_durumu = "Hazırlanıyor" İSE
    "Siparişiniz hazırlanıyor." yazdır

EĞER siparis_durumu = "Kargoya Verildi" İSE
    "Siparişiniz kargoya verildi." yazdır

EĞER siparis_durumu = "Teslim Edildi" İSE
    "Siparişiniz teslim edildi." yazdır

BİTİR
```

---

## 7. Girdi → Kontrol → Çıktı

```text
GİRDİ
↓
Sipariş durumu
↓
KOŞULU KONTROL ET
↓
Hangi durum?
↓
Uygun mesajı seç
↓
ÇIKTI
```

Örneğin:

```text
"Kargoya Verildi"
        ↓
Koşul kontrolü
        ↓
Kargoya Verildi mi?
        ↓
Evet
        ↓
"Siparişiniz kargoya verildi."
```

---

## 8. Koşul Nedir?

Koşul, bir durumun doğru olup olmadığını kontrol etmektir.

Örneğin:

```text
Yaş >= 18
```

ifadesi bir koşuldur.

Bu koşulun sonucu:

```text
Doğru (True)
```

veya:

```text
Yanlış (False)
```

olabilir.

Sipariş örneğinde ise:

```text
siparis_durumu = "Kargoya Verildi"
```

şeklinde bir kontrol yapıyoruz.

---

## 9. Karar Yapısı

Koşullu algoritmalarda temel yapı şu şekildedir:

```text
             KOŞUL
               ↓
        ┌──────┴──────┐
       EVET          HAYIR
        ↓              ↓
    Bir işlem       Başka işlem
```

Örneğin:

```text
Sipariş teslim edildi mi?
          ↓
     ┌────┴────┐
    EVET      HAYIR
     ↓          ↓
 Teslim     Durumu
 mesajı     kontrol et
```

Bu yapı programlamada `if` ve `else` gibi yapılarla ifade edilir.

---

## 10. Algoritmik Düşünme Açısından

```text
Girdi
 ↓
Koşulu kontrol et
 ↓
Karar ver
 ↓
Uygun işlemi yap
 ↓
Çıktı
```

Burada algoritma artık; 

> "Ne işlem yapacağım?"

sorusunu değil,

> "Hangi durumda hangi işlemi yapmalıyım?"

sorusunu da cevaplamaktadır.

---

## 11. Farklı Durumların İncelenmesi

### Durum 1

```text
Sipariş durumu = "Hazırlanıyor"
```

Çıktı:

```text
Siparişiniz hazırlanıyor.
```

### Durum 2

```text
Sipariş durumu = "Kargoya Verildi"
```

Çıktı:

```text
Siparişiniz kargoya verildi.
```

### Durum 3

```text
Sipariş durumu = "Teslim Edildi"
```

Çıktı:

```text
Siparişiniz teslim edildi.
```

---

