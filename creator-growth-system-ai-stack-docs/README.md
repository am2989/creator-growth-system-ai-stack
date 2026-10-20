# Creator Growth System: Manual do AI Stack e Plano Operacional de Crescimento (30 Dias)

Desafio Criativo final do bootcamp DIO: **Governança por Dados, Plano de Tração de 30 Dias e AI Stack Operacional**.

> **Nota:** os dados deste projeto são **fictícios**, criados para fins de exercício. O perfil é simulado: uma contabilista que cria conteúdo sobre contabilidade e análise de dados no LinkedIn (projeto "Contas com Dados").

## Documento de entrega

Documento completo (acesso público, modo leitor): **[https://docs.google.com/document/d/1ncll4-Dtwdu1x5j_EWrwAxCUj_JqUmnkON0YBj2AbGw/edit?usp=sharing]**

## Objetivo

Estruturar a governança contínua de um canal de conteúdo, com decisões orientadas por dados e memória estratégica:

1. Um ritual semanal fixo de 20 minutos com a triagem **Repetir, Parar e Testar** (R.P.T.).
2. Um plano de crescimento de 30 dias ancorado numa **única Métrica Mãe**, com 4 testes semanais encadeados.
3. Um **AI Stack operacional** de 4 camadas (Dados, Leitura, Hipóteses e Registo), operado por um Prompt Mestre de Governança.

## Metodologia

Todo o trabalho foi feito num **único chat** com um único LLM (Claude), para manter o contexto, a Métrica Mãe e o baseline coerentes do início ao fim. Cada resultado foi registado no documento de entrega.

## Estrutura do repositório

```
creator-growth-system/
├── README.md
└── docs/
    ├── 01-rotina-decisao-semanal.md
    ├── 02-plano-crescimento-30-dias.md
    └── 03-ai-stack-e-prompt-mestre.md
```

## Resumo dos três blocos

### Parte 1: Rotina de Decisão Semanal e Matriz R.P.T.

- Leitura pré-decisão: o alcance (+33%) e os salvamentos (+95%) cresceram, mas a conversão ficou praticamente parada. A tensão central é a distância entre atenção e conversão.
- Matriz R.P.T.: **Repetir** o carrossel e os posts de opinião, **Testar** o gancho do vídeo, **Parar** a enquete semanal.
- Ritual de 20 minutos, às segundas-feiras às 08:30, em 5 etapas cronometradas.
- Detalhe: [docs/01-rotina-decisao-semanal.md](docs/01-rotina-decisao-semanal.md)

### Parte 2: Plano de Crescimento de 30 Dias

- **Métrica Mãe:** conversões por 1.000 impressões. Baseline 0,45, meta 0,80 em 30 dias.
- **Esteira encadeada:** gancho do vídeo, depois CTA único, depois frequência do carrossel e, por fim, consolidação sem variáveis novas.
- **Gatilho de correção de rota** antes da Semana 3.
- Detalhe: [docs/02-plano-crescimento-30-dias.md](docs/02-plano-crescimento-30-dias.md)

### Parte 3: AI Stack Operacional

- 4 camadas: Dados (Planilha de Controlo), Leitura (Claude), Hipóteses (Claude) e Registo (Google Docs).
- Prompt Mestre de Governança Semanal, parametrizado, pronto a copiar todas as segundas-feiras.
- Plano de expansão em 3 níveis, com gatilhos numéricos.
- Detalhe: [docs/03-ai-stack-e-prompt-mestre.md](docs/03-ai-stack-e-prompt-mestre.md)

## Como usar o Prompt Mestre

1. Atualizar a Planilha de Controlo com as métricas da semana (minutos 0 a 3).
2. Abrir o prompt em `docs/03-ai-stack-e-prompt-mestre.md`, preencher os campos entre colchetes e colar no LLM, no mesmo chat do ciclo.
3. Aplicar a decisão R.P.T. e a hipótese da semana, e registar a entrada no documento.

## Competências demonstradas

- Governança de dados e tomada de decisão semanal
- Definição de Métrica Mãe, baseline e metas
- Desenho de experimentos encadeados com critérios de sucesso
- Engenharia de prompts e arquitetura de AI Stack

## Autoria

Alda Benta
