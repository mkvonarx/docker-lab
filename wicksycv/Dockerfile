FROM wicksy/base:latest

RUN apk update && \
    apk add bash && \
    apk add git && \
    pip install --upgrade pip && \
    pip install boto && \
    pip install boto3 && \
    pip install mkdocs && \
    addgroup wicksy && \
    adduser -h /home/wicksy -s /bin/bash -D -G wicksy wicksy && \
    mkdir -p /data/cv/ && \
    chown wicksy:wicksy /data/cv && \
    chmod -R 755 /data

EXPOSE 8080
VOLUME /data/cv

USER wicksy
WORKDIR /data/cv

CMD ["/usr/bin/mkdocs", "serve", "--dev-addr", "0.0.0.0:8080", "--theme", "readthedocs"]
