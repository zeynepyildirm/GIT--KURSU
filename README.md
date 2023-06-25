# GIT--KURSU
GİT NEDİR?

Git, bir versiyon kontrol sistemidir. Yani kısacası zaman içinde kaynakta yapılan değişiklikleri kontrol etmeye yarayan araçtır. Git özellikle yazılım sektöründe çok yaygın bir şekilde kullanılır. Eğer yazılım sektörüyle ilgileniyorsanız giti öğrenmeden, gitin ne olduğunu bilmeden ilerleme kaydedebilmek çok zor, hatta imkansız denebilir çünkü birçok projede, birçok kısımda karşılaşılacaktır.

GİTE NEDEN İHTİYAÇ DUYARIZ?

Git, bir yazılım projesinde çalışıyorsak sıkça kullandığımız bir versiyon kontrol sistemidir. Gitin özellikle projelerde kullanılmasının ana sebepleri birden çok kullanıcının aynı anda proje üzerinde değişiklik yapabilmesi, yapılan değişikliklerin kolayca kaydedilmesi, projenin kolay bir şekilde depolanabilmesidir. Genel olarak baktığımızda Git’i bilmenin bir programlama dili bilmek kadar hatta daha fazla önemli olduğunu söyleyebiliriz. İşe alım süreçlerinde Git, GitHub,GitLab, Bitbucket kullanımı bilinmesi bizim için önem arz eder.

GİT KURULUMU (WINDOWS)

