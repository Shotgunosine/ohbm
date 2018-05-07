FROM docker.elastic.co/elasticsearch/elasticsearch:6.2.4
USER root
ADD cors.yml /usr/share/elasticsearch/config/
RUN cat /usr/share/elasticsearch/config/cors.yml >> /usr/share/elasticsearch/config/elasticsearch.yml
RUN chown elasticsearch:elasticsearch config/elasticsearch.yml
RUN mkdir -p /etc/elasticsearch/ssl
COPY ssl/search.ohbm-openscience.org /usr/share/elasticsearch/config/ssl/search.ohbm-openscience.org
RUN  chmod 550 /usr/share/elasticsearch/config/ssl/search.ohbm-openscience.org &&  chmod 440 /usr/share/elasticsearch/config/ssl/search.ohbm-openscience.org/* \
     && chown -R elasticsearch:elasticsearch /usr/share/elasticsearch/config/ssl/search.ohbm-openscience.org
USER elasticsearch
