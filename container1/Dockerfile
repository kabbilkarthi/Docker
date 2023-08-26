FROM python:3.8
COPY . /cgi-bin
EXPOSE 7000
WORKDIR /cgi-bin
ENTRYPOINT python -m http.server 7000 
