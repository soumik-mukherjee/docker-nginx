# docker-nginx

### Pre-requisites
Please ensure host has `docker` and `docker-compose` installed before using this. You will also need `git` installed on the host if you want to clone this repo directly there directly. All following steps assume this approach.

### About the included NGINX configuration
The included configuration is a simple proxy server to a `kibana 5` instance. Alter as per your requirements. The included `conf` file with a `kibana 5` instance running on a private IP of `10.0.0.20` port `5601`, will allow you to access the `kibana 5` portal with the following url `http://<your_nginx_public_hostname>/app/kibana` 

### Starting the container
Once all setup and cloning of the repo is complete, `cd` to the directory `docker-nginx` and issue the following command 
``` bash
docker-compose up -d
```
That's it! you should be up and running. It would be useful to check the NGINX logs and ensure everything went fine (i.e. no errors), to do so use the following
``` bash
docker-compose logs nginx
```
To bring down the container, use
``` bash
docker-compose down
```
