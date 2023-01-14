# strimzi-charts

[Strimzi](https://strimzi.io/)-related Helm charts.

These charts were written with the following assumption in mind:

* You are running Kafka in [AWS MSK](https://aws.amazon.com/msk/)
* You are using TLS for the bootstrap servers (port `9094`)
* You are using TLS for ZooKeeper (port `2182`)

The environment variables have been [adjusted](https://github.com/Sebelino/strimzi-charts/commit/da98006e1e27a5dce52f3c5ace24710e189075fa) with this assumption in mind.

If your use case is different, contributions are welcome!
