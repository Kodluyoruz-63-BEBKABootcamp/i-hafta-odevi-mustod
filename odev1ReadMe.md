# Ödev 1
---------------------
## Hesaplarım

* [Github Hesabım](https://github.com/mustod)
* [Hackerrank](https://www.hackerrank.com/mustafadirier1)
* [Stack Overflow](https://stackexchange.com/users/19818250/mustafa-dirier)
* Visual Studio mustafa_dirier@outlook.com

---------------

## Docker ve Docker'a ait kavramlar nelerdir?
### Docker Nedir?

Docker en net tanımlamayla open source bir ‘container’ teknolojisidir. Docker, aynı işletim sistemi üzerinde, yüzlerce hatta binlerce birbirinden izole ve bağımsız containerlar sayesinde sanallaştırma sağlayan bir teknolojidir. Web uygulamalarımızın kolayca kurulumunu, testini, çalışmasını ve deploymentını sağlar. Bunun yanında sunucu maliyetlerini önemli ölçüde azaltır.

### Docker Daemon:

Hypervisor’ün dockerdaki karşılığıdır. Bütün CPU ve RAM vb gibi işletim sistemine ait işlerin yapıldığı bölümdür.

### Container Nedir:
Docker Daemon tarafından Linux çekirdeği içerisinde birbirinden izole olarak çalıştırılan process’lerin her birine verilen isimdir. Virtual Machine (Sanal Makina) analojisinde Docker’ı Hypervisor’e benzetirsek fiziksel sunucu üzerinde halihazırda koşturulmakta olan her bir işletim sisteminin (sanal sunucunun) Docker’daki karşılığı Container’dır.

### Image Nedir:
Containerlar layer halindeki Image’lardan oluşur. Docker Image ise containerlara kurulacak ve run edilecek olan uygulamaların veya OS’lerin image dosyalarıdır. Örnek verecek olursak mysql, mongodb, redis, ubuntu, mariadb.. Yüzlercesi mevcut. Buyrun: Docker Images List.
Fakat burada şöyle bir ayrıntı var. Aslında container içerisindeki imagelerin içeriklerinin ve tanımlamalarının gerekli tutulduğu bir dosya var. Bu dosyamızın adı: Dockerfile. Tamamen bu isimde, ne büyük ne de küçük harflerden oluşan, bir bakıma containerlar içindeki imagelerın registration’ını yapan bir dosya. Burda önemli nokta şu: Her bir image Dockerfile dediğimiz bu dosyanın altında tanımlanması zorunlu.

### Docker Registry Nedir:
Gelelim bence işin en zevkli kısmına. Tıpkı github gibi geliştiriciler açık kaynaklı olarak docker imagelerini yükleyerek ve DockerHub’ta paylaşarak imagelerin bizim de indirip kullanmamıza olanak sağlıyorlar. Kısaca imagelar Docker Registrylerde tutuluyor. 

komutu ile indirip artık bu image ile container oluşturabiliyorsunuz. Aslında github’a çok benziyor. Siz de kendiniz imageleri oluşturup yükleyip başkalarının da sizin yarattığınız imageları kullanmalarını sağlayabiliyorsunuz. İsterseniz Private olarak ta registerynizi tutabilirsiniz. Docker bu hizmeti de size sunuyor.

### Docker CLI Nedir:
Kullanıcının Docker Daemon ile konuşmasını sağlayan, docker komutlarının çalıştırıldığı CLI ekranıdır.

### Docker Compose Nedir:
Compose, birden fazla containere sahip docker uygulamalarını tanımlamak ve çalıştırmak için kullanılır. Compose ile uygulamanızın servislerini configure etmek için bir YAML dosyası kullanılır. Ardından, tek bir komutla configure ettiğiniz ayarlar ile tüm servislerinizi oluşturup ve başlatabilirsiniz.

>[Mustafa Alkan Medium Hesabı](https://medium.com/batech/docker-nedir-docker-kavramlar%C4%B1-avantajlar%C4%B1-901b37742ee0)

## Docker’ın Avantajları Nelerdir?

Docker saniyeler içerisinde başlar, çünkü içerisinde barındırdığı her bir container sadece birer processtir. Böylece karşımıza lightweight bir yapı karşımıza çıkar. Bu da bizi sanal makinelerin hantallığından kurtarmış oluyor aslında :)

### Daha hızlı deployment süreci:
İşte bence en önemli avantajı diyebilirim docker için. Dockerı kullanmak için yeni bir environment kurmaya gerek yoktur. Farklı sunucularda çalışmak isteyen developerlar sadece docker imageleri indirip o sunucuda imageleri çalıştırmaları yeterlidir. Böylece ‘benim makinemde çalışıyordu, sunucuda neden çalışmıyor!’ gibi sorunlardan da kurtulmuş oluruz :)

### Daha Kolay Yönetim ve Ölçeklendirme: 
Bir sanal makineye göre docker üzerindeki containerleri çok daha kolay bir şekilde çalıştırabiliriz veya istediğimiz zaman yok edebiliriz. Containerleri manage etmek için farklı toollar mevcut. En çok ta Orchestrator diye nitelendirdiğimiz Kubernetes teknolojisi daha popüler olarak kullanılıyor. Kubernetes, kısaca container kullanan uygulamaların dağıtımını, ölçeklendirmesini ve yönetilmesini otomatik hale getiren açık kaynak kodlu bir sistem. Kubernetes mimarisini ve çalışma sistemini detaylı olarak öğrenmek isterseniz sizin için çok faydalı olacağını düşündüğüm bir linki bırakıyorum: https://www.mshowto.org/kubernetes-nedir.html

### Daha İyi Kaynak Kullanımı:
Sanal makinelere göre tek bir sunucu üzerindeki kaynak tüketimi dockerda çok daha verimlidir. Daha az kaynak tüketimi ile daha fazla containeri çalıştırabiliriz.

### Deployment Verimliliği:
Dockerın en güzel yanlarında birisi de şu: Siz localinizde test ettiniz, uygulamanızı Test veya Live ortamınıza attınız. (veya daha çeşitli ortamlar (dev, staging, pre-prod vs..) Localde çalıştırdığınız her şey burada da aynı şekilde çalışacak. Container ve Imagelerin tutulduğu dockerfile’ları da Git üzerinde tutmanız işinizi daha da kolaylaştıracağından eminim.

### Farklı İşletim Sistemlerine Destek Vermesi

Docker Windows, Linux, MacOs gibi farklı işletim sistemlerine destek verir.

### Popüler Cloud Servislerle Entegre Edilebilir. 
Docker , AWS, Microsoft Azure, Ansible, Kubernetes, Istio ve daha fazla tool ve cloud hizmetlerle entegre şekilde çalışabilir.

>[Mustafa Alkan Medium Hesabı](https://medium.com/batech/docker-nedir-docker-kavramlar%C4%B1-avantajlar%C4%B1-901b37742ee0)

----------------------

## .Net Core versiyonları ve bu versiyonlar arasındaki farklar nelerdir?

![Sürüm geçmişi](https://i.hizliresim.com/EkGf1e.png)

>Vikipedia

### .NET Framework
Windows ve Web uygulamalarını destekler. Bugün, .NET Framework'te Windows uygulamaları oluşturmak için Windows Forms, WPF ve UWP'yi kullanabilirsiniz. ASP.NET MVC, .NET Framework'te Web uygulamaları oluşturmak için kullanılır.

### .NET Core
Windows, Mac ve Linux dahil tüm işletim sistemleri için uygulamalar oluşturmaya yönelik yeni açık kaynaklı ve platformlar arası çerçevedir. .NET Core yalnızca UWP ve ASP.NET Core'u destekler. UWP, Windows 10 hedefleri Windows ve mobil uygulamalar oluşturmak için kullanılır. ASP.NET Core, tarayıcı tabanlı web uygulamaları oluşturmak için kullanılır. 

> [Mahesh Chand, C# Corner](https://www.c-sharpcorner.com/article/difference-between-net-framework-and-net-core/#:~:text=NET%20Core-,is%20the%20new%20open%2Dsource%20and%20cross%2Dplatform%20framework%20to,build%20browser%2Dbased%20web%20applications.)

![sadasd](https://i.hizliresim.com/sLuNC0.png)

>Vikipedia

## .Net 5 geçilme ihtiyaçları nelerdir, geçiş sürecinin tamamlanmasıyla neler hedeflenmektedir.

İleride yalnızca bir .NET olacak ve bunu Windows, Linux, macOS, iOS, Android, tvOS, watchOS ve WebAssembly ve daha fazlasını hedeflemek için kullanabileceksiniz.

![](https://i.hizliresim.com/PLDqau.png)

.NET 5 = .NET Core vNext
.NET 5, .NET Core ile bir sonraki adımdır. Proje, .NET'i birkaç temel yoldan iyileştirmeyi amaçlamaktadır:

* Her yerde kullanılabilen ve tek tip çalışma zamanı davranışlarına ve geliştirici deneyimlerine sahip tek bir .NET çalışma zamanı ve çerçevesi oluşturun.
* .NET Core, .NET Framework, Xamarin ve Mono'dan en iyi şekilde yararlanarak .NET'in yeteneklerini genişletin.
* Bu ürünü, geliştiricilerin (Microsoft ve topluluk) birlikte çalışıp genişleyebilecekleri ve tüm senaryoları iyileştiren tek bir kod tabanından oluşturun.

NET Core hakkında sevdiğiniz her şey var olmaya devam edecek:

* GitHub'da açık kaynak ve topluluk odaklı.
* Çapraz platform uygulaması.
* Windows'ta Windows Forms ve WPF gibi platforma özgü yeteneklerden ve Xamarin'den her yerel platforma yerel bağlamalardan yararlanma desteği.
* Yüksek performans.
* Yan yana kurulum.
* Küçük proje dosyaları (SDK tarzı).
* Yetenekli komut satırı arayüzü (CLI).
* Visual Studio, Mac için Visual Studio ve Visual Studio Code entegrasyonu.

İşte yeni olacaklar:

* Çalışma zamanı deneyimleri hakkında daha fazla seçeneğiniz olacak (daha fazlası aşağıda).
* Java birlikte çalışabilirliği tüm platformlarda mevcut olacaktır.
* Objective-C ve Swift birlikte çalışabilirliği, birden çok işletim sisteminde desteklenecektir.
* CoreFX, .NET'in statik derlemesini (önceden - AOT), daha küçük ayak izlerini ve daha fazla işletim sistemi için desteği desteklemek üzere genişletilecektir.

![](https://i.hizliresim.com/C86p9i.png)

>[Introducing .NET 5](https://devblogs.microsoft.com/dotnet/introducing-net-5/)

## Markdown yazımı ve kullanımı

Hazırlığım ödevi Markdown Pad 2 IDE'si üzerinden hazırladım.

## Yazılım alanında takip ettiğiniz kişiler kimlerdir?

* [Hakkı Sağdıç](https://github.com/hakkisagdic) 
* [Mert Çobanoğlu](https://github.com/cobanov)
* [Atıl Samancıoğlu](https://github.com/atilsamancioglu)
* [Fuat Beşer](https://github.com/fuatbeser)
* [Engin Demiroğ](https://github.com/engindemirog)

## Microsoft Azure tarafında ne gibi hizmetler vardır?
### 1. Uygulama Geliştirme
* Azure yönetilen veritabanları
* Geliştirme ve test
* DevOps
* DevSecOps
* E-ticaret
* Oyun geliştirme
* Nesnelerin İnterneti
* Hızlı uygulama geliştirme
* Mikro hizmet uygulamaları
* Cep Telefonu
* Modern uygulama geliştirme
* Sunucusuz bilgi işlem
* Azure’daki mesajlaşma hizmetleri


### 2. Yapay Zeka
* Yapay Zeka
* Bilgi araştırma

### 3. Buluta Geçiş
* .NET uygulamaları geçişi
* Azure’a geçiş merkezi
* Geliştirme ve test
* Linux geçişi
* Ana bilgisayar geçişi
* Azure üzerinde SAP
* SQL Server geçişi
* Windows Server geçişi

### 4.Veri ve Analiz
* Blok zinciri
* İş zekası
* Bulut ölçeğinde analiz
* Nesnelerin İnterneti
* Daha güvenli çalışma alanı için Azure IoT
* Akıllı alanlar için Azure IoT

### 5. Hibrit Bulut ve Altyapı
* Yedekleme ve olağanüstü durum kurtarma
* Yüksek performanslı bilgi işlem (HPC)
* Hibrit bulut çözümleri
* Ultra düşük gecikmeli uç bilişim
* İş açısından kritik uygulamalar

### 6. Güvenlik ve idare
* Azure idaresi
* Yedekleme ve olağanüstü durum kurtarma
* Gizli bilgi işlem
* Azure ağ güvenliği

### 7.Sektör Çözümleri
* Enerji
* Finansal hizmetler
* Oyun geliştirme
* Kamu
* Sağlık ve yaşam bilimleri
* Üretim
* Medya ve eğlence
* Perakende

>[Microsoft Azure Solution](https://azure.microsoft.com/tr-tr/solutions/)

## Beğendiğiniz beş tane iş ilanı
Araştırdım farklı ve beğendiğim bir iş ilanı bulamadım. İş ilanından ziyade, benim için önemli olan firmanın konumu, çalışma ortamı, bilgi alabilirsem çalışanlardan işi ve işyeri hakkında düşünceleri.

## Github ile alakalı, takip ettiğiniz üzerine çalışılabileceğini düşündüğünüz repositorylerin listesi
* [Github Hesabım, Repositories](https://github.com/mustod?tab=repositories)

## Kodun kalitesinin metrik olarak ölçülmesinden ne anlamaktasınız?

Metrikler yazılımın ya da işlemlerin verilen özniteliklerin hangilerine sahip olduklarını gösteren nümerik ölçülerdir. Metriklere örnek olarak; “her bin satır koddaki hata sayısı”, “ortalama yazılım modülü boyutu”, verilebilir. Metrikler yazılım yaşam süreci boyunca toplanır ve analiz edilirler ve bize aşağıda verilen konularda yardımcı olurlar;

*  Yazılım kalite seviyesinin belirlenmesi
*  Proje zamanlama kestirimi(tahmin)
*  Zaman ilerlemesinin izlenmesi
*  Yazılım boyutu ve karmaşıklığının hesaplanması
*  Proje maliyetinin belirlenmesi
*  Süreçlerin iyileştirilmesi


 Yazılım kalite seviyesi ve proje maliyeti gibi amaçlar yeterince açıklanmadığı zaman, farklı yorumlara konu olabilir. Bu farklılıklar da karışıklığa ve çatışmaya sebep olabilirler. Örneğin, “uygulama çok nadiren çökmeli” şeklinde yapılan bir tanımlama yeterince belirli değildir. Burada “çok nadiren” kelimesini nasıl ölçeceksiniz? Bir günde bir mi?, hafta da bir mi? Ya da yılda bir mi?... Daha kesin bir amaç, “Uygulama yılda 3 defadan fazla çökmemelidir” şeklinde verilebilir. Bu şekilde belirtildikçe, amaç farklı yorumlara sebep olmaz ve daha ölçülebilir olur. Bir projeye görünürlük sağlamak için ölçülebilir, nesnel ölçütler olmadan projenin ilerlemesini ölçmek zordur; zamanında olup olmadığını, kalite hedeflerini karşılayıp karşılamadığını, müşteriye sevke hazır olup olmadığını… Ek olarak, “ölçemediğini geliştiremezsin”.

 Devamı olarak, bir organizasyonun süreçlerinin veya bir yazılımın geliştirilmesi, metriklerin toplanmasına ve nicel geliştirme amaçlarının belirlenmesine bağlıdır. Başarılı bir değerlendirme için, metrik toplama projenin başlangıcında başlamalı ve tüm yazılım yaşam döngüsü süresince, bakıma kadar devam etmelidir. Metriklerin toplanması ve analizi, önemli miktarda yönetimsel ve mühendislik çabası gerektirmektedir ancak ödemeler de buna değer durumdadır.

Kalite ise hangi yazılımın gereksinimlerini karşıladığının bir ölçüsü olduğundan dolayı, uyum derecesini ölçmemiz gerekmektedir. Yazılım kalite metriklerinin bir kümesini oluşturmakta yarar vardır. Bunlar proje için toplanan metrikler olup, tüm metriklerin bir alt kümesi olacaktır. Bu metrikler özel olarak yaşam döngüsü boyunca kullanılan yazılım kalite karakteristiklerine odaklanmışlardır.

#### Yazılım kalite metriklerinden en önemlileri aşağıda sıralandığı gibidir;

##### 1.Hata yoğunluğu

Hata yoğunluğu, yazılımın boyutuyla ilişkili olarak hataların sayısını ifade eder. Boyut tipik olarak binlerce satır kod (KLOC) şeklinde ifade edilir, dolayısıyla hata yoğunluğu hatasayısı/KLOC olarak ifade edilebilecektir. Hatanın kullanıcı gereksinimlerinden herhangi bir sapma olduğunu hatırlayınız. Bu yüzden hata yoğunluğu kalite ölçümü için kullanılan en önemli metriklerden biridir. Genel olarak yüksek hata yoğunluğu, düşük kalite demektir. Şirketler tipik olarak hataları türüne göre ve şiddetine göre karakterize ederler ki göreceli olarak önemlerine göre ayırt edilebilsin. 

Aşağıdaki örnek yüksek şiddette bir hatanın nasıl tanımlanabileceğini ve kalite amacını tanımlamaktadır:
 Bir sınıf bir hata, yazılım gereksinim şartnamesinin üçüncü bölümüne göre memnuniyeti karşılamak için başarısızdır. Uygulama 5 sınıftan oluşabilmekte ve ilk ayda her 1000 kullanıcı için 1 hata raporundan başka işlem yapamamaktadır.

##### 2.Sistem Güvenilirliği

Güvenilirlik sistemin uygunluğu ya da belirlenen bir peryotta sistem çökmesinin sıkılığıdır. Tipik olarak bu durum sistem çökmesi için ortalama zaman(MTTF) olarak kullanılır ve sistem çökmeleri arasındaki geçen zaman miktarıdır. MTTF emniyetle ilgili sıklıkla kullanılan bir metriktir(havayolu trafik kontrol sistemi, havacılık elektroniği ve silahlar).


Örneğin U.S hükumeti hava yolu trafik kontrol sistemini yıllık bazda üç saniyeden daha fazla erişilmez olmamasını görev kabul eder. Bir başka örnek hücresel ağlarda kullanılan iletişim anahtarlarında görülebilir. Büyük network sağlayıcılar, bu cihazların yılda %99.999 oranında erişilebilir olmasını görev sayar. Bu yılda 5 dakika 15 saniye kesinti anlamına gelmektedir. Okuyucu MTTF için neden %100 değil diye sorabilir. Cevap genel olarak bu oranın elde edilebilir olmadığıdır.

##### 3.Müşteri problemleri

Müşteri problemleri, müşterinin ürünü kullanırken aldığı tüm problemlerin sayısıdır. Problemlerden bazıları yazılımdaki geçerli hatalardan kaynaklanabilir. Diğer bazıları hata kaynaklı olmayabilir, kafa karıştırıcı kullanıcı ara yüzü, zayıf hazırlanmış dökümantasyon veya hataları çoğaltmak(yinelenen)(çoktan rapor edilmiş ve çözülmüş ama raporlama biriminin bilmediği hata) gibi sebeplerden dolayı olabilir. Yinelenen hatalar bir hatanın ne kadar yaygın olduğunun en iyi göstergesi olabilir. 

Bunlar farklı kullanıcılar tarafından karşılaşılan aynı hatalardır. Tüm bu durumlarda, problem bir hatadan kaynaklı olsun veya olmasın, müşteriler kullanışlılık problemi olarak algılanan sorunlarla karşılaşıyorlar ve sonuç olarak yazılımdan memnun olmuyorlar. Bu da müşteri problemlerini en önemli kalite göstergesi yapmaktadır. Bu metrik tipik olarak problem/kullanıcı/aylar ile ifade edilir. Bu ve diğer metrikler yazılım ürünü teslim edildikten sonra bölüm 7 de tartışıldığı gibi test ve bakım aşamasında toplanabilir.


##### 4.Uyumluluk (Cohesion) 


Bunge benzerliği σ(), iki varlık arasındaki özellik kümesinin kesişimi olarak adlandırılmaktadır. Benzerliğin bu genel tanımından yola çıkarak metotlar arasındaki benzerliğin derecesi, bu iki metot tarafından kullanılan nitelik değişkenleri kümesinin kesişimi olarak tanımlanmaktadır. Elbette metodun kullandığı nitelik değişkenleri metodun özellikleri değildir ama nesnenin metotları, kullandığı nitelik değişkenlerine oldukça bağlıdır.σ(M1,M2), M1 ve M2 metotlarının benzerliği, {Ii} = Mi metodu tarafından kullanılan nitelik değişkenleri olmak üzere σ(M1,M2) = {I1} n {I2}’dir.Metotların benzerlik derecesi, hem geleneksel yazılım mühendisliğindeki uyumluluk kavramı ile hem de kapsülleme ile ilişkilidir.

Metotların benzerlik derecesi, nesne sınıfının uyumluluğunun başlıca göstergesi olarak kabul görülebilir. Uyumluluk bir sınıftaki metot ve niteliklerin birbirleriyle ilgili olmasının ölçüsüdür. Bir sınıftaki metot parametrelerindeki ve nitelik tiplerindeki güçlü örtüşme iyi uyumluluğun göstergesidir. Eğer bir sınıf aynı nitelik değişkenleri kümesi üzerinde farklı işlemler yapan farklı metotlara sahipse, uyumlu bir sınıftır. Eğer bir sınıf birbiri ile ilgili olmayan işler yapıyorsa, birbirleriyle ilgili olmayan nitelik değişkenleri barındırıyorsa veya çok fazla iş yapıyorsa sınıfın uyumluluğu düşüktür.

##### 5.İşlevsellik
Yazılımın ihtiyaçları karşılama becerisi olarak tanımlanmaktadır. Uygunluk, doğruluk, birlikte çalışılabilirlik ve güvenlik konuları bu sınıf altında incelenmektedir.

##### 6.Karmaşıklık (Complexity) 

Karmaşıklık, sınıfların iç ve dış yapısını, sınıflar arası ilişkileri kavramadaki zorluğun derecesidir. “Bir nesnenin karmaşıklığı bileşiminin çokluğudur. Buna göre karmaşık bir nesne çok özelliğe sahip olur. Tanımdan hareketle (x, p(x)) nesnesinin karmaşıklığı özellik kümesinin kardinalitesi yani |p(x)| olur.

##### 7. Code Coverage
Yazılan testlerin kodun ne kadarını kapsadığını ölçer. Code Coverage için %80 gibi bir oran oldukça iyi gibi görünse de aslında az sayıda basit test yazarak dahi bu orana ulaşılabilmesi bir hayli kolaydır. Bu sebepten Code Coverage oranının %100 olması beklenmektedir.



##### 8.Güvenilirlik
Yazılımın düzgün çalışma halini muhafaza edebilme becerisi olarak tanımlanmaktadır. Olgunluk, hata toleransı ve geri kurtarma konuları bu sınıf altında incelenmektedir.

##### 9.Kullanılabilirlik
Yazılımın kullanım kolaylığı sağlayan yetenekleri olarak tanımlanmaktadır. Öğrenebilme, anlaşılabilirlik, işletilebilirlik ve kullanıcı etkileşimi konuları bu sınıf altında incelenmektedir.
  
##### 10.Verimlilik
Yazılımın ihtiyaç duyulan ölçüde yeterli performansla çalışabilme becerisi olarak tanımlanmaktadır. Zaman ve kaynak kullanımı konuları bu sınıf altında incelenmektedir.


##### 11.Bakılabilirlik
Yazılımın değişiklik veya düzeltme isteklerine adaptasyon yeteneği olarak tanımlanmaktadır. Değiştirilebilirlik, test edilebilirlik, analiz edilebilirlik ve bağışıklık konuları bu sınıf altında incelenmektedir.


##### 12.Taşınabilirlik
Yazılımın çalıştığı ortam değişikliklerine uyum sağlayabilme yeteneği olarak tanımlanmaktadır. Adaptasyon yeteneği, yüklenebilirlik özellikleri, ortam değiştirme imkânı ve diğer yazılımlarla uyum konuları bu sınıf altında incelenmektedir.


##### 13. Müşteri Memnuniyeti
Müşteri memnuniyeti metrikleri yaygın olarak müşteri memnuniyeti anketleri sayesinde toplanırlar. Cisco System gibi şirketler [5] müşterilerinden memnuniyet ölçüsü olarak 5 üzerinden bir geri besleme alırlar (5=çok memnun, 1=çok memnuniyetsiz).

IBM CUPRIMDSO kategorilerini kullanır (Yetenek/fonksiyonellik, kolay kullanım, başarım, güvenilirlik, bakım kolaylığı, yüklenebilirlik, dökümantasyon, servis, ayrıntılı tasarım). Hewlett-Packard FURPS(Fonksiyonellik, Kolay kullanım, güvenilirlik, başarım ve servis) metriğini kullanır [4]. Bu anketlerin sonucu ilgili şirketlerin kendi önceliklerini geliştirmeleri için yönlendirici olarak kullanılır.


##### 14.Nesne Sınıfları Arasındaki Bağımlılık (Coupling Between Object Classes – CBO)

Sınıfın bağımlı olduğu sınıf sayısıdır. Bu metrikte, bir sınıf içinde nitelik ya da metotlar diğer bir sınıfta kullanılıyorsa, iki sınıf arasında bağımlılık olduğu kabul edilmiştir. Sınıflar arasındaki aşırı bağımlılık modüler tasarıma zarar verir ve tekrar kullanılabilirliği azaltır. Bir sınıf ne kadar bağımsızsa başka uygulamalarda o kadar kolaylıkla yeniden kullanılabilir. Bağımlılıktaki artış, değişime duyarlılığı arttıracağından, yazılımın bakımını zorlaştırır. Bağımlılık aynı zamanda tasarımın farklı parçalarının ne kadar karmaşık test edileceği hakkında fikir verir. Bağımlılık fazla ise testlerin daha özenli yapılması gerektiğinden test maliyetleri artacaktır.


##### 15.Sınıfın Ağırlıklı Metot Sayısı (Weighted Methods per Class – WMC)

Bir sınıfın tüm metotlarının karmaşıklığının toplamıdır. Tüm metotların karmaşıklığı 1 kabul edilirse, sınıfın metot sayısı olur. Sınıfın metotlarının sayısı ve metotlarının karmaşıklığı, sınıfın geliştirilmesine ve bakımına ne kadar zaman harcanacağı hakkında fikir verebilir. Metot sayısı çok olan taban sınıflar, çocuk düğümlerde daha çok etki bırakırlar; çünkü tanımlanan tüm metotlar türetilen sınıflarda da yer alacaktır. Metot sayısı çok olan sınıfların uygulamaya özgü olma ihtimali yüksektir. Bu nedenle tekrar kullanılabilirliği düşürürler.


##### 16.Metotların Uyumluluğu (Lack of Cohesion in Methods – LCOM)

Bu metriğin birden çok tanımı olmakla birlikte ilk kez kullanılanı şu şekildedir: C1 sınıfının M1, M2, …, Mn metotları olduğunu ve {li} kümesinin de Mi metodunda kullanılan nitelik değişkenleri kümesi olduğunu kabul edelim. Bu durumda LCOM bu n kümenin kesişiminden oluşan ayrık kümelerin sayısıdır. Daha sonra bu tanım yenilenerek şu şekle getirilmiştir: P hiçbir ortak nitelik değişkeni paylaşmayan metot çiftlerinin kümesi, Q en az bir ortak nitelik değişkeni paylaşan metot çiftlerinin kümesi olsun. Bu durumda LCOM, |P| > |Q| ise |P|-|Q|, aksi halde 0 olur. Bunlarla birlikte literatürde farklı tanımlar da mevcuttur. Sınıfın uyumluluğunun düşük olması, sınıfın iki veya daha fazla alt parçaya bölünmesi gerektiğini gösterir. Düşük uyumluluk karmaşıklığı arttırır, bu nedenle geliştirme aşamasında hata yapma ihtimali yükselir. Ayrıca metotlar arasındaki ilişkisizliklerin ölçüsü sınıfların tasarımındaki kusurların belirlenmesinde de yardımcı olur.

##### 17.Specialization Index (SIX)

Kod karmaşıklığını ve bakım maliyetlerini arttırmasından dolayı overload edilmiş fonksiyon sayısının mümkün olduğunca az olması istenir.
Bundan dolayı SIX = (Overload Edilmiş
Metot Sayısı * DIT) / NOM şeklinde
hesaplanır. 1.2 (veya %120)'ye kadar
normal kabul edilir.
Nesne Yönelimli Metrikler
Alt Sınıf Sayısı ( Number of Children - NOC)
NOC metriği sınıftan türemiş alt sınıflarının sayısını verir.
Alt sınıf sayısı çoğaldıkça kalıtım özelliğine bağlı olarak yeniden kullanımın arttığı anlaşılır.
 
·Alt sınıf sayısının çokluğu sınıfın hatalı soyutlama yapıldığını , belki de hatalı bir hiyerarşi kurulduğunu gösterebilir.
NOC sınıfın nüfus alanı hakkında bir fikir verir.NOC metriği yüksek sınıflar gözden geçirme , test gibi süreçlerin daha dikkatli ve uzun tutulması gereken yerlerdir.
##### 18.Kod Büyüklüğü (Lines Of Code LOC)
Geleneksel olarak yazılımın boyutu satır
sayısı ile ölçülür. Satır büyüklüğü çeşitli şekillerde ölçülür :Satır Sayısı ( Lines Of Code – LOC ) ölçümü programın tüm satırlarının sayılmasıdır.
Yorum ve boşluk içermeyen (Non-comment Non-blank NCNB veya Source Lines Of Code SLOC ) programın yorum satırları ve boş satırlardan arındırılmış halidir.
Çalıştırılabilir yordam sayısı (Executable Statements EXEC) program içinde yer alan yordam sayısıdır.
##### 19.Yorum Oranı (Comment Percentage - CP)
Yorum oranı (Comment Percentage CP) programın için hazırlanmış yorum satırlarının (kod ile birlikte ya da dışarıda) , toplam programın yorum ve boşluk içermeyen satır sayısına (SLOC) bölümü ile bulunur.Yüksek yorum oranı programların anlaşılabiliğini arttıran ve bakımını kolaylaştıran bir faktördür. Yorum oranının %20 ila %30 arası olması tavsiye edilen bir durumdur.

##### Kaynaklar

1. U. Erdemir, U.Tekin, F.Buzluca, “Nesneye Dayalı Yazılım Metrikleri ve Yazılım Kalitesi” Yazılım Kalitesi ve Yazılım Geliştirme Araçları Sempozyumu (YKGS08), İstanbul, 2008.
2. Doç Dr. Feza Buzluca, İTÜ, BLG468E Object-Oriented Modeling and Design ders notları  http://ninova.itu.edu.tr/tr/dersler/bilgisayar-bilisim-fakultesi/2097/blg-468e/ekkaynaklar/
3. [Demet Akyol Blogspot](http://demetakyol.blogspot.com/2019/03/yazlm-kalitesinin-degerlendirilmesi-ve.html)
