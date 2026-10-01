# Görev Önceliklendirme

## 1. Problem

Bir görevin önem ve aciliyet durumuna göre önceliğini belirleyen bir algoritma oluşturulacaktır.

Görevin:

* Önem seviyesi
* Aciliyet seviyesi

bilgileri alınacaktır.

Bu bilgilere göre görev:

* Yüksek Öncelik
* Orta Öncelik
* Düşük Öncelik

olarak sınıflandırılacaktır.

---

## 2. Girdiler

Algoritmanın ihtiyaç duyduğu bilgiler:

* Önem seviyesi
* Aciliyet seviyesi

Örneğin:

```text
Önem = Yüksek
Aciliyet = Yüksek
```

---

## 3. İşlem

Öncelik belirlenirken iki bilgi birlikte değerlendirilir.

Örneğin:

```text
Önem yüksek + Aciliyet yüksek
→ Yüksek Öncelik
```

```text
Önem yüksek + Aciliyet düşük
→ Orta Öncelik
```

```text
Önem düşük + Aciliyet düşük
→ Düşük Öncelik
```

Burada algoritma yalnızca tek bir bilgiyi değil, **birden fazla koşulu birlikte değerlendirmektedir.**

---

## 4. Örnek

Bir görevin bilgileri:

```text
Önem = Yüksek
Aciliyet = Yüksek
```

Algoritma önce önem seviyesini kontrol eder:

```text
Önem yüksek mi?
→ Evet
```

Daha sonra aciliyet seviyesini kontrol eder:

```text
Aciliyet yüksek mi?
→ Evet
```

İki koşul da sağlandığı için:

```text
Öncelik = Yüksek
```

sonucu elde edilir.

---

## 5. Algoritma

```text
1. Başla
2. Önem seviyesini al
3. Aciliyet seviyesini al
4. Önem yüksek ve aciliyet yüksek ise yüksek öncelik belirle
5. Önem yüksek ve aciliyet düşük ise orta öncelik belirle
6. Önem düşük ve aciliyet yüksek ise orta öncelik belirle
7. Önem düşük ve aciliyet düşük ise düşük öncelik belirle
8. Öncelik seviyesini ekrana yazdır
9. Bitir
```

---

## 6. Sözde Kod 

```text
BAŞLA

önem değerini al
aciliyet değerini al

EĞER önem = "Yüksek" VE aciliyet = "Yüksek" İSE
    öncelik = "Yüksek"

DEĞİLSE EĞER önem = "Yüksek" VE aciliyet = "Düşük" İSE
    öncelik = "Orta"

DEĞİLSE EĞER önem = "Düşük" VE aciliyet = "Yüksek" İSE
    öncelik = "Orta"

DEĞİLSE
    öncelik = "Düşük"

öncelik değerini ekrana yazdır

BİTİR
```

---

## 7. Girdi → Koşullar → Çıktı

Algoritmanın genel yapısı:

```text
GİRDİ
↓
Önem seviyesi
Aciliyet seviyesi
↓
KOŞULLARI KONTROL ET
↓
Uygun kombinasyonu bul
↓
ÖNCELİK BELİRLE
↓
ÇIKTI
```

Örneğin:

```text
Önem = Yüksek
Aciliyet = Yüksek
        ↓
İki koşulu da kontrol et
        ↓
İkisi de doğru
        ↓
Yüksek Öncelik
```

---

## 8. "VE" Mantığı

```text
VE
```

"VE" kullanıldığında **iki koşulun da doğru olması** gerekir.

Örneğin:

```text
Önem = Yüksek
VE
Aciliyet = Yüksek
```

Bu iki koşuldan biri bile yanlışsa bu koşul sağlanmaz.

### Örnek

```text
Önem = Yüksek
Aciliyet = Yüksek
```

Sonuç:

```text
Doğru
```

Ancak:

```text
Önem = Yüksek
Aciliyet = Düşük
```

için:

```text
Yüksek VE Yüksek
```

koşulu sağlanmaz.

---

## 9. Farklı Durumların İncelenmesi

### Durum 1

```text
Önem = Yüksek
Aciliyet = Yüksek
```

Sonuç:

```text
Yüksek Öncelik
```

---

### Durum 2

```text
Önem = Yüksek
Aciliyet = Düşük
```

Sonuç:

```text
Orta Öncelik
```

---

### Durum 3

```text
Önem = Düşük
Aciliyet = Yüksek
```

Sonuç:

```text
Orta Öncelik
```

---

### Durum 4

```text
Önem = Düşük
Aciliyet = Düşük
```

Sonuç:

```text
Düşük Öncelik
```

---
