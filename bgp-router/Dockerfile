# base image
FROM ubuntu:22.04

# update and install bird routing deamon
RUN apt update && apt install iputils-ping -y && apt install bird2 -y

# start bgp server
CMD mkdir -p /run/bird && bird -d