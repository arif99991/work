Cloud Backup'ın dezavantajları

Sunucu Bulut Yedeklemelerinin avantajları hemen hemen tüm yedekleme programı satıcıları tarafından tekrar tekrar ayrıntılı olarak tartışılırken, bulut yedekleme stratejisinin dezavantajlarını da göz önünde bulundurmak önemlidir.

Tüm teknolojilerin ve stratejilerin artıları ve eksileri vardır ve bulut yedeklemelerinin kendi avantajları vardır. İşletmeniz için bulut yedeklemeleri düşünüyorsanız, yerel yedeklemelerin diğer yedekleme stratejilerine göre kendi avantajları olduğundan, bulut yedeklemeleri yerel bir yedekleme stratejisini değiştirmemeli (değiştirmemelidir).
Ayrıca bakınız [Cloud backup Windows Server](https://backupchain.com/en/cloud-backup/).

Üçüncü taraf bağımlılığı

Bulut yedeklemeleri kullanışlıdır. Kırılırsa verileri depolamak veya değiştirmek için donanım satın almanız gerekmez. Ancak, bunu düzgün ve güvenilir bir şekilde yapması için sağlayıcınıza güvenirsiniz.

Birçok sağlayıcı bu noktada finanse edilen şirketlerdir ve finansman kesilirse bir gecede ortadan kaybolabilir. Bu, şirketin yatırımcılarının birleşme veya satın alma yapmadığı geçmişte de böyleydi. Bazen bir bulut sağlayıcısının devralması gerçekleşir, ancak hizmet sözleşmesi ve fiyatlar değiştirilir, böylece ihtiyaçlarınız için doğru sağlayıcıyı bulamazsınız. Sağlayıcınızdan memnun olmama ihtimaliniz bizi bir sonraki noktaya getiriyor: sağlayıcının değişmesi.

Sağlayıcıları değiştirirken karşılaşılan zorluklar

Tabii ki, bulut yedekleme sağlayıcılarının çeşitli yazılım bileşenlerini içeren kendi altyapıları vardır. Bu altyapı verimlidir, ancak aynı zamanda tescillidir. Bulut sağlayıcıları, müşterileriyle uzun vadeli ortaklıklarla ilgileniyorlar çünkü müşteri kazanımı genellikle pahalıdır (Google, bulut yedeklemeleriyle ilgili anahtar kelimeler için tıklama başına yaklaşık 100 ABD doları ücret alır). Bu nedenle, sağlayıcıları değiştirmenin acısız ve hızlı bir yolunu sağlayan pek çok açık standart olmaması şaşırtıcı değildir, çünkü bu bulut sağlayıcılarının çıkarına değildir.

Ancak, şirketinizin bulutta büyük miktarda verisi varsa, başka bir sorun daha vardır: bant genişliği. Ayrıca bakınız [Veeam alternative](https://backupchain.com/en/download/)


IsP ve bant genişliğine bağımlılık

Verimli bir şekilde bağlanamıyorsanız bulut depolama işe yaramaz, bu da yüksek hız ve düşük maliyet anlamına gelir. Şirketiniz her ay terabaytlarca veri üretiyorsa, tüm bu verilerin bir süre bekleme süresine izin vermek için oluşturulandan biraz daha hızlı yüklenmesi gerekir. İnternet bağlantılarını gerekli bant genişliğiyle dağıtmanız ve her ay bunlar için ödeme yapmanız gerekir, bu da yalnızca bir bulut yedekleme sisteminin genel maliyetini artırmakla kalmaz, aynı zamanda ISS'nize ve hizmet kalitesine bağımlılık yaratır.

Sağlayıcınız, bölgede ihtiyacınız olan bağlantı hızlarını uygun bir fiyata sunan tek kişiyse, er ya da geç tekellerinden yararlanma ve orta vadede fiyatları radikal bir şekilde artırma şansı vardır.

Bununla birlikte, şu anda ABD'deki bulut yedeklemeleriyle ilgili temel sorun, çoğu işletmenin uygun fiyatlı, yüksek bant genişliğine sahip bir internet bağlantısına erişememesidir. Genel bir kural olarak, her GB veri için, yüklemeyi makul bir süre içinde bir gecede tamamlamak için günlük Mbps yükleme hızı belirtmek istersiniz.

Bulut üzerinden Hyper-V yedeklemeleri, bulutta günlük olarak güncellenmesi gereken çok büyük dosyalarla ilgilenen bulut yedeklemelerinin ilginç bir alt kümesidir. Bulut yedekleme sağlayıcıları, bu tür Hyper-V yedeklemesini nispeten yavaş bağlantılar üzerinden gerçekleştirmenin yollarını bulmuş olsalar da (örneğin, adım adım Windows 10 Hyper-V yedeklemelerine bakın), kurtarma sorununun hala dikkate alınması gerekir.


Kurtarma Konuları

Yukarıdaki nedenlerden dolayı, çoğu bulut sağlayıcısı, kısa bir süre içinde büyük miktarda veriyi kurtarmanız gerekmesi durumunda kurye ile gönderilen harici sabit sürücüleri kullanarak tohumlama ve hızlı kurtarma sunar.

Internet bağlantıları yerel ağ bağlantıları kadar hızlı olsaydı, bu tür bir hizmet gerekli olmazdı. Bulut veri kurtarma, iyi İnternet bant genişliğinin kullanılabilirliğine bağlı olduğundan, bağımsız bir yedekleme stratejisi olarak uygun olmayabilir. Hızlı bir geri yükleme için, yerel bir yedeklemenin kullanılabilir olması en iyisidir. Bulut yedeklemeleri, doğal afetler, vandalizm, hırsızlık vb. gibi yerel depolamanın tahrip olduğu nadir durumlarda dikkate alınmalıdır.
