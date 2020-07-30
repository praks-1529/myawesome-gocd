FROM gocd/gocd-agent-docker-dind:v20.5.0
USER root
RUN apk add --no-cache curl
RUN apk add --no-cache unzip
RUN apk add --no-cache terraform
ADD ./aws.credentials /root/.aws/credentials
RUN ["/usr/bin/curl", "https://awscli.amazonaws.com/awscli-exe-linux-x86_64.zip", "-o", "/root/awscliv2.zip"]
RUN ["/usr/bin/unzip", "/root/awscliv2.zip"]
RUN ["/aws/install", "--update"]
