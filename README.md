## DevX

```
helm upgrade -i argocd argo/argo-cd -f argocd/staging_values.yml -n argocd --create-namespace
```

```
kubectl -n argocd get secret argocd-initial-admin-secret -o jsonpath="{.data.password}" | base64 -d
```

```
kubectl port-forward service/argocd-server -n argocd 8080:443
```

```
kubectl apply -f argocd/staging_app.yml
```

## MinIO

```
helm install minio oci://registry-1.docker.io/bitnamicharts/minio -f minio.yml
```

```
export ROOT_USER=$(kubectl get secret --namespace default minio -o jsonpath="{.data.root-user}" | base64 -d)
```

```
export ROOT_PASSWORD=$(kubectl get secret --namespace default minio -o jsonpath="{.data.root-password}" | base64 -d)
```
```
echo "MinIO&reg; web URL: http://127.0.0.1:9001/minio"
kubectl port-forward --namespace default svc/minio 9001:9001
```