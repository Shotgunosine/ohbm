FROM docker.elastic.co/kibana/kibana:6.2.4
USER root
ADD ssl.yml /usr/share/kibana/config/ssl.yml
RUN cat /usr/share/kibana/config/ssl.yml >> /usr/share/kibana/config/kibana.yml
RUN chown kibana:kibana config/kibana.yml
COPY ssl/search.ohbm-openscience.org /usr/share/kibanda/config/ssl/search.ohbm-openscience.org
RUN  chmod 550 /usr/share/kibanda/config/ssl/search.ohbm-openscience.org &&  chmod 440 /usr/share/kibanda/config/ssl/search.ohbm-openscience.org/* \
     && chown -R kibana:kibana /usr/share/kibanda/config/ssl/search.ohbm-openscience.org
USER kibana
