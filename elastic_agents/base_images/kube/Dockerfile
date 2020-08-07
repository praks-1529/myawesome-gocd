FROM gocd/gocd-agent-docker-dind:v20.5.0
USER root
ADD ./.kube /root/.kube
#ADD ./.minikube /root/.minikube
ADD ./kubecfg-linux-amd64 /usr/local/bin/kubecfg
RUN chmod +x /usr/local/bin/kubecfg
RUN apk add --no-cache curl
RUN apk add --no-cache unzip
RUN curl -LO https://storage.googleapis.com/kubernetes-release/release/$(curl -s https://storage.googleapis.com/kubernetes-release/release/stable.txt)/bin/linux/amd64/kubectl
RUN chmod +x ./kubectl
RUN mv ./kubectl /usr/local/bin
