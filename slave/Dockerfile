FROM ma1dock1.platformlab.ibm.com/lcn-reg/jekins-jnlp-slave:2.52 

USER root

RUN apt-get update && apt-get -y install --no-install-recommends jq

COPY cfc-auto-helm-k8s /usr/local/bin/cfc-auto-helm-k8s

COPY cfc-auto-helm-k8sm /usr/local/bin/cfc-auto-helm-k8sm

COPY cfc-auto-build-k8s /usr/local/bin/cfc-auto-build-k8s

COPY cfc-auto-build-k8sm /usr/local/bin/cfc-auto-build-k8sm

COPY cfc-auto-deploy-k8s /usr/local/bin/cfc-auto-deploy-k8s

COPY cfc-auto-deploy-k8sm /usr/local/bin/cfc-auto-deploy-k8sm

COPY helm-2.1.3 /usr/local/bin/helm-2.1.3

COPY helm-2.0.0 /usr/local/bin/helm-2.0.0

COPY kubectl-1.5.2 /usr/local/bin/kubectl-1.5.2

COPY kubectl-1.4.7 /usr/local/bin/kubectl-1.4.7

RUN curl -fsSL https://get.docker.com/builds/Linux/x86_64/docker-1.11.1.tgz | tar --strip-components=1 -xvz -C /usr/local/bin/ docker/docker \


