FROM prom/prometheus:v2.14.0

RUN mkdir -p /tmp/prometheus
COPY prometheus.yml /tmp/prometheus.yml
COPY alerts.yml /tmp/alerts.yml
WORKDIR /tmp
ENTRYPOINT [ "/bin/prometheus", "--config.file=/tmp/prometheus.yml", "--storage.tsdb.path=/var/lib/prometheus" ]
