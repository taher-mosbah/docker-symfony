FROM ubuntu:14.04

CMD "sh" "-c" "echo nameserver 192.168.2.159 > /etc/resolv.conf"
CMD "sh" "-c" "echo nameserver 192.168.2.47 > /etc/resolv.conf"

#domain f6.fr
#nameserver 192.168.2.159
#nameserver 192.168.2.47


RUN apt-get install -y git

VOLUME /var/www/symfony

RUN mkdir -p /var/www/symfony

RUN mkdir -p /root/.ssh
RUN chown -R root:root /root/.ssh

ADD ./id_rsa /root/.ssh/id_rsa
#RUN cp ./id_rsa /root/.ssh/id_rsa
RUN chmod 600 /root/.ssh/id_rsa
RUN ssh-keyscan gitlab.fullsix.com >> /root/.ssh/known_hosts

RUN eval "$(ssh-agent -s)" && ssh-agent -s 

#RUN ping gitlab.fullsix.com -c 4

#RUN ssh-add /root/.ssh/id_rsa 

#RUN ssh-add

RUN ssh -v git@gitlab.fullsix.com:techsix/paradiski-experience-back.git

#RUN git clone -v git@gitlab.fullsix.com:techsix/paradiski-experience-back.git /var/www/symfony

#WORKDIR "/var/www/symfony"
#RUN pwd
#RUN 'chmod +x paradiski-experience-back/bin/resetdb && paradiski-experience-back/bin/resetdb'
#RUN cd /var/www/symfony/paradiski-experience-back/bin/ && ./resetdb