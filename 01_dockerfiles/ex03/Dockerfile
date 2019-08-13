FROM debian:9

MAINTAINER mcomet <mcomet@student.21-school.ru>

RUN apt-get update -y && apt-get upgrade -y && \
    apt-get install -y ca-certificates openssh-server wget vim

RUN wget https://packages.gitlab.com/install/repositories/gitlab/gitlab-ce/script.deb.sh && chmod 777 script.deb.sh && ./script.deb.sh && apt-get install -y gitlab-ce

EXPOSE 22 80 443

ENTRYPOINT (/opt/gitlab/embedded/bin/runsvdir-start &) && gitlab-ctl reconfigure && tail -f /dev/null


# /etc/gitlab/gitlab.rb     registry_nginx
# letsencrypt['enable'] = true
# /etc/ssh/sshd_config      password auth off
# AllowUswers git
#SSH key
