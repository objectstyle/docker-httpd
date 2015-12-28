# ObjectStyle HTTPD Docker Image
This is a HTTPD Docker image for ObjectStyle [site](http://www.objectstyle.com/). Built on top of [centos:centos7](https://hub.docker.com/_/centos/) image.

## Usage

`docker pull objectstyle/httpd`

Or, if you prefer to build it on your own:  
`docker build -t objectstyle/httpd .`

Run the image (example):  
`docker run -d --name httpd \
	--net=osllc \
	-p 80:80 \
	-p 443:443 \
	-v $CONF_ROOT:/etc/httpd/conf.d \
	-v $HTML_ROOT:/var/www \
	-v $SSL_ROOT:/etc/httpd/ssl \
	objectstyle/httpd`
