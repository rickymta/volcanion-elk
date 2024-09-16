ARG ELASTIC_VERSION

FROM docker.elastic.co/kibana/kibana:${ELASTIC_VERSION}

# Copy tệp cấu hình tùy chỉnh vào container
COPY config/kibana.yml /usr/share/kibana/config/kibana.yml

# Expose port
EXPOSE 5601
