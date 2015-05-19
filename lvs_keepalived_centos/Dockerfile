FROM tutum/centos-6.4:latest

MAINTAINER by anthony

RUN yum install -y ipvsadm keepalived

COPY keepalived.tmpl /app/keepalived.tmpl
COPY run.sh /app/run.sh
RUN chmod 755 /app/run.sh

# Install Docker-gen
COPY docker-gen /app/
RUN chmod u+x /app/docker-gen

CMD ["/app/run.sh"]

