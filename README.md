# Setup tools

```
kind create cluster --kubeconfig .kube-context.conf --name demo --config kind.yaml
kustomize build ./monitoring --enable-helm | kubectl apply -f - ; sleep 10
kustomize build ./cert-manager --enable-helm | kubectl apply -f - ; sleep 10
kustomize build ./istio --enable-helm | kubectl apply -f - ; sleep 10
kustomize build ./bookinfo --enable-helm | kubectl apply -f - ; sleep 10
```