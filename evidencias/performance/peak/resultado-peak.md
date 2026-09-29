# Evidência de Performance — Perfil Peak

## Configuração

- Collection: projeto-postman-performance
- Perfil de carga: Peak
- Carga base: 1 usuário virtual
- Usuários virtuais máximos: 10
- Duração: 1 minuto
- Critério de aprovação: P95 inferior a 1.000 ms

## Resultado geral

- Status: aprovado
- Total de requisições: 1.764
- Requisições por segundo: 29,08
- Tempo médio de resposta: 156 ms
- P90: 270 ms
- P95: 313 ms
- P99: 462 ms
- Taxa de erros: 0%
- Taxa de falhas: 0%

## Consumo da máquina geradora da carga

- Pico de CPU: 18,8%
- Pico de memória: 50%

Esses valores representam a máquina que executou o teste e não o servidor da API.

## Análise

O cenário foi aprovado porque o P95 obtido foi de 313 ms, permanecendo abaixo do limite definido de 1.000 ms.

Não foram identificados erros de comunicação nem falhas nas validações funcionais durante a execução.

A API permaneceu estável durante o período de carga máxima. A vazão ficou próxima de 55 requisições por segundo enquanto os 10 usuários virtuais permaneceram ativos.

A autenticação apresentou os maiores tempos de resposta, com média de 237 ms, P95 de 362 ms e tempo máximo de 2.009 ms.

A consulta de produtos apresentou média de 96 ms e P95 de 186 ms. A consulta de categorias apresentou média de 137 ms e P95 de 235 ms.

Foram observadas respostas isoladas acima de um segundo, mas elas não provocaram degradação contínua, erros ou reprovação do critério definido.

## Evidência visual

![Resultado do teste Peak](resultado-peak.png)