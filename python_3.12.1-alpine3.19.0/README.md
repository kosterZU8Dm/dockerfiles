# dockerfiles

## description
libffi-dev - need to psycorg2\
openssl-dev - need for pip connect to pypi.org

## command to build image:
```
cd <image directory>
docker build . -t <REPOSITORY>:<TAG>
```
## for example:
```
docker build . -t python:3.12.1-alpine3.19.0
```
