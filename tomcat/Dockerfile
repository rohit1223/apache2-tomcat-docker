FROM tomcat:7

# add context to /usr/local/tomcat/webapps
RUN apt-get install -y unzip

RUN rm -rf /usr/local/tomcat/webapps/*
#RUN rm -rf /usr/local/tomcat/webapps/ROOT/*

COPY ./companyNews.war /usr/local/tomcat/webapps/companyNews.war

RUN mkdir /usr/local/tomcat/webapps/ROOT && \
	unzip /usr/local/tomcat/webapps/companyNews.war -d /usr/local/tomcat/webapps/ROOT && \
	rm /usr/local/tomcat/webapps/companyNews.war 

EXPOSE 8009
