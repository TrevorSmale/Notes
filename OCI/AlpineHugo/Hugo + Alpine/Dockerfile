FROM alpine:latest

ARG HUGO_VERSION

RUN apk add --no-cache \
    curl \
    git \
    openssh-client \
    && curl -Ls https://github.com/gohugoio/hugo/releases/download/v${HUGO_VERSION}/hugo_extended_${HUGO_VERSION}_Linux-64bit.tar.gz | tar xz -C /usr/local/bin \
    && chmod +x /usr/local/bin/hugo

EXPOSE 80:80
CMD ["hugo", "server", "-p", "80"]
