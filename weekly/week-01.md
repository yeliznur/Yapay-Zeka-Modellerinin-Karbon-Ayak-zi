# 📅 1. Hafta – Proje Gelişim Raporu

## 🌿 Proje

**Yapay Zeka Modellerinin Karbon Ayak İzi Analizi**

---

## 🎯 Haftanın Amacı

Bu haftanın temel amacı, yapay zeka modellerinin karbon ayak izini analiz edebilmek için gerekli veri kaynaklarını incelemek, kullanılabilir bir veri yapısı oluşturmak, literatürde kullanılan enerji ve karbon hesaplama yaklaşımlarını araştırmak ve ilerleyen aşamalarda uygulanabilecek makine öğrenmesi yöntemleri için teknik altyapıyı değerlendirmekti.

Bu kapsamda proje; veri toplama, veri birleştirme, literatür taraması, özelliklerin belirlenmesi ve olası modelleme yaklaşımlarının araştırılması olmak üzere paralel şekilde ilerletildi.

---

## 📚 1. Literatür Taraması

Projenin metodolojik altyapısını oluşturmak amacıyla yapay zeka sistemlerinin enerji tüketimi, karbon emisyonları, GPU güç tüketimi ve karbon emisyonlarının makine öğrenmesi ile tahmini üzerine akademik çalışmalar incelendi.

Özellikle aşağıdaki konular araştırıldı:

- Yapay zeka modellerinin eğitim süreçlerinde enerji tüketimi
- Model deployment/inference süreçlerindeki enerji tüketimi
- Elektrik şebekesinin karbon yoğunluğunun emisyonlara etkisi
- GPU ve donanım özelliklerinin güç tüketimiyle ilişkisi
- Karbon emisyonu tahmininde makine öğrenmesi yöntemleri
- Feature selection ve feature engineering yaklaşımları
- Doğrusal ve doğrusal olmayan regresyon yöntemlerinin karşılaştırılması
- Model performanslarının R², MAE ve RMSE gibi metriklerle değerlendirilmesi

İncelenen çalışmalarda özellikle Linear Regression, Ridge, Lasso, Random Forest, XGBoost ve Neural Network gibi yöntemlerin karbon/enerji tüketimi tahmin problemlerinde değerlendirilebildiği görüldü.

Ayrıca GPU güç tüketimini tahmin etmeye yönelik çalışmalardan; FLOPs, donanım özellikleri ve işlem yükü gibi değişkenlerin enerji tüketimini açıklamada kullanılabileceği konusunda yararlanıldı.

Bu literatür taraması sonucunda model seçiminden önce veri yapısının, özelliklerin ve değişkenler arasındaki ilişkilerin detaylı şekilde incelenmesinin önemli olduğu belirlendi.

---

## 📊 2. Veri Kaynaklarının Araştırılması

Projenin temel veri ihtiyacını karşılamak amacıyla farklı veri kaynakları incelendi.

Özellikle:

- AI/ML modellerine ait model ve eğitim bilgileri
- Model parametreleri
- Training compute / FLOPs
- Training süresi
- Kullanılan donanım bilgileri
- Donanım miktarı
- Güç tüketimi
- Eğitim enerjisi
- Elektrik karbon yoğunluğu
- Eğitim karbon ayak izi

gibi değişkenlerin proje açısından kullanılabilirliği değerlendirildi.

Projenin temel amacı doğrultusunda farklı veri kaynaklarından gelen bilgilerin ortak bir veri yapısında birleştirilebilmesi üzerine çalışıldı.

---

## 🔗 3. Veri Birleştirme ve Veri Setinin Oluşturulması

Haftanın önemli çıktılarından biri, farklı kaynaklardan elde edilen verilerin bir araya getirilerek proje kapsamında kullanılabilecek daha kapsamlı bir veri yapısının oluşturulması oldu.

Veri birleştirme sürecinde model bilgileri ile enerji ve karbon ayak izi açısından kullanılabilecek değişkenler bir araya getirildi.

Veri yapısındaki sütunlar incelenerek:

- Sayısal değişkenler
- Kategorik değişkenler
- Model bilgileri
- Donanım bilgileri
- Eğitim bilgileri
- Enerji tüketimi
- Karbon yoğunluğu
- Karbon ayak izi

gibi farklı değişken grupları değerlendirildi.

Çalışmalar sonucunda **3.998 kayıt içeren bir veri seti oluşturuldu.**

Bu veri seti, projenin ilerleyen aşamalarında yapılacak veri analizi, özellik seçimi ve modelleme çalışmalarının temel veri kaynağı olarak kullanılmak üzere hazırlandı.

---

## 🧹 4. Veri Yapısının İncelenmesi

Oluşturulan veri setinin modelleme öncesinde kullanılabilirliğini değerlendirmek amacıyla veri yapısı incelendi.

Bu aşamada özellikle:

- Sütunların veri tipleri
- Sayısal ve kategorik değişkenler
- Eksik değerler
- Değişkenlerin değer aralıkları
- Model ve donanım bilgileri
- Enerji ve karbon değişkenleri

üzerinde duruldu.

