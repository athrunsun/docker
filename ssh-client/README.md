# ssh client in docker based on [Alpine linux](https://hub.docker.com/r/gliderlabs/alpine/)
## Get started
To ssh into a remote host,
```shell
docker run --rm -it --name ssh-client -v $HOME/.ssh/id_rsa:/mnt/ssh/id_rsa:ro okampfer/ssh-client -i /mnt/ssh/id_rsa <user>@<server>
```
