FROM alpine

SHELL ["/bin/ash", "-c"]

RUN apk update && apk --no-cache add --update \
    python3
RUN wget https://bootstrap.pypa.io/get-pip.py
RUN python3 get-pip.py
RUN rm -rf get-pip.py
RUN pip3 install awscli --upgrade
# create credential
RUN mkdir /root/.aws \
    && echo $'[default]\n \
output = json\n \
region = $AWS_DEFAULT_REGION\n \
aws_access_key_id = $AMAZON_ACCESS_KEY_ID\n \
aws_secret_access_key = $AMAZON_SECRET_ACCESS_KEY' \
> /root/.aws/config

