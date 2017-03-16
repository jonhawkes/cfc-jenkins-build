FROM ma1dock1.platformlab.ibm.com/lcn-reg/jenkins-jnlp-slave-ppc64le-root:2.52

USER root

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

RUN apt update \
    && apt-get -y --no-install-recommends install iptables conntrack util-linux socat cifs-utils wget containerd runc jq \
    && wget -k --no-check-certificate https://launchpad.net/ubuntu/+source/docker.io/1.10.3-0ubuntu6/+build/9604030/+files/docker.io_1.10.3-0ubuntu6_ppc64el.deb \
    && dpkg -i docker.io_1.10.3-0ubuntu6_ppc64el.deb \
    && rm -f docker.io_1.10.3-0ubuntu6_ppc64el.deb \
    && apt-get -f install \
    && rm -rf /var/lib/apt/lists/*

