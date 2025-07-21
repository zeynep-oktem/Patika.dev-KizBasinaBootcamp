# Proje Linki 

https://drive.google.com/file/d/12FyBq8W97Ig7yZrSwFv6-oBgYujrOrlP/view?usp=drive_link

# 📊 E-Ticaret Analiz Raporu

Bu proje, bir e-ticaret veri seti üzerinden satış analizlerini görselleştirmek için hazırlanmıştır. Rapor, Power BI kullanılarak oluşturulmuş ve müşteri, kategori, bölge bazlı analizler yapılmıştır.

---

## ✅ İçerik

### **Özet Sayfa**
- Toplam ciro, sipariş ve müşteri sayısı
- Haftaiçi/haftasonu satış dağılımı
- Saatlik satış tutarları
- Bölgelere göre satış adetleri

### **Müşteri Perspektifi**
- Tekil müşteri sayısı (kart)
- Kadın ve erkek müşteri sayısı (kart)
- Yaş gruplarına göre satış analizi (0-20 Genç, 20-35 Yetişkin, 35-55 Orta Yaş, 55+ Yaşlı)
- İstanbul’daki top 10 müşteri (tablo)
- Bölgelere göre müşteri sayısı (grafik)

### **Kategori Perspektifi**
- İstanbul’da yaşayan **genç** müşteri cirosu
- Kategorilere göre ağaç haritası

### **Ekstra**
- Bölgelere göre müşteri dağılımı haritası
- Saatlik ve haftaiçi/haftasonu satış grafikleri

---

## ✅ Kullanılan Teknolojiler
- **Power BI Desktop**
- **DAX** ile hesaplamalar ve ölçüler
- **Koşullu sütunlar** ve veri modelleme
- Power Query ile veri dönüştürme

---

## ✅ Yapılan Adımlar

### **1. Users Tablosu**
- Users tablosu Power BI’a yüklendi.
- Tablo adı **Kullanıcılar** olarak değiştirildi.
- `Birthdate` kolonu tarih formatına çevrildi.
- `DATEDIFF` fonksiyonu ile yaş hesaplandı.
- `Gender` kolonundan **E → ERKEK, K → KADIN** şeklinde koşullu sütun oluşturuldu.
- `Namesurname` kolonundan ad ve soyad ayrı sütunlara bölündü.
- `CREATEDDATE` ve `TELNR2` kolonları kaldırıldı.
- `PASSWORD_` kolonunun değerleri büyük harfe çevrildi.
---

### **2. Adres Tablosu**
- Tablo adı **Adres** olarak değiştirildi.
- Veri tipleri kontrol edildi.
- USERID ve CITY kolonları birleştirildi.

---

### **3. Items Tablosu**
- Tablo adı **Ürünler** olarak değiştirildi.
- `Category1 → ANAKATEGORI`, `Category2 → USTKATEGORI`, `Category3 → ALTKATEGORI`, `Category4 → ENALTKATEGORI` olarak yeniden adlandırıldı.
- Yeni bir koşullu sütun eklendi: Eğer ANAKATEGORI “SOGUKICECEKLER”, “CAY-KAHVE-SEKER”, “SICAK ICECEKLER” ise **ICECEKLER**, değilse mevcut ANAKATEGORI korundu.

---

### **4. OrderDetail Tablosu**
- Tablo adı **SiparisDetay** olarak değiştirildi.
- Tüm kolonların sayısal formatta olduğu kontrol edildi.

---

### **5. Orders Tablosu**
- Tablo adı **Siparis** olarak değiştirildi.
- `Date_` hariç tüm kolonlar sayısal formata getirildi.
- `Date_` kolonu çoğaltılıp saat bilgisi kaldırılarak sadece tarih formatına çevrildi.

---

### **6. Modelleme**
- Adres.ID → Siparis.ADRESSID
- Kullanıcılar.ID → Siparis.USERID
- Siparis.ID → SiparisDetay.ORDERID
- Ürünler.ID → SiparisDetay.ITEMID  
ilişkileri kuruldu.
- Kullanıcıların görmesini istemediğimiz teknik kolonlar gizlendi.

---

### **7. Bölgeler**
- İnternetten bölgeler ve şehirler tablosu eklendi.
- İlk satır kolon adı olarak ayarlandı.
- Tablo adı **Bölgeler** olarak değiştirildi.
- İl kolonları büyük harfe çevrildi ve Adres tablosundaki CITY ile eşleştirildi.

---

### **3 Perspektif Raporlama**
- **Özet Sayfa:** Haftasonu/haftaiçi satış grafiği, bölgelere göre satış grafiği, saatlik satış grafiği ve toplam metrikleri kart olarak gösterildi.
- **Müşteri Perspektifi:** Tekil müşteri, kadın/erkek müşteri sayıları, yaş grubuna göre satış grafiği ve İstanbul’daki top 10 müşteri tablosu oluşturuldu.
- **Kategori Perspektifi:** İstanbul’da yaşayan genç müşterilerin kategorilere göre cirosu ağaç haritasında gösterildi.

---

## ✅ Ölçüler
- Toplam Satış Adeti
- Toplam Ciro
- Toplam Müşteri Sayısı
- Toplam Sipariş Sayısı
- Haftasonu/Haftaiçi Satış
- Saatlik Satış
- Müşteri başına ciro
- Müşteri başına adet
- Ortalama sipariş tutarı

---

## ✅ Veri Yenileme
Bu raporda kullanılan veri seti **11 Temmuz’a kadar geçerli** en güncel veridir. Veri haftalık olarak yenilenebilir.

---

## 📷 Görseller
> Rapor sayfalarının ekran görüntüleri buraya eklenebilir:
> ![Giriş](C:\Users\zeyne\Desktop\Proje-2\img\img0.png)
> ![Özet Sayfa](C:\Users\zeyne\Desktop\Proje-2\img\img1.png)  
> ![Müşteri Perspektifi](C:\Users\zeyne\Desktop\Proje-2\img\img2.png)  
> ![Kategori Perspektifi](C:\Users\zeyne\Desktop\Proje-2\img\img3.png)  

---

## 📝 Nasıl Açılır?
Bu raporu açmak için **Power BI Desktop** kullanabilirsiniz.  

