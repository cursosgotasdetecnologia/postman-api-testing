# Evidência de Performance — Perfil Spike

## Configuração

- Collection: projeto-postman-performance
- Perfil de carga: Spike
- Carga base: 1 usuário virtual
- Usuários virtuais máximos: 10
- Duração: 1 minuto
- Critério de aprovação: P95 inferior a 1.000 ms

## Resultado geral

- Status: aprovado
- Total de requisições: 1.109
- Requisições por segundo: 18,80
- Tempo médio de resposta: 155 ms
- P90: 273 ms
- P95: 312 ms
- P99: 483 ms
- Taxa de erros: 0%
- Taxa de falhas: 0%

## Consumo da máquina geradora da carga

- Pico de CPU: 19,7%
- Pico de memória: 53,9%

Esses valores representam a máquina que executou o teste e não o servidor da API.

## Análise

O cenário foi aprovado porque o P95 obtido foi de 312 ms, permanecendo abaixo do limite definido de 1.000 ms.

Não foram identificados erros de comunicação nem falhas nas validações funcionais durante a execução.

A quantidade de requisições por segundo acompanhou o crescimento dos usuários virtuais e alcançou aproximadamente 50 requisições por segundo durante o pico.

Foi observada uma elevação isolada no tempo médio de resposta durante o crescimento da carga. Entretanto, a latência voltou para uma faixa estável e não ocorreu degradação contínua no momento de maior volume.

A autenticação apresentou os maiores tempos de resposta, com média de 241 ms, P95 de 355 ms, P99 de 675 ms e tempo máximo de 1.782 ms.

## Evidência visual

![Resultado do teste Spike](resultado-spike.png)