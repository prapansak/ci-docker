# CI/CD Docker


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


### VSTS Usage

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
