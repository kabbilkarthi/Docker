FROM ubuntu:latest
RUN apt-get update && apt-get install -y \
    python3 \
    curl \
    iputils-ping \
    openssh-server \
    openssh-client
ADD index.html index.html
ADD server.py server.py
EXPOSE 8000
EXPOSE 22
EXPOSE 2022
ENTRYPOINT python3 ./server.py
