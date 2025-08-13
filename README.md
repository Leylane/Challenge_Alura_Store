# 📊 Análise de Desempenho das Lojas – Alura Store

![Python](https://img.shields.io/badge/Python-3.10+-blue?logo=python)
![Jupyter](https://img.shields.io/badge/Jupyter-Notebook-orange?logo=jupyter)
![License](https://img.shields.io/badge/License-MIT-green)

[![Abrir no Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/Leylane/Challenge_Alura_Store/blob/main/notebooks/AluraStoreBr.ipynb)

Este projeto realiza uma análise detalhada de dados de vendas, desempenho e avaliações de quatro lojas fictícias da **Alura Store**, com o objetivo de identificar qual delas apresenta menor eficiência e recomendar a melhor opção para venda.

---

## 📌 Objetivo

Ajudar o proprietário de uma rede de lojas a decidir qual loja vender para iniciar um novo empreendimento, utilizando métricas de faturamento, satisfação dos clientes, custo de frete e perfil de produtos vendidos.

---

## Estrutura do projeto e organização dos arquivos
    Challenge_Alura_Store/
    ├─ notebooks/
    │  └─ AluraStoreBr.ipynb          # Notebook principal com a análise
    ├─ Database/
    │  ├─ loja_1.csv
    │  ├─ loja_2.csv
    │  ├─ loja_3.csv
    │  └─ loja_4.csv                   # Dados de cada loja
    ├─ img/                            # imagens exportadas dos gráficos
    │  ├─ grafico_faturamento.png
    │  ├─ comparativo_lojas.png
    │  ├─ media_avaliacoes.png
    │  ├─ mais_menos_vendidos.png
    │  └─ custo_frete.png
    |
    └─ README.md

---

## Exemplos de gráficos e insights obtidos
- **Faturamento por loja (barras verticais):** evidencia a Loja 4 com a menor receita total.  
  Exemplo: `img/grafico_faturamento.png`
- **Categorias mais vendidas (agrupamento de barras):** dominância de Móveis e Eletrônicos nas vendas.  
  Exemplo: `img/comparativo_lojas.png`
- **Média das avaliações por loja (barras horizontais):** leve destaque da Loja 3 (~4,05).
  Exemplo: `img/media_avaliacoes.png`
- **Mais e menos vendidos por loja (barras horizontais):** identifica produtos campeões e de baixa saída em cada loja.  
  Exemplo: `img/mais_menos_vendidos.png`
- **Custo médio de frete (dot plot):** Loja 4 com menor frete, sem impacto positivo no faturamento.  
  Exemplo: `img/custo_frete.png`

**Principais insights:**
- Loja 4: menor faturamento e avaliação mediana; portfólio com menos itens de alta rotatividade.  
- Loja 3: melhor média de avaliação dos clientes.  
- Frete: vantagem de custo na Loja 4 não se converteu em maior receita.  
- Categorias: Móveis e Eletrônicos lideram em todas as lojas.

---

## Instruções para executar o notebook

### Opção A) Executar no Google Colab (recomendado)
1) Clique no botão **“Abrir no Colab”** no topo deste README.  
2) Execute as células do notebook `notebooks/AluraStoreBr.ipynb`.  
3) Leitura dos dados no Colab (duas opções):

- **Direto do GitHub (raw)**:
~~~python
import pandas as pd
base = "https://raw.githubusercontent.com/Leylane/Challenge_Alura_Store/refs/heads/main/Database/"
loja1 = pd.read_csv(f"{base}/loja_1.csv")
loja2 = pd.read_csv(f"{base}/loja_2.csv")
loja3 = pd.read_csv(f"{base}/loja_3.csv")
loja4 = pd.read_csv(f"{base}/loja_4.csv")
~~~

- **Upload manual dos CSVs**:
~~~python
from google.colab import files
uploaded = files.upload()  # selecione os 4 arquivos CSV
~~~

> Dependências mínimas no Colab (rodar em uma célula no início do notebook):
~~~python
!pip -q install pandas matplotlib
~~~

### Opção B) Executar localmente (Jupyter Notebook)
1) Clone o repositório:
~~~bash
git clone https://github.com/Leylane/Challenge_Alura_Store.git
cd Challenge_Alura_Store
~~~

2) (Opcional) Crie e ative um ambiente virtual:
~~~bash
python -m venv .venv
# Windows
.venv\Scripts\activate
# macOS/Linux
source .venv/bin/activate
~~~

3) Instale as dependências:
~~~bash
pip install pandas matplotlib jupyter
~~~

4) Inicie o Jupyter e abra o notebook:
~~~bash
jupyter notebook notebooks/AluraStoreBr.ipynb
~~~

5) Garanta que os caminhos dos CSVs apontem para a pasta `data/`.  
   Para reprodutibilidade, você pode fixar versões:
~~~bash
pip install "pandas==2.2.2" "matplotlib==3.9.0"
~~~

---


