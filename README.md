# comfyui

Add comfyui helm repo:
```bash
helm repo add m11s https://m11s-io.github.io/helm-charts
```

Install comfyui:
```bash
helm upgrade -i comfyui m11s/comfyui \
  --namespace comfyui \
  --create-namespace \
  --set runtimeClassName=nvidia \
  --set resources.requests."nvidia\.com/gpu"=1 \
  --set resources.limits."nvidia\.com/gpu"=1
```


http://localhost:8188

```bash
kubectl -n comfyui port-forward svc/comfyui 8188:8188
```
  
