# strimzi-topic-operator

Helm chart for the
[standalone Strimzi Topic Operator](https://github.com/strimzi/strimzi-kafka-operator/tree/0.32.0/install/topic-operator).

[Example usage.](https://github.com/algodx-ab/eks-blueprints-add-ons/blob/d4441134c2cf576a9f138643a522eefe8b758553/add-ons/strimzi-topic-operator/Chart.yaml)

## Show chart
```bash
helm show all oci://ghcr.io/sebelino/strimzi-topic-operator --version 0.2.0
```

## Install chart
```bash
helm install strimzi-topic-operator oci://ghcr.io/sebelino/strimzi-topic-operator --namespace strimzi --version 0.2.0
```

## Render

```bash
helm template \
    --set 'kafkaBootstrapServers={broker-1:9094,broker-2:9094,broker-3:9094}' \
    --set 'zookeeperConnect={zookeeper-1:2182,zookeeper-2:2182,zookeeper-3:2182}' \
    --set 'resourceLabels=strimzi.io/cluster=my-cluster' \
    oci://ghcr.io/sebelino/strimzi-topic-operator \
    --version 0.2.0
```

## Build package
```bash
helm package .
ls strimzi-topic-operator-0.2.0.tgz
```

## Publish chart
```bash
helm push strimzi-topic-operator-0.2.0.tgz oci://ghcr.io/sebelino
```
