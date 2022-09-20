Hyper-V'yi Sanal Makinede Çalıştırma

Kısacası: yapılabilir ve işe yarar! Not: Her zaman olduğu gibi, iyi bir bilgisayara veya iyi bir sunucuya ihtiyacınız var. [VMware](https://backupchain.com/en/vmware-backup/) Workstation'ı kurun ve bir VM oluşturun. Henüz başlatmadığınızdan emin olun!

* ekleyin. Yeni sanal makinenin VMX dosyasına aşağıdaki satırları ekleyin:

Ardından VM'yi başlatın, Windows'u yükleyin ve işiniz bitti!

Temel olarak, muhtemelen denediğimiz gibi Hyper-V ile ana bilgisayar olarak çalışmıyor, ancak VMware Workstation 8, 9 ve 10 çok iyi çalıştı.

VMware'de birden çok Hyper-V VM'si barındırmak ve VM'ler eklemek istiyorsanız, önce iyi bir bilgisayara ihtiyacınız vardır. Yeterli RAM bir zorunluluktur ve iyi bir şerit RAID veya süper hızlı SSD sabit disk kesinlikle yardımcı olacaktır!

Yazılım testlerini ve benzerlerini çalıştırmak için bu oldukça yararlı bir senaryodur. Elbette, bazı BT yöneticileri inleyecek, bu desteklenmeyen bir senaryo, ancak [Backup Chain](https://backupchain.com/en/cloud-backup/) denemeyi seviyor. İnovasyon başarısızlık riski taşır, ancak başarıya 😉
odaklanmayı seviyoruz VM'leri iç içe barındırmak istiyorsanız, yukarıdaki numara artık Windows Server 2016'dan çalışmıyor. Hyper-V yedeklemeniz için gerçekten yazılımınız var mı?
 
 mce.enable = "TRUE"
 
 hypervisor.cpuid.v0 = "FALSE"
 
 vhv.enable = "TRUE" 
