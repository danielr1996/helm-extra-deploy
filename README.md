# helm-extra-deploy
Deploy arbitrary k8s manifests through an helm chart, specified in values.yaml

```sh
helm upgrade --install extra oci://ghcr.io/danielr1996/helm-extra-deploy/helm-extra-deploy:1.0.0 -f values.examples.yaml
```

```yaml
extraDeploy:
- apiVersion: v1
  kind: Secret
  metadata:
    name: secret1
  stringData:
    key: value
- apiVersion: v1
  kind: Secret
  metadata:
    name: secret2
  stringData:
    key: value
```