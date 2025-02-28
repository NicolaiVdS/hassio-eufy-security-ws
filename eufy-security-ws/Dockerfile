ARG BUILD_FROM
FROM $BUILD_FROM

WORKDIR /usr/src/app
RUN \
    set -x \
    && apk add --no-cache \
    nodejs \
    npm \
    jq \
    && git clone https://github.com/NicolaiVdS/eufy-security-ws.git . \
    && npm install --force

COPY run.sh /
RUN chmod a+x /run.sh
WORKDIR /data

CMD [ "/run.sh" ]
