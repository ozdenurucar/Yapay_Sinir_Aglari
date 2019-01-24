# Yapay Sinir Aglari

Yapay sinir ağları (YSA) insan beyninden esinlenmiştir.
Öğrenme sürecinin matematiksel olarak modellenmesi temeline dayanmaktadır.
YSA çalışmaları ilk olarak beynin biyolojik üniteleri olan nöronların modellenmesi ile başlamıştır. 
Günümüzde ise pek çok alanda uygulanmaktadır. 

Dış ortamdan veya diğer hücrelerden alınan girdiler, ağırlıklar yardımıyla hücreye bağlanır. Toplama fonksiyonu ile net girdi hesaplanır. Net girdinin aktivasyon fonksiyonundan geçirilmesiyle net çıktı hesaplanır. Bu işlem aynı zamanda bir hücrenin çıkışını verir.
Her bağlantının bir ağırlık değeri vardır. 
YSA, kendisine örnekler gösterildikçe bu ağırlık değerlerini değiştirir.
Hedef, ağa gösterilen örnekler için doğru çıkışları verecek ağırlıkları bulmaktır. 


![](https://github.com/ozdenurucar/Yapay_Sinir_Aglari/blob/master/Resimler/ysa_genelyapi.png)

## Yapay Sinir Ağının Öğrenme Özellikleri / Hata Fonksiyonu

İyi bir yapay sinir ağı  minimum hataya sahiptir. 
İyi bir öğrenme fonksiyonu yapay sinir ağını yüksek hatalı bir konfigürasyondan düşük hatalıya taşır. 
Yapay sinir ağınıdaki hata, hata ölçüm fonksiyonları ile ölçülür. 
Bu hata fonksiyonları eğitim kümesindeki örneklerin hatalarının tümünü temsil eder. Problemin tipine ve tasarımcının seçimine göre farklı Hata fonksiyonları kullanılabilir. 
En sık kullanılanları verilmiştir:
  Mean absolute error
  Mean squared error
  Sum squared error
