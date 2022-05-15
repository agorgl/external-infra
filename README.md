# external-infra

Deploys an external infrastructure in k8s, with the help of helm charts and helmfile.  
For a quickstart, copy and modify `.env.sample.yaml` to `.env.default.yaml` and run `helmfile apply`.

## Notes

To get the local ca certificate run:
```
kubectl -n external get secret local-ca-tls -o jsonpath='{.data.tls\.crt}' | base64 -d > local-ca.crt
```
