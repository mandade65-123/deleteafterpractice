FROM ubuntu:latest
#base image is added

LABEL dev="anup"
#giving tags to the docker 

RUN apt-get update && \
    apt-get install apache2 unzip -y && \
    rm -rf /var/www//html/index.html
#we installed webserver and unzip package and updated the base image

ADD https://templatemo.com/download/templatemo_623_novapay /var/www/html/templatemo_623_novapay.zip
# add will download static page from internet and move it in /var/www/html location


 WORKDIR /var/www/html 
 #changing/switching directories to /var/www/html 


RUN unzip templatemo_623_novapay.zip &&  \
    mv templatemo_623_novapay/* /var/www/html/
#unzip the directory and move static code into the /var/www/html
    
EXPOSE 80
    #the container will be having 88 port open

    #cmd is used to start the single running process on docker.
    CMD ["apache2ctl", "-D", "FOREGROUND"]
