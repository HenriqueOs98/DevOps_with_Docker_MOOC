FROM ubuntu:20.04

RUN apt update && apt upgrade 
RUN apt install curl -y
COPY script.sh .


CMD ["./script.sh"]