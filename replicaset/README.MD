# Explicação Técnica

## kind: ReplicaSet

O ReplicaSet é um controlador que assegura que um número especificado de réplicas de um Pod estejam rodando a todo momento. Ele oferece funcionalidades essenciais para garantir a alta disponibilidade dos Pods.

## metadata.name

Define o nome do ReplicaSet.

## spec.replicas

Define o número de réplicas desejadas.

## spec.selector

Especifica os rótulos que os Pods gerenciados pelo ReplicaSet devem ter. Isso deve coincidir com os rótulos definidos no template para garantir que os Pods sejam corretamente gerenciados.

## spec.template

Define o template para os Pods, incluindo metadados e especificações dos containers.

## Comentários Detalhados

### matchLabels e labels

É crucial que o rótulo definido em `matchLabels` no selector seja idêntico ao rótulo definido em `labels` no template de Pod. Isso assegura que o ReplicaSet possa identificar e gerenciar corretamente os Pods.
