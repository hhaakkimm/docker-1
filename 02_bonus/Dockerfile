FROM ubuntu
FROM alpine

MAINTAINER hakeemata <hhaakkimm@gmail.com>

RUN apt-get update && apt-get upgrade -y && apt-get install -y node npm git

RUN npm install yarn --global && npm install npm --global

RUN apk update && apk upgrade && apk add vim

CMD ["echo" "Workplace is ready"]
