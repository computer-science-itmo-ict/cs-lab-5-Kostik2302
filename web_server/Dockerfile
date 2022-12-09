FROM ubuntu:latest
RUN apt-get update && apt-get install -y apache2
RUN echo "<html> \n\
<head> \n\
  <title> I love Docker! </title> \n\
</head> \n\
<body> \n\
  <p> Hello world! I'm Konstantin Dolgov and I study at ITMO University! </p> \n\
</body> \n\
</html>" > var/www/html/index.html
RUN sed -i -e 's/Listen 80/Listen 80\nServerName localhost/' /etc/apache2/ports.conf
CMD ["apache2ctl", "-D", "FOREGROUND"]
EXPOSE 80
