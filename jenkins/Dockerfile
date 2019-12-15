FROM jenkins/jenkins:lts
EXPOSE 8080/tcp
EXPOSE 50000/tcp
USER root
RUN apt update && apt install -y \
    vim \
    locate \
    sudo \
    python3 \
    python3-pip \
    zip \
    less \
    unzip \
    man \
    curl
RUN curl -LO https://storage.googleapis.com/kubernetes-release/release/v1.17.0/bin/linux/amd64/kubectl
RUN chmod +x ./kubectl
RUN mv ./kubectl /usr/local/bin/kubectl
USER jenkins
