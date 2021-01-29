```
# kubectl config use-context local

# kubectl apply -f metrics-generator.yaml

gitrepo.fleet.cattle.io/monitoring created
```

```
kind: GitRepo
apiVersion: fleet.cattle.io/v1alpha1
metadata:
  name: metrics-generator
  namespace: fleet-default
type: fleet.cattle.io.gitrepo
spec:
  repo: https://github.com/jmatis/fleet-testing.git
  branch: main
  paths:
  - /metrics-generator
  targets:
  - clusterGroup: monitoring
```
