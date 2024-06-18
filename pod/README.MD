# Explicação Técnica

## kind: Pod

Um Pod é a menor unidade de execução no Kubernetes, que pode conter um ou mais containers. Abaixo estão dois exemplos de configuração de Pods: um simples e outro com labels detalhadas.

## Exemplo 1: Pod Simples (pod.yaml)

Este exemplo define um Pod básico com um único container.

## Exemplo 2: Pod com Labels (labels.yaml)

Este exemplo define dois Pods, cada um com labels adicionais que ajudam na categorização e gerenciamento:

### metadata.labels

- `app: web`: O rótulo 'app: web' é usado para categorizar o Pod como parte da aplicação 'web'.
- `versao: blue` e `versao: green`: Esses rótulos indicam que o Pod está executando a versão 'blue' ou 'green' da aplicação, respectivamente.
