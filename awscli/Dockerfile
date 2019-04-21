FROM alpine

SHELL ["/bin/ash", "-c"]

RUN apk update && apk --no-cache add --update \
    python3
RUN wget https://bootstrap.pypa.io/get-pip.py
RUN python3 get-pip.py
RUN rm -rf get-pip.py
RUN pip3 install awscli --upgrade
