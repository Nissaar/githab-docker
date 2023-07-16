# Gitlab Docker behind Traefik
This Setup is being used on Oracle Cloud Arm Instance
## Prerequisites
* Traefik installed 
* Docker network frontend created (See Traefik Readme)
### Image
There is no official Image for arm64 from Gitlab. We are therefore using `gitlab:latest` from [zengyx](https://github.com/zengxs/gitlab-arm64).
### Hostname
Will the hostname of the container
### Networks
Its the `frontend` network created when traefik is set up.
### Environment
This is the configuration for gitlab.
* nginx configuration has been added to run behind Traefik and https
* letsencrypt disabled as we will not be using it for certificate
* we have changed the Gitlab ssh port and exposed the port
### Labels
These are the lables for `Traefik`
