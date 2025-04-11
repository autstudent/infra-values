# Infrastructure Configuration

This repository contains the configuration parameters used by the Argo CD, working together with the infra-chart, in order to split up configuration at global, environment and cluster level.

The idea is to enable operation teams to configure each Openshift cluster easily modifying the respective configuration files that will be applied to the respective Cluster.

## Testing

```$bash
git clone  https://github.com/autstudent/infra-chart.git /tmp
helm template /tmp/charts/charts/infra-chart -f values-global.yaml -f des/values-env.yaml -f des/cluster01/values-cluster.yaml
```

NOTE: Values ​​files order in the previous command is important because the highest priority parameters are in the last file included

## Author

Asier Cidon @RedHat