### Challenge
📊 Desafio para Ciências de Dados - Projeto de Análise das Lojas — Alura Store


### 🏪 Comparação entre 4 Lojas  
Este projeto realiza uma análise completa de desempenho das quatro lojas da Alura Store, com base em dados fictícios de vendas.  
O objetivo é ajudar o **Sr. João** a decidir **qual loja deve ser vendida**. Para isso, analisamos indicadores como:

💰 Faturamento

⭐ Avaliação dos clientes

🚚 Frete médio

📦 Categorias de produtos mais vendidos

🔝 Produtos mais populares

📈 Visualizações com Matplotlib

🧮 Cálculo de Score de desempenho relativo

---

# 🚀 Requisitos
- Analisar os dados das lojas
- Criar gráficos para visualização
- Apresentar uma recomendação

---


# 📂 Estrutura da base de dados
  As quatro lojas possuem dados padronizados com as colunas:
- Produto
- Categoria do Produto
- Preço
- Frete
- Data da Compra
- Vendedor
- Local da compra
- Avaliação da compra
- Tipo de pagamento
- Quantidade de parcelas
- lat
- lon


---

## 📊 3. Análises Realizadas

### 🔸 **Faturamento por loja**
Calculado com base em:

### 🔸 **Avaliação Média dos Clientes**
Escala de 1 a 5 ⭐.

### 🔸 **Frete Médio**
Avaliação comparativa da eficiência logística.

### 🔸 **Produtos mais vendidos**
Top 5 por loja.

### 🔸 **Categorias mais lucrativas**
Faturamento por categoria.

### 🎨 **Visualizações criadas**
- 📌 Gráfico de barras → Faturamento  
- 📌 Gráfico de pizza → Categorias  
- 📌 Gráfico de dispersão → Preço × Avaliação  
- 📌 Boxplot de frete (extra)

---

## 🧮 4. O que é o *Score_ruim*?  
*(Mais alto = pior desempenho)*

O **Score_ruim** combina 3 fatores:

### ➤ 📉 1. Faturamento Relativo
Score_Faturamento = (Faturamento_max - Faturamento_loja) / Faturamento_max


### ➤ ⭐ 2. Avaliação Média Relativa
Score_Avaliação = (Avaliação_max - Avaliação_loja) / Avaliação_max


### ➤ 🚚 3. Frete Médio Relativo
Score_Frete = Frete_loja / Frete_max


### 🧩 Score Final
Score_ruim = Score_Faturamento + Score_Avaliação + Score_Frete


Quanto **maior**, pior o desempenho.

---

## 📝 5. Ranking do Score_ruim

| Loja | Score_ruim | Interpretação |
|------|------------|----------------|
| 🟥 Loja 1 | **1.017** | 🚨 Pior desempenho geral |
| 🟧 Loja 4 | 1.012 | Faturamento menor, mas avaliação um pouco melhor |
| 🟨 Loja 2 | 1.002 | Desempenho equilibrado |
| 🟩 Loja 3 | 0.999 | Melhor eficiência geral |

---

## 🧠 6. Por que a Loja 1 é a pior, mesmo com maior faturamento?

✔️ Ela possui:  
- ⭐ **Menor avaliação média** (3.98)  
- 🚚 **Maior frete médio** (34.69)

Esses dois fatores **pesam muito negativamente**, mesmo com faturamento alto.

### ✔️ O faturamento pode estar mascarando problemas:
- Insatisfação do cliente  
- Logística cara  
- Operação pouco eficiente  

### ✔️ E a diferença pequena de avaliação em relação à Loja 4?
Mesmo que pequena, **a Loja 4 tem frete menor**, e isso melhora seu score relativo.

---

## 🛑 7. Recomendação Final — Qual loja vender?

# 👉 **O Sr. João deve vender a Loja 1.**

### 🧨 Motivos principais:
1️⃣ **Maior Score_ruim entre todas** (pior desempenho relativo)  
2️⃣ **Avaliação mais baixa dos clientes**  
3️⃣ **Frete médio mais alto**  
4️⃣ **Faturamento alto, mas com baixa eficiência**  
5️⃣ **Demais lojas possuem desempenho mais equilibrado**

---


# 🧠 Como funciona o *Score_ruim*?

O **Score_ruim** é uma métrica criada para identificar a loja com o pior desempenho relativo.  
Ele combina três indicadores principais:  
✔ Faturamento  
✔ Avaliação média  
✔ Frete médio  

Quanto **maior** o Score_ruim, **pior** a loja está se saindo no geral.

### 🧮 Fórmula
- **Faturamento ruim** = (Faturamento_Máx - Faturamento_Loja) / Faturamento_Máx  
- **Avaliação ruim** = (Avaliação_Máx - Avaliação_Loja) / Avaliação_Máx  
- **Frete ruim** = Frete_Loja / Frete_Máx  
- **Score final** = soma dos 3 componentes  

---

# 📉 Interpretação dos Scores

| Loja | Score_ruim | Interpretação |
|------|------------|--------------|
| **Loja 1** | **1.018** | 📉 *Pior desempenho relativo* |
| **Loja 4** | **1.012** | ⚠ Próxima da pior |
| **Loja 2** | **1.002** | 👍 Desempenho saudável |
| **Loja 3** | **0.999** | 🟢 Melhor desempenho |

---

# 🏁 📌 **Recomendação Final — Qual loja vender?**

Depois da análise aprofundada:

### 🔥 **A Loja 1 é a pior no desempenho relativo e recomenda-se ser vendida.**

Mesmo com alto faturamento, ela apresenta:
- ⭐ **Menor avaliação média (3.98)**  
- 🚚 **Frete médio mais alto entre as lojas (34.69)**  
- ⚠ Problemas aparentes de operação e satisfação  
- 💸 Ineficiências que não acompanham o volume de vendas  

A pequena diferença de avaliação entre Loja 1 e Loja 4 **não** é suficiente para salvá-la:  
➡ A combinação de *menor avaliação + maior frete* a torna a mais problemática no conjunto geral.

---

# 📊 Outros Insights do Projeto
- A Loja 3 é a mais equilibrada  
- A Loja 2 tem o melhor custo-benefício para o cliente  
- A Loja 4 vende pouco, mas opera com custos menores  
- A Loja 1 vende muito, mas deixa clientes mais insatisfeitos

---

# 🛠 Tecnologias Usadas
- Python 🐍  
- Pandas  
- Matplotlib  
- Jupyter Notebook  

---

# 📘 Como Executar o Projeto
```bash
# 1. Clone o repositório
git clone https://github.com/seuusuario/seurepo.git

# 2. Entre na pasta
cd seurepo

# 3. Instale as dependências
pip install -r requirements.txt

# 4. Execute o script principal
python analise_lojas.py


