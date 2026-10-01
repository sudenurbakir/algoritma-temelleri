# Algoritmik Düşünce ve Programlama Temelleri

## 1. Algoritmik Düşünce Nedir?

Algoritmik düşünce, bir problemi çözmek için gerekli işlemleri belirlemek, problemi küçük parçalara ayırmak ve bu işlemleri doğru bir sıra içerisinde gerçekleştirmektir.

Algoritmik düşünmede amaç yalnızca bir sonuca ulaşmak değildir. Önemli olan, sonuca nasıl ulaşacağımızı sistematik bir şekilde belirlemektir.

Bir problemi çözerken kendimize şu soruları sorabiliriz:

* Problem nedir?
* Benden ne isteniyor?
* Hangi bilgilere ihtiyacım var?
* Bu bilgiler üzerinde hangi işlemleri yapmalıyım?
* İşlemleri hangi sırayla gerçekleştirmeliyim?
* Sonuç olarak ne elde etmeliyim?

Bu sorular, problemi adım adım düşünmemize yardımcı olur.

---

## 2. Problemi Parçalara Ayırmak

Algoritmik düşünmenin önemli aşamalarından biri, büyük bir problemi daha küçük parçalara ayırmaktır.

Örneğin:

> Bir kişinin yaşını hesaplayan bir program oluşturulması isteniyor.

Problemi doğrudan çözmeye çalışmak yerine şu şekilde parçalayabiliriz:

1. Kullanıcının doğum yılını al.
2. İçinde bulunulan yılı belirle.
3. Bulunulan yıldan doğum yılını çıkar.
4. Sonucu yaş olarak göster.

Böylece başlangıçta tek bir problem olarak gördüğümüz işlem, dört küçük adıma ayrılmış olur.

---

## 3. Girdi, İşlem ve Çıktı

Bir algoritmayı anlamanın en kolay yollarından biri problemi üç temel bölüme ayırmaktır:

### Girdi (Input)

Algoritmanın çalışması için ihtiyaç duyduğu bilgilerdir.

Örneğin yaş hesaplama probleminde:

```text
Doğum yılı
```

bir girdidir.

### İşlem (Process)

Girilen bilgiler üzerinde gerçekleştirilen işlemlerdir.

Yaş hesaplama örneğinde:

```text
Bulunulan yıl - doğum yılı
```

işlemdir.

### Çıktı (Output)

Algoritmanın işlem sonucunda ürettiği bilgidir.

Örneğin:

```text
Kişinin yaşı: 26
```

çıktıdır.

Temel yapı:

```text
GİRDİ
   ↓
İŞLEM
   ↓
ÇIKTI
```

---

## 4. Örnek: Doğum Yılına Göre Yaş Hesaplama

### Problem

Kullanıcının doğum yılı alınarak yaşının hesaplanması istenmektedir.

### Girdi

```text
Doğum yılı
Bulunulan yıl
```

### İşlem

```text
Yaş = Bulunulan yıl - Doğum yılı
```

### Çıktı

```text
Hesaplanan yaş
```

### Algoritma

```text
BAŞLA

Bulunulan yılı belirle.
Kullanıcının doğum yılını al.
Bulunulan yıldan doğum yılını çıkar.
Sonucu ekrana yazdır.

BİTİR
```

### Örnek

```text
Doğum yılı: 2000
Bulunulan yıl: 2026

2026 - 2000 = 26
```

Çıktı:

```text
Yaşınız: 26
```

> Not: Gerçek bir yaş hesabında kişinin doğum günü ve ayı da dikkate alınabilir. Bu örnekte algoritmanın temel mantığını öğrenmek amacıyla yalnızca yıl üzerinden hesaplama yapılmıştır.

---

# 5. Algoritmik Düşünmede İşlem Sırası

Bir algoritmada işlemlerin doğru sırada olması önemlidir.

Örneğin yaş hesaplama algoritmasında:

```text
1. Doğum yılını al.
2. Bulunulan yılı belirle.
3. İki yıl arasındaki farkı hesapla.
4. Sonucu göster.
```

işlemleri mantıklı bir sıradadır.

Ancak şöyle bir sıralama oluşturursak:

```text
1. Sonucu ekrana yazdır.
2. Doğum yılını al.
3. Yaş hesapla.
```

algoritma doğru şekilde çalışamaz.

Bu nedenle algoritma oluştururken yalnızca **hangi işlemlerin yapılacağını değil, hangi sırayla yapılacağını da** düşünmek gerekir.

---

# 6. Değişken Nedir?

Algoritmalarda işlem sırasında farklı bilgileri saklamamız gerekebilir.

Bu bilgileri tutmak için **değişkenler** kullanılır.

Örneğin:

```text
dogum_yili = 2000
bulunulan_yil = 2026
yas = 26
```

Burada:

* `dogum_yili` → doğum yılını tutar.
* `bulunulan_yil` → içinde bulunulan yılı tutar.
* `yas` → hesaplanan yaş bilgisini tutar.

Değişkenleri, program içerisinde bilgi saklayan alanlar olarak düşünebiliriz.

---

# 7. Değişkenlerle Basit Bir Algoritma

