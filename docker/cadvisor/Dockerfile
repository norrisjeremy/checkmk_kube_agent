ARG CADVISOR_VERSION=0.56.2
FROM ghcr.io/google/cadvisor:"${CADVISOR_VERSION}"
ARG GIT_HASH
RUN apk --no-cache upgrade --purge && \
    rm -rf /tmp/* && \
    rm -rf /var/cache/apk/*
RUN echo "${GIT_HASH}" > GIT_HASH.txt
