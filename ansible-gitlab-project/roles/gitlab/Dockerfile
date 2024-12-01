FROM ubuntu:latest

RUN apt-get update && apt-get install -y \
    curl \
    openssh-server \
    ca-certificates \
    tzdata \
    perl

RUN curl -sS https://packages.gitlab.com/install/repositories/gitlab/gitlab-ce/script.deb.sh | bash
RUN apt-get update && apt-get install -y gitlab-ce

EXPOSE 80 443 22

ENTRYPOINT ["gitlab-ctl", "reconfigure"]

