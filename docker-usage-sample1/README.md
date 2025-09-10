# Basit Docker Örneği

Projeyi Çalıştırmak İçin Buil Alalım:
```
docker build . -t pandas_test
```

. -> çalıştığım dizinin adı
pandas_test -> Image a verdiğim ad

Projeyi Çalıştıralım:
```
docker run pandas_test
```
pandas_test -> Image a verdiğim ad


Beklenen Çıktı:
```
   a
0  1
1  2
2  3
3  4
```