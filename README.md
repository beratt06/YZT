🎬 IMDb Film Veri Seti Analizi
Bu proje, bir IMDb film veri setini (movies_initial.csv) kullanarak temel veri temizleme, keşifsel veri analizi (EDA) ve görselleştirme adımlarını içerir. Analiz, pandas, numpy ve matplotlib kütüphaneleri kullanılarak gerçekleştirilmiştir.

Kullanılan Kütüphaneler
Pandas: Veri yükleme, temizleme ve manipülasyonu için.

NumPy: Sayısal hesaplamalar ve veri yapıları için.

Matplotlib: Veri görselleştirmesi için.

🛠️ Proje Adımları
Proje, 3 ana aşamadan oluşmaktadır:

1. Aşama: Veri Yükleme ve Hazırlık
movies_initial.csv dosyası yüklendi.

Yalnızca analiz için gerekli olan sütunlar (imdbID, title, director, genre, imdbRating, imdbVotes) seçildi.

Veri tipleri (object -> string, diğerleri -> float64) dönüştürüldü.

Eksik veriler (NaN) yönetildi:

Sayısal sütunlar (örn: imdbRating) ortalama değer ile dolduruldu.

Metinsel sütunlar (örn: director) "Unknown" string'i ile dolduruldu.

2. Aşama: Keşifsel Veri Analizi (EDA)
Veri setinin genel yapısını anlamak için data.head(), data.info() ve data.describe() gibi temel analiz fonksiyonları kullanıldı.

3. Aşama: Veri Görselleştirme
Analiz bulgularını görselleştirmek için Matplotlib kullanıldı.

📊 Analiz Görselleri
Proje kapsamında oluşturulan temel analiz grafikleri:

1. IMDb Puanı ve Oy Sayısı İlişkisi
Bu scatter plot (dağılım grafiği), filmlerin aldığı oy sayısı (X ekseni, logaritmik ölçekte) ile IMDb puanı (Y ekseni) arasındaki ilişkiyi gösterir. Genellikle oy sayısı arttıkça puanda da bir istikrar veya artış olup olmadığını görmek için kullanılır.

Buraya 1. ekran görüntünü ekle: ![IMDb Puan vs Oy Sayısı](path/to/screenshot-scatter-plot.png)

2. IMDb Puan Dağılımı (Histogram)
Bu histogram, veri setindeki filmlerin IMDb puanlarının genel dağılımını (frekansını) gösterir. Hangi puan aralığında daha fazla film yığıldığını net bir şekilde ortaya koyar.

Buraya 2. ekran görüntünü ekle: ![IMDb Puan Dağılımı](path/to/screenshot-histogram.png)

🚀 Nasıl Çalıştırılır?
Repoyu klonlayın veya dosyaları indirin.

Gerekli kütüphaneleri yükleyin:

Bash

pip install pandas numpy matplotlib
movies_initial.csv veri setinin script dosyasıyla aynı dizinde olduğundan emin olun.

Script'i çalıştırın:

Bash

python "yzt (3).py"
(Script'in adını analyze.py gibi daha temiz bir adla değiştirirsen, python analyze.py olarak çalıştırabilirsin.)
