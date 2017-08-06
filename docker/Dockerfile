FROM centos:7

MAINTAINER Ed Seymour <eseymour@redhat.com>

RUN yum install rsync -y && yum clean all -y 

VOLUME /srcd
VOLUME /dest

CMD rsync -apvH /srcd/ /dest/
