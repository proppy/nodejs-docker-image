nodejs-docker-image
===================

Source for `google/nodejs` docker base image.

## Description

`google/nodejs` bundles the latest version of [nodejs](https://nodejs.org) and [npm](https://npmjs.org) installed from [nodejs.org](http://nodejs.org/download/).

## Usage

- Create a Dockerfile in your nodejs application directory with the following content:
```
FROM google/nodejs
WORKDIR /app
ADD package.json /app/
RUN npm install
ADD . /app

CMD []
ENTRYPOINT ["/nodejs/bin/npm", "start"]
```

- Run the following command in your application directory:
```
docker build -t my/app .
```
