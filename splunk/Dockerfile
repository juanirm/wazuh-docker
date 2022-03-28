FROM centos
#USER admin

RUN yum install splunk-enterprise-package.rpm

ENV SPLUNK_HOME="/opt/splunk"
ENV SPLUNK_ETC="/opt/splunk/etc"

WORKDIR /opt/splunk
COPY --chown=splunk:splunk ./config/indexes.conf ./etc/system/local
COPY --chown=splunk:splunk ./config/inputs.conf ./etc/system/local

#ENTRYPOINT [ "./bin/splunk","start" ]
ENTRYPOINT ["bash"]