ARG LOKI_VERSION=3.0.0

FROM grafana/loki:${LOKI_VERSION} as builder

FROM dhi.io/hardened/alpine:latest

COPY --from=builder /usr/bin/loki /usr/local/bin/loki

COPY config.yaml /etc/loki/config.yaml

ENTRYPOINT ["/usr/local/bin/loki"]
CMD ["-config.file=/etc/loki/config.yaml"]
