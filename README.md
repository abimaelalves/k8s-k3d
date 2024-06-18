# Cluster Kubernetes com k3d

## Pré-requisitos

- Docker

## Instalar k3d

Para instalar o k3d, siga as instruções na [página do k3d](https://k3d.io/v5.6.3/#releases).

## Criar um Cluster Kubernetes Simples

Para criar um cluster Kubernetes simples com k3d, execute o comando:

```bash
k3d cluster create NOME_DO_CLUSTER
```

Informações do Cluster
Para listar os clusters existentes:

```bash
k3d cluster list
```

Para obter informações do cluster:

```bash
kubectl cluster-info
```

Para listar os nós do cluster:

```bash
kubectl get nodes
```

Deletar um Cluster
Para deletar um cluster, execute o comando:

```bash
k3d cluster delete NOME_DO_CLUSTER
```

Criar um Cluster com Recursos de Control Plane e Worker Nodes
Para criar um cluster com 3 servidores (control plane) e 3 agentes (worker nodes):

```bash
k3d cluster create meucluster --servers 3 --agents 3
```

Criar Redirecionamento de Porta para o Loadbalancer do Cluster

Para criar um cluster com redirecionamento de porta para o loadbalancer:

Observação: Usando -p "8081:30000@loadbalancer", o loadbalancer será o container criado automaticamente pelo Docker.

Estamos criando um mapeamento de entrada pela porta 8081

```bash
k3d cluster create meucluster --servers 3 --agents 3 -p "8081:30000@loadbalancer"
```
