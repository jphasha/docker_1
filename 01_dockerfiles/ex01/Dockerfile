FROM debian

# install the necessary enviromental stuff
RUN apt-get update && apt-get upgrade -y
RUN apt-get install -y wget && apt-get install -y tar && apt-get install -y bzip2

# create a user that we will use for the demo
ENV TS3SERVER_USR="demo_user"

# accessing the home directory of the demo user
WORKDIR /home/teamspeak

# download and extract the TeamSpeak3 server
RUN wget https://files.teamspeak-services.com/releases/server/3.9.1/teamspeak3-server_linux_amd64-3.9.1.tar.bz2 -O teamspeak3-server.tar.bz2
RUN tar -xvf teamspeak3-server.tar.bz2
RUN rm teamspeak3-server.tar.bz2

# accept TeamServer's EULA
ENV TS3SERVER_LICENSE="accept"

# expose the TCP port
EXPOSE 30033

# expose the listening port
EXPOSE 10011

# expose the server default port
EXPOSE 9987/udp

# enter the directory containing the server's executable
WORKDIR teamspeak3-server_linux_amd64

# run the executable
ENTRYPOINT sh ts3server_minimal_runscript.sh