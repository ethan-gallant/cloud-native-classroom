# envoy proxy
FROM envoyproxy/envoy:v1.24-latest AS envoy
COPY ./envoy.yaml /etc/envoy/envoy.yaml
CMD /usr/local/bin/envoy -c /etc/envoy/envoy.yaml
