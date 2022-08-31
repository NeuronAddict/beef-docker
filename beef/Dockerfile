FROM ruby:2.7 AS builder

ENV TERM=xterm
ENV LANG=en_US.UTF-8


RUN apt update && apt install -y curl locales sudo tar \
    && sed -i -e 's/# en_US.UTF-8 UTF-8/en_US.UTF-8 UTF-8/' /etc/locale.gen && \
           dpkg-reconfigure --frontend=noninteractive locales && \
           update-locale LANG=en_US.UTF-8

RUN curl -sL https://github.com/beefproject/beef/archive/master.tar.gz | tar -xzC /opt/

WORKDIR /opt/beef-master

RUN yes | /opt/beef-master/install

CMD ["./beef"]
