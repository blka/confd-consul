# confd-consul

A docker image containing consul server (based on `gliderlabs/consul-server`)
with [confd](https://github.com/kelseyhightower/confd)

## Usage

You can try out configuration with `docker-compose` and the provided `docker-compose.yml`

Available settings from environment variables:

```
CONSUL_ACL_DATACENTER
CONSUL_ACL_MASTER_TOKEN
CONSUL_ATLAS_INFRASTRUCTURE
CONSUL_ATLAS_TOKEN
CONSUL_DNS_PORT
CONSUL_HTTP_PORT
CONSUL_DOMAIN
CONSUL_ENCRYPT_KEY
```

## TODO

`confd` has a recent addition where you can set defaults for environment
variables (kelseyhightower/confd#410). Once that patch makes it into a release,
it would be great to try to set as many of the config file variables as
possible with using confd, and just have the defaults set. Once that lands,
all that is needed is to adjust the `CONFD_VERSION` in the [Dockerfile](./Dockerfile).

## License
MIT
