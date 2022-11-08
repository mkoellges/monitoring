# monitoring

Kubernets Monitoring Stacks

## Create Repo

```sh
flux create source git monitoring \
  --interval=1m0s \
  --url=https://github.com/mkoellges/monitoring.git \
  --branch=main \
  --namespace=flux-system \
  --export > ./clusters/MBP-von-Manfred/docker-desktop/monitoring/git-source.yaml
```

## Create Tenant

```sh
flux create tenant monitoring \
  --with-namespace=monitoring \
   --cluster-role=monitoring-full-access \
   --export > ./clusters/MBP-von-Manfred/docker-desktop/monitoring/flux-tenant.yaml
```
