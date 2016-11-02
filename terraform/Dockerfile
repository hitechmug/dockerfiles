FROM alpine

RUN apk add --no-cache --update curl && \
	curl -ko /terraform.zip https://releases.hashicorp.com/terraform/0.7.8/terraform_0.7.8_linux_amd64.zip && \
	unzip /terraform.zip && \
	mv terraform /bin/terraform && \
	rm /terraform.zip && \
	apk del curl
ENTRYPOINT ["terraform"]