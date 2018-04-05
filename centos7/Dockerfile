FROM centos:7
LABEL maintainer="Major Hayden <major@redhat.com>"
ADD yum-transaction.txt /tmp/yum-transaction.txt
RUN yum -y shell /tmp/yum-transaction.txt
RUN yum-builddep -y kernel
RUN rm -fv /tmp/yum-transaction.txt
CMD ["/bin/bash", "-c"]
