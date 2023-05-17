---
title: "Obisidan Kasa Entegrasyonu"
---

## Kurulum
Quartz'ı kullanmanın en çok tercih edilen yolu Obisidian' dır. Yeni bir Obisidian kasa oluşturabilir veya sahip olduğunuz bir kasayı bağlayabilirsiniz.

### Yeni Kasa

> [!info]
> Obsidian kurulu olduğu varsayılarak işleme devam ediyoruz.

Klonladığınız klasör içerisine girin. `/content` dizini içerisini temizleyin. Obsidian kasanızı `/content` klasörü olarak seçin.

> [!info]
> `/content` içerisindeki dosyalar, örnek dosyalardır. Eğer silinmesini istemiyorsanız adını değiştirebilirsiniz. Adını değiştirmeniz durumunda; `/content` adında yeni bir klasör oluşturmalı ve obisidan kasasını yeni oluşturulan klasöre tanımlamalısınız. 

### Mevcut Bir Kasayı Bağlama
Mevcut bir Kasayı kullanmanın en kolay yolu, mevcut kasa dizinindeki tüm dosyaları; `/content` klasörüne atmalısınız. Obsidian üzerinden kasanızı yeni dizine (`/content` olan dizine) taşımalısınız.

## Ayarlar
Harika. Obsidian' ı, Quartz' a bağladığınıza göre bazı ayarları düzeltelim.

`Ayarlar (Settings)` > `Dosyalar ve Bağlantılar (Files & Links)` sayfasına girin. Şu iki öğeyi düzenleyin.
1. `Yeni bağlantı biçimi (New link format)` için `Kasada Mutlak Yol (Absolute path in vault)` değerini seçin.
2. `Dahili bağlantıları otomatik olarak güncelleme (Automatically update internal links)` ayarını aktif edin.

![[assets/images/obisidan-vault-settings.png]]Örnek Ayar

## Şablonlar 
Her yeni Not oluşturmak istediğinizde meta verilerini eklemek sinir bozucu olur. Neyse ki, Obsidian yeni içerik eklemeyi gerçekten kolay hale getiren şablonları destekliyor.

> [!warning]
> Obsidian `/content` klasöründeki varsayılan dosyaları kaldırmışsanız. `/content/templates` klasör içerisindeki dosyaya göz atabilirsiniz.

`Ayarlar (Setting)` > `Çekirdek Eklentileri (Core Plugins)`'ne gidin ve Şablonlar eklentisini etkinleştirin. Ardından `Ayarlar (Setting)` > `Kısayol Tuşları (Hotkeys)`'na gidin ve `‘Şablonu Ekle’` (kısayol tuşu ayarlayın `[cmd]+T`). Bu şekilde, yeni bir not oluşturduğunuzda, yeni bir şablon için kısayol tuşuna basabilir ve gitmeye hazır olabilirsiniz!

