# HAVA DURUMU VERİ ANALİZİ PROJESİ
Bu proje,Python ve Pandas kullanarak şehir bazlı sıcaklık ve nem verilerinin analiz edilmesini amaçlamaktadır.
**Dosya adı:** `weather_data.csv`

### Kullanılan sütunlar:
- Date
- City
- Temperature (°C)
- Humidity

## 📊 Yapılan Analizler

### 1️⃣ Kütüphane ve Veri Yükleme
- Pandas ve NumPy kütüphaneleri import edildi
- CSV dosyası DataFrame’e yüklendi
- 
### 2️⃣ Veriyi Keşfetme
head() ile ilk 5 satır incelendi
tail() ile son 5 satır incelendi
describe() ile istatistiksel özet çıkarıldı
(ortalama, standart sapma, min–max değerler)

### 3️⃣ Sütun Seçimi
Date, City, Temperature sütunları seçildi
Şehir ve sıcaklık bilgileri birlikte görüntülendi

### 4️⃣ Filtreleme
Sıcaklık > 30°C olan kayıtlar
Sadece belirli bir şehre (ör. Bursa) ait veriler

### 5️⃣ Mantıksal Operatörler ile Filtreleme
İstanbul ve Nem > 60
Ankara veya Sıcaklık < 5
Sıcaklık < 10 veya Nem > 70

### 6️⃣ Sıralama
Sıcaklığa göre azalan sıralama
Neme göre azalan sıralama
Şehir adına göre alfabetik (artan) sıralama

### 7️⃣ Yeni Sütun Ekleme
Temperature_F: Fahrenheit cinsinden sıcaklık
(Temperature * 9/5) + 32
FeelsLike: Hissedilen sıcaklık
Temperature - (Humidity / 100)

### 8️⃣ Gruplama ve Analiz
Şehir başına kayıt sayısı
| City     |   Kayıt Sayısı |
|:---------|---------------:|
| Ankara   |             16 |
| Antalya  |             15 |
| Bursa    |             24 |
| İstanbul |             21 |
| İzmir    |             24 |
Şehir başına ortalama sıcaklık
| City     |   Ortalama Sıcaklık (°C) |
|:---------|-------------------------:|
| Ankara   |                 14.6376  |
| Antalya  |                  9.51096 |
| Bursa    |                 16.8927  |
| İstanbul |                 13.7152  |
| İzmir    |                 13.4592  |
Şehir bazlı özet istatistikler (groupby kullanılarak)
Şehir bazlı sıcaklık analizleri Excel dosyasına aktarıldı
Oluşturulan dosya: sehir_sicakliklari.xlsx
İçerik:
Ortalama sıcaklık
Maksimum sıcaklık
Minimum sıcaklık
Kayıt sayısı
| City     |   Ortalama_Sıcaklık |   Maksimum_Sıcaklık |   Minimum_Sıcaklık |   Kayıt_Sayısı |
|:---------|--------------------:|--------------------:|-------------------:|---------------:|
| Ankara   |            14.6376  |             34.8031 |          -2.45628  |             16 |
| Antalya  |             9.51096 |             33.9967 |          -1.66739  |             15 |
| Bursa    |            16.8927  |             34.5742 |          -0.828552 |             24 |
| İstanbul |            13.7152  |             32.5738 |          -3.34054  |             21 |
| İzmir    |            13.4592  |             31.6504 |          -3.80285  |             24 |

### 9️⃣ Verileri Dışa Aktarma (Export)
### ▶️ Notebook’u Çalıştırma
weather_analysis.ipynb dosyasını açın
Jupyter Notebook veya VS Code kullanın
Hücreleri sırasıyla çalıştırın (Ctrl + Enter)
Kod ve çıktıları birlikte inceleyin
