FROM websphere-liberty

MAINTAINER bob.hambleton@natwest.com

RUN mkdir -p /opt/ibm/wlp/usr/shared/apps/SampleWebApp.war

ADD SampleWebApp.war /opt/ibm/wlp/usr/shared/apps/SampleWebApp.war

WORKDIR  /opt/ibm/wlp/usr/shared/apps/SampleWebApp.war
RUN tar xvzf SampleWebApp.war
RUN rm SampleWebApp.war

ADD server.xml /opt/ibm/wlp/usr/servers/defaultServer/
ADD application.xml /opt/ibm/wlp/usr/servers/defaultServer/

ENV LICENSE accept
