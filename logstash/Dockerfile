ARG ELASTIC_VERSION=8.4.0

FROM docker.elastic.co/logstash/logstash:${ELASTIC_VERSION}

# Copy cấu hình pipeline vào container
COPY config/logstash.yml /usr/share/logstash/config/logstash.yml
COPY pipeline/logstash.conf /usr/share/logstash/pipeline/logstash.conf

# Expose port
EXPOSE 5000 5044
