FROM jenkins/jenkins:lts

USER root

RUN apt-get update && \
    apt-get install -y ca-certificates curl && \
    curl -fsSL https://get.docker.com | sh && \
    apt-get clean && \
    rm -rf /var/lib/apt/lists/*

RUN groupadd -f docker && \
    usermod -aG docker jenkins

USER jenkins