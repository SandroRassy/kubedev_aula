FROM ubuntu
RUN apt-get update
RUN apt-get install -y curl
RUN apt-get install -y sudo
RUN apt-get install -y vim
RUN curl -LO https://dl.k8s.io/release/$(curl -L -s https://dl.k8s.io/release/stable.txt)/bin/linux/amd64/kubectl
RUN adduser --disabled-password --gecos '' docker
RUN adduser docker sudo
RUN echo '%sudo ALL=(ALL) NOPASSWD:ALL' >> /etc/sudoers
USER docker
CMD /bin/bash
RUN sudo install -m 0755 kubectl /usr/local/bin/kubectl
RUN kubectl version --client
