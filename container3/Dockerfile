FROM ubuntu:latest
RUN apt-get update && apt-get install -y \
    python3 \
    apache2 \
    curl \
    iputils-ping \
    openssh-server \
    openssh-client \
    vim
COPY index.html /var/www/html/
COPY hello.py . 
RUN /etc/init.d/apache2 start 
RUN echo "ServerName localhost" >> /etc/apache2/apache2.conf
RUN service apache2 restart
CMD python3 hello.py;echo "Please check your localhost with the published port no"; apache2ctl -D FOREGROUND 
EXPOSE 80
EXPOSE 22
