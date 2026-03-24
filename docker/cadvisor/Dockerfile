# Using upstream cadvisor v0.56.2 instead of Checkmk's pinned v0.47.2.
# The original checkmk/cadvisor-patched image only applied Alpine security
# updates (apk upgrade) on top of stock cadvisor. Using a current upstream
# version includes those fixes natively
ARG CADVISOR_VERSION=0.56.2
FROM ghcr.io/google/cadvisor:"${CADVISOR_VERSION}"
ARG GIT_HASH
RUN apk --no-cache upgrade --purge && \
    rm -rf /tmp/* && \
    rm -rf /var/cache/apk/*
RUN echo "${GIT_HASH}" > GIT_HASH.txt
