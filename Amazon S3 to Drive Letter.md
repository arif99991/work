Amazon S3'ten Sürücü Harfine

Amazon S3 kovanızı Windows'ta gerçek bir sürücü olarak eşlemek mi istiyorsunuz? Tam da bunu yapan iyi bir araç var [burada](https://doctorpapadopoulos.com/map-amazon-s3-bucket-as-a-real-drive/). S3 kovanızı bir sürücü olarak bağladıktan sonra, doğrudan erişmek için Windows'taki herhangi bir uygulamayı kullanabilirsiniz. Bu, komut isteminde ve toplu iş dosyaları ve PowerShell komut dosyaları, anti-virüs tarayıcıları vb. içinden bile çalışır. Kendi makinenizdeki bir yerel ağ sürücüsü gibidir, ancak gerçek bir fiziksel sürücü olarak görünür.

Örneğin, Amazon S3 kovanızı X:\ ile eşleyebilir ve ardından dosyaları elle indirmek ve yüklemek zorunda kalmadan Word belgelerini doğrudan içinde düzenleyebilirsiniz. Buna ek olarak, Windows Dosya Gezgini'nde tıpkı diğer sürücülerde olduğu gibi dosyaları kopyalayıp yapıştırabilirsiniz. Önerilen aracımızdaki güzel bir işlev de Senkronizasyon özelliğidir. Buluttaki dosyaları yerel kopyanızla veya tam tersi şekilde senkronize etmek için senkronizasyon görevlerini otomatik olarak veya bir düğmeye tıklayarak çalıştırabilirsiniz.

Önerilen yazılımımızı yükledikten sonra, 'site ekle' seçeneğine tıklayın ve aşağıdaki örnekte gösterildiği gibi tüm Amazon S3 bilgilerini girin:

Yukarıdaki örnek Amazon S3 kovamızı X: sürücüsüne eşler. Profili kaydedip bağlan'a tıkladığınızda, X: sürücüsü Windows Dosya Gezgini'nde açılacaktır. Daha sonra diğer sürücüler gibi çalışmaya hazır hale gelir.
Tüm Windows Platformlarında S3'ü Monte Edilmiş Ağ Sürücüsü Olarak Eşleme

Yazılım tüm Windows platformlarında çalışır. Windows 7'den Windows 11 PC'ye ve Windows Server 2008'den 2022'ye. Windows ile otomatik olarak başlatabilirsiniz ve isterseniz site otomatik olarak bağlanacak şekilde yapılandırılabilir.

Amazon'a Genel Bakış

Amazon Web Services (AWS), 2006 yılında çevrimiçi posta siparişi şirketi Amazon.com'un bir yan kuruluşu olarak kurulan ABD'li bir bulut bilişim sağlayıcısıdır. Dropbox, Netflix, Foursquare veya Reddit gibi birçok popüler hizmet Amazon Web Services'e dayanmaktadır. Gartner, 2017 yılında AWS'yi bulut bilişim alanında önde gelen uluslararası sağlayıcı olarak sıralamıştır.

Tarih

AWS, geliştiriciler için talep üzerine BT altyapısı sağlamak üzere 2006 yılında kuruldu; başlangıçtan itibaren odak noktası son kullanıcılardan ziyade işletmelerdi. Şirket, e-ticaret platformunun işletilmesi için küresel olarak dağıtılmış veri merkezlerine ve yüksek kullanılabilirliğe sahip hizmetlere ve Amazon Web Services ile üçüncü taraflara da sunulacak olan diğer uygulamalara yönelik arayüzlere ihtiyaç duyuyordu. Ancak Amazon, kapasitesini daha iyi kullanmak için bu adımı atmadı. İlk AWS sanal sunucu hizmeti, şirketin Güney Afrika'daki tesislerinden birinde tasarlandı.
Amazon Web Hizmetleri kısmen ücretsiz olarak sunulmaktadır. Kasım 2010'da şirket, bilgi işlem gücü (750 saat) ve diğer popüler AWS hizmetlerini sınırlı olarak içeren Ücretsiz Kullanım Katmanı adlı bir program başlattı. İlk yılın sonunda, müşteriler ticari bir plana geçmeli ve normal ücretleri ödemelidir. Ücretsiz koşulun sunulması, rakip şirket Rackspace tarafından özellikle desteklenen OpenStack'e karşı bir tepki olarak görülüyor.
Amazon ayrıca Almanya, Romanya ve Hollanda'da AWS için geleceğin teknolojileri üzerinde çalıştığı geliştirme merkezleri işletiyor. Grup, Frankfurt am Main'da üç veri merkezi işletmektedir.
Ekim 2021'de AWS, Birleşik Krallık'taki gizli veriler için bir bulut sistemi kurmak üzere Birleşik Krallık istihbarat servislerinden (MI5, MI6 ve GCHQ) büyük bir sözleşme aldı.

