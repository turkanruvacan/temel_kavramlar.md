#   Dosya Sistemleri: NTFS vs ext4 vs APFS
    Dosya sistemi (File System), verilerin disk üzerinde nasıl saklanacağını, adlandırılacağını, gruplandırılacağını ve bunlara nasıl erişileceğini belirleyen kurallar bütünüdür.
        => NTFS (New Technology File System):   Microsoft tarafından geliştirilen, Windows işletim sistemlerinin varsayılan dosya sistemidir. 
                                                Büyük dosya boyutlarını destekler, gelişmiş kullanıcı izinleri (güvenlik) ve veri bütünlüğü (journaling) özelliklerine sahiptir.
        =>ext4 (Fourth Extended Filesystem):    Linux çekirdeğini kullanan sistemlerin (Ubuntu, Debian vb.) standart ve en yaygın dosya sistemidir.
                                                Parçalanmayı (fragmentation) minimumda tutar, yüksek kararlılık ve büyük veri depolama kapasiteleri sunar. 
        => APFS (Apple File System):            Apple tarafından macOS, iOS ve diğer Apple cihazları için özel olarak geliştirilmiştir.
                                                Flash depolama (SSD) birimleri için optimize edilmiştir; anlık kopyalama (cloning) ve hızlı anlık görüntüler (snapshots) alma özellikleriyle öne çıkar.

#   Blok Yapısı Nedir?
    Dosya sistemleri, dosyaları disk üzerine tek parça halinde veya rastgele kaydetmez. 
    Diski blok (veya sektör/cluster) adı verilen sabit boyutlu küçük parçalara böler.
        Çalışma Mantığı: Örneğin, bir blok boyutu 4 KB olarak belirlendiyse, 1 KB büyüklüğünde bir metin dosyası kaydettiğinizde bile sistem o dosya için 4 KB'lık bir blok tahsis eder (geri kalan kısım boş kalır).
        Büyük dosyalar ardışık veya zincirleme birden fazla bloğa bölünerek saklanır. Dosya sisteminin bu blokları ne kadar verimli yönettiği, dosya okuma/yazma hızını doğrudan etkiler.
        
#   HDD vs SSD Çalışma Prensipleri
    Depolama birimlerinin veri okuma ve yazma hızlarındaki devasa fark, tamamen fiziksel ve elektronik yapı leursındaki ayrılıktan kaynaklanır.
        =>HDD (Hard Disk Drive):            İçerisinde dönen manyetik diskler (platter) ve bu diskler üzerinde hareket eden mekanik bir okuma/yazma kafası barındırır. 
                                            Veriye ulaşmak için fiziksel kafanın doğru sektöre hareket etmesi gerekir. 
                                            Bu mekanik hareket gecikmeye (latency) yol açar.
        => SSD (Solid State Drive):         Hareketli hiçbir mekanik parça içermez. 
                                            Tamamen elektronik NAND Flash bellek yongalarından oluşur. 
                                            Elektrik sinyalleriyle doğrudan mikroçipler üzerinden veri okuyup yazar. 
                                            Bu nedenle HDD'lere kıyasla katlarca daha hızlı çalışır ve modern sistemlerde standart olarak tercih edilir
       
