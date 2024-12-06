
House Price Prediction
# California Housing Price Prediction Project

## Proje Amacı
Bu projenin amacı, Kaliforniya'daki ev fiyatlarını tahmin etmek için bir makine öğrenmesi modeli geliştirmektir. Model, Kaliforniya'daki her blok grubu için nüfus, ortalama gelir ve ortalama ev fiyatları gibi özellikleri kullanarak ev fiyatlarını tahmin edecektir. Bu tahminler, emlak piyasası analizleri, yatırım kararları ve bölgesel ekonomik planlama için kullanılabilir.

## Kullanılacak Teknolojiler ve Adımlar
Proje, aşağıdaki teknolojiler ve adımlarla gerçekleştirilecektir:

### Teknolojiler
- Python 3.x
- Google Colab
- Pandas
- NumPy
- Scikit-learn
- Matplotlib
- Seaborn
- Git ve GitHub

### Adımlar
1. **Veri Toplama**: Kaliforniya Nüfus Sayımı verilerini `housing.csv` dosyasından yüklemek.
2. **Veri Keşfi ve Analizi**: Verilerin genel yapısını ve istatistiklerini incelemek.
3. **Veri Temizleme**: Eksik verileri doldurmak veya kaldırmak, veri türlerini düzeltmek.
4. **Özellik Mühendisliği**: Yeni özellikler oluşturmak ve mevcut özellikleri dönüştürmek.
5. **Veri Görselleştirme**: Veri dağılımını ve ilişkilerini görselleştirmek.
6. **Veri Bölme**: Veriyi eğitim ve test setlerine ayırmak.
7. **Model Eğitimi**: Farklı makine öğrenmesi algoritmaları ile modelleri eğitmek.
8. **Model Değerlendirme**: Modelleri performans metrikleri ile değerlendirmek ve karşılaştırmak.
9. **Model İyileştirme**: Model performansını artırmak için hiperparametre optimizasyonu yapmak.
10. **Sonuçları Paylaşma**: Model sonuçlarını ve bulguları raporlamak.

## Veri Seti
Veri seti, Kaliforniya Nüfus Sayımı'ndan alınmıştır ve aşağıdaki özellikleri içermektedir:
- `longitude`: Boylam bilgisi
- `latitude`: Enlem bilgisi
- `housing_median_age`: Evlerin medyan yaşı
- `total_rooms`: Toplam oda sayısı
- `total_bedrooms`: Toplam yatak odası sayısı
- `population`: Nüfus
- `households`: Hane sayısı
- `median_income`: Medyan gelir
- `median_house_value`: Medyan ev fiyatı

## Proje Adımları
1. **Gereksinimleri Yükleyin**:
   ```bash
   !pip install pandas numpy scikit-learn matplotlib seaborn
   
2.Veri Setini Yükleyin:

python
import pandas as pd
housing = pd.read_csv("housing.csv")

3.Veri Keşfi ve Analizi:

python
housing.head()
housing.describe()
housing.info()
4.Veri Temizleme:

python
housing = housing.dropna(subset=["total_bedrooms"])  # Eksik değerleri kaldırma örneği

5.Özellik Mühendisliği ve Görselleştirme:

python
import matplotlib.pyplot as plt
housing.hist(bins=50, figsize=(20,15))
plt.show()

6.Veri Bölme ve Model Eğitimi:

python
from sklearn.model_selection import train_test_split
train_set, test_set = train_test_split(housing, test_size=0.2, random_state=42)

7.Model Değerlendirme ve İyileştirme:

python
from sklearn.linear_model import LinearRegression
model = LinearRegression()
model.fit(train_set.drop("median_house_value", axis=1), train_set["median_house_value"])

8.Sonuçları Paylaşma: Model performansını değerlendirin ve sonuçları raporlayın.

Katkıda Bulunanlar
Selcen Bilek

Lisans
Bu proje MIT lisansı altında lisanslanmıştır - ayrıntılar için LICENSE dosyasına bakın.


Bu `README.md` dosyası, projenizin amacını, kullanılacak teknolojileri, veri setini ve proje adımlarını özetlemektedir. 



