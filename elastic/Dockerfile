FROM docker.elastic.co/elasticsearch/elasticsearch:6.2.4
USER root
ADD cors.yml /usr/share/elasticsearch/config/
RUN cat /usr/share/elasticsearch/config/cors.yml >> /usr/share/elasticsearch/config/elasticsearch.yml
RUN chown elasticsearch:elasticsearch config/elasticsearch.yml
USER elasticsearch
