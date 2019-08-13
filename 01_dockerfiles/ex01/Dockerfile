FROM debian

MAINTAINER mcomet <mcomet@student.21-school.ru>

ENV TS3SERVER_LICENSE=accept

EXPOSE 9987/udp 10011 30033

WORKDIR /home/teamspeak

RUN	apt-get update -y && apt-get upgrade -y && \
	apt-get install wget bzip2 -y && \
	wget https://files.teamspeak-services.com/releases/server/3.9.1/teamspeak3-server_linux_amd64-3.9.1.tar.bz2 && \
	tar -xvf teamspeak3-server_linux_amd64-3.9.1.tar.bz2

WORKDIR teamspeak3-server_linux_amd64

ENTRYPOINT sh ts3server_minimal_runscript.sh
