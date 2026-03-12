# 📊 Olist E-commerce: Análise de 360º de Operações e Fidelidade

Este projeto consiste em uma **Análise Exploratória de Dados (EDA)** profunda no dataset da Olist (maior marketplace do Brasi). O objetivo foi transformar dados brutos em inteligência logística, financeira e estratégica para otimizar a operação e entender o comportamento de consumo.

[![Kaggle](https://img.shields.io/badge/Kaggle-Dataset-20BEFF?style=for-the-badge&logo=kaggle&logoColor=white)](https://www.kaggle.com/datasets/olistbr/brazilian-ecommerce)

---

## 🛠️ Tecnologias e Metodologia
* **Linguagem:** Python
* **Bibliotecas:** Pandas, Seaborn, Matplotlib, NumPy
* **Engenharia de Dados:** Implementação de um **Pipeline Master** (Super Merge) unindo 6 tabelas (Pedidos, Itens, Produtos, Reviews, Clientes e Tradução) em um único DataFrame otimizado.
* **Rigor Estatístico:** Tratamento de outliers utilizando o método **IQR (Interquartile Range)** em variáveis críticas como Preço, Frete e Tempo de Entrega, garantindo que as análises reflitam a realidade operacional.

---

## 🚀 Insights das 5 Perguntas de Negócio

### 1. Logística: A Psicologia do Prazo
**Pergunta:** Como a antecedência de entrega impacta a satisfação?
* **Insight:** Identificamos uma estratégia de **Expectativa Conservadora**. A Olist estica o prazo para estados distantes (como o **Acre**, que recebe em média **20 dias antes** do previsto). Isso gera surpresas positivas que blindam a satisfação. Em estados com prazos mais "reais" (como **Alagoas**, ~8 dias de folga), as notas são significativamente menores.

### 2. Financeiro: A "Armadilha do Frete" (Freight Trap)
**Pergunta:** Qual o peso do frete no bolso do cliente e como isso trava as vendas?
* **Insight:** Criamos a métrica `is_freight_trap` para fretes que superam **40% do valor total**. Categorias como "Casa e Conforto" frequentemente caem nesta zona, resultando em volumes de vendas baixíssimos. O frete não é apenas um custo, é um **bloqueador de conversão**.

### 3. Operacional: Vendedor vs. Transportadora
**Pergunta:** Vendedores rápidos garantem notas melhores?
* **Insight:** **A logística pesa 2x mais que o vendedor.** A correlação negativa entre tempo de transporte e nota é o dobro da do tempo de postagem. O cliente é muito mais punitivo com o atraso do caminhão do que com a demora do vendedor para embalar o produto.

### 4. Estratégico: A Elite de Pareto
**Pergunta:** Como o faturamento está concentrado entre os vendedores?
* **Insight:** O faturamento não é movido por quem vende "baratinho". Os **Top 10%** dos vendedores controlam a maior fatia do faturamento vendendo itens com ticket médio **36% superior** ao restante da base. Confiança e valor agregado vencem a guerra de preços.

### 5. CRM: Onde Mora a Fidelidade?
**Pergunta:** Quais categorias trazem o cliente de volta?
* **Insight:** A fidelidade é movida por **projetos e reposição**. Categorias como "Cama, Mesa e Banho" e "Beleza & Saúde" lideram a recompra. O cliente retorna para completar enxovais ou repor itens consumíveis, mostrando o caminho para estratégias de retenção (LTV).

---

## 📈 Conclusão Geral
O projeto prova que a **Logística é o principal motor de satisfação**, mas o **Frete é a maior barreira de crescimento**. Para escalar em regiões distantes, a recomendação estratégica é a regionalização de estoques para reduzir o custo logístico e aumentar a competitividade em itens de ticket médio baixo.

---

### Como reproduzir
1. Clone o repositório.
2. Certifique-se de ter os arquivos `.csv` originais na pasta raiz.
3. Execute o notebook para visualizar o pipeline de tratamento e os gráficos gerados.
