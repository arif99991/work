Yaygın Hyper-V yedekleme stratejileri

Hyper-V sanal makinelerini yedeklemek kolay olabilir; ancak, tesise bağlı olarak, karmaşık hale de gelebilir.

Hyper-V için birkaç yaygın olağanüstü durum kurtarma senaryosu vardır:

VM'leri yedekleyin ve bir yedekleme geçmişi tutun. Örneğin, her gece yedekleyin ve son 7 gün canlı
yedeklemeleri ve çevrimdışı yedeklemeleri (sıcak veya soğuk yedeklemeler) aracısız yedekleme olarak bilinen sabit tutun Durum depolanan yedeklemeler (dondurucu yedeklemeler) VM içindeki yedeklemeler (aracı yedekleme
)

Canlı Hyper-V VM çoğaltması


Ana bilgisayardan alınan yedeklemeler

Hyper-V canlı yedeklemeleri

Canlı yedeklemeler çoğu kullanıcının istediği şeydir. Canlı yedeklemeler, Hyper-V ve VSS, Microsoft Windows XP ve sonraki sürümlerin Birim Gölge Hizmeti tarafından sağlanır.

Eski işletim sistemleri VSS sağlamaz ve bu nedenle canlı yedekleme araçlarıyla uyumlu değildir.

Canlı yedeklemelerin düzgün çalışması için aşağıdakilere sahip olmanız gerekir:

VSS etkin ana bilgisayar işletim sistemi ve düzgün çalışan VSS. (Windows Server 2008 ve sonrası)
VSS etkin konuk işletim sistemi. VM'ler Windows XP veya Server 2003 ve sonraki sürümlerinde çalışıyor olmalıdır. Ana bilgisayar işletim sisteminizin sürümüne bağlı olarak, bazı Linux varyantları desteklenebilir.
Her VM'de en son Hyper-V tümleştirme hizmetlerinin yüklü olması gerekir.
NTFS dosya sistemlerini kullanmalısınız
Yeterli RAM ve disk alanınız olmalıdır (en az 10 GB sabit disk alanı ve 1 GB RAM)
Yeterince büyük bir VSS bellek alanınız olmalıdır. VSSUIRUN.EXE veya vssadmin kullanarak 10 GB'ın üzerinde sınırsız veya yüksek sınırlar ayarlayın.

Yedekleme uygulaması işlemi başlatır ve Windows, Hyper-V ve VSS'yi içerir. Yedekleme sinyali de VM'ye gönderilir. VM 'nin VSS 'si daha sonra tetiklenir ve VM içinde VSS isteklerini işleyebilecek tüm hizmetleri bilgilendirir. Ardından, VM kesintisiz çalışmaya devam ederken yedekleme sanal makinenin neredeyse donmuş, uygulama ve kilitlenmeyle tutarlı bir durumunu devralır.


Çevrimdışı VM yedeklemeleri

VSS özellikli hizmetleriniz veya işletim sistemleriniz yoksa çevrimdışı VM yedeklemeleri harikadır. Ancak çevrimdışı yedeklemeler bazen "daha iyi" olduğu için. VM'nin işletim sistemi de dahil olmak üzere tüm hizmetlerin kapatılması gerekir. Ardından yedekleme alınır ve VM yeniden önyüklenir. Bu, VM'nin düzenli aralıklarla önyüklenebilir olmasını sağlar; ancak, gerekli kesinti süresi birçok ayar için sorun olabilir.

VM'leri yeniden başlatmak iyidir, çünkü sistemdeki Windows ve diğer geçici alanları siler ve VM'nin gerçekten önyüklenebilir olmasını sağlar. Bazen VHD'ler bozulabilir veya bir virüs veya yazılım hatası önyükleme işleminde sorunlara neden olabilir. Yedekler her zaman canlı u getirilirseVM hiçbir zaman yeniden başlatılmazsa, hatalar hiçbir zaman açılmaz ve fark edilmez.

Ayrıca, yönetici genellikle sanal sunucunun VSS uyumsuz hizmetler çalıştırıp çalıştırmadığını bilmez. Ayrıca bakınız [Hyper-V live backup](https://backupchain.com/en/live-backup/), [Certification](https://backupchain.com/en/how-to-become-a-certified-backup-engineer/), [VMware backups](https://backupchain.com/en/vmware-backup/).

Örnekler şunları içerir: Microsoft Access
MySQL
Özel veritabanları ve düz dosya veri deposu düzenlemeleri


Depolanan durum yedeklemeleri

Kaydedilen Durum, Microsoft'un VSS uyumlu olmayan işletim sistemlerinden (genellikle) en az veri kaybıyla makul derecede yararlı yedeklemeler oluşturmak için icat ettiği şeydir:



Windows Server 2008/R2 ve 2012 konak sunucularındaki
çoğu Linux türevi Windows Server 2000 ve Windows'un eski veya var olmayan Hyper-V tümleştirme hizmetlerine

sahip önceki
Modern sürümlerinde VM'nin geçerli bir Hyper-V Tümleştirme Hizmeti yüklemesi yoksa, Kaydedilmiş Durum modunda yedeklenir.

Yedeklemeler ayrıca "Kaydedilmiş Durum" modunda da gerçekleştirilebilir (karar, yedekleme uygulaması tarafından değil, Hyper-V yönetimi tarafından verilir):

Yeterli kaynak yoksa (RAM, yüksek oranda parçalanmış RAM'de olduğu gibi)
VM işletim sistemi bir önyükleme veya kapatma işleminde


Canlı Hyper-V VM çoğaltması

VM'leri bir sunucudan başka bir sunucuya çoğaltabilir ve geçmiş sürümlerin X sürümlerinin sayısını korumak için yedek sürüm oluşturmayı da kullanabilirsiniz. Sanal sabit diskleri sıkıştırmak ve yinelenenleri kaldırmak yerine, VSS onları kilitlenme ve uygulamayla tutarlı bir duruma getirdikten sonra kopyalanabilirler. Kurtarma sunucusunda, sanal diskler yerel biçimlerinde ve başlatılmaya hazır olduklarından, gerekirse gecikme olmadan herhangi bir zamanda önyüklenebilirler.


VM içinde gerçekleştirilen aracı yedeklemeleri
Bazı senaryolar, VM
içinde oluşturulması gereken yedeklemeler gerektirir:

Linux veya Windows Server 2000
gibi ana bilgisayardan canlı olarak yedeklenemeyen VSS uyumlu olmayan bir işletim sistemi kullanıyorsunuz VM içinde iSCSI veya ana bilgisayarda fiziksel olarak bulunan bağlı bir bölüm gibi doğrudan bağlı depolama alanı kullanırsınız.


Her iki stratejinin de çalışmasını sağlayan

başka bir çözüm olan Hyper-V için Granüler Yedekleme, BT yöneticilerinin VM'lerdeki dosyalara ana bilgisayardan erişmesine olanak tanıyan yenilikçi bir özelliktir. VM'lerin sanal disklerine ana bilgisayardan erişilebiliyorsa, VM'lere yazılım yüklemeden VM klasörlerinin canlı yedeklemesini gerçekleştirebilirsiniz. Hyper-V için bu yedekleme çözümüne ve buna bakın.
