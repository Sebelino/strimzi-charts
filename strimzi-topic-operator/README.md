# strimzi-topic-operator

Helm chart for the
[standalone Strimzi Topic Operator](https://github.com/strimzi/strimzi-kafka-operator/tree/0.32.0/install/topic-operator).

## Show package
```bash
helm show all oci://ghcr.io/sebelino/strimzi-topic-operator --version 0.2.0
```

## Install package
```bash
helm install strimzi-topic-operator oci://ghcr.io/sebelino/strimzi-topic-operator --namespace strimzi --version 0.2.0
```

## Build package
```bash
helm package .
ls strimzi-topic-operator-0.2.0.tgz
```

## Publish package
```bash
helm push strimzi-topic-operator-0.2.0.tgz oci://ghcr.io/sebelino
```
