# TeamSpeak
# From a debian image you will add the appropriate sources to create a TeamSpeak
# server, that will launch along with your container. It will be deemed valid if at least
# one user can connect to it and engage in a normal discussion (no far-fetched setup), so
# be sure to create your Dockerfile with the right options. Your program should get the
# sources when it builds, they cannot be in your repository.

FROM debian

ENV TS3SERVER_LICENSE=accept

WORKDIR /home/teamspeak

EXPOSE 9987/udp 10011 30033

RUN apt-get update -y && apt-get upgrade -y
RUN apt-get install wget -y
RUN apt-get install bzip2 -y
RUN wget http://dl.4players.de/ts/releases/3.2.0/teamspeak3-server_linux_amd64-3.2.0.tar.bz2
RUN tar xvf teamspeak3-server_linux_amd64-3.2.0.tar.bz2
RUN rm teamspeak3-server_linux_amd64-3.2.0.tar.bz2

CMD ["sh", "teamspeak3-server_linux_amd64/ts3server_minimal_runscript.sh"]

# docker build -t ex01 .
# docker run -it --rm --name ex1 -e TS3SERVER_LICENSE=accept -p 9987:9987/udp -p 10011:10011 -p 30033:30033 teamspeak

# https://linux.die.net/man/8/apt-get
# apt-get is the command-line tool for handling packages, and may be considered the user's "back-end" to other tools using the APT library.
# wget is a command line utility for downloading files from the Internet. 
# bzip2 file compression program 
# 
# x (extract) - untar or extract a tar file.
# v – Verbosely show the .tar file progress.
# f – File name type of the archive file.
