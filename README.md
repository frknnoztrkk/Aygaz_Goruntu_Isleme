Aygaz Görüntü İşleme Bootcamp Projesi

Proje Hedefi
Bu proje, Convolutional Neural Network (CNN) modelinin temellerini öğrenmek ve geliştirmek için tasarlanmıştır. Amacımız, belirli hayvan türlerini sınıflandırabilen bir model oluşturmak ve ardından modelin başarısını artırmak için çeşitli görsel manipülasyon tekniklerini uygulamaktır. Proje boyunca, modelin başarısını değerlendirmek ve sonuçları iyileştirmek için farklı test senaryoları üzerinde çalışılmıştır.

Proje Adımları
1. Veri Setinin Hazırlanması
Proje için kullanılan veri seti, Animals with Attributes 2 adını taşıyan bir koleksiyondan alınmıştır. Bu koleksiyon, 50 farklı hayvan türünü içermektedir, ancak biz yalnızca 10 sınıf üzerinde çalıştık. Bu sınıflar şunlardır:

-Collie
-Dolphin
-Elephant
-Fox
-Moose
-Rabbit
-Sheep
-Squirrel
-Giant Panda
-Polar Bear

Veri setindeki her sınıf için ilk 650 resim alınmış ve kullanılabilir veri seti oluşturulmuştur. Veriler, eğitim ve test verilerine ayrılmış ve her resim uygun boyuta getirilip normalize edilmiştir.

2. CNN Modelinin Tasarlanması
CNN modelinde, aşağıdaki katmanlar kullanılarak hayvan sınıflandırması yapılmıştır:

-Konvolüsyon Katmanları: Resimler üzerinde filtreleme yaparak özellikleri çıkaran temel katmanlardır.
-Aktivasyon Katmanları: ReLU fonksiyonu kullanılarak, modelin doğrusal olmayan özelliklerini öğrenmesi sağlanmıştır.
-Havuzlama Katmanları: Resimlerin boyutlarını küçültmek için kullanılmıştır.
-Fully Connected Katmanları: Modelin çıktıyı sınıflandırmak için kullanılan son katmanlardır.
-Dropout Katmanları: Aşırı öğrenmeyi engellemek için bu katman eklenmiştir.

3. Veri Augmentation (Veri Artırma)
Modelin genelleme yeteneğini artırmak için veri artırma teknikleri kullanılmıştır. Bu teknikler:

-Dönme (Rotation)
-Ölçekleme (Scaling)
-Yansıma (Flipping)
-Bulanıklaştırma (Blurring)
Yukarıdaki tekniklerle eğitim verisi çeşitlendirilerek, modelin farklı durumlarda da doğru tahmin yapabilmesi sağlanmıştır.

4. Modelin Test Edilmesi
Model eğitildikten sonra, test verisi üzerinde test edilmiştir. Başarı oranı, doğruluk (accuracy) ve kayıp (loss) gibi metriklerle izlenmiştir. Test sonuçlarına göre modelde optimizasyon yapılmış ve parametreler değiştirilmiştir.

5. Resim Manipülasyonu ve Renk Sabitliği
Test verileri üzerinde farklı ışık koşullarıyla manipülasyon yapılmıştır. Bu manipülasyonlar, modelin ışık değişimlerine karşı dayanıklılığını test etmek amacıyla uygulanmıştır. Ayrıca, manipüle edilmiş test verilerine renk sabitliği algoritması uygulanmıştır. Bu algoritma, bozuk renkleri düzelterek modelin daha doğru sonuçlar üretmesini hedeflemiştir.

6. Model Başarılarının Karşılaştırılması
Son olarak, modelin başarı oranları üç farklı test seti üzerinde karşılaştırılmıştır:

-Orijinal Test Seti
-Işık Manipülasyonu Yapılmış Test Seti
-Renk Sabitliği Uygulanan Test Seti
Her bir test setinin başarı oranları ölçülerek, farklı test koşullarında modelin performansı değerlendirilmiştir.

Kullanılan Kütüphaneler
-TensorFlow: Modelin eğitimi ve değerlendirilmesi için kullanıldı.
-OpenCV: Görüntü işleme işlemleri ve manipülasyonlar için kullanıldı.
-scikit-learn: Eğitim ve test veri setlerinin bölünmesi için kullanıldı.
-Matplotlib: Veri görselleştirmesi için kullanıldı.

Sonuçlar
Proje sonunda elde edilen başarı oranları şu şekildedir:

-Orijinal Test Seti Başarı Oranı: %61.92
-Işık Manipülasyonu Yapılmış Test Seti Başarı Oranı: %50.51
-Renk Sabitliği Uygulanan Test Seti Başarı Oranı: Modelin başarısı arttı, ancak daha fazla test yapılması gerekebilir.
