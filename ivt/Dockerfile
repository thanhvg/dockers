# start from base
FROM ubuntu:16.04

RUN apt-key adv --keyserver hkp://p80.pool.sks-keyservers.net:80 --recv-keys B97B0AFCAA1A47F044F244A07FCC7D46ACCC4CF8
RUN echo "deb http://apt.postgresql.org/pub/repos/apt/ precise-pgdg main" > /etc/apt/sources.list.d/pgdg.list

RUN apt-get -yqq update

RUN apt-get install -y python-software-properties software-properties-common postgresql-9.6 postgresql-contrib-9.6 libpq-dev

# install system-wide deps for python and node
# RUN apt-get -yqq install apt-utils
# RUN apt-get update && apt-get install -y --no-install-recommends apt-utils
# python
RUN apt-get -yqq install build-essential libssl-dev libffi-dev python3-dev python3-pip curl gnupg subversion

# COPY requirements.txt ./
# RUN pip3 install -r requirements.txt

RUN curl -sL https://deb.nodesource.com/setup_6.x | bash
RUN apt-get install -yq nodejs

RUN pip3 install cx_freeze
RUN pip3 install pyusb
RUN pip3 install flask

RUN apt-get -yqq install python3-numpy python3-dns

RUN pip3 install eventlet
RUN pip3 install requests
RUN pip3 install psycopg2
RUN pip3 install pillow
RUN pip3 install dnspython

#Install tensorflow package

RUN pip3 install tensorflow==1.10

RUN pip3 install pyinstaller

