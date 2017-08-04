FROM ma1dock1.platformlab.ibm.com/lcn-reg/jenkins-jnlp-slave-s390x-root:2.52

USER root

COPY cfc-auto-helm-k8s /usr/local/bin/cfc-auto-helm-k8s

COPY cfc-auto-build-k8s /usr/local/bin/cfc-auto-build-k8s

COPY cfc-auto-deploy-k8s /usr/local/bin/cfc-auto-deploy-k8s

COPY helm /usr/local/bin/helm

COPY kubectl-1.7 /usr/local/bin/kubectl-1.7

RUN wget ftp://ftp.unicamp.br/pub/linuxpatch/s390x/redhat/rhel7.3/docker-17.05.0-ce-rhel7.3-20170523.tar.gz \
    && tar --strip-components=1 -zxvf  docker-17.05.0-ce-rhel7.3-20170523.tar.gz -C /usr/local/bin/ docker-17.05.0-ce-rhel7.3-20170523/docker
