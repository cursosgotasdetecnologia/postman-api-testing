# postman-api-testing

![Postman](https://img.shields.io/badge/Postman-FF6C37?style=for-the-badge&logo=postman&logoColor=white)
![GitHub Actions](https://img.shields.io/badge/GitHub_Actions-2088FF?style=for-the-badge&logo=githubactions&logoColor=white)
![Newman](https://img.shields.io/badge/Newman-CLI-333333?style=for-the-badge)
![Allure Report](https://img.shields.io/badge/Allure-Report-65C88C?style=for-the-badge)

Repositório da segunda etapa de uma formação em Postman, iniciada na aula 46. Reúne Collections e recursos locais para exercitar testes funcionais de API, cenários de segurança, carga, monitoramento e automação visual com Postman Flows, além de integrações selecionadas com Postman CLI, Newman e GitHub Actions.

## 📚 Módulos da Formação — Segunda Etapa

Esta etapa amplia o projeto com recursos avançados do Postman, automação em CI/CD, análise de resultados e organização das entregas em um portfólio profissional da formação Gotas de Tecnologia.

### Módulo 13 — Mock Server
Preparação de respostas simuladas com Examples, organização de cenários de sucesso e erro e utilização do Mock Server por frontend e outros consumidores da API.

### Módulo 14 — Postman Agent Mode / IA
Uso do Agent Mode com contexto e prompts, análise dos testes gerados, execução das validações e exploração de Postman AI Skills.

### Módulo 15 — Git, GitHub e VS Code para Projetos de API
Estruturação do repositório, integração com Native Git e versionamento de Collections e Environments, com revisão e sincronização das alterações.

### Módulo 16 — Postman CLI e Newman
Preparação da suíte para execução pelo terminal, reutilização de testes entre Collection, folders e requests e comparação prática entre as ferramentas.

### Módulo 17 — CI/CD com GitHub Actions e Postman CLI
Automação dos testes em pipelines, configuração de variáveis e Secrets e demonstração de falhas e testes ignorados.

### Módulo 18 — Relatórios Automatizados com Newman e Allure
Preparação do projeto Node.js, execução com Newman, análise do Allure Report e armazenamento e consulta do relatório como artifact no GitHub Actions.

### Módulo 19 — Postman CLI com API Key
Autenticação no Postman Cloud, execução de Collections por seus IDs e configuração da integração com CI/CD.

### Módulo 20 — Testes de Performance de APIs com Postman
Execução dos perfis Fixed, Ramp Up, Spike e Peak, interpretação das métricas, critérios de aprovação e automação com Postman CLI e GitHub Actions.

### Módulo 21 — Segurança de APIs para QA
Verificações práticas baseadas em OWASP: controle de acesso, propriedades, funções, exposição de dados, recursos, fluxos, integrações, SSRF e SQL Injection.

### Módulo 22 — Monitor
Preparação de uma Collection para monitoramento, agendamento de execuções e análise do histórico, com evidências de falha controlada e recuperação.

### Módulo 23 — Flows
Preparação de dados e scripts, criação manual de blocos e geração do Flow a partir da Collection. Exploração de Success, Fail, visualização dos resultados, pausa e organização visual, com versionamento no projeto.

### Módulo 24 — Documentação
Elaboração de descrições de pastas e Collections com Agent Mode e ChatGPT, seguida de revisão com base nas requisições e scripts existentes.

### Módulo 25 — Projeto Final / Portfólio
Organização do README, publicação do Allure Report com GitHub Pages e apresentação das entregas, com orientações para aplicação profissional
e continuidade dos estudos.

🔗 [Projeto da primeira etapa — fundamentos e automação com Postman](https://github.com/cursosgotasdetecnologia/api-testes-postman)

🎓 [Conheça as formações da Gotas de Tecnologia](https://gotasdetecnologia.com.br/cursos/)


## Collections

| Collection | Finalidade | Caminho relativo |
|---|---|---|
| **Projeto QA Automation - Etapa 2** | Requests para autenticação e operações com produtos, categorias e fornecedores na API real, além de cenários de requisição para Mock Server. Inclui exemplos de resposta salvos. | [`postman/collections/Projeto QA Automation - Etapa 2/`](<postman/collections/Projeto QA Automation - Etapa 2/>) |
| **projeto-postman-advanced** | Testes funcionais para login, produtos, categorias e fornecedores, junto de cenários de autenticação, controle de acesso e riscos inspirados no OWASP API Security. | [`postman/collections/projeto-postman-advanced/`](postman/collections/projeto-postman-advanced/) |
| **projeto-postman-performance** | Três requests (login, listagem de produtos e categorias) usados nos cenários de teste de carga. | [`postman/collections/projeto-postman-performance/`](postman/collections/projeto-postman-performance/) |
| **projeto-postman-monitor** | Quatro requests para saúde da API, autenticação, primeira página de produtos e consulta de fornecedores; a evidência registra 19 assertions. | [`postman/collections/projeto-postman-monitor/`](postman/collections/projeto-postman-monitor/) |
| **projeto-postman-flows** | Oito requests que percorrem autenticação e ciclo de vida de um produto, da criação à exclusão e conferência de que deixou de existir. | [`postman/collections/projeto-postman-flows/`](postman/collections/projeto-postman-flows/) |

## Recursos implementados

- **Mocks:** a Collection `Projeto QA Automation - Etapa 2` contém requests para cenários como categoria existente, inexistente ou inválida, categoria duplicada e ausência de token. Esses arquivos descrevem requests; não constituem, por si só, um servidor Mock em execução. A variável `projetoQAAutomationMockUrl` deve ser configurada para usar um endpoint de Mock apropriado.
- **Testes automatizados:** scripts de resposta validam status HTTP, conteúdo e campos das respostas em requests das Collections. A pasta de exemplos de uma request contém respostas ilustrativas/salvas; elas não são uma execução de teste nem substituem os scripts e seus resultados.
- **Segurança:** a Collection `projeto-postman-advanced` agrupa cenários de autenticação, autorização, exposição de dados, paginação, injeção e integrações. São verificações implementadas nas requests, não uma certificação de segurança da API.
- **Performance:** `projeto-postman-performance` serve de base para perfis Fixed, Ramp Up, Peak e Spike no Postman CLI. Há execuções documentadas tanto no Postman CLI quanto no GitHub Actions.
- **Monitor:** a Collection `projeto-postman-monitor` foi usada em um Monitor do Postman Cloud. O histórico registrado inclui execução aprovada, falha controlada de assertion e recuperação.
- **Flows:** os arquivos locais em `postman/flows/` representam fluxos do Postman. Um fluxo encadeia autenticação, operações de produto e tratamento de sucesso/falha. O diagrama e a execução pertencem ao recurso Postman Flows, não apenas aos requests da Collection.

## Estrutura do repositório

| Caminho | Conteúdo |
|---|---|
| `.github/workflows/` | Workflows de Postman CLI, execução pelo Postman Cloud, performance e relatório Allure. |
| `.postman/resources.yaml` | Mapeamentos entre recursos locais e objetos do Postman Cloud. |
| `postman/collections/` | Collections e requests em YAML, com definições, scripts e exemplos associados. |
| `postman/environments/` | Environments locais para as Collections. |
| `postman/globals/` | Globals do workspace. |
| `postman/flows/` | Exports locais dos dois Postman Flows. |
| `newman/collections/` e `newman/environments/` | Exportações JSON da Collection avançada e do Environment usado com Newman. |
| `newman/reports/` | Relatório HTML versionado: [`relatorio-aula66.html`](newman/reports/relatorio-aula66.html). |
| `evidencias/` | Documentos Markdown e imagens de execuções registradas de Flows, Monitor e performance. |

Os arquivos Postman em YAML e os exports JSON de Newman são recursos locais distintos. O mapeamento em `.postman/resources.yaml` associa Collections, Environments, Globals e Flows locais a recursos do Postman Cloud; ele não significa que todos esses recursos sejam executados localmente ou no CI.

## Pré-requisitos e configuração

- Postman para abrir e trabalhar com as Collections, Environments e Flows.
- Postman CLI para os fluxos de execução com CLI.
- Newman para executar os exports JSON presentes em `newman/`.
- Acesso à API de teste apropriada e, para funcionalidades Cloud, uma conta Postman com os recursos correspondentes.
- Para executar os workflows, um repositório GitHub com Actions habilitado e as variáveis/Secrets correspondentes configurados.

Antes de executar:

1. Selecione o Environment adequado à Collection e configure as variáveis necessárias: `projetoQAAutomationBaseUrl`, `projetoQAAutomationEmail`, `projetoQAAutomationPassword`, `projetoQAAutomationAccessToken`, `projetoQAAutomationProductId`, `projetoQAAutomationCategoryId`, `projetoQAAutomationSupplierId`, `projetoQAAutomationAccessTokenUsuario01`, `projetoQAAutomationAccessTokenUsuario02`, `projetoQAAutomationConsumerEmail`, `projetoQAAutomationConsumerPassword`, `projetoQAAutomationEstoqueProdutoId`, `projetoQAAutomationMockUrl` e `token`, conforme o cenário.
2. Configure valores de autenticação com segurança. Os Environments versionados contêm valores preenchidos; confira-os e substitua dados sensíveis antes de compartilhar ou executar contra qualquer ambiente. Não versione credenciais reais.
3. Confira a URL-base e o ambiente de destino. Algumas requests criam, alteram ou excluem dados; há também uma request de limpeza de arquivos de produtos que pode apagar todos os arquivos desse recurso.
4. Para execução via GitHub Actions, configure as variáveis e Secrets indicados na tabela de workflows.

O Environment avançado também é usado pelos recursos de performance, Monitor e Flows. Variáveis como `projetoQAAutomationAccessToken` e `projetoQAAutomationProductId` podem ser preenchidas por scripts durante uma sequência de requests.

## Formas de execução

### Postman

Abra os recursos YAML no modo de trabalho local do Postman ou use o mapeamento configurado em `.postman/resources.yaml` para trabalhar com os recursos vinculados ao Postman Cloud. Selecione o Environment correspondente, configure seus valores locais e execute a Collection ou requests individualmente. Para Flows e Monitor, use os recursos correspondentes do Postman Cloud; os arquivos locais são exports/configurações, não uma execução automática desses serviços.

O Mock Server precisa de um endpoint configurado em `projetoQAAutomationMockUrl`; o repositório não declara um endpoint de Mock ativo em `.postman/resources.yaml`.

### Postman CLI

O workflow `postman-cloud-cli.yml` usa os arquivos locais da Collection avançada e do Environment. A forma geral de execução é:

```bash
postman collection run postman/collections/projeto-postman-advanced \
  --environment postman/environments/projeto-postman-advanced-env.environment.yaml
```

O workflow fornece valores de configuração com `--env-var` sem incluí-los no repositório. Para executar localmente, configure as variáveis necessárias no Environment ou forneça overrides seguros. A Collection avançada é a única executada por esse workflow local.

Há também um workflow separado que executa uma Collection e um Environment identificados no Postman Cloud. A execução de performance usa o comando `postman performance run` contra os recursos Cloud e recebe perfil/limites pela configuração do próprio workflow.

### Newman

O repositório inclui exports JSON próprios para Newman. Com Newman instalado e o Environment configurado localmente, a execução da Collection avançada pode ser iniciada assim:

```bash
newman run newman/collections/projeto-postman-advanced.postman_collection.json \
  -e newman/environments/projeto-postman-advanced-env.postman_environment.json
```

Não há `package.json` nesta cópia para instalar Newman por dependências locais. O relatório em `newman/reports/relatorio-aula66.html` é um artefato já versionado; sua presença não implica que o workflow Allure seja executável com os arquivos desta branch.

## Workflows do GitHub Actions

| Workflow | Finalidade | Gatilhos | Variáveis do repositório | Secrets |
|---|---|---|---|---|
| [`postman-cloud-cli.yml`](.github/workflows/postman-cloud-cli.yml) | Executar `projeto-postman-advanced` e seu Environment local com Postman CLI. | `workflow_dispatch`; `push` para `main` quando há alterações em `postman/**` ou `.github/workflows/**`. | `API_BASE_URL` | `API_TEST_EMAIL`, `API_TEST_PASSWORD` |
| [`postman-api-tests.yml`](.github/workflows/postman-api-tests.yml) | Autenticar o Postman CLI e executar a Collection avançada e o Environment pelos recursos identificados no Postman Cloud. | Somente `workflow_dispatch`. | `API_BASE_URL` | `POSTMAN_API_KEY`, `API_TEST_EMAIL`, `API_TEST_PASSWORD` |
| [`performance-tests.yml`](.github/workflows/performance-tests.yml) | Executar teste de performance via Postman CLI e publicar o log como artifact com retenção de 7 dias. | Somente `workflow_dispatch`; solicita `virtual_users` (padrão `10`) e `duration_minutes` (padrão `1`). | `POSTMAN_PERFORMANCE_COLLECTION_ID`, `POSTMAN_ENVIRONMENT_ID` | `POSTMAN_API_KEY` |
| [`allure-report.yml`](.github/workflows/allure-report.yml) | Executar a demonstração Newman/Allure e salvar o relatório como artifact com retenção de 7 dias. | Somente `workflow_dispatch`. | `API_BASE_URL` | `API_TEST_EMAIL`, `API_TEST_PASSWORD` |

Os nomes na tabela são os nomes esperados pela configuração do GitHub Actions; os valores devem ser definidos no repositório, não neste README. Os workflows não cobrem todas as Collections: os fluxos de CI executam a Collection avançada, performance ou a demonstração Allure, conforme cada configuração. A Collection de etapa 2, o Monitor e os Flows não têm workflow de execução dedicado nesta cópia.

### Dependência específica do Allure

`allure-report.yml` faz checkout da branch `demo-allure`, configura Node.js e Java e executa `npm ci` e Newman sobre `newman/allure-demo/`. Nesta cópia da branch principal não há `package.json` nem `newman/allure-demo/`; portanto, os arquivos necessários à demonstração não estão disponíveis aqui. O workflow depende do conteúdo existente na branch `demo-allure` e não deve ser entendido como executável diretamente com os arquivos desta `main`.

O relatório Allure é salvo como **GitHub Actions artifact**. 

### [DEMO] Allure Report publicado

[Acessar o relatório Allure](https://cursosgotasdetecnologia.github.io/postman-api-testing/)

Este relatório utiliza a suíte de demonstração da branch `demo-allure`, preparada com falhas controladas para exercitar a identificação e a análise de testes reprovados.

A execução registrada apresentou:
- 12 testes executados;
- 9 aprovados;
- 3 reprovados;
- 75% de aprovação.

A publicação no GitHub Pages foi concluída com sucesso. 
O workflow termina com status de falha para preservar o resultado real dos testes da demonstração.

As reprovações devem ser consultadas em **Suites** no relatório.


## Evidências e resultados registrados

As métricas a seguir descrevem execuções registradas nos documentos; não garantem o desempenho atual da API.

| Evidência | Resumo |
|---|---|
| [Postman Monitor](evidencias/monitor/evidencia-monitor.md) | Registra uma execução Healthy com 4 requests, 19 assertions aprovadas e nenhum erro, além de uma falha controlada e a recuperação do Monitor. |
| [Postman Flows](evidencias/flows/evidencia-flows.md) | Documenta o ciclo de produto, a confirmação HTTP 404 após exclusão e cenários controlados de falha de autenticação e divergência de estoque. |
| [Performance — Postman CLI](evidencias/performance/postman-cli/analise-performance-cli.md) | Execução Fixed: 10 usuários virtuais por 1 minuto, 3.133 requests, 50,53 requests/s e P95 de 310 ms; sem erros ou falhas de assertions registrados. |
| [Performance — GitHub Actions](evidencias/performance/postman-github/analise-performance-github.md) | Execução Fixed: 10 usuários virtuais por 1 minuto, 1.831 requests, 30,02 requests/s e P95 de 469 ms; sem erros ou falhas de assertions registrados. |
| [Performance — Fixed](evidencias/performance/fixed/resultado-fixed.md) | Execução aprovada registrada com 886 requests e P95 de 334 ms. |
| [Performance — Fixed com reprovação controlada](evidencias/performance/fixed/resultado-reprovado.md) | Registra reprovação do critério de vazão (meta de 200 requests/s, resultado de 46,56), sem erros ou falhas funcionais reportados. |
| [Performance — Peak](evidencias/performance/peak/resultado-peak.md) | Execução aprovada registrada com 1.764 requests e P95 de 313 ms. |
| [Performance — Ramp Up](evidencias/performance/ramp-up/resultado-ramp-up.md) | Execução aprovada registrada com 1.768 requests e P95 de 285 ms. |
| [Performance — Spike](evidencias/performance/spike/resultado-spike.md) | Execução aprovada registrada com 1.109 requests e P95 de 312 ms. |

## Resultados e limitações

- Os registros de performance mostram cenários aprovados e uma reprovação intencional por critério de vazão. São medições das execuções documentadas, dependentes do ambiente e das condições de carga daquele momento.
- A evidência do Monitor registra detecção de falha de assertion e recuperação; isso documenta a configuração testada, não disponibilidade contínua do Monitor.
- Os arquivos `.flow` e o mapeamento em `.postman/resources.yaml` não garantem que os recursos correspondentes permaneçam acessíveis no Postman Cloud. Monitor, Flows, Mock Server e execuções por IDs dependem de configuração/acesso Cloud.
- Os exemplos de resposta salvos junto a requests servem como referência. Não devem ser interpretados como assertions implementadas ou resultados de execução.
- O relatório Allure depende de outra branch e não há, nesta cópia, package manifest nem exports da demonstração. GitHub Pages também não faz parte desta etapa.