Örneğin bir ürünün toplam fiyatını hesaplayalım.

Ürün fiyatı:

```text
250 TL
```

Ürün adedi:

```text
3
```

Algoritma:

```text
BAŞLA

urun_fiyati = 250
urun_adedi = 3

toplam_tutar = urun_fiyati * urun_adedi

toplam_tutarı ekrana yazdır

BİTİR
```

Sonuç:

```text
250 × 3 = 750 TL
```

Burada üç farklı bilgi kullanılmıştır:

```text
urun_fiyati
urun_adedi
toplam_tutar
```

---

# 8. Algoritmik Düşüncede Problem Analizi

Bir problemi çözmeye başlamadan önce problemi anlamamız gerekir.

Örneğin:

> Bir öğrencinin üç sınav notunun ortalamasını hesaplayan algoritmayı oluşturun.

Problemi şu şekilde analiz edebiliriz.

### Girdi

```text
1. sınav notu
2. sınav notu
3. sınav notu
```

### İşlem

Öncelikle notları toplarız.

```text
toplam = not1 + not2 + not3
```

Daha sonra toplamı sınav sayısına böleriz.

```text
ortalama = toplam / 3
```

### Çıktı

```text
Öğrencinin sınav ortalaması
```

### Algoritma

```text
BAŞLA

1. sınav notunu al.
2. sınav notunu al.
3. sınav notunu al.

Notları topla.
Toplamı 3'e böl.

Ortalama değerini ekrana yazdır.

BİTİR
```

---

# 9. Bir Problemi Çözerken Kullanılabilecek Genel Yaklaşım

Yeni bir problemle karşılaştığımızda aşağıdaki sırayı kullanabiliriz:

### 1. Problemi tanımla

Benden ne isteniyor?

### 2. Girdileri belirle

Hangi bilgilere ihtiyacım var?

### 3. İşlemleri belirle

Bu bilgiler üzerinde ne yapacağım?

### 4. İşlem sırasını oluştur

Hangi işlem önce, hangisi sonra yapılmalı?

### 5. Çıktıyı belirle

Sonuç olarak ne göstermeliyim?

### 6. Çözümü kontrol et

Oluşturduğum algoritma doğru sonucu veriyor mu?

Bu yaklaşım, farklı problemlerde tekrar tekrar kullanılabilir.

---

# 10. Algoritmik Düşünme Örnekleri

Algoritmik düşünceyi geliştirmek için günlük hayattaki işlemleri bile algoritma olarak düşünebiliriz.

### Örnek: Çay hazırlamak

```text
BAŞLA

Su koy.
Suyu kaynat.
Bardağa çay koy.
Sıcak suyu ekle.
Şeker ekle.
Karıştır.

BİTİR
```

### Örnek: ATM'den para çekmek

```text
BAŞLA

Kartı ATM'ye yerleştir.
Şifreyi gir.
Para çekme işlemini seç.
Çekilecek tutarı gir.
Hesap bakiyesini kontrol et.
Para çekme işlemini gerçekleştir.
Kartı al.

BİTİR
```

Burada henüz koşulları detaylandırmadık.

Örneğin:

> Bakiye yeterli değilse ne olacak?

sorusunu ilerleyen derste **koşul ifadeleri** ile ele alacağız.

---

# 11. Algoritmik Düşünmenin Temel Özellikleri

İyi hazırlanmış bir algoritmanın:

* Açık olması,
* Adımlarının anlaşılır olması,
* İşlemlerin doğru sırada olması,
* Girdilerinin belirli olması,
* Beklenen bir çıktı üretmesi,
* Gereksiz adımlar içermemesi,
* Farklı durumlar için gerektiğinde geliştirilebilir olması

beklenir.

Algoritma oluştururken amacımız problemi gereksiz şekilde karmaşıklaştırmak değil, çözümü mümkün olduğunca anlaşılır ve sistematik hâle getirmektir.

---

# 12. Algoritmik Düşünce ve Programlama

Algoritma ile programlama aynı şey değildir.

**Algoritma**, problemin nasıl çözüleceğini ve hangi adımların izleneceğini açıklar.

**Programlama** ise bu çözümün bir programlama dili kullanılarak bilgisayar tarafından uygulanabilir hâle getirilmesidir.

Örneğin:

```text
Algoritma
↓
Doğum yılını al
↓
Bulunulan yıldan çıkar
↓
Sonucu göster
```

Bu algoritma daha sonra Python, C#, Java gibi farklı programlama dilleriyle kodlanabilir.

Bu nedenle öncelikle problemin çözüm mantığını anlamak, ardından bunu bir programlama diline aktarmak önemlidir.

---

# 13. Genel Özet

Algoritmik düşünce, problemlere sistematik bir şekilde yaklaşmamızı sağlar.

Bir problemle karşılaştığımızda:

```text
PROBLEMİ ANLA
      ↓
GİRDİLERİ BELİRLE
      ↓
İŞLEMLERİ BELİRLE
      ↓
İŞLEM SIRASINI OLUŞTUR
      ↓
ÇIKTIYI BELİRLE
      ↓
SONUCU KONTROL ET
```


