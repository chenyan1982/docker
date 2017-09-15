FROM tomcat:jre8

# admin/admin user
ADD ./tomcat-users.xml /usr/local/tomcat/conf/
 
 EXPOSE 8080
# EXPOSE 8080

 RUN mkdir /usr/local/tomcat/webapps/apidocs
 RUN mkdir /usr/local/tomcat/webapps/apidocs/WEB-INF
 RUN mkdir /usr/local/tomcat/webapps/apidocs/doc

 ADD ./WEB-INF/web.xml /usr/local/tomcat/webapps/apidocs/WEB-INF/web.xml

 VOLUME "/usr/local/tomcat/webapps/apidocs/doc"
 WORKDIR /usr/local/tomcat/webapps/apidocs/doc

# tomcat
 CMD ["/usr/local/tomcat/bin/catalina.sh", "run"]