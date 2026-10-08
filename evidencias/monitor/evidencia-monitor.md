# Evidência — Postman Monitor

## Configuração

- Collection: projeto-postman-monitor
- Environment: projeto-postman-advanced-env
- Quantidade de requests: 4
- Quantidade de assertions: 19
- Região: US East
- Frequência final: diária

## Recursos monitorados

1. Saúde da API
2. Autenticação do administrador
3. Primeira página de produtos
4. Consulta de fornecedores

## Resultado inicial

- Status: Healthy
- Requests executadas: 4
- Assertions aprovadas: 19
- Assertions reprovadas: 0
- Erros de execução: 0

## Falha controlada

Foi alterado temporariamente o status esperado da consulta de fornecedores de HTTP 200 para HTTP 201.

A API continuou retornando HTTP 200 e o Monitor registrou corretamente a falha da assertion.

## Recuperação

Após restaurar o resultado esperado para HTTP 200, uma nova execução foi realizada e o Monitor voltou ao estado Healthy.

O histórico demonstrou o ciclo:

- execução aprovada;
- falha identificada;
- recuperação comprovada.

## Evidências visuais

![Histórico do Monitor](evidencia-monitor.png)
