# Análise de Queimadas no Brasil (1998–2017)

Este projeto foi desenvolvido como parte do curso **Profissão: Analista de Dados** da EBAC, em parceria com a empresa **Semantix**.

O objetivo principal é investigar a evolução dos focos de queimadas no Brasil entre os anos de 1998 e 2017, identificar padrões temporais e regionais, e aplicar técnicas de análise de dados e machine learning para gerar insights e previsões relevantes.

---

##  Problema

As queimadas são uma ameaça constante ao meio ambiente brasileiro, especialmente na região amazônica e no Cerrado. Com o aumento da frequência e da intensidade ao longo dos anos, entender como esses focos se comportam é essencial para ações preventivas e políticas públicas.

Este projeto busca responder: **os focos de queimadas estão aumentando no Brasil? Onde e quando ocorrem mais? E é possível prever sua ocorrência com base em dados históricos?**

---

##  Coleta de Dados

- **Fonte:** Instituto Nacional de Pesquisas Espaciais (INPE)
- **Tipo de dados:** Estruturados (CSV)
- **Variáveis principais:** `year`, `month`, `state`, `number` (número de focos de queimadas)

O arquivo foi coletado diretamente do portal público de dados do INPE.

---

##  Análise Exploratória (EDA)

A análise exploratória identificou:

- Um crescimento de **+83,3%** nos focos de queimadas entre 1998 e 2017.
- **Mato Grosso** como o estado com maior número de focos no período.
- Aumento expressivo nos meses de seca (julho a setembro).
- Tendência temporal ascendente com variações sazonais.

---

##  Modelagem Estatística / Machine Learning

### Insight 6 — Modelo preditivo (Random Forest)

Foi desenvolvido um modelo preditivo utilizando **Random Forest Regressor** para estimar o número de focos de queimadas com base em três variáveis: **ano, mês e estado**.  
Os dados foram divididos em **treino (80%)** e **teste (20%)**.

####  Resultados obtidos

- **RMSE:** 179,13 → o erro médio nas previsões foi de aproximadamente 179 focos.
- **R²:** 0,2153 → o modelo explicou cerca de 21,5% da variação nos dados.

####  Importância das variáveis

- **Estado:** 44%
- **Mês:** 28,8%
- **Ano:** 27,1%

####  Interpretação

Apesar de não atingir alta precisão (R² baixo), o modelo confirma que as queimadas no Brasil estão fortemente associadas a **fatores sazonais e regionais**.

Mesmo com um modelo simples, é possível antecipar períodos e locais de maior risco, reforçando o valor da análise de dados para ações preventivas.

---

##  Dashboard (Looker Studio)

O projeto inclui um dashboard interativo no Looker Studio com:

- Gráfico de linha com evolução anual
- Gráfico de colunas por estado
- Indicadores de destaque (valores absolutos e crescimento)
- Gráfico medidor com a variação percentual



> Acesse o dashboard online: [🔗 Link do Looker Studio](https://lookerstudio.google.com/reporting/ddab568d-2930-4e9b-81c5-8508a67c4436)



