# Pre requisitos:
docker

# Instalar k3d:
https://k3d.io/v5.6.3/#releases

# Criar cluster k8s (Simples):
k3d cluster create NOME_DO_CLUSTER

# Infos do cluster:
k3d cluster list
kubectl cluster-info
kubectl get nodes

# Deletar cluster:
k3d cluster delete NOME_DO_CLUSTER

# Criar cluster com recursos de control plane e worker node:
k3d cluster create meucluster --servers 3 --agents 3

# Criar redirecionamento de porta para o loadbalancer do cluster:
k3d cluster create meucluster --servers 3 --agents 3 -p "808:30000@loadbalancer"
    obs: -p "8080:30000@loadbalancer" o loadbalancer seria o container que docker cria automaticamente, ou seja estamos criando um mapeamento de entrada pela porta 8080

