1. Get the name of all the nodes and their taint effect if any. <br/>**K8s** version used - **v1.19.5**

<details>
  <summary>Click to expand!</summary>

`kubectl get nodes -o jsonpath='{range $.items[*]} {.metadata.name} {.spec.taints[*].effect}{"\n"}'`

**Output**

```
kubemaster NoSchedule
kubenode01
kubenode02
```

</details>
