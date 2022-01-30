Referência
https://www.youtube.com/watch?v=1lx91nhzNe0


##Baixar Kind
```
curl -Lo ./kind https://kind.sigs.k8s.io/dl/v0.11.1/kind-linux-amd64
chmod +x ./kind
sudo mv ./kind /usr/local/bin/
```
**Obs**:Arquivos do Kind são binaŕios, sendo assim mover para pasta `/usr/local/bin/` para facilitar

##Criar Cluster
```
kind create cluster --name cluster01 --config kind-config.yaml
```

```
kind delete cluster
```

#iniciando ingress
kubectl apply -f teste-ingress.yaml









Outras Referências:

https://docs.microsoft.com/en-us/azure/aks/ingress-tls?tabs=azure-cli

https://docs.oracle.com/pt-br/iaas/Content/ContEng/Tasks/contengsettingupingresscontroller.htm

https://kubernetes.io/docs/concepts/services-networking/ingress/

#dns
https://www.valuehost.com.br/blog/configurar-dns-no-linux/

https://kubernetes.io/docs/concepts/services-networking/ingress/#tls

https://www.ti-enxame.com/pt/ssl/o-kubernetes-nginx-ingress-controller-nao-obtem-certificados-tls/833932524/
