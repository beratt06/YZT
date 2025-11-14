# 🎬 IMDb Film Analizi Projesi

Bu proje, IMDb film verileri üzerinde veri temizleme, keşifsel veri analizi (EDA) ve veri görselleştirme işlemleri yapan bir Python çalışmasıdır. Pandas, NumPy ve Matplotlib kütüphaneleri kullanılmıştır.

# 📌 Proje Amaçları

Bu projenin temel hedefleri:

IMDb film verilerini yüklemek ve düzenlemek

Eksik verileri doğru yöntemlerle doldurmak

Veri seti üzerinde temel istatistiksel özetler oluşturmak

IMDb puanı ile oy sayısı arasındaki ilişkiyi incelemek

Grafiklerle veri dağılımını analiz etmek


# 📂 Veri Seti

Projede kullanılan veri dosyası: movies_initial.csv

Kullanılan kolonlar:

imdbID

title

director

genre

imdbRating

imdbVotes

# 🧹 Aşama 1: Veri Hazırlama
✔ Veri Yükleme
data = pd.read_csv('movies_initial.csv')

✔ Sütun Seçimi
Analiz için gerekli sütunlar filtrelendi.

✔ Veri Tipi Dönüşümü

Metinsel veriler → string

Sayısal veriler → float64

✔ Eksik Veri Temizleme

Sayısal boşluklar → ortalama değer ile dolduruldu

Metinsel boşluklar → "Unknown" değeri ile dolduruldu

# 📊 Aşama 2: Keşifsel Veri Analizi (EDA)

Bu bölümde:

data.describe().T ile özet istatistikler çıkarıldı

Veri tipleri (dtypes) incelendi

Veri seti şekli (shape) analiz edildi

data.info() ile genel yapı kontrol edildi

# 📈 Aşama 3: Veri Görselleştirme

<img width="960" height="747" alt="Ekran görüntüsü 2025-11-15 004200" src="https://github.com/user-attachments/assets/0e84c681-9291-464b-8c68-46a431b0d44b" />

🎯 1. IMDb Puan Dağılımı Histogram
plt.figure(figsize=(10, 6))
plt.hist(data['imdbRating'].dropna(), bins=30, color='skyblue', edgecolor='black')
plt.title('IMDb Puanlarının Dağılımı (Histogram)')
plt.xlabel('IMDb Puanı')
plt.ylabel('Film Sayısı (Frekans)')
plt.grid(axis='y', linestyle='--', alpha=0.7)
plt.show()

🚀 Nasıl Çalıştırılır?

Depoyu klonlayın:

git clone <repo-url>


Gerekli kütüphaneleri yükleyin:

pip install pandas numpy matplotlib


Python dosyasını çalıştırın:

python yzt.py


movies_initial.csv dosyasının aynı klasörde olduğundan emin olun.

📘 Lisans

Bu proje eğitim amaçlıdır ve serbestçe kullanılabilir.
