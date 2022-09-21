Sanal makineleri buluta yedeklemek istiyorsanız, VM bulut yedekleme sisteminizi planlarken göz önünde bulundurmanız gereken bazı konular şunlardır.

Önce bulut yedeklemesinin her iki tarafına da sahip misiniz yoksa bir yerden depolama alanı satın almanız mı gerekiyor? Bazı çözümler bu konuda esneklik sunarken, diğerleri sunmaz.

VM'ler buluta yedeklendiğinde, genellikle sektör düzeyinde yedeklenir. Bu, sanal sabit disklerin bölümlerinin buluta gönderildiği anlamına gelir. Çözüm, verilerinizi göndermeden önce şifreliyor mu ve bulut bağlantısı da şifreleniyor mu? Buluttaki yedekleme verileri şifreli kalır mı?

Sektör düzeyinde yedekleme birçok senaryo için iyi olsa da, dosya düzeyinde bir yaklaşım bazen daha iyidir ve/veya gerekirse yedeklenen verilere daha kolay erişim sağlar. Çözüm, buluttaki VM dosyalarına erişmek ve yedeklemek için VM'ye bir aracının yüklenmesini (ve ayrıca uzun vadede de korumanız gerektiğini) gerektiriyor mu?

Çözüm, yinelenen verileri yedekten kaldıran yinelenenleri kaldırma sağlıyor mu? Durum böyle değilse, tüm VM 'nin her seferinde yedeklenmesi gerekir. Hafıza da büyük ölçüde boşa harcanırdı.

Çözüm, İnternet bağlantısının bir an için kesilmesi veya sıfırdan yeniden yüklenmesi gibi bozuk bağlantıları etkili bir şekilde işleyebilir mi? Ayrıca bakınız [Virtual machine backup software](https://backupchain.com).


Sonunda herhangi bir nedenle sıkışıp kalırsanız size yardımcı olacak biri var mı? Azure veya S3 gibi genel depolama alanıyla kendi bulut sisteminizi oluşturmanın önemli bir sorunu, genellikle uygulamaya özel destek olmamasıdır. Belleğe özgü destek için ödeme yapmanız gerekir, ancak "homebrew" sisteminin (komut dosyaları veya çeşitli yazılım bileşenleri kullanılarak) en büyük dezavantajı, bakım ve sorun giderme için kaynak eksikliğidir.
