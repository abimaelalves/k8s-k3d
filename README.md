# Configuração do Cluster Kubernetes com k3d

## Pré-requisitos

- Docker

## Instalar k3d

Para instalar o k3d, siga as instruções na [página de lançamentos do k3d](https://k3d.io/v5.6.3/#releases).

## Criar um Cluster Kubernetes Simples

Para criar um cluster Kubernetes simples com k3d, execute o comando:

```bash
k3d cluster create NOME_DO_CLUSTER
```bash

k3d cluster list

kubectl cluster-info

kubectl get nodes
