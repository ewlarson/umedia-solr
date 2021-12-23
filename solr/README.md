# Solr Docker

This directory contains a Dockerfile that serves as the base docker image for running Solr in CI.

This image adds:
- a security.json file which allows us to make changes to solr via basic auth. It runs with an embedded zookeeper on a separate port.
- scripts for solr setup in CI.

### Update and Rebuild

You must have an account under the ewlarson dockerhub organization to push to
dockerhub.

To update and rebuild the image:

```bash
docker login # login to docker hub
docker build -t ewlarson/umedia-solr:{solr version}-{Dockerfile version} .
docker push ewlarson/umedia-solr:{solr version}-{Dockerfile version}
```

```bash
docker login # login to docker hub
docker build -t ewlarson/umedia-solr:7.3-v1.0.0 .
docker push ewlarson/umedia-solr:7.3-v1.0.0
```
