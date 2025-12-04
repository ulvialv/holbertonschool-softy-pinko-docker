FROM ubuntu:latest

RUN apt-get update
RUN apt-get upgrade -y

# Python3 və pip3 quraşdır
RUN apt-get install -y python3 python3-pip

# EXTERNALLY-MANAGED error-unu aradan qaldır (Holberton tələb edir)
RUN rm /usr/lib/python*/EXTERNALLY-MANAGED || true

# Flask-i pip3 ilə quraşdır
RUN pip3 install flask

# İş qovluğu
WORKDIR /app

# API faylını image-ə kopyala
COPY ./api.py /app/api.py

# Container işə düşəndə Flask serveri başlasın
CMD ["python3", "api.py"]
