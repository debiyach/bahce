---
title: İnternet Nasıl Çalışır?
---

>[!tip] Kısaca
>
>İnternet, birbiriyle iletişim halindeki bilgisayar ağına verilen addır.

>[!info]  MDN Web Docs
>
>İnternetin tarihi biraz karanlıktır. 1960'larda ABD ordusu tarafından finanse edilen bir araştırma projesi olarak başladı, ardından 1980'lerde birçok devlet üniversitesi ve özel şirketin desteğiyle bir kamu altyapısına dönüştü. İnterneti destekleyen çeşitli teknolojiler zaman içinde gelişti, ancak çalışma şekli o kadar da değişmedi: İnternet, bilgisayarları birbirine bağlamanın ve ne olursa olsun bağlı kalmanın bir yolunu bulmalarını sağlamanın bir yoludur.

## Derinlere İnelim

### Basit bir ağ

İki bilgisayarın iletişim kurması gerektiğinde, onları ya fiziksel olarak (genellikle Ethernet kablosuyla) ya da kablosuz olarak (örneğin Wi-Fi veya Bluetooth sistemleriyle) birbirine bağlamanız gerekir. Tüm modern bilgisayarlar bu bağlantılardan herhangi birini sürdürebilir.

>[!info] Not
>
> Bu makalenin geri kalanında sadece fiziksel kablolardan bahsedeceğiz, ancak kablosuz ağlar da aynı şekilde çalışır.

![[images/internet-nasil-calisir/image-23-59-14-482-10-06-2023.png]]

Böyle bir ağ iki bilgisayarla sınırlı değildir. İstediğiniz kadar bilgisayarı bağlayabilirsiniz. Ancak işler hızla karmaşıklaşır. Diyelim ki on bilgisayar bağlamaya çalışıyorsanız, bilgisayar başına dokuz fiş olmak üzere 45 kabloya ihtiyacınız vardır!

![[images/internet-nasil-calisir/image-23-59-24-932-10-06-2023.png]]

Bu sorunu çözmek için, bir ağdaki her bilgisayar yönlendirici adı verilen özel bir küçük bilgisayara bağlanır. Bu yönlendiricinin tek bir görevi vardır: tren istasyonundaki bir işaretçi gibi, belirli bir bilgisayardan gönderilen bir mesajın doğru hedef bilgisayara ulaşmasını sağlar. B bilgisayarına bir mesaj göndermek için A bilgisayarının mesajı yönlendiriciye göndermesi gerekir, yönlendirici de mesajı B bilgisayarına iletir ve mesajın C bilgisayarına ulaşmamasını sağlar.

Sisteme bir yönlendirici eklediğimizde, 10 bilgisayardan oluşan ağımız yalnızca 10 kablo gerektirir: her bilgisayar için tek bir fiş ve 10 fişli bir yönlendirici.

![[images/internet-nasil-calisir/image-23-59-42-663-10-06-2023.png]]

### Ağlardan oluşan bir ağ

Buraya kadar her şey yolunda. Peki ya yüzlerce, binlerce, milyarlarca bilgisayarı birbirine bağlamak? Elbette tek bir yönlendirici bu kadar geniş ölçekli olamaz, ancak dikkatli okursanız, bir yönlendiricinin diğerleri gibi bir bilgisayar olduğunu söylemiştik, o halde bizi iki yönlendiriciyi birbirine bağlamaktan alıkoyan nedir? Hiçbir şey, öyleyse bunu yapalım.

![[images/internet-nasil-calisir/image-23-59-55-003-10-06-2023.png]]

Bilgisayarları yönlendiricilere, sonra da yönlendiricileri yönlendiricilere bağlayarak sonsuz ölçeklendirme yapabiliyoruz.

![[images/internet-nasil-calisir/image-00-00-07-970-11-06-2023.png]]

Böyle bir ağ, İnternet dediğimiz şeye çok yaklaşıyor ama bir şeyi kaçırıyoruz. Biz bu ağı kendi amaçlarımız için kurduk. Dışarıda başka ağlar da var: arkadaşlarınız, komşularınız, herkes kendi bilgisayar ağına sahip olabilir. Ancak eviniz ile dünyanın geri kalanı arasında kablo döşemek pek mümkün değil, peki bunu nasıl halledebilirsiniz? Örneğin elektrik ve telefon gibi evinize bağlı kablolar zaten var. Telefon altyapısı zaten evinizi dünyadaki herhangi bir yere bağlar, bu yüzden ihtiyacımız olan mükemmel kablodur. Ağımızı telefon altyapısına bağlamak için modem adı verilen özel bir ekipmana ihtiyacımız var. Bu modem, ağımızdan gelen bilgileri telefon altyapısı tarafından yönetilebilir bilgilere dönüştürür ve bunun tersi de geçerlidir.

![[images/internet-nasil-calisir/image-00-00-18-954-11-06-2023.png]]

