# Parte 3: AI Stack Operacional e Prompt Mestre de Governança

## Ferramentas

- **Dados:** Planilha de Controlo (Google Sheets), com exportação das estatísticas do LinkedIn
- **Leitura e Análise:** Claude
- **Registo e Inteligência:** Google Docs

## 1. Arquitetura das 4 Camadas

| Camada | Ferramenta | Função | Frequência | Saída |
|---|---|---|---|---|
| 1. Dados | Planilha de Controlo + exportação do LinkedIn | Guardar métricas por publicação; calcular a Mãe e os secundários | Segunda-feira, minutos 0 a 3 | Tabela semanal e Mãe calculada |
| 2. Leitura | Claude + Prompt Mestre | Ler sinais e tensões, avaliar a Mãe, aplicar R.P.T. | Segunda-feira, minutos 3 a 13 | Leitura de 3 frases e matriz R.P.T. |
| 3. Hipóteses | Claude + esteira de 30 dias | Definir a hipótese única de 7 dias | Segunda-feira, minutos 13 a 17 | Hipótese numa linha |
| 4. Registo | Google Docs | Guardar decisão, hipótese e aprendizado | Segunda-feira, minutos 17 a 20 | Entrada datada |

**Fluxo:** a planilha entrega os dados, o Claude lê e decide, a hipótese nasce da leitura e o documento guarda tudo. No ciclo seguinte, o registo volta ao Claude como contexto.

## 2. Prompt Mestre de Governança Semanal

Copiar todas as segundas-feiras, preencher os campos entre colchetes e colar no mesmo chat do ciclo.

```text
Atue como auditor de performance e estratega de growth do projeto [NOME DO PROJETO] no canal [CANAL]. Vamos rodar o ritual semanal de 20 minutos da [DATA DA SEGUNDA-FEIRA]. Seja direto, use apenas os dados fornecidos e declare explicitamente quando a amostra for pequena demais para concluir.

CONTEXTO FIXO DO CICLO:
- Métrica Mãe: [NOME DA MÉTRICA MÃE]
- Baseline: [VALOR]
- Meta do ciclo: [META] até [DATA FINAL]
- Rampa semanal: S1 [X], S2 [X], S3 [X], S4 [X]
- Semana atual do ciclo: [1, 2, 3 ou 4]
- Teste ativo da semana que terminou: [VARIÁVEL, HIPÓTESE, MÉTRICA E CRITÉRIO DE SUCESSO]
- Gatilho de correção de rota: [SINAL NUMÉRICO]

DADOS BRUTOS DA SEMANA (cole a tabela da planilha):
[COLE AQUI: por publicação, formato, impressões, salvamentos, comentários, cliques, conversões]

DADOS DA SEMANA ANTERIOR PARA COMPARAÇÃO:
[COLE AQUI]

INICIATIVAS ATIVAS:
[LISTE FORMATOS E SÉRIES EM EXECUÇÃO]

ENTREGUE, NESTA ORDEM:
1. LEITURA DE SINAIS E TENSÕES: o que cresceu, o que caiu, qual é a principal tensão e o que pode ser ruído de algoritmo em vez de sinal (máximo 5 linhas).
2. PROGRESSO DA MÉTRICA MÃE: valor da semana, valor acumulado do ciclo, distância para a rampa e para a meta, e se o gatilho de correção de rota foi acionado (sim ou não, com o número).
3. VEREDITO DO TESTE ATIVO: confirmado, refutado ou inconclusivo, com base no critério definido antes do teste. Não reinterprete o critério depois de ver os dados.
4. DECISÃO R.P.T.: para cada iniciativa, REPETIR, PARAR ou TESTAR, com o dado de suporte. No máximo um TESTAR por ciclo.
5. HIPÓTESE DO PRÓXIMO CICLO DE 7 DIAS: uma única variável isolada, no formato Se [AÇÃO], então [EXPECTATIVA MENSURÁVEL], medido por [MÉTRICA], com critério de sucesso e de invalidação e a conexão com a semana seguinte da esteira.
6. ENTRADA DE REGISTO: 4 linhas prontas para colar no documento (data, decisão, hipótese, aprendizado).

Regras: não invente dados; se faltar informação, liste o que falta; não proponha mais de uma variável nova por semana.
```

## 3. Plano de Expansão do Stack

| Nível | Quando entra | O que adicionar | Ganho |
|---|---|---|---|
| Atual | Até cerca de 20 publicações por mês, num só canal | Planilha manual, Claude e Google Docs | Custo zero e controlo total |
| Nível 2 | Mais de 40 publicações por mês, segundo canal, ou recolha semanal acima de 10 minutos | Painel no Looker Studio ligado à Planilha de Controlo | Mãe e rampa visíveis sem cálculo manual |
| Nível 3 | Mais de 100 conversões por mês | Automação que importa métricas e envia o Prompt Mestre ao Claude por API, com registo gravado numa base de dados | Ritual preparado antes de segunda-feira; os 20 minutos passam a ser só decisão |

**Regra de expansão:** só se automatiza um passo manual depois de ele ter sido executado de forma estável durante pelo menos 4 ciclos.
