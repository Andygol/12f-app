---
title: Ana Sayfa
description: Yazılım hizmeti (SaaS) uygulamaları oluştururken esneklik, taşınabilirlik ve ölçeklenebilirlik sağlama yöntemleri.
hide:
 - toc
 - navigation
---

## Giriş

Modern çağda yazılımlar çoğunlukla "web uygulaması" ya da "yazılım hizmeti" olarak isimlendirilen servisler olarak sunulurlar. *On iki faktörlü uygulama*, servis olarak çalışan yazılımlar (İng. *software as a service* veya *SaaS*) geliştirmek için bir yöntembilimdir. Bu yöntembilimin kuralları ve faydaları şunlardır:

* Projenin kurulum otomasyonu için **açıklayıcı** (İng. declarative) biçimler kullanır. Bu şekilde, projeye yeni katılan geliştiricilerin geliştirmeye başlama zamanını ve maliyetinı en aza indirir;
* Üzerinde çalıştığı işletim sistemi ile arasında **basit bir bağlılık** vardır. Bu, tüm çalıştırma ortamlarına (Docker gibi *container* sistemleri ve sıradan işletim sistemlerine) **maksimum uyumluluk** sağlar;
* Sunucu ve sistem yönetimine olan ihtiyacı ortadan kaldıran modern **bulut platformlarına kurulum** için uygundur;
* Geliştirme ve canlı yayın ortamları arasında **farklılıklaşmayı minimize ederek**, maksimum çeviklik ile **sürekli dağıtımı**n önünü açar;
* Kullanılan araçlarda, mimaride veya geliştirme pratiklerinde önemli değişikliklere gerek duymadan **ölçeklenebilir**.

On iki faktör uygulaması herhangi bir programlama dili ile yazılmış ve yardımcı (veritabanları, kuyruk işleyiciler, önbellek, vb. gibi) servislerin herhangi bir kombinasyonuna sahip tüm uygulamalara uygulanabilir.

## Arkaplan

Bu belgeye katkıda bulunan kişiler, yüzlerce uygulamanın geliştirilmesi ve yayınlanmasında doğrudan yer almış, ve dolaylı olarak <a href="http://www.heroku.com/" target="_blank">Heroku</a> platformundaki üzerinde çalıştığımız yüz binlerce uygulamanın geliştirilmesi, çalıştırılması ve ölçeklendirilmesine tanık olmuştur.

Bu belge birçok yazılım servisinde edindiğimiz deneyim ve gözlemlerimizin bir sentezidir. Uygulama geliştirme aşamasındaki ideal pratiklerin, uygulamaların zaman içindeki organik büyüyüşlerine gösterilen özel ilginin, bir uygulamanın kodları üzerinde çalışan geliştiriciler arasındaki işbirliği dinamiklerinin, ve <a href="http://blog.heroku.com/archives/2011/6/28/the_new_heroku_4_erosion_resistance_explicit_contracts/" target="_blank">yazılım erozyonunun getirdiği masraftan kaçınmanın</a> toplamı niteliğindedir.

Motivasyonumuz modern uygulama geliştirmelerinde gördüğümüz bazı sistemik problemlere olan farkındalığı arttırmak, bahsi geçen problemler için ortak bir terminoloji belirlemek, ve bu problemlere karşı bir dizi çözüm konsepti sunmaktır. Bu konsept oluşturulurken, Martin Fowler'ın kitapları olan *<a href="https://books.google.com/books/about/about/Patterns_of_enterprise_application_archi.html?id=FyWZt5DdvFkC" target="_blank">Patterns of Enterprise Application Architecture</a>* ve *<a href="https://books.google.com/books/about/Refactoring.html?id=1MsETFPD3I0C" target="_blank">Refactoring</a>*'den ilham alınmıştır.

## Bu belgeyi kim okumalı?

Servis yazılımı geliştiren tüm geliştiriciler. Bu tür uygulamaları yayınlayan ve yöneten operasyon mühendisleri.

## On İki Faktör

### [I. Kod tabanı](./codebase.md)

Sürüm kontrol sistemi üzerinde tek bir kod tabanı, birden fazla dağıtım

### [II. Bağımlılıklar](./dependencies.md)

Bağımlılıkların açıkça tanımlanması ve izole edilmesi

### [III. Yapılandırma](./config.md)

Yapılandırma ayarlarını ortam değişkeni olarak saklama

### [IV. Yardımcı servisler](./backing-services.md)

Yardımcı servisleri iliştirilmiş kaynaklar olarak ele almak

### [V. Derleme, yayınlama, çalıştırma](./build-release-run.md)

Derleme ve çalıştırma aşamalarını tam olarak ayırma

### [VI. Süreçler](./processes.md)

Uygulamayı bir veya daha fazla bağımsız süreç olarak çalıştırma

### [VII. Port bağlama](./port-binding.md)

Servisin portlar üzerinden sunulması

### [VIII. Eş zamanlılık](./concurrency.md)

Süreç modeli ile ölçeklendirme

### [IX. İmha edilebilirlik](./disposability.md)

Hızlı başlangıç ve zararsız sonlanma ile maksimum servis sağlığı

### [X.Geliştirme/Üretim Eşitliği](./dev-prod-parity.md)

Geliştirme, test etme ve canlı yayın ortamının birbirine olabildiğince benzer olması

### [XI. Günlükler](./logs.md)

Günlükleri olay akışı olarak ele almak

### [XII. Yönetici Süreci](./admin-processes.md)

Yönetici/yönetim görevlerini tek seferlik süreçler olarak çalıştırma
