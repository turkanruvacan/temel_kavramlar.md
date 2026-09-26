İşletim Sistemleri

     Kernel (Çekirdek)
    =>Kernel, işletim sisteminin donanımla doğrudan iletişim kuran en temel katmanıdır. 
    =>CPU, bellek ve diğer donanım kaynaklarına erişimi kontrol eder, uygulamalarla donanım arasında aracılık yapar. 
    =>Kullanıcı programları donanıma doğrudan erişemez; bunun yerine kernel'den istekte bulunur (system call).

    Süreç (Process) – İş Parçacığı (Thread) Farkı
    =>Süreç, çalışan bir programın kendi belleğine ve kaynaklarına sahip bağımsız bir örneğidir. 
    =>Thread ise bir sürecin içinde çalışan, aynı belleği paylaşan daha küçük bir yürütme birimidir. 
    =>Bir süreçte birden fazla thread bulunabilir; bu sayede aynı programın farklı işleri paralel şekilde yürütülebilir.

    Bellek Yönetimi
    =>İşletim sistemi, çalışan tüm süreçlere gerektiği kadar bellek ayırmak ve bu belleği güvenli şekilde izole etmekle sorumludur. 
    =>Sanal bellek (virtual memory) tekniğiyle, fiziksel RAM yetersiz kaldığında disk üzerinde geçici alan (swap) kullanılabilir.
    => Bu sayede birden fazla program aynı anda çalışsa bile birbirinin belleğine müdahale edemez.

    CPU Zamanlayıcıları (Schedulers)
    =>Zamanlayıcı, CPU'nun hangi sürecin ne kadar süreyle çalışacağına karar veren bileşendir. 
    =>Tek bir CPU çekirdeği bile, süreçler arasında çok hızlı geçiş yaparak (context switching) aynı anda birden fazla program çalışıyormuş hissi verir. 
    =>Farklı zamanlama algoritmaları (Round Robin, Priority Scheduling vb.) performans ve adalet dengesini sağlamak için kullanılır.

    Sanallaştırma (Virtualization)
    =>Bir işletim sisteminin, fiziksel donanım üzerinde birden fazla "sanal" bilgisayar gibi davranmasını sağlayan tekniktir. 
    =>Bu sayede tek bir makinede birden fazla işletim sistemi aynı anda çalışabilir (örneğin VirtualBox, VMware ile).
