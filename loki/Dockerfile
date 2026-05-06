FROM dhi.io/loki:3.6

COPY config.yaml /etc/loki/config.yaml

EXPOSE 3100

ENTRYPOINT ["/usr/bin/loki"]
CMD ["-config.file=/etc/loki/config.yaml"]
