FROM alpine:latest


RUN apk add --update curl bash
RUN curl https://storage.googleapis.com/golang/go1.7.3.linux-amd64.tar.gz | tar xz

ENV PATH /go/bin:/usr/local/go/bin:$PATH
ENV GOPATH /go:/go/src/app/_gopath

RUN mkdir -p /go/src/app /go/bin && chmod -R 777 /go

#FROM alpine

#ENV TERRAFORM_VERSION=0.7.7
#ENV TF_DEV=true
#ENV GOPATH /go
#ENV PATH $GOPATH/bin:/usr/local/go/bin:$PATH


#RUN apk add --update git go bash
#WORKDIR $GOPATH/src/github.com/hashicorp/terraform

#RUN git clone https://github.com/hashicorp/terraform.git ./ && \
#    git checkout v${TERRAFORM_VERSION} && \
#    /bin/bash scripts/build.sh

#WORKDIR $GOPATH