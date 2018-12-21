# A developing environment to code in nodejs, but using yarn rather than npm

FROM ubuntu

RUN apt-get update && apt-get upgrade -y && apt-get install -y nodejs npm git vim emacs

RUN npm install yarn --global && npm install npm --global

# How to build it?
# docker build -t a03 .

# How to run it?
# docker run --rm -ti a03

# Yarn is a package manager https://yarnpkg.com/
