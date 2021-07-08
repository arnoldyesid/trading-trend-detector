# base image  
FROM ubuntu:18.04
# to install packects
RUN apt-get update && apt-get install -y \
net-tools inetutils-traceroute \
iputils-ping xinetd telnetd

# setup environment variable 
COPY requirements.txt ./usr/app/
ENV DockerHOME=/usr/app
# set work directory  
RUN mkdir -p $DockerHOME  

# where your code lives  
WORKDIR $DockerHOME  

# set environment variables  
ENV PYTHONDONTWRITEBYTECODE 1
ENV PYTHONUNBUFFERED 1  
# install dependencies
RUN apt-get update -y
RUN apt-get install python3-pip -y
# copy whole project to your docker home directory. COPY . $DockerHOME  
# run this command to install all dependencies  
RUN pip3 install -r requirements.txt
# port where the Django app runs  
EXPOSE 8000  

