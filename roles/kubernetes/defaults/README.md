## Kubernetes cluster infrastructure services manifests references
The references below are the examples the manifests in ```kubernetes_infra_services``` param are based upon.\
If a certain manifest doesn't have open issues that requires workarounds or no custom changes before applying are desired, direct link to the manifest is used, for example: Weave network plugin, Weave scope and TLSer (which is maintained by gefen).\
Otherwise, the manifest is saved under the [files/manifests] directory (of this role) with its custom changes and/or workarounds and applied to the kubernetes cluster from this directory.

---
### Weave network Plugin (as daemon-set with rbac) ref:
- https://www.weave.works/docs/net/latest/kube-addon/

### Weave scope in standalone mode ref:
- https://www.weave.works/docs/scope/latest/installing/#k8s

### Kubernetes dashboard (with rbac, listen to http instead of https, with full admin access to api instead of minimal access) ref:
- https://github.com/kubernetes/dashboard
- https://raw.githubusercontent.com/kubernetes/dashboard/master/src/deploy/alternative/kubernetes-dashboard.yaml
- https://github.com/kubernetes/dashboard/wiki/Access-control#authorization-header

### Nginx ingress controller (as daemon-set with rbac) and lego ref:
- https://github.com/kubernetes/ingress/blob/master/examples/rbac/nginx/nginx-ingress-controller-rbac.yml
- https://github.com/kubernetes/ingress/blob/master/examples/daemonset/nginx/nginx-ingress-daemonset.yaml

### Kube lego (with rbac) ref:
- https://github.com/jetstack/kube-lego/blob/master/examples/nginx/lego/deployment.yaml

### Heapster (with rbac) ref:
- https://github.com/kubernetes/heapster/blob/master/deploy/kube-config/rbac/heapster-rbac.yaml
- https://github.com/kubernetes/heapster/blob/master/deploy/kube-config/standalone/heapster-controller.yaml

### TLSer (with rbac) ref: 
- https://github.com/GefenOnline/tlser/blob/master/deploy/k8s/tlser.yml


[files/manifests]:../files/manifests
