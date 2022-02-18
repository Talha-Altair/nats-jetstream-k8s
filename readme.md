# NATS JETSREAM NFS

This Helm Chart provisions a NATS server with jetstream enabled and an NFS server as it's persistent storage solution.

## Using

Edit the values.yaml file and set the following:

    namespace: The Namespace in which the NATS and NFS components will be deployed.

    storage: The amount of storage to provision for the NFS server and the Nats Server.

```
helm install nats-jetstream-nfs --namespace=<namespace> --generate-name
```

here, make sure the ```<namespace>``` is the same as the one you set in the values.yaml file.

## Testing

Ping the output URLs given after the helm installation

## Deprovisioning

```
helm list --namespace=<namespace>
```

Note the name of the helm deployment, which is auto-generated.

```
helm uninstall <name> --namespace=<namespace>
```