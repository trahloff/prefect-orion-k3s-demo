# flows

Prefect Orion examples

## Getting started

Prerequisites:

- make
- node (required for pyright)
- python >= 3.7
- sqlite 3

To start:

- Install the [development environment](CONTRIBUTING.md#Development-environment): `make install`

## Usage

1. `make basic-flow`
1. `make ui` then navigate to [http://localhost:4200/](http://localhost:4200/)

The orion sqlite database is stored in _~/.prefect/orion.db_

### Kubernetes

Create k3d cluster

```
make cluster
```

Deploy minio (for remote storage when using Kubernetes), prefect agent and api

```
make kubes-minio kubes-prefect
```

Navigate to the Prefect UI at [http://localhost:4200/](http://localhost:4200/) (NB: might take a minute or two to be ready).

The minio UI is accessible at [http://localhost:9001](http://localhost:9001). See `make minio-creds` for user/password.

## References

- [Orion tutorials](https://orion-docs.prefect.io/tutorials/first-steps/)
