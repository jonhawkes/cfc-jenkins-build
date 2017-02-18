# How to build Jenkins Master 

(1)```git clone https://github.com/jenkinsci/docker.git```

(2)```git checkout c47ac48692a7fb48470107336c37419e57b0384c```

(3)change Docker file:
Change base image to "ma1dock1.platformlab.ibm.com/library/ibmjava-ppc64le:8-sdk"
or "ma1dock1.platformlab.ibm.com/library/ibmjava:8-sdk"

Add unzip in  ```RUN apt-get update && apt-get install -y git curl *unzip* && rm -rf /var/lib/apt/lists/*```

Change tini version to v0.10.0

(4) Build tini binary for ppc64le

```git clone https://github.com/krallin/tini.git```

```git checkout v0.10.0```

```cmake .```

```make```

```mv tini-static .../docker```

