# Python (FastAPI) ile Docker Örneği

Projeyi Çalıştırmak İçin Buil Alalım:
```
docker build . -t my_fastapi
```

. -> çalıştığım dizinin adı
my_fastapi -> Image a verdiğim ad

Projeyi Çalıştıralım:
```
docker run my_fastapi
```
my_fastapi -> Image a verdiğim ad


Beklenen Çıktı:
```
INFO:     Started server process [1]
INFO:     Waiting for application startup.
INFO:     Application startup complete.
INFO:     Uvicorn running on http://0.0.0.0:8000 (Press CTRL+C to quit) 
```

http://0.0.0.0:8000 buna tıklayınca proje açılmıyor çünkü şuan localimde 8000 portunda çalışmıyor. Container içinde 8000 portunda çalışıyor.

Localimdeki ve Containerdaki 8000 portunu eşleştirmek gerek:
```
docker run -p 8000:8000 my_fastapi
```

"http://localhost:8000/" -> buraya gittiğimde şimdi görüntüleyebilirim

Beklenen Çıktı:
```
{"message":"Hello World"}
```