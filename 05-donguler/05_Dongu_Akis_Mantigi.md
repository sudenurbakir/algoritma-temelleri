# Döngü Akış Mantığı

## 1. Döngü Akış Mantığı Nedir?

Döngü akış mantığı, bir döngünün başlangıçtan bitişe kadar hangi adımları izlediğini anlamamızı sağlar.

Bir döngü yalnızca işlemleri tekrar etmez. Aynı zamanda:

1. Başlar.
2. Koşulu kontrol eder.
3. İşlemi gerçekleştirir.
4. Değeri değiştirir.
5. Koşulu tekrar kontrol eder.
6. Koşul yanlış olduğunda sona erer.

Bu sıralamayı anlamak, döngüleri doğru kullanabilmek için önemlidir.

---

## 2. Basit Bir Döngünün Akışı

1'den 5'e kadar sayıları yazdıran bir döngüyü inceleyelim.

```text 
       BAŞLA
          |
          v
      sayaç = 1
          |
          v
     sayaç <= 5 ?
       /      \
    Evet      Hayır
      |          |
      v          v
  Sayıyı yazdır  BİTİR
      |
      v
  sayaç = sayaç + 1
      |
      └───────────────┐
                      |
                      v
                Koşulu tekrar
                   kontrol et
```

Burada döngü, koşul yanlış olana kadar aynı akışı tekrarlar.

---

## 3. Döngünün Adım Adım Çalışması

Örneğimizde başlangıç değeri 1'dir.

### 1. Tekrar

```text
sayaç = 1
```

Koşul:

```text
1 <= 5 → Doğru
```

İşlem:

```text
1 yazdır
```

Sayaç artırılır:

```text
sayaç = 2
```

### 2. Tekrar

```text
2 <= 5 → Doğru
```

```text
2 yazdır
```

Sayaç:

```text
3
```

### 3. Tekrar

```text
3 <= 5 → Doğru
```

```text
3 yazdır
```

Sayaç:

```text
4
```

### 4. Tekrar

```text
4 <= 5 → Doğru
```

```text
4 yazdır
```

Sayaç:

```text
5
```

### 5. Tekrar

```text
5 <= 5 → Doğru
```

```text
5 yazdır
```

Sayaç:

```text
6
```

### Son kontrol

```text
6 <= 5 → Yanlış
```

Koşul yanlış olduğu için döngü sona erer.

---

## 4. Döngünün Bitiş Noktası

Bir döngünün mutlaka bir noktada sona ermesi gerekir.

Örneğimizde:

```text
sayaç <= 5
```

koşulu kullanılmıştır.

Sayaç her tekrarda 1 artırıldığı için sonunda 5'ten büyük olur.

Bu durumda:

```text
koşul = yanlış
```

olur ve döngü sona erer.

Bu nedenle döngü oluştururken şu soruyu sormak önemlidir:

> **Döngünün sona ermesini sağlayacak durum nedir?**

---

## 5. Sonsuz Döngü Nasıl Oluşur?

Eğer döngünün koşulu hiçbir zaman yanlış hale gelmezse döngü sonsuza kadar devam edebilir.

Örneğin:

```text
BAŞLA

    sayaç = 1

    sayaç <= 5 OLDUĞU SÜRECE

        sayacı yazdır

BİTİR
```

Burada sayaç hiçbir zaman artırılmadığı için sürekli:

```text
1 <= 5
```

olur.

Sonuç olarak döngü:

```text
1
1
1
1
1
...
```

şeklinde devam eder.

Bu nedenle döngülerde **bitiş koşulunun nasıl sağlanacağı** mutlaka düşünülmelidir.

---

## 6. For ve While Akışının Karşılaştırılması

### For Döngüsü

Genel mantık:

```text
Başlangıç
   ↓
Koşulu kontrol et
   ↓
İşlemi gerçekleştir
   ↓
Artır / azalt
   ↓
Koşulu tekrar kontrol et
   ↓
Koşul yanlış → BİTİR
```

### While Döngüsü

Genel mantık:

```text
Başlangıç
   ↓
Koşulu kontrol et
   ↓
Doğru mu?
  /   \
Evet  Hayır
 ↓      ↓
İşlem  BİTİR
 ↓
Koşulu etkileyen değeri değiştir
 ↓
Koşulu tekrar kontrol et
```

İki döngünün temelinde de koşul kontrolü ve tekrar mantığı bulunur.

---

## 7. Döngü Akışında Dikkat Edilmesi Gerekenler

Bir döngü oluştururken şu sorulara cevap vermek faydalıdır:

1. Döngü nereden başlayacak?
2. Hangi koşula göre devam edecek?
3. Her tekrarda hangi işlem yapılacak?
4. Her tekrarda hangi değer değişecek?
5. Döngü ne zaman sona erecek?
6. Döngünün sonsuz hâle gelme ihtimali var mı?

Bu sorular, döngünün mantığını kurmamıza yardımcı olur.

---

## 8. Kısa Özet

* Döngü belirli bir akışı tekrar eder.
* Koşul, döngünün devam edip etmeyeceğini belirler.
* Her tekrarın sonunda döngüyü etkileyen değer değişebilir.
* Koşul yanlış olduğunda döngü sona erer.
* Bitiş koşulu doğru oluşturulmazsa sonsuz döngü oluşabilir.
* For ve while döngülerinin çalışma biçimleri farklı olsa da temelinde tekrar ve koşul mantığı vardır.

**NOT:**

> **Döngünün en önemli sorusu: "Ne zaman duracağım?"**

Bir döngüyü oluştururken yalnızca tekrar eden işlemi değil, **o tekrarın ne zaman sona ereceğini de** düşünmeliyiz.
