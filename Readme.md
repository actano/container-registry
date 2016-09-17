# container-registry

This repository provides a `docker-compose.yml` for running a docker registry and a web frontend for it.

## How to run?

1. Create a `./certs` directory and put your TLS certificate and key file inside.
2. Create a `./auth` directory and put your `htpasswd` file inside.
3. Create a `./data` directory. The docker images will be persisted here.
3. Define the following environment variables, e.g. by creating an `.env` file
  * `REGISTRY_HOST` - the public host name under which the registry will be available
  * `TLS_CERTIFICATE_FILE` - the file name of the TLS certificate file (just the basename) inside the `./certs` directory
  * `TLS_KEY_FILE` - the file name of the TLS key file (just the basename) inside the `./certs` directory
  * `HTPASSWD_FILE` - the file name of the htpasswd file (just the basename) inside the `./auth` directory
4. Run `docker-compose up [-d]`
