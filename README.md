# BTC Hareket Analizcisi

## Proje Amacı
Bu proje, 2018-2024 yılları arasında Bitcoin fiyat verilerini kullanarak zaman serilerindeki fiyat değişimlerini analiz etmeyi ve gelecekteki hareketleri tahmin etmeyi amaçlamaktadır. Bitcoin, dalgalı bir yapıya sahip olduğu için piyasa katılımcıları için fiyat hareketlerini anlamak büyük önem taşır. Proje kapsamında, fiyat hareketlerinin analiz edilmesi, belirli dönemlerde büyük fiyat değişimlerinin tespit edilmesi ve bu değişimlerin hacim ile ilişkisi incelenmiştir. Ayrıca, makine öğrenimi teknikleri ile fiyat trendlerinin tahmin edilmesi ve fiyatların hangi zaman dilimlerinde daha aktif olduğu belirlenmiştir.

## Veri Seti
Proje, Kaggle üzerinde yer alan Bitcoin Historical Datasets 2018-2024 veri setini kullanmaktadır. Bu veri seti, günlük, 4 saatlik, 1 saatlik ve 15 dakikalık zaman dilimlerinde fiyat hareketlerini, hacmi ve volatiliteyi içermektedir. Proje, kullanıcıdan girdi almaksızın yüklenen veriler üzerinden işlemlerini gerçekleştirir.

## Kullanılan Yöntemler

### Keşifsel Veri Analizi (EDA)
EDA, veri setinin genel istatistiksel özelliklerini incelemek ve fiyat hareketlerini anlamak amacıyla kullanıldı. Fiyat yüzdesel değişimleri histogram grafikleri ve korelasyon matrisleri aracılığıyla görselleştirildi. Bu sayede, fiyat değişikliklerinin dağılımı, veriler arasındaki ilişkiler ortaya konulmuştur.

### Hareketli Ortalamalar ve Volatilite
Zaman serisi analizinde kullanılan hareketli ortalamalar (7, 21 ve 50 periyotluk) ve volatilite hesaplamaları (20 periyotluk) kullanılarak, fiyatlardaki trendler ve dalgalanmalar incelendi. Hareketli ortalamalar, belirli bir dönemdeki ortalama fiyat hareketini gösterirken, volatilite, fiyatın bu dönemler içerisindeki dalgalanmasını ifade eder. Bu tekniklerle piyasadaki trendler daha net bir şekilde ortaya konulmuştur.

### Büyük Fiyat Hareketlerinin Tespiti
Yüzdesel fiyat değişimlerine dayalı eşik değerler belirlenerek (örneğin, günlük veriler için %5 ve üzeri), büyük fiyat hareketlerinin yaşandığı zaman dilimleri tespit edilmiştir. Bu tespitler sonucunda, hangi ay, gün ve saatte en büyük fiyat hareketlerinin yaşandığına dair istatistikler üretilmiştir. Bu bilgiler, piyasanın hangi zaman dilimlerinde daha volatil olduğunu anlamaya yönelik önemli bilgiler sağlamıştır.

### Lineer Regresyon ile Fiyat Tahmini
Hareketli ortalamalar ve volatilite gibi teknik göstergeler kullanılarak, lineer regresyon modeli ile fiyat trendleri tahmin edilmeye çalışılmıştır. Model, bağımlı değişken olarak fiyat yüzdesel değişimlerini ve bağımsız değişkenler olarak hareketli ortalamalar ve volatiliteyi kullanarak gelecekteki fiyat hareketlerini tahmin eder. Modelin başarısı, Mean Squared Error (MSE) ve R-Squared (R2) metrikleri ile değerlendirilmiştir.

### Gözetimsiz Öğrenme (K-Means Kümelemesi)
Bitcoin fiyatlarındaki yüzdesel değişimler üzerinde gözetimsiz öğrenme algoritması olan K-Means kümeleme kullanılmıştır. Bu yöntemle, fiyat değişimleri benzer davranışlara göre 3 kümeye ayrılarak, hangi dönemlerde benzer fiyat hareketlerinin gerçekleştiği incelenmiştir. K-Means kümeleme, etiketlenmemiş veriler üzerinden gerçekleştirilmiştir ve bu veriler gruplara ayrılarak benzerlikleri ortaya konmuştur. Gözetimsiz öğrenme, veri setinde etiketleme yapılmadan eğitilen bir model olduğu için, bu kısım özellikle Bitcoin fiyat hareketlerinin keşifsel analizi açısından önem taşımaktadır.

## Sonuç
Bu proje kapsamında, Bitcoin fiyatlarındaki dalgalanmalar, büyük hareketler ve fiyat tahminleri incelenmiş ve makine öğrenimi modelleri ile analiz edilmiştir. Keşifsel veri analizi ile fiyat hareketlerinin dağılımı ve korelasyonları ortaya konulmuş, lineer regresyon modeli ile fiyat tahminleri gerçekleştirilmiştir. Ayrıca, gözetimsiz öğrenme yöntemi olan K-Means ile fiyat hareketleri kümelere ayrılmıştır. Bu proje, finansal piyasalarda fiyat hareketlerinin anlaşılmasına yönelik güçlü bir araç sunarak gelecekteki olası hareketleri daha iyi tahmin etme potansiyeline sahiptir.

## Kaggle Linki
Projenin Kaggle'daki versiyonuna aşağıdaki linkten ulaşabilirsiniz:

Kaggle: BTC Hareket Analizcisi (https://www.kaggle.com/code/emrekonce/btc-hareket-analizcisi)
