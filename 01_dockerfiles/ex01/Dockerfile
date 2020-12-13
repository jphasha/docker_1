FROM debian

RUN apt-get update && apt-get upgrade
RUN adduser --disabled-login teamspeak
WORKDIR /home/teamspeak
RUN wget http://dl.4players.de/ts/releases/3.12.1/teamspeak3-server_linux_amd64-3.12.1.tar.bz2
RUN tar xvf teamspeak3-server_linux_amd64-3.12.1.tar.bz2
WORKDIR /teamspeak3-server_linux_amd64
RUN mv * /home/teamspeak
WORKDIR /..
RUN rm -rf teamspeak3-server_linux_amd64-3.12.1.tar.bz2
RUN touch /home/teamspeak/.ts3server_license_accepted
RUN sudo nano /lib/systemd/system/teamspeak.service