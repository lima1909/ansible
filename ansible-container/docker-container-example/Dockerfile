FROM docker:dind 

Maintainer lima1909 

RUN apk update && apk upgrade && \
    apk add --no-cache \
	py-pip \
    	python-dev \
    	python3-dev \
    	git \
    	ansible \
    	gcc \
    	curl \
    	bash \
	vim  \
	linux-headers \
	musl-dev

RUN mkdir /my && \
    mkdir /my/ansible && \
    mkdir /my/workspace && \
    mkdir /my/workspace/first && \
    cd /my/ansible && \
    git clone https://github.com/ansible/ansible-container.git && \
    cd ansible-container && \
    pip install regex && \
    pip install ansible-container[docker,openshift]

ADD container.yml /my/workspace/first/container.yml
ADD web /my/workspace/first/web
ADD hello.html /my/workspace/first/hello.html
ADD .bashrc /root/.bashrc

ENTRYPOINT ["dockerd-entrypoint.sh"]
CMD []
