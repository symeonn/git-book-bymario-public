# K8S

Basic commands:

### Azure:

az login

```text
az login

az aks get-credentials --resource-group <resource-group> --name <resource-name> --admin
```

#### Contexts

```text
kubectl config use-context <context> 
```

kubectl -n test2 get pods -w

kubectl -n test2 describe pods `<pod_id>`

kubectl -n test2 delete pod nuadu-rabbitmq-0 --grace-period=0 --force

kubectl -n test2 logs `<pod_id>`

## scale pod

kubectl -n test2 scale deployment nuadu-ingress --replicas=2

\#tunel

```text
kubectl -n test port-forward nuadu-configuration-67cb6495f6-f5rzl 8888:8888
```

\#ssh to pod  
`winpty kubectl -n test2 exec -it nuadu-system-api-spring-59f65549b4-5phzr -- bash`

Modyfikacja ilości węzłów robić na Azure

