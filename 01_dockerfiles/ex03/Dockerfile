FROM golang

RUN adduser --disabled-login --gecos 'Gogs' git

USER git

ENV USER git

RUN mkdir -p $GOPATH/src/github.com/gogits && \
	cd $GOPATH/src/github.com/gogits && \
	git clone --depth=1 -b develop https://github.com/gogits/gogs && \
	cd gogs && \
	go build -tags 'sqlite'

WORKDIR $GOPATH/src/github.com/gogits/gogs

ENTRYPOINT ./gogs web
