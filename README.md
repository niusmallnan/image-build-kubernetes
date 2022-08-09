# rancher/hardened-kubernetes

## Build
Build hardened kubernetes needs to include the rfo release version and the build meta to work properly. Just running
`make` will hardcode `v1.21.2-rfodev-build<todaysdate>`. If you want to set your own versions for testing and when 
pushing a tag to the repo to make a release you will want to add the full version of kubernetes rfo release and
the build meta like the following.

```sh
TAG=v1.21.2-rfor1-build20210706 make
```

## Pushing a Release
You will need to know the RFO version you are releasing before you can build hardened kubernetes. For example a current
release is `v1.21.2+rfor1` and this translates to a hardened kubernetes build tag of `v1.21.2-rfor1-build<date Ymd>`. 
Let this project build and release images and set your version in the [dockerfile](https://github.com/rancher/rke2/blob/master/Dockerfile)
