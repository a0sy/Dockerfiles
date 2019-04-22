FROM alpine

SHELL ["/bin/ash", "-c"]

ARG terraform_version="0.11.13"

WORKDIR /root/terraform

RUN apk update && apk --no-cache add --update \
    vim \
    git
RUN wget https://releases.hashicorp.com/terraform/${terraform_version}/terraform_${terraform_version}_linux_amd64.zip \
    && unzip terraform_${terraform_version}_linux_amd64.zip
ENV PATH $PATH:/root/terraform

