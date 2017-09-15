FROM tomcat:jre8

# admin/admin user
ADD ./tomcat-users.xml /usr/local/tomcat/conf/
 
 EXPOSE 8080
# EXPOSE 8080

 VOLUME "/usr/local/tomcat/webapps"
 WORKDIR /usr/local/tomcat

# tomcat
 CMD ["/usr/local/tomcat/bin/catalina.sh", "run"]