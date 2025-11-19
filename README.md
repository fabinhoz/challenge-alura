# Challenge 📊 

## Data Science: Projeto de Análise das Lojas — Alura Store
---

### 🏪 Objetivo  
Este projeto apresenta uma análise completa de desempenho das quatro lojas da Alura Store, utilizando dados fictícios de vendas (um arquivo de base de dados .CSV por loja).
O objetivo é orientar o Sr. João na decisão estratégica sobre qual unidade deverá ser vendida para viabilizar um novo empreendimento.

Para isso, foi avaliado um conjunto de indicadores-chave que refletem eficiência comercial, satisfação do cliente e desempenho operacional, incluindo:

💰 Faturamento

⭐ Avaliação dos clientes

🚚 Frete médio

📦 Categorias de produtos mais vendidos

🔝 Produtos mais populares

📈 Visualizações com Matplotlib

🧮 Cálculo de Score de desempenho relativo


Essa análise integrada permite identificar, de forma objetiva, qual loja apresenta menor eficiência e é a melhor candidata para ser vendida.

---

### 📘 Aprendizagem

Este projeto também serve como prática dos principais conceitos de Ciência de Dados com Python, incluindo:

🐍 Manipulação de dados com Pandas

📊 Criação de visualizações utilizando Matplotlib

📑 Carregamento, limpeza e tratamento de arquivos CSV

📈 Análise de métricas essenciais, como faturamento, avaliações, desempenho operacional e categorias mais vendidas

🔍 Interpretação de resultados para apoiar decisões de negócio

---

### 🚀 Requisitos do Desafio

Para concluir a análise, foi necessário:

📥 Carregar e analisar os datasets das quatro lojas 

📊 Produzir gráficos para apoiar a interpretação visual dos dados

🧠 Gerar insights baseados em métricas de desempenho

📝 Apresentar uma recomendação final para o Sr. João sobre qual loja vender

---

### 📂 Estrutura da Base de Dados

Cada uma das quatro lojas possui um dataset padronizado com as seguintes colunas:
#### Lojas: [loja_1](datasets/loja_1.csv), [loja_2](datasets/loja_2.csv), [loja_3](datasets/loja_3.csv), [loja_4](datasets/loja_4.csv)

* Produto
* Categoria do Produto
* Preço
* Frete
* Data da Compra
* Vendedor
* Local da compra
* Avaliação da compra
* Tipo de pagamento
* Quantidade de parcelas
* lat (latitude)
* lon (longitude)

---

### 📊 Análises Realizadas

O projeto explora cada loja a partir de indicadores essenciais de desempenho comercial e operacional:

#### 🔸 Faturamento por Loja

Cálculo da receita total para identificar quais unidades geram maior retorno financeiro.

#### 🔸 Avaliação Média dos Clientes

Média das avaliações na escala de 1 a 5 estrelas, refletindo a satisfação dos consumidores.

#### 🔸 Frete Médio

Comparação direta do custo logístico entre as lojas para avaliar eficiência e competitividade.

#### 🔸 Produtos Mais Vendidos

Ranking dos Top 5 produtos de cada loja, revelando preferências e padrões de consumo.

#### 🔸 Categorias Mais Lucrativas

Análise do faturamento segmentado por categoria para identificar os nichos mais fortes.

---

### 🎨 Gráficos Gerados

Para apoiar a interpretação dos dados, foram produzidas diferentes gráficos:


![Gráfico - Faturamento](assets/faturamento_total_por_loja.png)


![Gráfico - Média das avalações](assets/media_avaliacao.png)


![Gráfico - Top 5 vendas por categoria mais vendidas](assets/top5_categorias_mais_vendidas_todas_lojas.png)


![Gráfico - As 3 vendas por categoria menos vendidas](assets/top3_categorias_menos_vendidas_todas_lojas.png)


![Gráfico - Preco_x_avaliacao](assets/faturamento_x_avaliacao_media.png)

---

### 🧠 O que é e como funciona o Score_ruim?

O **Score_ruim** é uma métrica criada para identificar, de forma simples e objetiva, qual loja apresenta o pior desempenho relativo.

Ele combina três fatores essenciais do negócio:

### 💰 Faturamento

### ⭐ Avaliação média dos clientes

### 🚚 Frete médio

Quanto **maior** o Score_ruim, **pior** é o desempenho geral.


### 🧮 Fórmula
O cálculo é feito padronizando cada métrica e somando seus “pesos negativos”:

- **Faturamento ruim** = (Faturamento_Máx - Faturamento_Loja) / Faturamento_Máx  
- **Avaliação ruim** = (Avaliação_Máx - Avaliação_Loja) / Avaliação_Máx  
- **Frete ruim** = Frete_Loja / Frete_Máx  
- **Score final** = soma dos 3 componentes  

---

### 📉 Interpretação dos Scores

| Loja | Score_ruim | Interpretação |
|------|------------|--------------|
| **Loja 1** | **1.018** | 📉 *Pior desempenho relativo* |
| **Loja 4** | **1.012** | ⚠ Operação fraca, mas com frete menor |
| **Loja 2** | **1.002** | 👍 Desempenho saudável e equilibrado |
| **Loja 3** | **0.999** | 🟢 Melhor desempenho |

---

### 🏁 📌 **Recomendação Final — Qual loja vender?**

Depois da análise aprofundada:
Recomenda-se que o Sr. João venda a Loja 1. Mesmo que ela tenha o maior faturamento, isso não significa saúde operacional.
O Score_ruim revela problemas importantes:

### 🔥 **A Loja 1 é a pior no desempenho relativo e recomenda-se ser vendida.**

Mesmo com alto faturamento, ela apresenta:
1. ⭐ Menor avaliação média entre as lojas (3.98)
2. 🚚 Maior frete médio (34.69)
3. 💸 Alto faturamento, mas com ineficiência operacional
4. 😟 Sinais claros de insatisfação dos clientes
5. 📉 Desempenho relativo que não se sustenta no longo prazo

A diferença pequena de avaliação em relação à Loja 4 não compensa o frete muito mais alto — isso puxa o score para baixo de maneira decisiva.

A pequena diferença de avaliação entre Loja 1 e Loja 4 **não** é suficiente para salvá-la:  
➡ A combinação de *menor avaliação + maior frete* a torna a mais problemática no conjunto geral.

---

### 📊 Outros Insights do Projeto
- A Loja 3 é a mais equilibrada  
- A Loja 2 tem o melhor custo-benefício para o cliente  
- A Loja 4 vende pouco, mas opera com custos menores  
- A Loja 1 vende muito, mas deixa clientes mais insatisfeitos

---

### 🛠 Tecnologias Usadas
- Python 🐍  
- Pandas  
- Matplotlib  
- Jupyter Notebook
- Google Colab  

---

### 📂 Diretórios
```bash

challenge-alura/
│
├── assets/
│   ├── faturamento_total_por_loja.png
│   ├── faturamento_x_avaliacao_media.png
│   ├── media_avaliacao.png
│   ├── top3_categorias_menos_vendidas_todas_lojas.png
│   └── top5_categorias_mais_vendidas_todas_lojas.png
│
├── datasets/
│   ├── loja_1.csv
│   ├── loja_2.csv
│   ├── loja_3.csv
│   └── loja_4.csv
│
├── outputs/
│   ├── resumo_lojas.csv
│   └── top_produtos_lojas.csv
│
├── Challenge_alura.ipynb
└── README.md
```
---

## 📖 Autor
Fábio Zinetti
<https://github.com/fabinhoz>