Bazı değişkenlerin doğrudan sayısal modellemeye uygun hale getirilmesi ve veri ön işleme uygulanması gerektiği görüldü.

Bu nedenle ilerleyen aşamalar için veri temizleme, uygun veri tiplerine dönüştürme, eksik değerlerin değerlendirilmesi ve gerekli dönüşümlerin uygulanması planlandı.

---

## 🧩 5. Feature Engineering İçin Özelliklerin Belirlenmesi

Modelleme aşamasına geçmeden önce karbon emisyonunu açıklayabilecek değişkenlerin belirlenmesi üzerine çalışıldı.

Özellikle aşağıdaki değişkenlerin proje açısından önemli olabileceği değerlendirildi:

- Model parametre sayısı
- Training FLOPs
- Training süresi
- Hardware quantity
- Training power
- Training energy
- Carbon intensity
- Model architecture
- Kullanılan donanım
- Model türü

Bunun yanında mevcut değişkenlerden yeni özellikler türetilebilecek olası yaklaşımlar da değerlendirildi.

Örneğin hesaplama yükü ile enerji/güç tüketimi arasındaki ilişkiyi temsil edebilecek verimlilik tabanlı özelliklerin ilerleyen aşamada incelenmesi planlandı.

---

## 🤖 6. Algoritma ve Model Araştırması

Literatür taramasıyla paralel olarak proje için kullanılabilecek makine öğrenmesi algoritmaları araştırıldı.

Henüz nihai model seçimi yapılmadı. Ancak aday yöntemler arasında:

- Linear Regression
- Ridge
- Lasso
- Random Forest
- XGBoost
- LightGBM
- Neural Network

gibi yöntemler değerlendirildi.

Buradaki temel yaklaşım, doğrudan tek bir algoritma seçmek yerine farklı model türlerinin karşılaştırılabileceği bir yapı oluşturmaktır.

Özellikle veri setindeki değişkenler arasındaki ilişkilerin doğrusal olmayabileceği göz önünde bulundurularak ağaç tabanlı modellerin de değerlendirilmesi planlandı.

---

## 📖 7. İncelenen Literatürden Çıkarımlar

Hafta boyunca incelenen çalışmalar sonucunda üç temel konu öne çıktı:

### Enerji tüketimi

Model büyüklüğü, işlem yükü, donanım ve çalışma süresi gibi faktörlerin enerji tüketimiyle ilişkili olduğu görüldü.

### Karbon yoğunluğu

Aynı miktarda enerji tüketilse bile kullanılan elektrik kaynağının karbon yoğunluğuna bağlı olarak ortaya çıkan karbon emisyonunun değişebileceği görüldü.

### Makine öğrenmesi ile tahmin

Karbon emisyonları ile farklı çevresel ve teknik değişkenler arasındaki ilişkilerin karmaşık olabileceği ve bu nedenle farklı makine öğrenmesi modellerinin karşılaştırılmasının anlamlı olabileceği değerlendirildi.

---

## 📌 8. Haftanın Somut Çıktıları

Bu hafta sonunda proje kapsamında:

- Akademik literatür taraması gerçekleştirildi.
- Enerji tüketimi ve karbon emisyonu hesaplama yaklaşımları incelendi.
- Karbon emisyonu tahmininde kullanılabilecek makine öğrenmesi algoritmaları araştırıldı.
- Projede kullanılabilecek veri kaynakları incelendi.
- Farklı veri kaynaklarından gelen bilgiler üzerinde veri birleştirme çalışması yapıldı.
- Veri yapısındaki temel değişkenler incelendi.
- Feature Engineering için kullanılabilecek değişkenler değerlendirildi.
- **3.998 kayıt içeren proje veri seti oluşturuldu.**
- İlerleyen modelleme aşamasında değerlendirilebilecek algoritmalar belirlendi.

---

## 🚀 Sonraki Aşama İçin Temel Yönelim

Oluşturulan 3.998 kayıtlık veri seti ve yapılan literatür çalışması, projenin sonraki aşamalarındaki veri analizi ve modelleme çalışmalarının temelini oluşturacaktır.

Bir sonraki aşamada veri setinin daha detaylı incelenmesi, değişkenlerin proje hedefiyle ilişkilerinin değerlendirilmesi, gerekli veri ön işleme ve feature engineering çalışmalarının yapılması ve literatür doğrultusunda uygun modelleme yaklaşımının belirlenmesi hedeflenmektedir.

---

## 📊 Haftalık Özet

| Çalışma Alanı | Durum |
|---|---|
| Literatür taraması | ✅ Gerçekleştirildi |
| Veri kaynaklarının incelenmesi | ✅ Gerçekleştirildi |
| Veri birleştirme | ✅ Gerçekleştirildi |
| Veri setinin oluşturulması | ✅ 3.998 kayıt |
| Veri yapısının incelenmesi | ✅ Gerçekleştirildi |
| Feature Engineering araştırması | 🔄 İncelendi / geliştirilecek |
| Algoritma araştırması | 🔄 Aday modeller belirlendi |
| Nihai model seçimi | ⏳ Sonraki aşama |
| Model eğitimi | ⏳ Sonraki aşama |
