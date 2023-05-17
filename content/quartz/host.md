---
title: "Çevrimiçi Barındırma"
---
## Github Pages Üzerinde Barındırma
Quartz, konuşlandırılması zahmetsiz olacak şekilde tasarlanmıştır. Quartz'ı doğrudan, depodan çatalladı ve klonladıysanız, her şey yolunda olmalı! Aşağıdaki adımları izleyin.


###  GitHub Eylem (Actions) İzinlerini Etkinleştir
Varsayılan olarak GitHub, iş akışlarının dosyalarınızı değiştirmesini devre dışı bırakır (güvenlik amaçlı). Ancak Quartz, gerçek site dosyalarını GitHub'a geri yazmak için buna ihtiyaç duyar.

>[!info]
>Quartz, `hugo` şubesine bir taahhüt geldiğinde; Github Eylemlerini tetikler. Bu işlemin sonunda ana şubeye statik site için gerekli dosyaları aktarmış olur.

1. Deponuzda `Settings > Action > General > Workflow Permissions` sayfasına gidin.
2. `Read and Write Permissions` işaretleyiniz.

Aşağıdaki görsel gibi olacaktır:
![](images/quartz-host-workflow-setting.png)

### GitHub Sayfalarını (Github Pages) Etkinleştirin 

>[!warning]
>Bu işlem için daha öncesinde Github Sayfaları için alan adı (domain) doğrulama işlemlerinizi yapmanız gerekmektedir. 

1. `Settings > Pages` sayfasına gidiniz.
2. Kaynağı `/(root)` kullanarak `master`'dan (`hugo`'dan değil) dağıtacak şekilde ayarlayın.
3. Opsiyonel olarak, özel alan adına yönlendirebilirsiniz.

Aşağıdaki görsel gibi olacaktır:
![[images/quartz-host-github-pages.png]]

### Değişiklikleri Göndermek
Değişikliklerinizi internette görmek için GitHub'a göndermemiz gerekiyor. Quartz bir `git` deposudur. Bu nedenle güncellemek, normal bir yazılım projesiymiş gibi takip edeceğiniz iş akışıyla aynıdır.

```bash

# Quartz klasörüne gidin
cd <path-to-quartz>

# Tüm değişiklikleri ekleyin ve taahhüt edin
git add .
git commit -m "mesaj açıklaması"

# Değişiklikleri Github'a gönderin ve sitenizi güncelleyin
git push origin hugo

```

_Not:_ Burada özellikle `hugo` şubesine gönderim yapıyoruz. GitHub eylemimiz, bu şube her gönderilmiş değişikliği algılandığında otomatik olarak çalışır ve ardından yeniden dağıtım için ana şubeyi günceller.

### Site Kurulumu ve Ayarları

Şimdi siteyi kurup çalıştıralım. Daha önce hiç site barındırmadınız mı? Sorun değil. Zaten sahip olduğunuz alan adınız mı var veya Quartz'ınızı alt alan adı olarak mı kullanmak istiyorsunuz? Bunları yapabileceksiniz.

Burada, sitemizi dağıtmak için GitHub'ın ücretsiz sayfa barındırma hizmetinden yararlanıyoruz. `baseURL` değerini `/config.toml` içinde değiştirin.

>[!warning]
>  `baseURL`'nizin sonunda bir `/` olduğundan emin olun!

[Referans `config.toml` dosyası için tıklayınız.](https://github.com/jackyzha0/quartz/blob/hugo/config.toml)

```toml
baseURL = "https://<alan-adiniz>/"
```


Bunu bir alt alan adı altında kullanıyorsanız (örneğin `<github-kullanici-adiniz>.github.io/quartz`), sondaki `/` işaretini ekleyin. Bunu özellikle GitHub kullanıyorsanız yapmanız gerekir!

```toml
baseURL = "https://<github-kullanici-adiniz>.github.io/quartz/"
```

`/.github/workflows/deploy.yaml` dosyasındaki `cname` değerini değiştirin. Yine, kullanabileceğiniz özel bir alan adınız yoksa `<github-kullanici-adiniz>.github.io` adresini kullanabilirsiniz.

>[!warning]
>Lütfen `cname` değeriinin herhangi bir yol olmaması gerektiğini unutmayın. 
>Olabilecek değerler:
> - debiyach.github.io
> - `kullanici-adi.github.io`
> - `alan-adi.com`
> 
> Olamayacak değerler:
> - `https://debiyach.github.io/`
> - `alan-adi.com/`

```yml {title=".github/workflows/deploy.yaml"}
- name: Deploy  
  uses: peaceiris/actions-gh-pages@v3  
  with:  
	github_token: ${{ secrets.GITHUB_TOKEN }} # Buraya dokunmayın! Github otomatik doldurur.
	publish_dir: ./public  
	publish_branch: master
	cname: <alan-adiniz>
```

Özel bir alan adınız mı var? [Quartz ile nasıl ayarlayacağınızı öğrenin.](https://quartz.jzhao.xyz/notes/custom-Domain/)

### Dosyaları Yok Sayma
Tüm notlarınızın yalnızca bir alt kümesini mi yayınlamak istiyorsunuz? Endişelenmeyin, Quartz bunu iki adımlı basit bir işlem haline getiriyor.

❌ [Yayınlanan sayfaların hariç tutulması]([Excluding pages from being published](https://quartz.jzhao.xyz/notes/ignore-notes/))

## Docker Desteği
Eğer bir barındırma hizmeti kullanmak istemiyorsanız, bunun yerine [Docker](https://quartz.jzhao.xyz/notes/docker/) kullanarak barındırma yapabilirsiniz! Ne yaptığınızı bilmiyorsanız bu yöntemi kullanmayın derim.





