---
title: "Değişiklikleri Önizleme"
---

Quartz sitenizin internete dağıtmadan önce nasıl göründüğünü önizlemek istiyorsanız, aşağıdakiler talimatlar, yerel olarak çalıştırmak için uygun bağımlılıkları yükleyerek size rehberlik eder.

## `hugo-obsidian` Yüklemek
Bu adım Hugo'nun ayrıştırması için geri bağlantıların listesini oluşturacaktır.

> [!info]
> [Golang](https://golang.org/doc/install) ( > = 1.16 ) sahip olduğunuzdan emin olun.

```bash
# `hugo-obsidian`ı yerel olarak kurun ve bağlayın
go install github.com/jackyzha0/hugo-obsidian@latest
```

`command not found: hugo-obsidian` hatasıyla karşılaşıyorsanız, `GOPATH` ayarladığınızdan emin olun. Terminalinizin `hugo-obsidian`'ı yürütülebilir olarak doğru bir şekilde tanımasına izin verecektir.

## Hugo' yu Yükleme

> [!info]
> [CMake](https://cmake.org/download/) yüklü olduğundan emin olun.

Hugo, Quartz'a güç veren statik site üreticisidir. İlk olarak, [Hugo'yu “ genişletilmiş ” Sass / SCSS sürümüyle yükleyin](https://gohugo.io/getting-started/installing/). Aşağıdaki kodları sırayla çalıştırın. 

```bash
# Yerel Quartz klasörünüze gidin
cd <yerel-quarz-klasor-yolu>

# Yerel sunucunu başlat
make serve

# http://localhost:1313/ adresine girip değişikliklere bakabilirsin.
```

## Docker

> [!info]
> [CMake](https://cmake.org/download/) ve [Docker](https://docs.docker.com/engine/install/) yüklü olduğundan emin olun.

Terminal açın ve aşağıdaki kodu çalıştırın.

```bash 

# Docker kullanarak, yerel sunucu başlatır
make docker

# İşlem tamamlandığında, http://localhost:1313/ adresine girip değişikliklere bakabilirsin.

```
