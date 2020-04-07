FROM jrei/systemd-ubuntu

RUN apt-get update -y

RUN apt-get install gnupg -y

RUN apt-get install ca-certificates -y

RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv D68FA50FEA312927

RUN echo "deb https://repo.mongodb.org/apt/ubuntu xenial/mongodb-org/3.2 multiverse" | tee /etc/apt/sources.list.d/mongodb-org-3.2.list

RUN apt-get install apt-transport-https -y

RUN apt-get update -y

RUN apt-get upgrade -y

RUN apt-get install -y mongodb-org=3.2.20 mongodb-org-server=3.2.20 mongodb-org-shell=3.2.20 mongodb-org-mongos=3.2.20 mongodb-org-tools=3.2.20

# RUN rm /lib/systemd/system/mongod.service

# COPY environment/db/mongod.service /lib/systemd/system/mongod.service

RUN rm /etc/mongod.conf

COPY environment/db/mongod.conf /etc/mongod.conf

EXPOSE 27017

# RUN mkdir /data && mkdir /data/db

# CMD systemctl restart mongod && systemctl enable mongod 

CMD bash
