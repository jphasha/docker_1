# FROM debian

# RUN apt-get update && apt-get upgrade
# RUN apt-get install -y wget && apt-get install -y tar && apt-get install -y bzip2
# RUN adduser --disabled-login teamspeak
# WORKDIR /home/teamspeak
# RUN wget http://dl.4players.de/ts/releases/3.12.1/teamspeak3-server_linux_amd64-3.12.1.tar.bz2
# RUN tar xvf teamspeak3-server_linux_amd64-3.12.1.tar.bz2
# WORKDIR /teamspeak3-server_linux_amd64
# RUN mv * /home/teamspeak
# WORKDIR /..
# RUN rm -rf teamspeak3-server_linux_amd64-3.12.1.tar.bz2
# RUN touch /home/teamspeak/.ts3server_license_accepted
# RUN sudo nano /lib/systemd/system/teamspeak.service


# OTHER PEOPLE STUFF

# FROM debian

# ENV TS3SERVER_USR="teamspeak_usr"
# ENV TS3SERVER_GRP="teamspeak_grp"
# ENV TS3SERVER_LICENSE="accept"

# RUN apt-get update \
# 	&& apt-get upgrade -y \
# 	&& apt-get install -y \
# 	wget \
# 	tar \
# 	bzip2

# RUN groupadd $TS3SERVER_GRP && useradd -G $TS3SERVER_GRP $TS3SERVER_USR

# RUN wget https://files.teamspeak-services.com/releases/server/3.9.1/teamspeak3-server_linux_amd64-3.9.1.tar.bz2 -O teamspeak3-server.tar.bz2
# RUN tar -xvf teamspeak3-server.tar.bz2
# RUN rm teamspeak3-server.tar.bz2

# RUN chown -R $TS3SERVER_USR:$TS3SERVER_GRP /teamspeak3-server_linux_amd64 

# USER $TS3SERVER_USR:$TS3SERVER_GRP

# RUN chmod -R 774 /teamspeak3-server_linux_amd64

# # Opening file tranfers (tcp) port
# EXPOSE 30033 

# # Opening listening port
# EXPOSE 10011

# # Opening server default port
# EXPOSE 9987/udp