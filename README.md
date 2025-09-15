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

## Kaynaklar

- [📺Kurs Video Linki](https://www.youtube.com/watch?v=ISdxKNCftKs)