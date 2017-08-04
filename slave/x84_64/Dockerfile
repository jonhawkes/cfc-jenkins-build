FROM ma1dock1.platformlab.ibm.com/lcn-reg/jekins-jnlp-slave-root:2.52

RUN apt-get update && apt-get -y install --no-install-recommends jq

COPY cfc-auto-helm-k8s /usr/local/bin/cfc-auto-helm-k8s

COPY cfc-auto-build-k8s /usr/local/bin/cfc-auto-build-k8s

COPY cfc-auto-deploy-k8s /usr/local/bin/cfc-auto-deploy-k8s

COPY helm-2.5.0 /usr/local/bin/helm

COPY kubectl-1.7 /usr/local/bin/kubectl

RUN curl -fsSL https://get.docker.com/builds/Linux/x86_64/docker-1.11.1.tgz | tar --strip-components=1 -xvz -C /usr/local/bin/ docker/docker

