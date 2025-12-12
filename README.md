# Análise de Risco de Evasão Escolar

Este projeto realiza uma análise preditiva de risco de evasão escolar a partir de uma base de 150 alunos, utilizando indicadores de desempenho acadêmico (nota média) e frequência (faltas) para construir um score de risco e classificar os estudantes em faixas de atenção. 

## Objetivo

Identificar alunos com maior probabilidade de evasão para apoiar decisões de intervenção pedagógica, monitoramento e ações preventivas baseadas em dados.

## Base de dados

- 150 alunos.
- 12 variáveis, incluindo:
  - Nota média.
  - Frequência (%).
  - Faltas.
  - Participação em atividades extras.
  - Participação em programa de apoio.
  - Indicador de evasão (Sim/Não).
- Arquivo: `dados/base_alunos_score_evasao.xlsx`.

## Metodologia

O score de risco foi construído em três etapas principais:

1. Preparação da base de dados com normalização das variáveis de interesse.
2. Cálculo de um índice de risco combinando:
   - Faltas normalizadas (peso de 60%).
   - Nota invertida e normalizada (peso de 40%).
3. Classificação dos alunos em faixas de risco:
   - **ALTO**: score ≥ 70
   - **MÉDIO**: score entre 40 e 69
   - **BAIXO**: score < 40

A fórmula geral do score de risco é:

Risco = 100 × (0,6 × Faltas_normalizadas + 0,4 × Nota_invertida_normalizada)

## Principais resultados

- Proporção de alunos por faixa de risco (ALTO, MÉDIO, BAIXO).
- Comparação entre alunos que evadiram e que permaneceram na instituição em termos de:
  - Nota média.
  - Faltas.
  - Frequência.
- Identificação de aproximadamente um quarto da base como alunos em risco ALTO de evasão, o que orienta ações de acompanhamento direcionado.

Mais detalhes, gráficos e tabelas estão no relatório em `relatorio/relatorio_analise_risco_evasao.pdf`.

## Ferramentas e competências

- Excel para tratamento de dados, tabelas dinâmicas e gráficos.
- Conceitos de banco de dados e mineração de dados.
- Construção de score de risco a partir de múltiplas variáveis.
- Análise descritiva e interpretação de indicadores educacionais.
