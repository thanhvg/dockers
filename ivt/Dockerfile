# start from base
FROM ubuntu:16.04

# install system-wide deps for python and node
RUN apt-get -yqq update
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
RUN pip3 install psycopg2
RUN pip3 install pillow
RUN pip3 install dnspython

#Install tensorflow package

RUN pip3 install tensorflow

RUN pip3 install pyinstaller

