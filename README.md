AWS cli in minimal footprint
============================

Automatic built minimal docker image for AWS cli based on Alpine Linux (`library/alpine:latest`), around 100+MB.

## Usage

Run in interactive mode:
```
docker run --rm -it -v <config_path>:/root/.aws:ro -v <option_yml>:/aws:ro hhcordero/awscli <argument>
```

Ex:
```
docker run --rm -it -v ~/aws:/root/.aws:ro hhcordero/awscli /bin/sh
```

Refer to <http://docs.aws.amazon.com/cli/latest/userguide/cli-chap-getting-started.html> for detail.

## More information
Alpine Linux: <https://registry.hub.docker.com/_/alpine/>

AWS cli: <https://aws.amazon.com/cli/>
