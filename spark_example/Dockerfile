FROM gcr.io/spark-operator/spark-py:v3.1.1

WORKDIR /

USER root

RUN mkdir /var/test_nfs

RUN chmod 777 /var/test_nfs

VOLUME /var/test_nfs

RUN apt-get -y --allow-releaseinfo-change-suite update
RUN apt-get -y install vim
RUN apt-get -y install nano
RUN apt-get -y install less
RUN apt-get -y install tini

COPY ./pi2.py /var/pi2.py
COPY ./filelist.py /var/filelist.py


