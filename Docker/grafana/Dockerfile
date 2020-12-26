FROM grafana/grafana:7.3.5

USER root
RUN apk update 
RUN apk add gettext 
RUN apk --no-cache add curl && rm -rf /var/lib/apt/lists/*

WORKDIR /etc/grafana
COPY datasources ./datasources

WORKDIR /app
COPY entrypoint.sh ./
RUN chmod u+x entrypoint.sh

ENTRYPOINT ["/app/entrypoint.sh"]