Bileşenler

Sunucu

EC2 (Elastic Compute Cloud), Linux veya Microsoft Windows Server dağıtımlarını çalıştıran sanal sunuculardır. Sabit bir sözleşme süreleri yoktur ve saat başına hatta saniye başına faturalandırılırlar. Aralarından seçim yapabileceğiniz, mevcut RAM ve sanal işlemcilere karşılık gelen bilgi işlem birimlerine göre farklılık gösteren çeşitli oranlar vardır. Diğer sağlayıcılarla karşılaştırıldığında, sanal makine örnekleri kalıcı değildir. Yani, örnek sonlandırıldığında RAM içeriği silinir.
Depolama

S3 (Basit Depolama Hizmeti), teorik olarak herhangi bir miktarda veriyi depolayabilen ve kullanıma göre faturalandırılan bir dosya barındırma hizmetidir. Erişim HTTP/HTTPS üzerinden yapılır. Amazon ilk olarak dizinlere ve dosyalara benzeyen ve diğer sağlayıcıların taklit ettiği standart haline gelen kova ve nesne kavramını tanıttı. Amazon ayrıca Elastic File System ile ağ sürücüleri ve Glacier ile dosya arşivleme imkanı da sunuyor. Amazon yüzde "99,9999999" veri saklama sözü veriyor.
Amazon Elastic Block Store (EBS), Amazon EC2 örneklerine eklenebilen blok düzeyinde depolama sağlar.



Büyük miktarda veri aktarımını kolaylaştırmak için AWS, Snowball hizmeti aracılığıyla kiralanabilir disk depolama alanı sağlamakta ve büyük miktarda veri paket hizmetleri aracılığıyla kopyalanıp geri yüklenebilmektedir. Çok büyük miktarda verinin (birkaç yüz terabayttan petabayta kadar) buluta aktarılması böylece çok daha hızlıdır.

ağ

CloudFront, EC2 veya S3 gibi diğer AWS hizmetlerinden gelen içeriği, erişim sürelerini azaltmak için küresel olarak dağıtılmış bir şekilde sunabilen bir içerik dağıtım ağıdır. Hizmet HTTP(S) protokolü ile sınırlıdır ve bölgeye bağlı olarak erişilen gigabayt bazında ücretlendirilir. Yapılandırmaya bağlı olarak, tek tek dosyalar veya tüm etki alanları CloudFront aracılığıyla, isteğe bağlı olarak SSL ile şifrelenerek sağlanabilir. Buna ek olarak Amazon, Route 53 adı altında IP adreslerinin ve alan adlarının karşılıklı olarak çevrilmesine olanak tanıyan bir alan adı hizmeti işletmektedir. Faturalandırma, kullanılan bölgelere göre aşamalı olarak yapılır.

Veritabanı

Sanal veritabanı olarak SimpleDB veya İlişkisel Veritabanı Hizmeti (kısaca RDS) kullanılabilir. İlki, nesneler ve özellikler şeklinde organize edilebilen basit - yani ilişkisel olmayan - bilgileri depolamak için tasarlanmıştır. Amazon'a göre SimpleDB hala beta test aşamasındayken, RDS resmi olarak desteklenmektedir. İlişkisel Veritabanı Hizmetleri MySQL, Microsoft SQL Server veya Oracle tabanlı sanal veritabanlarını içerir. SimpleDB yalnızca kullanılan bellek miktarına göre faturalandırılırken, Amazon RDS ücretleri seçilen örneğin bellek ve işlem gücüne dayanır.
Geliştirme

Amazon, Java, Python, Docker ve diğer platformlar için bir PaaS olan Elastic Beanstalk'ı sunmaktadır. Ayrıca, Basit İş Akışı Hizmeti (SWS), Basit E-posta Hizmeti (SES), Basit Kuyruk Hizmeti (SQS) veya Basit Bildirim Hizmeti (SNS) ile geliştiricilere daha fazla hizmet sağlanmaktadır. İkincisi, örneğin diğer AWS hizmetlerinden e-posta veya SMS yoluyla belirli olaylar hakkında bildirim göndermek için uygundur. Buna ek olarak, uygulamalar üçüncü taraflarca sipariş edilebilecekleri AWS Marketplace olarak adlandırılan Amazon Web Hizmetleri'nde dağıtılabilir.

Rehber