Böylece telefon altyapısına bağlanmış olduk. Bir sonraki adım, mesajları ağımızdan ulaşmak istediğimiz ağa göndermektir. Bunu yapmak için ağımızı bir **İnternet Servis Sağlayıcısına** (İSS) bağlayacağız. **İSS**, hepsi birbirine bağlı olan ve diğer İSS'lerin yönlendiricilerine de erişebilen bazı özel yönlendiricileri yöneten bir şirkettir. Böylece ağımızdan gelen mesaj **İSS** ağları üzerinden hedef ağa taşınır. İnternet tüm bu ağ altyapısından oluşur.

![[images/internet-nasil-calisir/image-00-00-29-261-11-06-2023.png]]

### Bilgisayar bulma

Eğer bir bilgisayara mesaj göndermek istiyorsanız, hangi bilgisayar olduğunu belirtmeniz gerekir. Bu nedenle, bir ağa bağlı her bilgisayarın kendisini tanımlayan ve "**IP adresi**" (**IP**, *İnternet Protokolü* anlamına gelir) olarak adlandırılan benzersiz bir adresi vardır. Bu adres, noktalarla ayrılmış dört sayıdan oluşan bir dizidir, örneğin: `192.168.2.10`.

Bu bilgisayarlar için gayet iyidir, ancak biz insanlar bu tür bir adresi hatırlamakta zorlanırız. İşleri kolaylaştırmak için, bir IP adresini alan adı adı verilen insan tarafından okunabilir bir adla takma ad (`domain name`) olarak kullanabiliriz. Örneğin (yazım sırasında IP adresleri değişebilir) `google.com`, `142.250.190.78` IP adresinin üstünde kullanılan alan adıdır. Yani alan adını kullanmak, İnternet üzerinden bir bilgisayara ulaşmamızın en kolay yoludur.

![[images/internet-nasil-calisir/image-00-00-39-407-11-06-2023.png]]

### İnternet ve web

Fark edebileceğiniz gibi, bir Web tarayıcısı ile Web'de gezindiğimizde, bir web sitesine ulaşmak için genellikle alan adını kullanırız. Bu, İnternet ve Web'in aynı şey olduğu anlamına mı geliyor? Bu o kadar basit değil. Gördüğümüz gibi, İnternet milyarlarca bilgisayarın birbirine bağlanmasını sağlayan teknik bir altyapıdır. Bu bilgisayarlar arasında bazı bilgisayarlar (Web sunucuları olarak adlandırılır) web tarayıcılarına anlaşılabilir mesajlar gönderebilir. İnternet bir altyapıdır, Web ise bu altyapının üzerine inşa edilmiş bir hizmettir. E-posta ve [IRC](https://developer.mozilla.org/en-US/docs/Glossary/IRC) gibi internetin üzerine inşa edilmiş başka hizmetler olduğunu da belirtmek gerekir.

### İntranetler ve Extranetler

İntranetler, belirli bir kuruluşun üyeleriyle sınırlı olan özel ağlardır. Genellikle üyelerin paylaşılan kaynaklara güvenli bir şekilde erişmeleri, işbirliği yapmaları ve iletişim kurmaları için bir portal sağlamak amacıyla kullanılırlar. Örneğin, bir kuruluşun intraneti departman veya ekip bilgilerini paylaşmak için web sayfaları, önemli belgeleri ve dosyaları yönetmek için paylaşılan sürücüler, iş yönetimi görevlerini yerine getirmek için portallar ve wiki'ler, tartışma panoları ve mesajlaşma sistemleri gibi işbirliği araçları barındırabilir.

Extranetler Intranetlere çok benzer, ancak diğer kuruluşlarla paylaşıma ve işbirliğine izin vermek için özel bir ağın tamamını veya bir kısmını açarlar. Genellikle bir işletme ile yakından çalışan müşteriler ve paydaşlarla güvenli ve emniyetli bir şekilde bilgi paylaşmak için kullanılırlar. Genellikle işlevleri bir intranet tarafından sağlananlara benzer: bilgi ve dosya paylaşımı, işbirliği araçları, tartışma panoları vb.

Hem intranetler hem de extranetler İnternet ile aynı tür bir altyapı üzerinde çalışır ve aynı protokolleri kullanır. Bu nedenle farklı fiziksel konumlardan yetkili üyeler tarafından erişilebilirler.

![[images/internet-nasil-calisir/image-00-00-56-371-11-06-2023.png]]

## Önerilen Kaynaklar
- [How the Internet Works in 5 Minutes](https://www.youtube.com/watch?v=7_LPdttKXPc)
- [How does the INTERNET work?](https://www.youtube.com/watch?v=x3c1ih2NJEg)
- [The Internet: IP Addresses & DNS](https://youtu.be/5o8CwafCxnU)

## Kaynakça 
- [MDN](https://developer.mozilla.org/en-US/docs/Learn/Common_questions/Web_mechanics/How_does_the_Internet_work#intranets_and_extranets)