/*
Ağ Temelleri (Networking)
    # Temel Ağ Bileşenleri
        IP (Internet Protocol)
            =>Ağa bağlı her cihaza atanan benzersiz kimlik numarasıdır. 
            =>Ev adresiniz gibi düşünebilirsiniz; verinin hangi cihaza gideceğini belirler.
    
        Port
            =>Cihaza ulaşan verinin hangi uygulamaya veya servise teslim edileceğini belirten kapı numarasıdır. 
            =>IP adresi binayı gösterirken, port numarası daire kapısını temsil eder.
                80: HTTP (Güvenliksiz web trafiği)
                443: HTTPS (Güvenli web trafiği)
                22: SSH (Uzaktan güvenli erişim)
                3306: MySQL veritabanı bağlantısı

        DNS (Domain Name System)
            =>İnsanların hatırlamakta zorlandığı sayısal IP adreslerini (örn: 142.250.185.78) alan adlarına (örn: google.com) çeviren telefon rehberidir.

        TCP (Transmission Control Protocol)
            =>Güvenilir ve sıralı veri iletimi sağlayan protokoldür. Veri gönderilmeden önce "3'lü El Sıkışma" (3-Way Handshake) ile bağlantı kurulur. 
            =>Paket kaybı yaşanırsa veri tekrar gönderilir.
                Kullanım Alanları: Web siteleri (HTTP/HTTPS), e-posta (SMTP), dosya transferi (FTP).


        UDP (User Datagram Protocol)
            =>Hız odaklı, bağlantısız bir protokoldür. 
            =>Verinin eksiksiz gidip gitmediğini kontrol etmez, onay beklemez.
                Kullanım Alanları: Canlı yayınlar, çevrim içi oyunlar, VoIP (sesli aramalar).

    # Paket Yapısı ve Çalışma Mantığı
        =>İnternet üzerinden büyük bir veri gönderilirken metin veya dosya tek parça halinde gitmez; paket (packet) adı verilen küçük parçalara bölünür.  
        =>Bir ağ paketi temel olarak üç ana bölümden oluşur:
            1)Header (Başlık): Paketin yönlendirme bilgilerini taşır.
                =>Gönderici IP ve Port
                =>Alıcı IP ve Port
                =>Protokol türü (TCP/UDP) ve Paket Sıra Numarası
            2) Payload (Veri Yükü): Taşınan asıl içeriktir (dosyanın bir parçası, mesaj metni vb.).
            3) Trailer (Altbilgi/Kuyruk): Paketin yolda bozulup bozulmadığını denetleyen hata kontrol kodlarını (CRC) içerir.
                Nasıl Çalışır?
                    Veri gönderici tarafta parçalanıp paketlenir, yönlendiriciler (router) aracılığıyla ağda yol alır ve alıcı tarafta başlıklar okunarak doğru sırayla birleştirilir.
    # Ağ Teşhis ve Analiz Araçları
        Ping
            =>Bir sunucuya veya cihaz erişilebilir durumda mı ve aradaki gecikme süresi (latency) ne kadar sorularını yanıtlar. 
            =>ICMP protokolünü kullanır.
                    ping google.com
        Traceroute (Windows'ta tracert)
            =>Gönderilen bir paketin hedef sunucuya varana kadar hangi yönlendiricilerden (router/hop) geçtiğini adım adım gösterir.
            =>Ağdaki tıkanıklık veya kopukluğun nerede olduğunu tespit etmek için kullanılır.
                    traceroute google.com   # Linux / macOS
                    tracert google.com      # Windows
        Nslookup
            =>Bir alan adının (domain) hangi IP adresine karşılık geldiğini sorgular veya DNS sunucu kayıtlarını kontrol eder.
                    nslookup google.com