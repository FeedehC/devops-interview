#FROM ubuntu
#FROM python:3-alpine
#FROM python:3.7-alpine
#FROM python:3.7-slim
FROM python:3.7
#FROM alpine

WORKDIR /app

#Copia los archivos a la carpeta (workdir)
COPY . .

#RUN apk add --update --no-cache python3 py3-pip
    #&& pip install --no-cache-dir -U pip wheel setuptools
RUN apt update && apt install python3 python3-pip libgraphviz-dev nodejs npm -y

RUN pip install -r requirements.txt

EXPOSE 5000

CMD ["python", "manage.py", "runserver", "0.0.0.0:5000"]