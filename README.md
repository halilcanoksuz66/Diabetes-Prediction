
# Diyabet Tahmin Projesi

Bu proje, çeşitli sağlık göstergelerine dayalı olarak hastaların diyabet olma olasılığını tahmin etmek için makine öğrenmesi algoritmalarını kullanmaktadır. Kullanılan veri seti, bireylerin glukoz seviyeleri, kan basıncı, BMI, yaş ve daha fazlası gibi bilgileri içermektedir. Lojistik Regresyon, Destek Vektör Makinesi (SVM) ve Karar Ağaçları gibi çeşitli makine öğrenmesi modelleri, tahminsel modelin oluşturulmasında kullanılmıştır.

## İçindekiler
- [Giriş](#giriş)
- [Veri Seti](#veri-seti)
- [Kullanılan Algoritmalar](#kullanılan-algoritmalar)
- [Kurulum](#kurulum)
- [Kullanım](#kullanım)
- [Sonuçlar](#sonuçlar)
- [Lisans](#lisans)

## Giriş

Diyabet, dünya çapında milyonlarca insanı etkileyen kronik bir hastalıktır. Erken tahmin ve teşhis, hastalığın etkili bir şekilde yönetilme şansını önemli ölçüde artırabilir. Bu projede, makine öğrenmesi kullanarak, bir hastanın diyabet olma olasılığını tahmin etmek amacıyla çeşitli sağlık göstergeleri kullanılmıştır.

## Veri Seti

Bu projede kullanılan veri seti, ünlü **Pima Indian Diabetes Database** veri setidir ve Pima Indian kökenli kadın hastalara ait verilerden oluşmaktadır. Veri setindeki özellikler şunlardır:
- **Glukoz**
- **Kan Basıncı**
- **Cilt Kalınlığı**
- **İnsülin**
- **BMI**
- **Diyabet Pedigri Fonksiyonu**
- **Yaş**
- **Sonuç** (hedef değişken, hastanın diyabet olup olmadığını gösterir)

Veri seti 768 örnek ve 9 özellik (8 giriş özelliği ve 1 hedef değişken) içermektedir.

## Kullanılan Algoritmalar

Bu projede şu makine öğrenmesi algoritmaları kullanılmıştır:
1. **Lojistik Regresyon**: İkili sınıflandırma için kullanılır (diyabetli vs diyabetsiz).
2. **Destek Vektör Makinesi (SVM)**: Doğrusal sınıflandırma için güçlü bir algoritmadır.
3. **Karar Ağacı**: Veri modellemesi ve giriş özelliklerine dayanarak sonuç tahmini yapmak için kullanılan bir algoritmadır.

Bu algoritmalar, modellerin performansını değerlendirmek için çapraz doğrulama kullanılarak test edilmiştir.

## Kurulum

Bu projeyi yerel makinenizde çalıştırabilmek için Python yüklü olmalı ve gerekli kütüphaneler kurulmuş olmalıdır. Gereksinimlerinizi aşağıdaki `pip` komutuyla yükleyebilirsiniz.

```bash
pip install numpy pandas scikit-learn seaborn matplotlib
```

## Kullanım

1. Depoyu klonlayın:
   ```bash
   git clone https://github.com/kullanıcıadı/diyabet-tahmin.git
   cd diyabet-tahmin
   ```

2. Modelleri eğitmek ve performanslarını değerlendirmek için `diyabet_tahmin.py` script'ini çalıştırın:
   ```bash
   python diyabet_tahmin.py
   ```

Script, farklı modellerin performans sonuçlarını (doğruluk oranları) gösterecek ve her model için karışıklık matrisi (confusion matrix) çıktısını verecektir.

## Sonuçlar

Modellerin performansı şu metriklerle değerlendirilebilir:
- **Doğruluk**: Doğru tahminlerin oranı.
- **Hassasiyet (Precision)**: Pozitif tahminlerin ne kadarının doğru olduğu.
- **Duyarlılık (Recall)**: Gerçek pozitiflerin ne kadarının doğru tahmin edildiği.
- **F1 Skoru**: Hassasiyet ve duyarlılığın harmonik ortalaması.

## Lisans

Bu proje MIT Lisansı ile lisanslanmıştır - detaylar için [LICENSE](LICENSE) dosyasına bakın.