Giti aktif olarak kullanabilmek için öncelikle bilgisayara kurulum yapmak gerekmektedir. İlk olarak ‘Git download’ araması yaparak resmi siteye giriş yapmalıyız. ( https://git-scm.com/downloads )

Mavi ekran içindeki ‘Download’ yazısına tıklayarak indirebiliriz. Çıkan sayfada 32 ve 64 bitlik iki ayrı indirme seçeneği çıkacaktır. Bilgisayarımıza uygun olanı seçip indirmeliyiz. İndirmiş olduğumuz Git kurulum dosyasını çalıştırıyoruz. İlk açılan pencerede kullanım koşullarına ‘Next’ seçeneğine tıkladıktan sonra nereye kurulacağını gösteriyor, öyle kalabilir isterseniz değiştirebilirsiniz. O adımı da geçtikten sonra “Select Components” bölümü gelecektir yine varsayılan olarak kalabilir Next seçeneğine tıklayıp devam edebiliriz.

Bu adımdan sonra gelecek olan “Select Start Menu Folder” adımını da direkt olarak geçebiliriz. Daha sonraki adımda varsayılan olarak kullandığınız editörü seçmemiz gerekiyor. Biz Visual Studio Code’u bilgisayarımıza daha önceden indirip kullandığımız için “Use Visual Studio Code as Git’s default editor” seçeneğini seçtik. Siz isterseniz başka bir editör seçip o şekilde devam edebilirsiniz.

Metin editörünü seçtikten sonra karşımıza yandaki gibi bir ekran açılacak o ekranda Git’i ne şekilde kullanacağımızı seçmemiz gerekiyor. Önerilen seçenek olan “Git from the command line and also from 3rd-party software” seçiyoruz. Git’in ne olduğunu yeni öğrenmeye başladığınız için size de bunu seçmenizi öneriyoruz.

Daha sonrasında bağlantı sağlayacağımız yöntem olan “Use the OpenSSL Library” seçeneğini seçmemiz gerekiyor.

Herhangi bir değişiklik yapmaya gerek kalmadan “Checkout Windows-style, commit Unix-style line endings” seçeneğini seçerek devam ediyoruz

Karşımıza çıkan ekranda ‘Use MinTTY’ seçeneğini seçip devam ediyoruz. Bir sonraki sayfada da ‘Default’ seçeneğini seçiyoruz.

Hiçbir değişiklik yapmadan önerilen ayarı seçip devam edip bilgisayara kurulumunu tamamlayabilirsiniz. Genel olarak default’ları seçerek devam ettik. Böylece gitin bilgisayara kurulumunu tamamlamış olduk.

GIT KURULUMU (MAC)

Mac işletim sisteminizde XCode kurulu ise zaten varsayılan olarak Git sisteminizde kuruludur.

Macte terminal açmak için ‘command’ ve ‘space’ tuşlarına bastıktan sonra ‘Finder’ kısmına “Terminal” yazarak direkt Terminal açılımını yapabilirsiniz. Terminal, genel anlamda yazdığımız kodları işletim sistemi ile çalıştıran bir konsoldur. Bu terminalden bir Git versiyonunun olup olmadığını kontrol edebiliriz.

Eğer Terminalde Gitin yüklü olmadığını tespit ettiysek Gitin resmi sitesine giderek “Download for Mac” tuşuna basarak hangi indirme yöntemini kullanmak istiyorsak onu seçiyoruz ve kurulumu yapıyoruz. Yüksek olasılıkla bu indirme işlemine gerek kalmadan sistemde Git yüklü halde bulunur.

GİT KURULUMUNU TEST EDELİM

Açılan ekrana “ git version “ yazıyoruz. Aşağıda olduğu gibi sürüm yazıyorsa kurulumu başarıyla tamamlamışsınız demektir.

GİT NASIL KULLANILIR?

Git Projesi oluşturmak için öncesinde temel birkaç komutu inceleyelim:

Görseldeki gibi “pwd” komutu ile terminal üzerinde bulunduğumuz dizinin tam adresini alırız.

ls” komutu listelemek anlamına gelmektedir. Bize bulunduğumuz dizideki dosyaları ve dizimleri listeler.

“cd” komutu ise bize diziyi değiştirme imkanı sunar.cd den sonra bir boşluk bırakılıp gidilmek istenen dizinin adı yazılırsa ve onu da listelemek için o dizinin yanına “ls” yazılırsa o dizi listelenir.

Şimdi ise Git Projesi oluşturmaya başlayabiliriz

proje_dizin adlı bir klasör oluşturduğumuzu varsayalım.”cd proje_dizin” satırı bize bu proje_dizin içerisinde olduğumuzu anlatır. Bunun bir Git projesi olduğunu belirtmek için “git init” komutunu yazarız. Artık projemiz bir Git projesidir. Ancak klasörü açtığımızda klasörde bir değişiklik gözlemleyemeyiz. Bunun sebebi Git dosyalarının gizli dosya komutunda yüklenmesidir. “ls -a” komutu ile .git dosyasının yüklendiğini görürüz. Bu şekilde Git projemiz oluşturulmuş oldu.

TEMEL GIT KAVRAMLARI

Temel komutları anlatmadan önce bazı terimlerin ne anlama geldiğini öğrenmemizin daha doğru olacağını düşünmekteyiz.

Working Directory: Çalışma dizinini yani klasörünü ifade eder. Projenize ait dosya ve klasörleri barındıran klasördür.

Stage Area: Geçiş bölgesidir. Git sisteminde projenizin kopyasını almak istediğinizde doğrudan depoya gönderilmez. Önce Stage Area adı verilen bir geçiş bölgesine gönderilir.

Repository : Proje dosyalarını uzak bir sunucuda depolar.

Branch : Projenin birçok bölümünü derli toplu şekilde tutulmasını sağlar.

Checkout : Mevcut branch üzerindeki commit’lerin üzerinde geçiş yapabilmemizi sağlar.

Fork : Repository’nin bir kopyasının alınmasıdır.

Pull Request (PR): Fork edilen proje üzerinde değişiklikler yaptıktan sonra gerçek repository’e gönderilerek o projenin sahibi olan geliştiricinin değerlendirmesine sunmaktır.

Merge : Branch üzerinde yaptığımız değişiklikleri master branch’i üzerinde birleştirme işlemidir.

Master : Reponun ana branchidir. Git üzerinde hiçbir işlem yapmazsak değişikler master branchi üzerinden devam eder.

Commit : Proje dosyalarınızda belli bir değişiklik yaptığınızda o değişikliğin anlık görüntüsünün alınıp kaydedilmesine denir.

TEMEL GIT KOMUTLARI

git config
En çok kullanılan git komutlarından biri, e-posta, kullanıcı adı ve dosya biçimi vs. için tercih edilen kullanıcıya özgü yapılandırma değerlerini ayarlamak için kullanılır.

git init
Bu komut yeni git dizini oluşturmak için kullanılır. Başka bir deyişle git init komutu bilgisayarınızda oluşturmuş olduğunuz bir klasörün Git’e tanımlanması için kullanılmaktadır. Yani, masaüstünüzde oluşturduğunuz bir klasörü yerel bir repository (depo) yapmaya yarar.

git add
Git add komutu, dizine dosyalar eklemek için kullanılabilir. Örneğin “Git add dosya.txt” komutu mevcut dizindeki “dosya.txt” dosyasını dizine ekler.

git clone
git clone komutu dizin kontrol amaçları için kullanılır. Bu komutunu kullanarak Github’ta bulunan bir repository’i bilgisayarınıza kopyalayabilirsiniz.

git commit
Geçiş bölgesinde yer alan değişiklikleri depoya bildirmek için commit komutu kullanılır. Önce add, sonra commit komutunun kullanılmasıyla proje klasöründeki tüm değişiklikler depoya bildirilmiş yani kopyalanmış, yedeği alınmış olur.

git status
Proje dosyalarının o anki durumu hakkında bilgi verir. Durumu değiştirilmiş dosyaları gösterir.

git checkout
Dal oluşturmak veya dallar arasında geçiş yapmak için kullanılır. Aşağıdaki ilk örnek yeni bir dal oluşturup ona geçerken, ikinci örnek bir daldan diğer dala geçmek için kullanılır.

git remote
Bu komut bir kullanıcının bir uzak dizine bağlanmasını sağlar. Aşağıdaki komut şu anda yapılandırılmış uzak dizinleri listeler

Bu komut da kullanıcının yerel dizini uzak bir dizine bağlamasını sağlar

git branch
Dalları listelemek, oluşturmak ya da silmek için kullanılabilir. Sadece bir dalı silmek için -d eklenmelidir.

em bilgisayarımızdaki hem de projemizi bağladığımız uzak sunucudaki (Github, Gitlab gibi) dalları listelemek içinse aşağıdaki komut kullanılır.

git tag
Etiketleme, belirli taahhütleri basit kısımlara işaretlemek için kullanılır.

git merge
Bulunduğunuz branch ile başka bir branch’ı birleştirmek için aşağıdaki gibi bir komut yapısı kullanılır.

git diff
İki branc arasındaki farklılıkları listelemek için aşağıdaki komut yapısı kullanılır.

git pull
Uzak sunucudaki proje dosyaları üzerindeki bir değişiklik veya ekleme varsa onları bizim localimizdeki proje dosyaları ile birleştirir.

git log
Projenizde yaptığınız tüm commit işlemlerini listelemek yani tüm yedekleri görüntülemek istiyorsanız log komutunu kullanabilirsiniz. Aşağıdaki ikinci örnek bir çıktının örneğidir.

git reset
Dizini ve çalışma dizinini son tamamlama durumuna sıfırlamak için, git reset komutu kullanılır.

git stash
Hemen işlenmeyecek değişiklikleri geçici olarak kaydetmeye yardımcı olur.

git rm
Dosyaları dizinden ve çalışma dizininden kaldırmak için kullanılabilir.

Klasör silmek için ise -r parametresi kullanmanız gerekiyor. R parametresi recursive ifadesinin kısaltılmış halidir. Kendi kendini yineleme, kendi kendini çağırma anlamına gelir.

git show
Herhangi bir git nesnesi hakkında bilgi görüntülemek için git show komutu kullanılır.

git fetch
Bir kullanıcının bu nesneleri şu anda yerel çalışma dizininde bulunmayan uzak dizinden almasına izin verir.

git Is-tree
Bir ağaç nesnesini, her maddenin adı ve modu ile blob’un SHA-1 değerini birlikte görüntülemek için git ls-tree komutunu kullanın.

git catfile
SHA-1 değeri ile, git cat-file komutunu kullanarak bir nesnenin türünü görüntüleyin.

gitk
gitk komutu yerel bir dizin için grafiksel arayüzdür.

git instaweb
Bu komutla bir web sunucusu yerel depo ile arabirimde çalıştırılabilir. Bir web tarayıcı da kendisine otomatik olarak yönlendirilir.

git gc
Depoyu gereksiz dosyaları temizleyerek, çöp toplama yoluyla optimize etmek için kullanılır.

git archive
Bu komut, bir kullanıcının tek bir dizin ağacının bileşenlerini içeren bir zip veya tar dosyası oluşturmasını sağlar.

git prune
git prune komutu aracılığıyla, gelen işaretçilerine sahip olmayan nesneler silinir.

git fsck
GIT dosya sisteminin bütünlüğünü kontrol etmek için git fsck komutunu kullanılır. Bozuk nesneler tanımlanır.

git rebase
Bu komut, başka bir şubedeki taahütlerin tekrar uygulanması için kullanılır.

git push
En çok kullanılan komutlardan biridir. Commit’lediğimiz dosyaları uzak sunucudaki repository’e gönderir.

GITHUB NEDİR?

Github, Git yazılımı ile entegre olmuş bir depolama alanıdır. Githubda Git projeleri saklanabilir ve yönetilebilir. Githubın en önemli olanaklarından biri oluşturduğunuz bir projeyi dünyanın her yerinden insana ulaştırma fırsatıdır. Projeden bir kısmı veya bir parçası başka projelerde kullanılabilir. Biz de gördüğümüz bir projeden istediğimizi kısmı alma imkanına sahip oluruz. Yani GitHub depolama dışında aynı konuyla ilgilenen insanların etkileşime girmesi açısından da oldukça önemlidir.

GITHUB NASIL KULLANILIR?

Yeni Bir Proje Oluşturmak:

“Creat a new repository” kısmından yeni bir proje oluşturabilir, bu projeyi özel tutma veya dünyayla açık hale getirebiliriz.

GITHUB’A PROJE NASIL YÜKLENİR?

Masaüstümüzde Terminalimizi açarak göndermek istediğimiz dizin üzerinden işlemlerimizi uygularız. GitHub’da oluşturduğumuz projenin bağlantısını Terminale eklememiz gerekir. “git remote add” komutu ile uzak bir bağlantı eklemek istediğimizi belirtiriz. Daha sonrasında ise kopyaladığımız bağlantıyı yapıştırırız.”git push -u” komutu ile bütün dosyaları aktarmış oluruz. Komut devamında yüklemeyi yapabilmek için GitHub kullanıcı adımızı ve şifremizi Terminale yazmalıyız. Bu işlemlerden sonra GitHub’a başarılı şekilde dosya yüklemesi yapmış oluruz.

Oluşturulmuş Bir Projeyi Kullanma ve Değişiklik Yapma

Bunun için öncelikle Terminale “git clone” yazarak yanına projenin kopyaladığımız bağlantısını yapıştırırız. Sonrasında ise Terminal üzerinden “cd “ yazarak yanına istediğimiz klasörü yazarız. Bu sayede o klasöre gelmiş oluruz. Proje üzerinde istediğimiz değişiklikleri yaptıktan sonra neleri değiştirdiğimizi görmek istiyorsak “git status” kodu ile bunları görmemiz mümkün olacaktır.Değiştirilen kısımları görmek için “git add” kodunun yanına eklenecek yapıları yazarız. Eğer projenin güncel halini görmek istiyorsak tekrardan “git status” kodu ile görüntüleme yapmamız gerekir. İstediğimiz değişiklikleri yaptıktan sonra “git push” kodu ile projenin son halini GitHub’a aktarabiliriz. Böylece başka bir proje üzerinde istediğimiz değişiklikleri sağlamış olduk.

PULL REQUEST NEDİR?

Başkasının projesinin üzerinde çalışarak yaptığımız değişiklikleri projenin sahibine bildirmek için kullandığımız iletidir. Yaptığımız değişiklikleri kendi koduyla birleştirmesini talep ederiz.

FETCH ve PULL

Fetch ve Pull kavramları zaman zaman birbirine karışabilir.

Fetch, remote branchdeki değişikliklerin bilgilerini indirmek için kullanılır. Pull ise bu değişiklikleri entegre etmeye yarar.

CLONE

Dosyaları yedeklemek ve bir kopyasını oluşturmak için kullanılır.

FORK

Başka birinin oluşturduğu projeyi kendi hesabımıza kopyalamamıza “fork” adı verilir.

GIT VE GITHUB FARKI

Git ve github birbiriyle bağlantılı olsa da tamamen farklıdır. Konsept ve terimler farklıdır. Git, bilgisayarda bulunan bir uygulamadır. Github ise git ile yazılan projeler için kullanılan bir depolama servisidir. GitHub olmadan da Git kullanmak mümkündür. Git, internet olmadan bile kullanılabilir. Bir kayıt işlemi gerektirmez.

GitHub ise Git projelerini saklamak için kullanılan çevrimiçi bir servistir. Kayıt olma işlemleri GitHub kullanmak için gereklidir.

GIT ve GITHUB’IN KARİYERDEKİ ETKİSİ

Yazılım kariyerinde Git kullanmanın bir zorunluluk haline geldiğinden bahsetmiştik. Git depolama alanı olarak birçok seçenek olsa da en popüleri ve en yaygın kullanılanı olan GitHub da bu bağlamda neredeyse bir zorunluluk taşır.

GitHub, özellikle işe alım sürecinde iş veren için sizin birikiminizi ve deneyiminizi ölçmek amacıyla bakabileceği ilk yerlerden biri olabilir. Bu yüzden GitHub’a proje yüklemek oldukça önemlidir. Hem mesleki anlamda iş bulma sürecini kolaylaştırır hem de siz de bu süreçte kendinizi ne kadar geliştirdiğinizi izleyebilirsiniz. Başka insanlardan yardım alarak projenizi bir üst seviyeye çıkarabilir, siz de başkalarına yardımcı olabilirsiniz.

KAYNAKÇA

https://dev.to/aciklab/git-ve-github-nedir-nasil-kullanilir-bmk
https://coderspace.io/blog/git-nedir-nasil-kullanilir/
https://www.hostinger.web.tr/rehberler/github-kullanimi-basit-git-komutlari
https://tr.linkedin.com/pulse/terminal-%C3%BCzerinden-github-repository-olu%C5%9Ftur-de%C4%9Fi%C5%9Fiklik-tekin
https://www.youtube.com/watch?v=wl7zxkd80X4&list=PLPrHLaayVkhnNstGIzQcxxnj6VYvsHBHy&index=5
http://www.yucelalkan.com/temel-git-komutlari
https://www.btkakademi.gov.tr/portal/course/versiyon-kontrolleri-git-ve-github-1943
KURSU ANLATTIĞIMIZ VİDEO LİNKİ: https://www.youtube.com/watch?v=HshtaVI0aTQ&t=10s&ab_channel=BeyzaH%C4%B1z
