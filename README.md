# Opsistock

Copie o código abaixo e cole no seu arquivo README.md.
Markdown
#  OptiStock Enterprise

![Status](https://img.shields.io/badge/status-concluído-brightgreen?style=flat-square)
![Python](https://img.shields.io/badge/python-3.9%2B-blue?style=flat-square)
![React](https://img.shields.io/badge/react-18-61DAFB?style=flat-square&logo=react)
![Math](https://img.shields.io/badge/math-SymPy%20%7C%20Calculus-orange?style=flat-square)

> **Sistema de Inteligência de Supply Chain** desenvolvido para otimização de custos, precificação dinâmica e gestão de risco, utilizando **Cálculo Diferencial** e dados reais de varejo.

---
# Descrição
O projeto propõe uma solução para empresas que apresentam dificuldade na presificação de seus produtos, Ele serve como apoio para a tomada de decisões gerenciais, sendo projetado para auxiliar as empresas na definição de preços de venda. Seu objetivo é ajudar na determinação do preço ótimo, permitindo escolhas mais estratégicas e eficientes.

---

## O Motor Matemático
Diferente de sistemas tradicionais com fórmulas estáticas ("hardcoded"), nosso backend utiliza a biblioteca `SymPy` para realizar **Cálculo Simbólico em tempo real**.

### 1. Otimização de Estoque (EOQ)
Buscamos o **Custo Mínimo Global** analisando a função de Custo Total ($TC$).
* **1ª Derivada:** $TC'(Q) = 0$ (Encontra os pontos críticos).
* **2ª Derivada:** $TC''(Q) > 0$ (Confirma a concavidade positiva/sorriso, provando que é um ponto de mínimo e não de máximo).

### 2. Precificação Inteligente
Maximização da função Lucro ($L$) encontrando o ponto onde a Receita Marginal iguala o Custo Marginal.
* **Prova Real:** Validação via concavidade negativa ($\cap$) para garantir o lucro máximo.

### 3. Gestão de Risco Estocástica
Utilizamos a Distribuição Normal (Z-Score) aplicada sobre o desvio padrão real das vendas ($\sigma$) para calcular o Estoque de Segurança dinâmico.

---

## Tecnologias Utilizadas

| Área | Tecnologias |
| :--- | :--- |
| **Backend** | Python 3.9+, FastAPI, Uvicorn |
| **Data Science** | Pandas (ETL), NumPy, SymPy (Math Core), SciPy |
| **Frontend** | React.js, TailwindCSS, Recharts (Data Viz) |
| **Database** | SQLite (Persistência Leve), CSV Dataset Processing |

---

## Como Rodar o Projeto

Siga os passos abaixo para executar a aplicação localmente.

## 1. Abra o terminal dentro da pasta backend

cd C:\Users\Pichau\Desktop\optistock\backend

## 2. Instale dependências

pip install fastapi uvicorn pandas numpy sympy scipy python-multipart

## 3. Rode o backend

Aperte em " Run "

## 4. Abra outra janela do terminal e vá para o frontend

cd C:\Users\Pichau\Desktop\optistock\frontend

## Estrutura do Projeto
```
Plaintext
/
├── backend/
│   ├── app/
│   │   ├── main.py          # Entry point da API
│   │   ├── clean_engine.py  # Motor matemático & Processamento do CSV
│   │   └── database.py      # Conexão SQLite
│   └── data/
│       └── OnlineRetail.csv # Dataset Transacional
├── frontend/
│   ├── src/
│   │   ├── components/      # Componentes UI (Cards, Gráficos)
│   │   └── App.js           # Lógica da Interface
└── README.md
```

Validação com Dados Reais
O sistema foi validado utilizando o dataset Online Retail (UCI Machine Learning Repository). O algoritmo ingere 500.000+ transações, agrupa vendas por SKU, remove inconsistências e calcula a volatilidade real para recomendações precisas.

```
Projeto desenvolvido para o curso de Ciência da Computação (CESUPA).
[Everton Gustavo] - Backend & Math
[Filipe Cesar] - Frontend & UI
[Ian Carlos] - Data Analysis
```

