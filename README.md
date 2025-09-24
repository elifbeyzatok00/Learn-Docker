# Learn-Docker: Python ile Docker Kullanımı Örnekleri

Bu depo, Docker'ın temellerini öğrenmek ve Python projelerinde nasıl kullanılacağını göstermek amacıyla hazırlanmıştır. Hem basit bir Python scripti hem de FastAPI tabanlı bir web uygulamasının Docker ile nasıl containerize edileceğini örneklerle bulabilirsiniz.

## İçerik

- **docker-usage-sample1/**  
  Basit bir Python scriptinin (pandas ile) Docker container'ında çalıştırılması örneği.
- **docker-usage-sample2/**  
  FastAPI ile yazılmış bir web uygulamasının Docker container'ında çalıştırılması örneği.

## Hızlı Başlangıç

Her bir örnek klasöründe, ilgili uygulamayı Docker ile nasıl build ve run edeceğinize dair adımların yer aldığı bir `README.md` dosyası bulunmaktadır.

## Docker Terimleri

**Dockerfile:** Adımları tek tek yazacağımız *dosya*.

**Image:** Dockerfile'a yazdığımız adımları takip ederek, örneğin Python'ı indir, pandas'ı indir gibi işlemleri yapıp çalıştırmak üzere hazır hale getirdiğimiz *paket*.

**Container:** Hazırladığımız bu Image'ı çalıştıracağımız *ortam*.

![Docker](docker.png)

## Container Sunucu Mudur?

Hayır, container bir **sunucu** değildir ama onun üzerinde bir uygulama çalıştırabilirsiniz. Aradaki farkı şöyle netleştirebiliriz:

* **Container:** **Fiziksel bir sunucuda ya da sanal bir makinede çalışan bir yazılım katmanı**dır. Yani kendisi fiziksel olarak ayrı bir makine değildir, ama sunucunun işletim sistemi üzerinde izole bir ortam olarak çalışır.
* **Sunucu (Server):** Fiziksel ya da sanal bir makineyi ifade eder. Üzerinde bir işletim sistemi çalışır ve container’ları barındırabilir.

Özetle:

* **Container**, uygulamanın çalıştığı izole, hafif bir ortamdır; kendi dosya sistemi ve bağımlılıkları vardır ama fiziksel bir makine değildir.
* **Sunucu**, fiziksel veya sanal bir makinedir; üzerinde işletim sistemi çalışır ve container’ları barındırabilir.
* **Image → Container → Çalışan uygulama** zinciri ile düşünülebilir.
* Container, sunucunun kaynaklarını kullanır ve geçici bir ortam sağlar; kalıcı veri için volume gerekir.

Yani container, **sunucu üzerinde çalışan küçük bir sanal çalışma ortamıdır**, kendisi ayrı bir sunucu değildir.

## Docker’ın Öne Çıkan Avantajları Neler?

⭐ **Taşınabilirlik** → Docker konteynerleri, “bir kez paketle, her yerde çalıştır” mantığıyla tüm işletim sistemlerinde (Linux, Windows, macOS) aynı şekilde çalışır.

⭐ **Versiyonlama** → İmajların farklı sürümleri tutulabilir, böylece geri dönüş (rollback) kolaydır.

⭐ **Kaynak yönetimi** → Bellek (memory), CPU, disk gibi kaynaklar kolayca sınırlanabilir veya ölçeklendirilebilir.

* **Hızlı kurulum** → Uygulamalar ve bağımlılıkları tek bir imajda tutulduğu için “çalışmıyor” sorunlarını (dependency hell) büyük ölçüde ortadan kaldırır.
* **Hafiflik** → Sanal makinelere göre daha az kaynak tüketir; çünkü host işletim sistemi çekirdeğini paylaşır.
* **İzolasyon** → Her uygulama kendi konteynerinde bağımsız çalıştığı için güvenlik ve kararlılık artar.
* **Otomasyon ve CI/CD entegrasyonu** → GitHub Actions, GitLab CI, Jenkins vb. sistemlerle kolay entegre olur; test, build ve deploy süreçlerini hızlandırır.
* **Kolay paylaşım** → Docker Hub ve özel registry’ler sayesinde imajlar hızlıca paylaşılabilir.
* **Mikroservis uyumluluğu** → Uygulamaları küçük, yönetilebilir parçalara bölerek dağıtık sistemler geliştirmeyi kolaylaştırır.

## Kaynaklar

- [📺Kurs Video Linki](https://www.youtube.com/watch?v=ISdxKNCftKs)
