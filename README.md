# Metro Similasyonu

* Ankara'daki bir metro ağını simule ederek en hızlı ve en az aktarmalı rotayı bulmaya yönelik bir python uygulamasıdır.*

## Kullanılan kütüphaneler

* collections.deque: BFS algoritmasında kuyruk yapısını etkin kullanabilmek için tercih edilmiştir.

* heapq: A* algoritmasında öncelikli kuyruk oluşturmak için kullanılmıştır.

* defaultdict: Metro hatlarını saklarken varsayılan bir liste yapısı oluşturarak her hattın istasyonlarını kolayca saklamak için kullanılmıştır.

* typing: Kodun daha anlaşılır ve güvenli hale getirilmesi amacıyla kullanılmıştır.

## Algoritmaların Çalışma Mantığı
### BFS Algoritması
*BFS algoritması, en az aktarmalı rotayı bulmak için kullanılmıştır*

#### Nasıl çalışır

* Başlangıç istasyonu kuyruğa eklenir.
* Kuyruktaki istasyon, komşuları ile kontrol edilir.
* Eğer bir komşu istasyon hedef istasyon ile eşleşirse algoritma duru ve en uygun rota döndürülür.
* En az durak değiştirerek hedefe ulaşmak amaçlanır.

### A* Algoritması

*En hızlı rotayı bulmak için kullanılmıştır.*

#### Nasıl çalışır

* Başlangıç istasyonu kuyruğa eklenir.
* En az süreye sahip istasyon kuyruktan çıkartılır.
* Komşular kontrol edilir ve yeni hesaplanan süre ile kuyruğa eklenir.
* Hedef istasyona ulaşıldığında algoritma durur ve toplam yolculuk sürelerini hesaplar.

## Neden BFS ve A*Kullanıldı

* BFS : Her aktarmanın bir maliyeti olduğu varsayıldığında en az aktarmalı rotayı bulmak için idealdir.
* A* : Zaman bazlı değerlendirme yaparak toplam yolculuk sürelerini optimize eder.

## Örnek Kullanım ve Test Sonuçları

### AŞTİ'den OSB'ye en az aktarmalı rota:

* En az aktarmalı rota: AŞTİ -> Kızılay -> Ulus -> Demetevler -> OSB

### AŞTİ'den OSB'ye en hızlı rota:

* En hızlı rota (15 dakika): AŞTİ -> Kızılay -> Demetevler -> OSB


## Projeyi Geliştirme Fikirleri

* Gerçek zamanlı veri kullanılarak istasyonlar arasu yoğunluk ekleme.
* Metro sefer saatleri ekleyerek en az bekleme süresini hesaplama.
* Uygulamayı interaktif bir hale getirmek.
* Metro sefer saatleri yoğunluğuna göre alternatif rota önerme.
