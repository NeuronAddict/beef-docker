FROM debian

ENV TERM=xterm
ENV LANG=en_US.UTF-8

ADD https://github.com/beefproject/beef/archive/master.tar.gz /opt/

RUN apt update && apt install -y locales sudo \
    && sed -i -e 's/# en_US.UTF-8 UTF-8/en_US.UTF-8 UTF-8/' /etc/locale.gen && \
           dpkg-reconfigure --frontend=noninteractive locales && \
           update-locale LANG=en_US.UTF-8

WORKDIR /opt/beef-master

RUN echo -e "\n\n\n" | /opt/beef-master/install

CMD ["./beef"]
