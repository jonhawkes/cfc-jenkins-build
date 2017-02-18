#How to build Jenkins Slave

(1)```git clone https://github.com/jenkinsci/docker-jnlp-slave.git```

(2)```cd docker-jnlp-slave/```

(3)```git checkout 2.52```

(4)Change Dockerfile:
change base image from openjdk:8-jdk to ma1dock1.platformlab.ibm.com/library/ibmjava-ppc64le:8-sdk or ma1dock1.platformlab.ibm.com/library/ibmjava:8-sdk)

(5)Add:
```RUN apt-get update && apt-get install -y curl git```
