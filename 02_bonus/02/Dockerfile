# Containerize the server of your favorite game, like Minecraft
# https://minecraft.net/en-us/download/server/

FROM debian

RUN apt-get update && apt-get upgrade -y && apt-get install -y wget default-jre

WORKDIR minecraft

RUN wget https://launcher.mojang.com/mc/game/1.13/server/d0caafb8438ebd206f99930cfaecfa6c9a13dca0/server.jar

RUN echo 'eula=true' > eula.txt

EXPOSE 25565

ENTRYPOINT java -Xmx1024M -Xms1024M -jar server.jar

# How to build it?
# docker build -t a02 .

# How to run it?
# docker run --rm -d -p 25565:25565 a02

# The default JRE is used for compiling and launching Java programs in all projects.
# -Xmxn   Specify the maximum size, in bytes, of the memory allocation pool.
