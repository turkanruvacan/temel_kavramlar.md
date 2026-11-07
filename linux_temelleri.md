#   Linux Temelleri
    Linux, dünya genelindeki sunucuların, bulut altyapılarının, konteynerlerin (Docker) ve geliştirici ortamlarının kalbidir. 
    Bir bilgisayar mühendisi veya yazılımcı olarak grafik arayüzlerin arkasındaki bu güçlü komut satırı dünyasına hâkim olmak, sistemleri yönetebilmek için kritik bir beceridir.

1. Temel Terminal Komutları
    =>  ls (List): Bulunduğunuz dizindeki dosya ve klasörleri listeler. (ls -la komutu gizli dosyaları ve detaylı izinleri gösterir.)
    =>  cd (Change Directory): Klasörler arasında geçiş yapmanızı sağlar (Örn: cd /var/log).
    =>  grep: Dosyalar veya gelen çıktılar içerisinde belirli bir metni veya kelimeyi aramak için kullanılır.
    =>  mkdir (Make Directory): Yeni bir klasör oluşturur (Örn: mkdir projeler).
    =>  chmod (Change Mode): Dosya ve dizinlerin okuma, yazma, çalıştırma izinlerini değiştirir.
    =>  top: Sistemdeki çalışan anlık süreçleri (processes), CPU ve RAM tüketimini canlı olarak gösterir.

2. Paket Yönetimi
    =>  apt (Advanced Package Tool): Ubuntu, Debian ve türevlerinde kullanılır. (Örn: sudo apt update && sudo apt install nginx)
    =>  dnf: Fedora, RHEL ve CentOS gibi sistemlerde kullanılan modern paket yöneticisidir.
    =>  pacman: Arch Linux tabanlı sistemlerde kullanılan hızlı paket yöneticisidir.

3. Dosya İzinleri (Permissions)
    Çok kullanıcılı güvenli bir işletim sistemi olduğu için her dosya ve klasörün kimler tarafından okunabileceğini, yazılabileceğini veya çalıştırılabileceğini belirleyen kuralları vardır.
İzin Türleri:
    =>  r (Read / Okuma): Dosyayı okuma veya dizin içeriğini listeleme.
    =>  w (Write / Yazma): Dosyayı değiştirme veya dizin içine dosya ekleme/silme.
    =>  x (Execute / Çalıştırma): Dosyayı program olarak çalıştırma veya dizine giriş yapabilme.
    =>  Sahiplik Grupları: İzinler User (Sahip), Group (Grup) ve Others (Diğer herkes) olmak üzere üç kategoriye ayrılır (Örn: chmod 755 dosya.sh).

4. Servisler ve Süreç Yönetimi (systemctl)
Modern Linux sistemlerinde arka planda çalışan servisleri (web sunucuları, veritabanları vb.) yönetmek için systemctl aracı kullanılır.
    =>  Servis Durumunu Kontrol Etme: sudo systemctl status nginx
    =>  Servisi Başlatma: sudo systemctl start mysql
    =>  Servisi Durdurma: sudo systemctl stop postgresql
    =>  Sisteme Açılışında Otomatik Başlatma (Enable): sudo systemctl enable docker
