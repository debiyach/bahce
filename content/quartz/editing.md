---
title: "Notları Düzenle"
---

## Düzenleme
Kuvars, [[hugo]] sistemi üzerinde çalışır. Bu yüzden tüm notlar [Markdown](https://www.markdownguide.org/) formatında yazılır.

## Klasör Yapısı
İşte neyin ne olduğuna dair kabaca bir genel bakış.

**Bahçenizdeki tüm içerik `/content` klasör** içerisinde yer almalıdır. Düzenleme yapmak için dosyalardan herhangi birini açabilir, doğrudan değişiklik yapabilir ve kaydedebilirsiniz. İçeriği istediğiniz herhangi bir klasörde düzenleyebilirsiniz.

**Ana sayfayı düzenlemek için `/content/_index.md`dosyasını düzenleyebilirsiniz.**

## Meta Değerleri
Dosyalar için meta veriler söz konusu olduğunda `Hugo` seçicidir. Başlığınızın çift tırnaklı olduğundan ve dosyanızın üstünde böyle bir başlığa sahip olduğunuzdan emin olun, aksi takdirde oluşturulan sayfanın bir başlığı olmayacaktır!

```
---
title: "Example Title"
tags:
- example-tag
---

Rest of your content here...

```

Daha fazla bilgi için [buraya](https://gohugo.io/content-management/front-matter/) göz atabilirsiniz.

## Obsidian
Dijital bahçenizi düzenlemenin ve büyütmenin bir yolu olarak [Obsidiyen](http://obsidian.md/) kullanmanızı öneririm. Tüm yerel dosyalarınızı önizlemek için gerçekten güzel bir editör ve grafik arayüzü ile birlikte gelir.

Bu adım **şiddetle tavsiye edilir**.
> 🔗 [[quartz/obsidian-vault-integration|Obsidian Entegrasyonu]]

## Değişiklikleri Önizleme
Bu adım tamamen isteğe bağlıdır. Çoğunlukla dijital bahçelerin yayınlanmış sürümünü internete açmadan önce yerel (kendi bilgisayarınızda) olarak görmek isteyenler içindir. _Şiddetle tavsiye edilir_ ancak gerekli değildir.

> 👀 [[preview|Önizleme]]

Gerçek ortama en yakın görünüm için Obsidian' ın önizleme seçeneği sizin için en ideal çözümdür.

## Değişiklikeri Yayınlama
Artık dijital bahçenizi Quartz kullanarak yönetmenin temellerini bildiğinize göre, bunu internette yayınlayabilirsiniz!

> 🌍 Adım 5: [[quartz/host|Çevrimiçi Barındırma]]

Sorun mu yaşıyorsunuz? [[sss|SSS ve Sorun Giderme kılavuzu]]na göz atabilirsiniz.