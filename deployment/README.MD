# Explicação Técnica

## kind: Deployment

O Deployment tem uma estrutura similar ao ReplicaSet, mas oferece funcionalidades avançadas, como:
- Atualizações declarativas de Pods.
- Rollback automático para versões anteriores no caso de falhas.
- Escalonamento de Pods.
- Gerenciamento de estratégias de atualização (como RollingUpdate e Recreate).

## metadata.name

Define o nome do Deployment.

## spec.replicas

Define o número de réplicas desejadas, assim como no ReplicaSet.

## spec.selector

Especifica os rótulos que os Pods gerenciados pelo Deployment devem ter. Isso deve coincidir com os rótulos definidos no template para garantir que os Pods sejam corretamente gerenciados.

## spec.template

Define o template para os Pods, incluindo metadados e especificações dos containers, semelhante ao ReplicaSet.

## Comentários Detalhados

### matchLabels e labels

É crucial que o rótulo definido em `matchLabels` no selector seja idêntico ao rótulo definido em `labels` no template de Pod. Isso assegura que o Deployment possa identificar e gerenciar corretamente os Pods.
