# 34456

## Current behavior

Hey there. I'm trying to make renovate-bot automatically update my `docker-compose.yaml` file by adjusting the n8n image version. **Issue is that it is taking the last semver version, but it corresponds to the `next` tag which is a pre-release one.**

![image](https://github.com/user-attachments/assets/f1e263bd-f912-43a2-bc72-2f30ca48f6bc)

n8n releases can be found : 
- On their [website](https://docs.n8n.io/release-notes/)
- On their [Github repo](https://github.com/n8n-io/n8n/releases)
- On their [Dockerhub](https://hub.docker.com/r/n8nio/n8n/tags)

## Expected behavior

My docker compose contains a `image: docker.n8n.io/n8nio/n8n:1.78.0` , and I would like it to update to the `latest` equivalent in semver.

We should be able to specify to Renovate-Bot a Docker tag to follow I suppose. That is at least my thinking. 

## Current workaround

[This issue](https://github.com/renovatebot/renovate/discussions/14015) says that we could use the `latest` tag on the compose file. This is not a viable solution as it asks to check the pinned dependency sha256 each time on the PR to see from which version we update and to which one.

## Link to the Renovate issue or Discussion

- https://github.com/renovatebot/renovate/discussions/34456
