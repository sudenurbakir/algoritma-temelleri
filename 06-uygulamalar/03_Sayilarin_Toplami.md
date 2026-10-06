# Sayıların Toplamı

Bu uygulamada kullanıcıdan birden fazla sayı alıp bu sayıların toplamını hesaplayan bir algoritma oluşturacağız.

Bu uygulamanın amacı, daha önce öğrendiğimiz **döngüleri** gerçek bir problem üzerinde kullanmayı görmektir.

---

## 1. Problem

Kullanıcıdan **5 tane sayı** alınacak.

Program bu sayıların toplamını hesaplayacak ve sonucu ekrana yazdıracak.

Örneğin:

```text
10
20
5
15
30
```

Bu sayıların toplamı:

```text
80
```

olur.

---

## 2. Girdi - İşlem - Çıktı

### Girdi

Kullanıcıdan 5 adet sayı alınır.

### İşlem

Alınan sayılar tek tek toplama eklenir.

### Çıktı

Sayıların toplamı ekrana yazdırılır.

---

## 3. Burada Yeni Olan Ne?

Daha önce şöyle bir işlem yapmıştık:

```text
toplam = 10 + 20 + 5 + 15 + 30
```

Ama sayıların kaç tane olduğunu önceden bilmediğimiz veya çok fazla sayı olduğu durumlarda her sayıyı tek tek yazmak pratik değildir.

Burada **döngü** kullanabiliriz.

Mantık:

```text
Başlangıçta toplam = 0

1. sayıyı al → toplama ekle
2. sayıyı al → toplama ekle
3. sayıyı al → toplama ekle
4. sayıyı al → toplama ekle
5. sayıyı al → toplama ekle

Son toplamı yazdır
```

---

## 4. Toplam Değişkeni

Burada önemli bir kavram var:

```text
toplam
```

Bu değişken, o ana kadar elde ettiğimiz toplam değeri tutar.

Başlangıçta:

```text
toplam = 0
```

olsun.

İlk sayı 10 ise:

```text
toplam = 0 + 10
toplam = 10
```

İkinci sayı 20 ise:

```text
toplam = 10 + 20
toplam = 30
```

Üçüncü sayı 5 ise:

```text
toplam = 30 + 5
toplam = 35
```

Bu şekilde devam eder.

Buradaki **30, 35 gibi değerler ara sonuçlardır.**

En sonunda:

```text
toplam = 80
```

olur.

---

## 5. Algoritmanın Adımları

1. Başla.
2. Toplam değişkenini 0 olarak başlat.
3. 5 kez tekrarla:

   * Kullanıcıdan bir sayı al.
   * Aldığın sayıyı toplama ekle.
4. Toplamı ekrana yazdır.
5. Bitir.

---

## 6. Sözde Kod 

```text
BAŞLA

    toplam = 0

    5 KEZ TEKRARLA
        sayıyı al
        toplam = toplam + sayı

    toplamı yazdır

BİTİR
```

---


