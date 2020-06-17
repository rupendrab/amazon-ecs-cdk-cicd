FROM alpine:latest


RUN \
	mkdir /root/bin /aws; \
	apk -Uuv add groff less bash python3 py-pip jq curl docker && \
	pip3 install --upgrade pip; \
	pip3 install awscli && \
	rm /var/cache/apk/* && \


WORKDIR $HOME

COPY entrypoint.sh /usr/local/bin/entrypoint.sh

RUN chmod a+x /usr/local/bin/entrypoint.sh

ENTRYPOINT ["/usr/local/bin/entrypoint.sh"]
