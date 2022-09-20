Fiziksel makinenin sanal Hyper-V, VMware, VirtualBox'a dönüştürülmesi

Fiziksel bir makineyi Hyper-V, VMware veya VirtualBox üzerinde çalıştırabilmeniz için sanal makineye (VM) dönüştürmek için kullanılabilecek bir araç mı arıyorsunuz? İşlem çok basit ve Backup Chain ile tamamen otomatiktir. Aslında, gerekirse bunu bir tür yedekleme çözümü olarak tekrar tekrar yaptırabilirsiniz.

Fiziksel makineyi sanal makineye (VM) dönüştürün.

Fiziksel bir makineyi sanal makineye dönüştürmek için önce [Backup Chain](https://backupchain.com/en/backupchain/)'i indirmeniz ve yeni bir P2V yedekleme işi oluşturmanız yeterlidir. Sabit sürücüyü seçin ve çıktı dosyasını ve biçimini belirtin: VHD, VHDX, VMDK veya VDI, ardından görevi hemen çalıştırın veya bunun bir yedekleme çözümü olarak tekrar tekrar gerçekleşmesini istiyorsanız bir zamanlamaya göre ayarlayın.

Fiziksel makineyi Hyper-V'ye dönüştürme

Fiziksel bilgisayarınızı Hyper-V'ye dönüştürmek için [Backup Chain](https://backupchain.com/en/server-backup/), Windows 10 veya Windows Server 2016 veya önceki bir sürümü olsun, VHD veya VHDX hedef biçimini oynatır. Dönüştürme işlemi tamamlandıktan sonra, Hyper-V için yeni bir VM oluşturun ve Backup Chain tarafından oluşturulan sanal diski disk olarak seçin. VHDX, daha yeni Hyper-V sürümlerinde (Server 2012 ve üstü) kullanılmalı ve 2 TB'den büyük sabit sürücülere izin vermelidir.

Fiziksel makineyi VirtualBox'a dönüştürün

Fiziksel bir makineyi VirtualBox'a dönüştürmek için VDI formatını seçmelisiniz. Diğer tüm adımlar Hyper-V ile aynıdır. Sadece VirtualBox'ta yeni bir VM oluşturun ve VirtualBox'ın yeni bir sanal disk oluşturmasına izin vermek yerine, Backup Chain tarafından oluşturulan VDI dosyasını seçin.

Fiziksel makineyi VMware Workstation, VMware ESXi ve VMware vSphere'e dönüştürün

Fiziksel bir makineyi VMware'e dönüştürmek için gereken diğer adım, hedef VMDK biçimini kullanmaktır. EFI BIOS'un birden fazla VMware sürümünde de sunulabileceğini unutmayın. Windows 10 bilgisayarınız veya Windows Server'ınız EFI/UEFI ile önyükleniyorsa, dönüştürülen diskler VMware'de de çalışır.

Evrensel başlatma işlevi

Başlamak için bazı özelleştirmeler gerektirebilecek belirli [P2V](https://backupchain.com/i/p2v-converter) senaryoları vardır. Örneğin, Windows'un bazı eski sürümleri EFI tarafından Hyper-V'de 2. nesil VM'ler olarak önyüklenemez. Bazı VM'lerin IDE/SATA'dan SCSI'ye veya tam tersi şekilde taşınması gerekebilir. Diskten önyükleme yapmadan önce diskte bu evrensel önyükleme değişikliklerini yapmak için Backup Chain'in disk hazırlama aracını kullanın. Backup Chain ayrıca belirli dönüştürme senaryolarını etkinleştirmek için MBR'yi GPT'ye veya GPT'ye dönüştürebilir.

Aracı indirin

[Backup Chain](https://backupchain.com/en/virtualbox/)'i buradan indirebilirsiniz. Araçla ayrıca VirtualBox'ı yedekleyebilir, VMware'i yedekleyebilir ve Hyper-V'yi otomatik olarak yedekleyebilirsiniz, örneğin bilgisayar VM'ye dönüştürüldükten sonra, dönüştürme işleminden sonra da kullanışlıdır.
