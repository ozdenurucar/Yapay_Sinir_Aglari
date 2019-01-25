## Yapay Sinir Ağları

Yapay sinir ağları (YSA) insan beyninden esinlenmiştir.
Öğrenme sürecinin matematiksel olarak modellenmesi temeline dayanmaktadır.
YSA çalışmaları ilk olarak beynin biyolojik üniteleri olan nöronların modellenmesi ile başlamıştır. 
Günümüzde ise pek çok alanda uygulanmaktadır. 

Dış ortamdan veya diğer hücrelerden alınan girdiler, ağırlıklar yardımıyla hücreye bağlanır. Toplama fonksiyonu ile net girdi hesaplanır. Net girdinin aktivasyon fonksiyonundan geçirilmesiyle net çıktı hesaplanır. Bu işlem aynı zamanda bir hücrenin çıkışını verir.
Her bağlantının bir ağırlık değeri vardır. 
YSA, kendisine örnekler gösterildikçe bu ağırlık değerlerini değiştirir.
Hedef, ağa gösterilen örnekler için doğru çıkışları verecek ağırlıkları bulmaktır. 


![](https://github.com/ozdenurucar/Yapay_Sinir_Aglari/blob/master/Resimler/ysa_genelyapi.png)

**Yapay Sinir Ağının Öğrenme Özellikleri / Hata Fonksiyonu**

İyi bir yapay sinir ağı  minimum hataya sahiptir. 
İyi bir öğrenme fonksiyonu yapay sinir ağını yüksek hatalı bir konfigürasyondan düşük hatalıya taşır. 
Yapay sinir ağınıdaki hata, hata ölçüm fonksiyonları ile ölçülür. 
Bu hata fonksiyonları eğitim kümesindeki örneklerin hatalarının tümünü temsil eder. Problemin tipine ve tasarımcının seçimine göre farklı Hata fonksiyonları kullanılabilir. 
En sık kullanılanları verilmiştir:

Mean absolute error
  
Mean squared error
  
Sum squared error


**Yapay Sinir Ağının Öğrenme Özellikleri / Learning Rate**

Büyük öğrenme oranı: sistemin veriyi çok hızlı öğrenir, toplam hata artar. 

Düşük öğrenme oranı: sistem çok yavaş öğrenir, eğitim zamanı artar ancak hata azalır. 

**Yapay Sinir Ağının Öğrenme Özellikleri / Momentum**

Yapay sinir ağı her adımda daha az hata değerine sahip bir noktaya gelmek isteyecektir. 
Birden çok iterasyon sonucunda sistem minimum hatalı olan noktaya erişecektir. 
Eğitim sırasında, yapay sinir ağı hatanın azaldığı yerde durmayı sürdürmek ister. 
Yapay sinir ağı için local minima tuzağına düşmek doğaldır ve bu durum global minimuma ulaşmasına engel olabilir. 
Momentum öğrenme algoritmasını local minimumdan kaçacak şekilde önceki yönde tutmaya çalışır. 

**Yapay Sinir Ağının Öğrenme Özellikleri / Durdurma kriteri**

Zaman eşik değerine ulaştığında bitebilir.

Önceden tanımlı epoch değeri vardır algoritma bu epoch a ulaştığında bitebilir.

Önceden tanımlı hata değerine eriştiğinde bitebilir.

İki epoch arasındaki hata değeri azaldığında eğitim bitebilir. Eğitim devam etse bile performansta çok fazla değişiklik olmayacağı hesap edilir.  

### Multilayer Perceptron (MLP) Genel Yapısı

![](https://github.com/ozdenurucar/Yapay_Sinir_Aglari/blob/master/Resimler/mlp.png)

Yapay Sinir Ağı, yapay sinir hücrelerinin (perceptron) birbirlerine bağlanması sonucu oluşan yapılardır.

Yapay Sinir Ağı mimarisi katmanlardan kurulmuştur. 
Katmanların sayısı Yapay Sinir Ağının işlemsel karmaşıklığını ifade etmektedir. 
Daha çok sayıda katmandan oluşan ANN’ler her zaman daha az katmandan oluşanlara göre daha fazla işlem zamanı talep edeceklerdir. 

Giriş katmanı (1), 

Gizli katman (n), 

Çıkış katmanı (1). 	

**Giriş Katmanı:** YSA’ya dış dünyadan bilgilerin geldiği katmandır. Bu katmandaki nöronların sayısı giriş sayısı kadardır. Her nöron bir girişe aittir. girdiler herhangi bir işleme uğramadan gizli katmana iletilirler.

**Gizli katmanlar:** Giriş katmanından aldığı bilgiyi işleyerek bir sonraki katmana iletir Bu katman asıl bilgi işlemenin gerçekleştirildiği katmandır. Her gizli katmandaki nöron sayısı değişkenlik gösterebilir. Genelde bu katmandaki nöronların sayısı giriş ve çıkış katmanındaki nöron sayılarından fazladır. Gizli katman sayısı ağın karmaşıklığını da kontrol altında tutmaya yarar. 

**Çıkış katmanı:** Gizli katmandan gelen bilgiyi işler ve giriş katmanına gelen girdiye uygun olarak üretilen çıktıyı dış dünyaya gönderir.Nöronların sayısı sistemden beklenen çıkışlar kadardır. Her nöron tek bir çıkışa aittir. 



