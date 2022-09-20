Hyper-V: Bilmeniz Gereken 18 Şey

Aşağıda, Hyper-V kullanırken karşılaşabileceğiniz 18 tuzağın kısa bir listesi bulunmaktadır. Bu listeyi, Hyper-V'yi yedeklemek için bir araç oluşturduğumuz yıllar boyunca derledik. Bu arada, Microsoft Hyper-V bağlantısı burada.

Aşağıdaki noktaların ayrıntılı bir analizi için bkz: Bilmeniz Gereken 18 Hyper-V Tuzağı.

Tuzak #1: Özel bir [Backup for Hyper-V](https://backupchain.com/en/hyper-v-backup/) yedekleme yazılımı yerine komut dosyaları kullanma: PowerShell işi yapabilir, ancak Microsoft'un Hyper-V API'lerini düzenli olarak değiştirdiğini ve birçok komut dosyasının uygun hata işlemeye sahip olmadığını bilmemiz gerekir. Çoğu zaman, ev yapımı komut dosyaları, kaputun altındaki çeşitli yapılandırma senaryolarını ele almak için önemli özelliklerden de yoksundur.

Tuzak #2: Yeterince sık yedekleme
yapmamak 

Tuzak #3: Hyper-V sanal makine yapılandırmalarının karmaşıklığını hafife almak: VM yapılandırmalarıyla uğraşmak için yalnızca sanal bir sabit diske işaret etmekten
çok daha fazlası var 

Tuzak #4: VSS'yi optimize etmemek (Birim Gölge Kopyası Hizmeti): Microsoft, yakında saçlarınızı kaybetmenizi sağlamak için VSS'yi oluşturdu

Tuzak #5: Ana bilgisayarda ve VM'lerde yeterli boş alan ve RAM yok. Kaynak eksikliği, Windows'ta bir fiyasko için önemli bir bileşendir...

Tuzak #6: Dinamik olarak büyüyen / genişleyen sanal sabit diskleri kullanma: Evet, kullanışlı gelirler, ancak bu hemen hemen tüm pozitiflerdir.

Tuzak #7: Çok sık yedekleyin: Paranoya BT Tuzak #8'de bile pahalıdır
: Disk uyarılarını görmezden gelmek. Oldukça fazla paraya mal olan yanlış bir isimlendirme. Yaklaşık 40.000 müşteriyle çalıştıktan sonra, sabit disk uyarısının bir uyarı değil% 99,9 olduğunu biliyoruz. Bu, sabit disk sürücüsü duman içinde yükselmeden
önce harekete geçmek için yapılan son çağrıdır Tuzak #9: Hyper-V Integration Services'ı güncel tutun. Hyper-V Yöneticisi VM Tümleştirme Hizmeti sürümünü görüntülemediğinden, bu özellikle Windows Server 2008 R2'de bir sorundur.

Tuzak #10: Yedekleme hedefinde yeterli alan yok.

Tuzaklar #11: Yeterli depolama alanı satın almamak. Hiç yetersiz, nokta.

Tuzak #12: Yedekleme aracını güncel tutmayın. Hyper-V, herkesi meşgul edecek kadar sık dahili olarak değişir.

Tuzak #13: VM'lere ve Hyper-V ana bilgisayarlarına Windows güncelleştirmeleri yüklenmez: Windows Server 2016'da, VM'lerin tümleştirme hizmetlerini otomatik olarak güncelleştirdiği söylenir. Sonunda.... Ancak, diğer tüm yazılım güncellemeleri için bu işlemi kendiniz yönetmeniz gerekir.

Tuzak # 14: RAM ve sabit disk hatalarını düzenli olarak test etmiyorsunuz: Daha önce Bit Red ile hiç ilgilenmediyseniz (Bit Red & Data Loss: Hasar Potansiyelinin Farkında mısınız?), Henüz hiçbir şey görmediniz.

Tuzak No. 15: Sıkıştırma çok yüksek veya çok düşük

Tuzak #16: Aynı sabit sürücüden çok fazla VM çalıştırın. "Bir yatak odasında çok fazla yatak" var mı?

Tuzak #17: Bir altyapı satın alırken Hyper-V yedeklemesi planlanmamıştır

Tuzak #18: Hyper-V ana bilgisayarlarında

NTFS sıkıştırması veya şifrelemesi ya da Bitlocker kullanma Bugüne kadar, NTFS sıkıştırması kusurluydu. Ek olarak, dosya sistemi düzeyinde şifreleme ve sıkıştırma, önemli performans düşüşüne ve en azından ciddi parçalanmaya neden olur. Bu nedenle, bir üretim sisteminde, bu NTFS işlevlerinin kullanılmasını önermeyiz.

Yukarıdaki tuzakların her biri aşağıda ayrıntılı olarak açıklanmıştır: Bilmeniz Gereken 18 Hyper-V Tuzağı. [Remote backup](https://backupchain.com/en/remote-backup-software/)
