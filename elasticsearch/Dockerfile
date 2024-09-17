ARG ELASTIC_VERSION=8.4.0

FROM docker.elastic.co/elasticsearch/elasticsearch:${ELASTIC_VERSION}

# Copy tệp cấu hình tùy chỉnh vào container
COPY config/elasticsearch.yml /usr/share/elasticsearch/config/elasticsearch.yml

# Expose port
EXPOSE 9200 9300
