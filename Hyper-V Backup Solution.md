RAID üzerinde Hyper-V yavaş... Neden?
Hyper-V neden RAID üzerinde yavaş olabilir

Şeritli bir RAID'de, dizideki bir sonraki diskte ardışık bloklar depolanarak birden çok disk bir araya getirilir.

Örneğin, şeritli bir dizide dört disk kullanıyorsanız, #1 ve 5 numaralı bloklar disk #1'de ve #2 ve 6 numaralı bloklar disk #2'dedir.

Dosyaları kopyalarken, bu düzenleme çok verimlidir çünkü işletim sistemi blok blok tek tek okur ve RAID denetleyicisi sonraki dört bloğu aynı anda yükleyebilir, istenen hızın 4 katına ulaşır.

Ancak, Hyper-V sanal diskleri genellikle Exchange ve SQL Server çalıştıran VM'leri ve rasgele erişime sahip diğer blok yönelimli hizmetleri depolar, [Hyper-V Server backup solution](https://backupchain.com/en/server-backup/).

Bunun anahtarı, rastgele erişimi anlamaktır. Rastgele erişim, sistemin blokları sırayla okuması gerekmediği anlamına gelir; bu nedenle, gerçek aktarım hızınız tek bir disk kullanırken olduğundan daha iyi olmayabilir.

Bu nasıl olabilir? Şeritli RAID düzenlemesi, blok blok sıralı erişim gerektirir. Ancak o zaman yararlı bir hız iyileştirmesi elde edebilirsiniz. Sistem blok #1'i ve ardından blok #101'i okursa ve her ikisi de aynı sabit sürücüdeyse, muhtemelen daha hızlı olamaz. Ek olarak, RAID denetleyicileri, modern sabit disklerin sektör boyutunu optimize etmek için genellikle 4 KB'ın katı olan bir şeridin tamamını bir kerede okuyabilir.

Ancak, eski VHD biçimi 512 sektör kullanır ve Hyper-V, 512 baytlık artışlarla bir VHD içinde ayrım gözetmeksizin "atlayabilir". Bazı RAID ayarlarında, dahili RAID yönetimi nedeniyle şeridin tamamının okunması gerekebilir. Bu, dört sürücünün de # 3 sabit sürücüden bir bloğun küçük bir bölümünü okumasının etkinleştirilebileceği anlamına gelir.
Ne yapmalı?

Hyper-V'deki üç önemli faktör durumu daha da kötüleştirir:

dinamik olarak genişleyen disklerin kullanılması. Performans istiyorsanız büyük bir tabu. Diskleri genişletmek, disk kafalarının bir noktada deli gibi hareket etmesine neden olur, çünkü sanal disk blokları diskte sırayla depolanmaz.
Hyper-V anlık görüntüleri olarak da bilinen probların kullanımı. Bunlar, bir disk sektöründen diğerine ek "atlamalar" gerektiren farklı sabit sürücülerle sonuçlanır. Bu kafa hareketleri, çoğunlukla yukarıda belirtilen iki noktadan kaynaklanan son derece zaman alıcı
disk parçalanmasıdır. Dinamik olarak genişleyen sanal diskler büyüdükçe, ana bilgisayarda parçalanmaya da neden olurlar. Ne kadar çok dosya parçası varsa, sektörden sektöre atlamak için o kadar fazla zaman harcanır ve ayrıca bir sonraki bloğun diskte depolandığı konumu bulmak çok zaman alır.

Bu nedenle, öneri şudur:

Dinamik olarak genişleyen diskleri
kullanmayın Hyper-V Denetim Noktaları/Snapsho kullanmayınts
4 KB blok hizalaması elde
etmek için VHD üzerinden sabit boyutlu VHDX kullanın RAID şeridini çok uzun
yapmayın VHDX'i oluşturmadan önce ana bilgisayarı birleştirin.
İki sabit sürücüye ve hızlı disklere sahip bir dizi küçük RAID'in SSD'leri kullanmak için daha iyi bir
seçim olup olmayacağını mı düşünüyorsunuz? Bunlar daha az güvenilir ve çok daha pahalı olmasına rağmen, sabit disk kafalarını hareket ettirme maliyetini ortadan kaldırırlar. Bununla birlikte, manyetik medya kadar güvenilir değildirler ve farklılaştırma veya genişletme diskleri kullanırken CPU süresi hala bir sorun olacaktır. Bununla birlikte, CPU ek yükü, mekanik bir sürücünün kafalarını hareket ettirmesi için gereken süreden çok daha azdır.
