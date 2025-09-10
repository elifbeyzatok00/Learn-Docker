FROM python:3.12

WORKDIR /src

ADD requirements.txt .

RUN pip install -r requirements.txt

ADD ./app ./app

CMD ["python", "./app/main.py"]