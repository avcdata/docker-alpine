FROM bhuisgen/alpine-base:latest
MAINTAINER Boris HUISGEN <bhuisgen@hbis.fr>

ENV TERRAFORM_VERSION=0.8.6

RUN apk add --update zip && \
    curl -sSL https://releases.hashicorp.com/terraform/${TERRAFORM_VERSION}/terraform_${TERRAFORM_VERSION}_linux_amd64.zip -o /tmp/terraform.zip && \
    unzip /tmp/terraform.zip -d /usr/bin && \
    rm /tmp/terraform.zip && \
    apk del zip && \
    rm -rf /var/cache/apk/*

ENTRYPOINT ["terraform"]
CMD []

VOLUME ["/data"]
WORKDIR /data
