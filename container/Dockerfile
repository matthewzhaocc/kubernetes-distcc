FROM ubuntu:latest
RUN apt-get update
RUN apt upgrade -y
RUN apt install build-essential apt-transport-https -y
RUN apt install wget -y
RUN wget https://github.com/distcc/distcc/releases/download/v3.4/distcc-3.4.tar.gz
RUN tar -xvf distcc-3.4.tar.gz
RUN apt install libiberty-dev python3 python3-pip -y
WORKDIR /distcc-3.4
RUN ./configure
RUN make
RUN make install
RUN useradd distcc
EXPOSE 3632
CMD distccd --daemon --listen 0.0.0.0 --allow 0.0.0.0/0 --verbose --log-stderr --enable-tcp-insecure && sleep infinity