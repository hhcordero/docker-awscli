AWS cli in minimal footprint
============================

Automatic built minimal docker image for AWS cli based on Alpine Linux (`library/alpine:latest`), around 100+MB.

## Usage

Build image on your local:
```
docker build -t <image_name> .
```

Run in interactive mode, mount your .aws directory (contains config and credentials files):
```
docker run --rm -it -v <config_path>:/root/.aws:ro <image_name> /bin/sh
```

Ex:
```
docker run --rm -it -v ~/aws:/root/.aws:ro aws /bin/sh
aws s3 <arguments>
```

Refer to <http://docs.aws.amazon.com/cli/latest/userguide/cli-chap-getting-started.html> for detail.

## More information
Alpine Linux: <https://registry.hub.docker.com/_/alpine/>

AWS cli: <https://aws.amazon.com/cli/>
