# Evidência de Performance — Perfil Fixed

## Configuração

- Collection: projeto-postman-performance
- Perfil de carga: Fixed
- Usuários virtuais: 3
- Duração: 1 minuto
- Critério de aprovação: P95 inferior a 1.000 ms

## Resultado geral

- Status: aprovado
- Total de requisições: 886
- Requisições por segundo: 14,73
- Tempo médio de resposta: 150 ms
- P90: 250 ms
- P95: 293 ms
- P99: 497 ms
- Taxa de erros: 0%
- Taxa de falhas: 0%

## Consumo da máquina geradora da carga

- Pico de CPU: 20,5%
- Pico de memória: 50%

Esses valores representam a máquina que executou o teste e não o servidor da API.

## Análise

O cenário foi aprovado porque o P95 obtido foi de 293 ms, permanecendo abaixo do limite definido de 1.000 ms.

Não foram identificados erros de comunicação nem falhas nas validações funcionais durante a execução.

A autenticação apresentou os maiores tempos de resposta entre as requisições executadas, com média de 247 ms, P95 de 349 ms
e tempo máximo de 1.890 ms.

## Evidência visual

![Resultado do teste Fixed](resultado-fixed.png)