AWS Kimlik ve Erişim Yönetimi (IAM olarak adlandırılır), bir kuruluş içindeki kullanıcıları ve kaynakları yönetmeye yönelik bir dizin hizmetidir. Amazon IAM olmadan, herhangi bir AWS hizmetine giriş, yönetici ayrıcalıkları veren ve üretim kullanımında güvenlik riski oluşturabilecek kişisel bir Amazon hesabıyla sınırlıdır. Kimlik ve Erişim Yönetimi, kullanıcılar oluşturmak, onları gruplandırmak ve EC2 veya S3 gibi neredeyse tüm AWS hizmetlerine erişimlerini kontrol etmek için kullanılabilir.

Yönetim

Son yıllarda Amazon, temel teklifleri yönetmeye yarayan birçok web hizmeti geliştirdi. Örneğin, Mayıs 2009'da Amazon CloudWatch, EC2 üzerindeki sanal sunucuları izleme ve gerekirse seçilen tarifeyi ve kaynaklarını kullanıma (ölçeklenebilirlik) göre otomatik olarak ayarlama imkanı sunmuştur. 2012'nin başından bu yana, üçüncü taraf web sunucuları aracılığıyla uygulanan ve büyük hacimli verilerin aktarımını kolaylaştırmayı ve BT güvenliğini ve veri korumasını iyileştirmeyi amaçlayan Amazon Direct Connect ile Amazon Web Services'e özel ağ bağlantıları kurulabilmektedir.
Diğerleri

Diğer tüm hizmetler teknik hizmetlere dayanırken, Amazon Mechanical Turk (Turk şaftının İngilizce adından sonra) bir istisnadır: küçük görevlere bölünebilen ve insanlar tarafından işlenebilen işler burada yayınlanabilir. Bunlar arasında örneğin World Wide Web'de basit arama işleri veya münferit cümlelerdeki yazım hatalarının düzeltilmesi sayılabilir. Mekanik Türk, görüntülerdeki nesneleri (insanlar veya hayvanlar gibi) tanımak için de yaygın olarak kullanılmaktadır. Hizmet halen beta test aşamasındadır.



Eleştiri

Amazon Web Services'deki ciddi güvenlik açıkları defalarca fark edildi, bu nedenle platform uzmanlar tarafından kritik olarak görülüyor. Buna ek olarak, 2013 yılında Amazon'un CIA'den büyük bir sipariş aldığı ve halka açık bulutunu işleteceği öğrenildi ve bu da teklifin veri koruması konusunda daha fazla şüphe uyandırdı. Amazon, IBM ve diğer adaylara karşı AWS ile ödülü kazandı.
Aralık 2010'da Amazon Web Services, WikiLeaks tarafından kendi sunucuları üzerindeki yükü azaltmak için kısa bir süre kullanıldı. Bu sunucular diplomatik gönderilerin yayınlanması nedeniyle baskı altındaydı ve bazen artık hiç içerik sağlayamıyordu. Şirketten yapılan resmi açıklamaya göre Amazon, müşteri ilişkisinin ortaya çıkmasından kısa bir süre sonra WikiLeaks'e erişimi engelledi, çünkü burada "yasadışı materyaller" mevcuttu. Ancak gözlemciler, özellikle Senatör Joe Lieberman açısından siyasi baskının belirleyici neden olduğunu düşünüyor. Amazon'un bu kararı kamuoyunda tartışmalara yol açmış ve medyanın yoğun ilgisini çekmiştir.
Amazon, veri merkezlerini özellikle elektrik kesintilerine karşı endüstri standardı prosedürlere göre koruduğunu iddia ediyor. Ancak şirket, ciddi sorunların tekrar tekrar ortaya çıkması nedeniyle eleştirilmektedir. Örneğin, Ağustos 2011'de bir yıldırım düşmesi, İrlanda veri merkezindeki hizmetlerin kullanılamamasına neden olmuş ve bunun sonucunda diğer birçok çevrimiçi hizmet kesintiye uğramıştır. Bu dava, Amazon'un yanı sıra Microsoft'un da etkilenmesi nedeniyle yaygın ilgi gördü. Temmuz 2012'de de benzer bir arıza meydana gelmiş, bu arıza acil durum güç kaynağı tarafından giderilmiş, ancak kısa bir süre sonra bu güç kaynağı da teknik bir arızaya maruz kalmıştır. Üçlü bir kesintinin ardından Amazon, sistemlerini yeterince test etmemekle suçlandı. Daha yakın zamanda, Ağustos 2013'te yaşanan bir kesinti diğerlerinin yanı sıra Vine ve Instagram'ı da sekteye uğrattı. 



