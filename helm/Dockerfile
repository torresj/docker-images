FROM ubuntu

RUN apt-get update; apt-get install -y curl git

RUN curl -LO https://dl.k8s.io/release/v1.23.0/bin/linux/amd64/kubectl

RUN install -o root -g root -m 0755 kubectl /usr/local/bin/kubectl

RUN curl -fsSL -o get_helm.sh https://raw.githubusercontent.com/helm/helm/main/scripts/get-helm-3

RUN chmod 700 get_helm.sh

RUN ./get_helm.sh

RUN helm plugin install https://github.com/chartmuseum/helm-push.git
