FROM alpine:latest

RUN apk add --update --no-cache openssl openjdk11-jre-headless python3 py3-setuptools py3-pip curl

RUN pip3 install --no-cache rpm

WORKDIR /build

ADD katello-certs-tools /build

RUN touch katello-ssl-tool.1
RUN /usr/bin/python3 setup.py install

RUN rm -rf /build

ARG KUBECTL_VERSION=1.27.3
RUN curl -L https://storage.googleapis.com/kubernetes-release/release/v${KUBECTL_VERSION}/bin/linux/amd64/kubectl -o /usr/bin/kubectl && \
    chmod +x /usr/bin/kubectl

CMD [ 'katello-ssl-tool' ]
