### Query readiness of service
``` json
kubectl get pod -l k8s-app=policycenter-app -o jsonpath='{.items[*].status.containerStatuses[*].ready}'
```
``` go
kubectl get pod -l k8s-app=policycenter-app -o go-template="{{range .items}}{{range .status.containerStatuses}}{{.ready}}{{end}}{{end}}"
```
