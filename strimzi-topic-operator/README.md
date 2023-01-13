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

## Render

```bash
helm template \
    --set 'kafkaBootstrapServers={broker-1:9094,broker-2:9094,broker-3:9094}' \
    --set 'zookeeperConnect={zookeeper-1:2182,zookeeper-2:2182,zookeeper-3:2182}' \
    --set 'resourceLabels=strimzi.io/cluster=my-cluster' \
    .
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
