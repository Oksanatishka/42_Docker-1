# From an alpine image you’ll add to your container your favorite text editor, vim or
# emacs, that will launch along with your container.

FROM alpine

RUN apk update && \
    apk upgrade && \
    apk add vim

CMD	["vim"]

# How to build it?
# docker build -t ex00 .

# How to run it?
# docker run --rm -ti ex00

# p.s. this exercise requires Char docker-machine

# https://www.cyberciti.biz/faq/10-alpine-linux-apk-command-examples/
# APK stands for Alpine Linux package manager. You use the apk command to delete, install, upgrade, 
# or list software on a running Alpine Linux based system.
# apk add pkgName // to install a package(s) by name
# apk update && apk upgrade // to upgrade running Alpine Linux
