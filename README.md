# CI/CD Docker

## Docker Image

### Docker hub
[plimble/ci](https://hub.docker.com/r/plimble/ci/)

### Tags

- [go (ci/go/Dockerfile)](https://github.com/plimble/ci-docker/blob/master/ci/go/Dockerfile)
- [node (ci/node/Dockerfile)](https://github.com/plimble/ci-docker/blob/master/ci/node/Dockerfile)
- [latest (go and node) (ci/Dockerfile)](https://github.com/plimble/ci-docker/blob/master/ci/Dockerfile)
- [vsts (vsts/Dockerfile)](https://github.com/plimble/ci-docker/blob/master/vsts/Dockerfile)

## Tools
- go
  - dep
  - go-bindata
- node
  - yarn
- rancher
- kubectl
- helm
- docker

## VSTS Agent

```sh
docker run -d \
-e VSTS_ACCOUNT=<ACCOUNT> \
-e VSTS_TOKEN=<PERSONAL_TOKEN> \
-e VSTS_POOL=<POOL_NAME> \
-e VSTS_AGENT=<AGENT_NAME> \
-e VSTS_WORK='/var/vsts/$VSTS_AGENT' \
-v /var/vsts:/var/vsts \
-v /var/run/docker.sock:/var/run/docker.sock \
--name vsts-agent1 \
plimble/ci:vsts
```
