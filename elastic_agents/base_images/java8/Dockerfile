FROM gocd/gocd-agent-docker-dind:v20.5.0
USER root
RUN apk add --no-cache maven
RUN apk add --no-cache openjdk8
RUN apk add --no-cache terraform
RUN apk add --no-cache python3 py-pip
RUN pip install awscli
ADD ./aws.credentials /root/.aws/credentials
