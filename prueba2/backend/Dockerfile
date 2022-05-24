#FROM ubuntu
FROM alpine

WORKDIR /apps

#Copia los archivos a la carpeta /apps (workdir)
COPY . .

RUN apk add --update --no-cache python3 py3-pip
#RUN apt update && apt install python3 python3-pip -y

RUN pip install -r requirements.txt

EXPOSE 5000

CMD ["python", "__init__.py"]