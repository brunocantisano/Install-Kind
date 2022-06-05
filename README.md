# Criação de cluster Kubernets através da instalação do Kind

[![Instalando Kubernetes com o Kind](https://res.cloudinary.com/marcomontalbano/image/upload/v1654392933/video_to_markdown/images/youtube--1lx91nhzNe0-c05b58ac6eb4c4700831b2b3070cd403.jpg)](https://www.youtube.com/watch?v=1lx91nhzNe0 "Instalando Kubernetes com o Kind")

## Baixando o Kind

```sh
curl -Lo ./kind https://kind.sigs.k8s.io/dl/v0.11.1/kind-linux-amd64
chmod +x ./kind
sudo mv ./kind /usr/local/bin/
```

>Obs: **Arquivos do Kind são binaŕios, sendo assim mover para pasta `/usr/local/bin/` para facilitar**

## Criando o Cluster

```sh
kind create cluster --name cluster01 --config kind-config.yaml
```

```sh
kind delete cluster
```

## Listando os clusters

```sh
kind get clusters
```

## Listando os nodes

```sh
kind get nodes
```

## Deploy o app de exemplo

```sh
kubectl apply -f Deployment-Service.yaml
```

## Obtendo porta do serviço

```sh
kubectl get service service-app-example -n namespace-app-example
```

## Fazendo port-forward para acessar o service localmente
```sh
kubectl port-forward service/service-app-example :80 -n namespace-app-example
```

<!-- ## Iniciando o Ingress

```sh
kubectl apply -f teste-ingress.yaml
``` -->

Outras Referências:

* [Ingress TLS](https://docs.microsoft.com/en-us/azure/aks/ingress-tls?tabs=azure-cli)

* [IAAS](https://docs.oracle.com/pt-br/iaas/Content/ContEng/Tasks/contengsettingupingresscontroller.htm)

* [Ingress](https://kubernetes.io/docs/concepts/services-networking/ingress/)

* [DNS](https://www.valuehost.com.br/blog/configurar-dns-no-linux/)

* [TLS](https://kubernetes.io/docs/concepts/services-networking/ingress/#tls)

* [Certificates](https://www.ti-enxame.com/pt/ssl/o-kubernetes-nginx-ingress-controller-nao-obtem-certificados-tls/833932524/)

## Desenvolvedores/Contribuintes :octocat:

<table>
    <tr>
        <td align="center"><a href="https://github.io/brunocantisano"><img style="border-radius: 50%;" src="https://avatars2.githubusercontent.com/u/11641388?s=400&u=0ba16a79456c2f250e7579cb388fa18c5c2d7d65&v=4" width="100px;" alt="" /><br /><sub><b>Bruno Cantisano</b></sub></a><br /><a href="https://github.com/brunocantisano" title="Bruno Cantisano">:metal:</a></td>
        <td align="center"><a href="https://github.io/Thiagosnts"><img style="border-radius: 50%;" src="https://avatars.githubusercontent.com/u/39925677?v=4" width="100px;" alt="" /><br /><sub><b>Thiago Santos</b></sub></a><br /><a href="https://github.io/Thiagosnts/" title="Thiago Santos">:sunglasses:</a></td>        
    </tr>
</table>
