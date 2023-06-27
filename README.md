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