# 📊 Análise Estratégica e Comportamental de Vendas da SuperStore

## 📄 Visão Geral do Projeto

Este projeto apresenta uma análise de dados completa da rede SuperStore, dividida em duas fases principais:

1.  **Análise Exploratória e Comportamental:** Focada em entender o desempenho histórico de vendas e o comportamento dos clientes através de análises de Séries Temporais, Cohort (Retenção) e RFM (Segmentação).
2.  **Análise Estratégica e de Hipóteses:** Utiliza a metodologia Fato-Dimensão para formular e validar hipóteses de negócio, fornecendo insights diretos para a tomada de decisão.

O objetivo final é transformar dados brutos em inteligência acionável para otimizar estratégias de marketing, gestão de estoque e foco regional.

---

## 🔬 Fase 1: Análise Exploratória e Comportamental

Nesta fase, o foco foi explorar os dados para entender padrões e tendências. O script `analise_exploratoria.py` foi utilizado para gerar as seguintes visualizações.

### 1. Desempenho de Vendas ao Longo do Tempo

A análise da série temporal da receita mensal mostra um crescimento consistente ano a ano, com picos sazonais claros nos últimos trimestres, indicando um forte impacto das vendas de fim de ano.

![Gráfico de Receita Mensal](graficos/grafico_receita_mensal_aprimorado.png)

### 2. Análise de Retenção de Clientes (Cohort)

O mapa de calor revela que a retenção de clientes é mais forte no primeiro mês após a aquisição, mas apresenta uma queda acentuada posteriormente. Isso aponta para a necessidade de estratégias de engajamento pós-compra para aumentar a lealdade do cliente a longo prazo.

![Gráfico de Retenção Cohort](graficos/grafico_cohort_retencao_aprimorado.png)

### 3. Segmentação de Clientes (RFM)

A análise RFM (Recência, Frequência, Valor Monetário) permitiu segmentar a base de clientes em grupos estratégicos. Identificamos um pequeno, mas valioso, grupo de "Campeões" e uma grande oportunidade de reengajamento com os clientes "Hibernando".

![Gráfico de Segmentação RFM](graficos/grafico_rfm_segmentos_aprimorado.png)

---

## 🎯 Fase 2: Análise Estratégica e Validação de Hipóteses

Com base nos insights da fase exploratória, formulamos hipóteses de negócio utilizando a metodologia Fato-Dimensão para guiar a estratégia da empresa. O script `analise_estrategica.py` foi utilizado para validar estas hipóteses.

* **Pergunta de Negócio:** Quais são as características dos clientes, produtos e regiões que mais geraram faturamento para a SuperStore?
* **Fato (Métrica Principal):** `Sales` (Vendas)

### Validação das Hipóteses

**Hipótese 1: O segmento "Consumer" gera mais receita.**
* **Resultado:** Confirmado. O segmento "Consumer" é responsável pela maior parte do faturamento, seguido por "Corporate".

![Gráfico Vendas por Segmento](graficos/h1_vendas_por_segmento.png)

**Hipótese 2: A região "West" (Oeste) possui o maior faturamento.**
* **Resultado:** Confirmado. A região Oeste lidera com uma margem significativa sobre as demais, tornando-se uma área de foco estratégico.

![Gráfico Vendas por Região](graficos/h2_vendas_por_regiao.png)

**Hipótese 3: A categoria "Technology" é a que mais contribui para o faturamento.**
* **Resultado:** Confirmado. Tecnologia é a categoria de maior receita, apesar de "Office Supplies" ter um volume maior de pedidos.

![Gráfico Vendas por Categoria](graficos/h3_vendas_por_categoria.png)

**Hipótese 4: Descontos maiores estão negativamente correlacionados com o lucro.**
* **Resultado:** Confirmado. O gráfico de dispersão mostra que, a partir de um certo nível (geralmente acima de 20%), os descontos levam a prejuízo, especialmente na região Central.

![Gráfico Desconto vs. Lucro](graficos/h4_desconto_vs_lucro.png)

## 🚀 Conclusões e Próximos Passos

* **Foco Estratégico:** A empresa deve concentrar esforços de marketing e expansão na **região Oeste** e nos produtos da categoria de **Tecnologia**, mirando principalmente o segmento **Consumer**.
* **Política de Descontos:** A estratégia de descontos precisa ser revisada, pois descontos agressivos estão corroendo a lucratividade.
* **Engajamento de Clientes:** É crucial implementar campanhas de reativação para os clientes "Hibernando" e programas de fidelidade para os "Campeões" identificados na análise RFM.

## 🛠️ Como Executar o Projeto

1.  Clone este repositório: `git clone https://github.com/Ricksooon/analise-rfm-cohort-python.git`
2.  Navegue até o diretório do projeto.
3.  Instale as dependências necessárias: `pip install pandas matplotlib seaborn`
4.  Certifique-se de que os arquivos de dados (`orders.csv`, `customers.csv`, etc.) estão na pasta `dados/`.
5.  Execute os scripts de análise:
    ```bash
    python analise_exploratoria.py
    python analise_estrategica.py
    ```
6.  Os gráficos atualizados serão salvos na pasta `graficos/`.
