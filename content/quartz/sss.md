---
title: "SSS"
---

Sorun mu yaşıyorsunuz? İşte Quartz'ı kurarken insanların karşılaştığı sık karşılaşılan soruların ve sorunların bir listesi.

Hazır buradayken [Discord'a davetlisiniz.](https://discord.gg/cRFFHYye7t) 🙂

### Quartz'ın Lateks desteği var mı?
Evet!  [Buraya tıklayın ve demoyu görüntüleyin. CJK + Lateks Desteği ( 원试 )](https://quartz.jzhao.xyz/notes/CJK-+-Latex-Support-%E6%B5%8B%E8%AF%95/)

### Quartz'ta Obsidian Plugin> kullanabilir miyim?
Eklenti doğrudan markdown çıktısına etki etmiyorsa, kullanamazsınız.
En kolay yol, aradığınız işlevselliği destekleyen kendi HTML kısmi eklemenizdir.

### GitHub sayfalarım Quartz'ı değil, sadece README'yi gösteriyor
`master` şubesini dağıtacak şekilde seçmelisiniz. `hugo` şubesini değil! [[quartz/host|Buraya bir göz atın.]]

### Bazı sayfalarımda son değiştirilen tarih olarak ‘ 1 Ocak 0001 ’ var
```shell
# Quartz kurulu olduğu dizine gidin. Aşağıdaki kodu çalıştırın.
git config core.ignorecase true

# Global olarak bu kodu da çalıştırabilirsiniz. Fakat önerilmez
git config --global core.ignorecase true
```


### Sayfalarımın yalnızca bir alt kümesini yayınlayabilir miyim?
Evet! Quartz seçici yayınlamayı gerçekten kolaylaştırır. Bu [rehbere göz atabilirsiniz.](https://quartz.jzhao.xyz/notes/ignore-notes/)

### GitHub Sayfalarında değil, kendim barındırabilir miyim?
Evet! Oluşturulan tüm dosyalar `/public` altında bulunabilir.

### # `command not found: hugo-obsidian`
`GOPATH` doğru olarak ayarladığınızdan emin olun! Terminaliniz, `hugo-obsidian` yürütülebilir (executable) bir dosya olarak tanımadığı için bu hatayı vermiştir. 

```shell
# `~.zshrc` kullanan Mac kullanıcı aşağıdaki kodu çalıştırabilir.
export GOPATH=/Users/$USER/go
export PATH=$GOPATH/bin:$PATH

# Terminalinizi yeniden başlatın
source ~/.bash_profile
```


### Notlarım oluşmuyor
Muhtemelen Markdown dosyalarınıza ön madde eklemeyi unuttunuz. Aşağıdaki içeriklere göz atın.
- [[quartz/editing|Notları Düzenle]]
- [[quartz/obsidian-vault-integration|Obsidian Kasa Entegrasyonu]]

### Özel alan adım çalışmıyor!
[[quartz/host|Barındırma]] rehberine göz atabiliriniz.

### Analitiği nasıl ayarlarım?
Quartz varsayılan olarak analiz için [Plausible](https://plausible.io/) kullanır.
Google Analytics'i kullanmayı tercih ediyorsanız, bunu takip edebilirsiniz [Hugo belgelerindeki rehber](https://gohugo.io/templates/internal/#google-analytics).
Alternatif olarak, Google Analytics verileriniz için [bu kılavuzu takip edebilirsiniz.](https://plausible.io/docs/google-analytics-import).

### Ana sayfadaki içeriği nasıl değiştirebilirim?
`/content/_index.md` sayfasındaki içeriği düzenleyebilirsiniz.

### Renkleri nasıl değiştiririm?
Temayı `assets/custom.scss` dosyasını düzenleyerek değiştirebilirsiniz. Özelleştirme ve tema oluşturma hakkında daha fazla ayrıntı [özelleştirme kılavuzunda]([customization guide

### Nasıl resim eklerim?
`/content` klasörü içerisinde herhangi bir yere resminizi yerleştirebilirsiniz.
```markdown
Örnek resim (resim bu yolda olsun /content/notes/images/example.png)
![Örnek resim](/content/notes/images/example.png)
```

### Etkileşimli grafiğim ve geri bağlantılarım güncel değil
Varsayılan olarak, `linkIndex.json` (Quartz'ın Etkileşimli Grafik ve Geri Bağlantıları oluşturmak için ihtiyaç duyduğu) yerel olarak yeniden oluşturulmaz. Bunu ayarlamak için [[quartz/editing|yerel düzenleme kılavuzuna bakın.]]

### React/Vue/başka bir çerçeve kullanabilir miyim?
Maalesef yok. Muhtemelen `/layouts/_default/single.html` dosyasını düzenleyerek çalışmasını sağlayabilirsiniz ancak Quartz bununla çalışmak üzere tasarlanmamıştır. Bu çerçevelerle yapmaya çalıştığınız şeylerin %99'unu sadece vanilya `HTML/CSS/JS` kullanarak mükemmel bir şekilde başarabilirsiniz.


## Hala Sorun mu Yaşıyorsun?
Quartz mükemmel değil! Hala sorun yaşıyorsanız, GitHub deposunda makul ölçüde sağlayabileceğiniz kadar bilgi içeren bir sorun gönderin. Alternatif olarak, bana mesaj gönderebilirsiniz [Twitter](https://twitter.com/_jzhao) ve en kısa sürede size geri dönmeye çalışacağım.

🐛 [Bir Sorun Gönder](https://github.com/jackyzha0/quartz/issues)