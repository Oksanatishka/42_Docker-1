# Talking cow
# cowsay is a program that generates ASCII pictures of a cow with a message.
# https://en.wikipedia.org/wiki/Cowsay
# fortune is a program that displays a pseudorandom message from a database of quotations that first appeared in Version 7 Unix.
# https://en.wikipedia.org/wiki/Fortune_(Unix)
# lolcat produces rainbow of colors in terminal.
# https://github.com/busyloop/lolcat
# Flag -t is important in docker run --rm -t a00 command. Without this flag cow will get no color.

FROM debian

RUN apt-get update && apt-get install -y cowsay fortune lolcat

ENTRYPOINT /usr/games/fortune | /usr/games/cowsay | /usr/games/lolcat

# How to build it?
# docker build -t a00 .

# How to run it?
# docker run --rm -ti a00
