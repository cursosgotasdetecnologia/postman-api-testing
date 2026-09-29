# Evidência de Performance — Perfil Ramp Up

## Configuração

- Collection: projeto-postman-performance
- Perfil de carga: Ramp Up
- Usuários virtuais máximos: 10
- Duração: 1 minuto
- Critério de aprovação: P95 inferior a 1000 ms

## Resultado geral

- Status: aprovado
- Total de requisições: 1.768
- Requisições por segundo: 29,13
- Tempo médio de resposta: 147 ms
- P90: 253 ms
- P95: 285 ms
- P99: 426 ms
- Taxa de erros: 0%
- Taxa de falhas: 0%

## Consumo da máquina geradora da carga

- Pico de CPU: 25,3%
- Pico de memória: 52,5%

Esses valores representam a máquina que executou o teste e não o servidor da API.

## Análise

O cenário foi aprovado porque o P95 obtido foi de 285 ms, permanecendo abaixo do limite definido de 1.000 ms.

Não foram identificados erros de comunicação nem falhas nas validações funcionais durante a execução.

A carga começou com um usuário virtual, aumentou gradualmente até atingir 10 usuários e permaneceu nesse nível durante a etapa final.

Mesmo com o crescimento progressivo da carga, o tempo médio de resposta permaneceu estável. O gráfico apresentou apenas uma elevação inicial, possivelmente relacionada ao aquecimento da aplicação ou ao estabelecimento das primeiras conexões.

## Evidência visual

![Resultado do teste Ramp Up](resultado-ramp-up.png)