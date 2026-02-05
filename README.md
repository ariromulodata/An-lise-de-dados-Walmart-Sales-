# 📊 Quais fatores influenciam as vendas semanais das lojas do Walmart?

Para começar, é importante entender que o **Walmart não é uma entidade única**.  
Cada loja possui características próprias, e sua **geolocalização influencia diretamente o comportamento de compra**, gerando particularidades relevantes entre unidades.

Empresas que vendem produtos físicos precisam compreender o comportamento de seus clientes para:

- Otimizar estoque  
- Definir estratégias de marketing mais eficientes  
- Reduzir perdas  
- Maximizar faturamento  
- Prever sazonalidades  

Nesse contexto, a **análise de dados torna-se essencial** para apoiar decisões **baseadas em evidências**, e não apenas em intuição.

---

## 🎯 Objetivo da Análise

O objetivo desta análise é entender os **principais fatores que influenciam as vendas semanais das lojas do Walmart**, utilizando **dados históricos de vendas previamente tratados** do dataset.

### Objetivos específicos:

- Analisar o comportamento das vendas ao longo do tempo, identificando **padrões e sazonalidade**
- Comparar o desempenho entre lojas, identificando unidades **acima ou abaixo da média**
- Avaliar o **impacto de semanas com feriado** nas vendas
- Investigar a relação entre **variáveis externas** (temperatura, desemprego, preço do combustível) e o volume de vendas
- Gerar insights que apoiem decisões de **planejamento, estoque e estratégia comercial**
- Utilizar os insights para levantar **hipóteses** e, posteriormente, realizar **Testes de Hipóteses Estatísticas**

---

## 📂 Fonte dos Dados

- **Origem:** Kaggle  
- **Empresa:** Walmart  
- **Tipo:** Dados reais de varejo físico  
- **Descrição:** Vendas semanais por loja  

---

## 🗂️ Estrutura do Dataset

- **Quantidade de linhas:** 6.435  
- **Quantidade de colunas:** 8  

-Unidade de análise:
- Uma **loja** em uma **semana específica**

---

## 📊 Principais Variáveis

| Variável        | Descrição |
|-----------------|-----------|
| Store           | Identificador da loja |
| Date            | Semana da venda |
| Weekly_Sales    | Valor total vendido na semana (USD) |
| Holiday_Flag    | Indica se a semana contém feriado (0 = não, 1 = sim) |
| Temperature     | Temperatura média da semana (Fahrenheit) |
| Fuel_Price      | Preço médio do combustível |
| CPI             | Índice de Preços ao Consumidor |
| Unemployment    | Taxa de desemprego |

---

## 🔍 Metodologia

A análise foi conduzida seguindo o **fluxo padrão da Análise Exploratória de Dados (EDA)**.  
As etapas técnicas utilizadas são descritas a seguir.

### 1️⃣ Coleta e carregamento
- O dataset foi obtido no site **Kaggle**
- Os dados foram carregados em ambiente **Python**
- Utilizou-se a biblioteca **Pandas** para manipulação inicial, limpeza e preparação

---

### 2️⃣ Limpeza e preparação
Foram realizadas as seguintes verificações:

- Valores ausentes e nulos  
- Duplicidade de registros  
- Validação dos tipos de dados  

📌 **Observação:**  
Os dados apresentaram **boa qualidade**, não sendo necessária a remoção de registros.

---

### 3️⃣ Análise Exploratória
A análise buscou identificar **tendências e padrões** entre as variáveis, utilizando:

- Histogramas  
- Gráficos de barras  
- Gráficos de linha  
- Gráficos de dispersão  

---

### 4️⃣ Ferramentas e Tecnologias

- **Python** como linguagem principal de análise  
- **Pandas** para manipulação e análise de dados  
- **Matplotlib** para visualização dos gráficos  
- **Jupyter Notebook** como ambiente de desenvolvimento e execução da análise  

### Agora vamos ao que interessa. Os dados em gráficos e suas respectivas análises :

---<img width="570" height="449" alt="git" src="https://github.com/user-attachments/assets/c71ad62d-ab4b-4ffc-8250-65d05c4f0154" />
## 📊 Distribuição das Vendas Semanais

O gráfico apresenta a **distribuição das vendas semanais**, onde:

- O **eixo X** representa o valor de vendas por semana  
- O **eixo Y** representa a frequência  

### Principais Evidências

- Maior concentração de vendas entre **US$ 500 mil e US$ 1,5 milhão**
- **Eventos raros** com valores entre **US$ 2,5 milhões e US$ 3,5 milhões**
- Presença de **assimetria positiva** (cauda à direita)

📌 **Insight:**  
Os eventos atípicos na faixa de **US$ 2,5 a 3,5 milhões** tendem a **inflar a média geral**, tornando a mediana uma medida mais representativa do comportamento típico das vendas semanais.

