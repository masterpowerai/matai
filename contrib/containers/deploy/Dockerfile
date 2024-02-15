FROM phusion/baseimage:focal-1.0.0
LABEL maintainer="masterpowerai Developers <dev@masterpowerai.org>"
LABEL description="Dockerised masterpowerai, built from Travis"

ARG USER_ID
ARG GROUP_ID

ENV HOME /home/masterpowerai

# add user with specified (or default) user/group ids
ENV USER_ID ${USER_ID:-1000}
ENV GROUP_ID ${GROUP_ID:-1000}
RUN groupadd -g ${GROUP_ID} masterpowerai && \
    useradd -u ${USER_ID} -g masterpowerai -s /bin/bash -m -d /home/masterpowerai masterpowerai && \
    mkdir /home/masterpowerai/.masterpowerai && \
    chown ${USER_ID}:${GROUP_ID} -R /home/masterpowerai

COPY bin/* /usr/local/bin/

RUN chmod a+x /usr/local/bin/*

USER masterpowerai

VOLUME ["/home/masterpowerai"]

EXPOSE 16091 9999 26091 26092

WORKDIR /home/masterpowerai
