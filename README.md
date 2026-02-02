# 📊 Website Traffic & Engagement Analysis

![Python](https://img.shields.io/badge/Python-3.11-blue?style=for-the-badge&logo=python&logoColor=white)
![Pandas](https://img.shields.io/badge/Pandas-Data_Analysis-150458?style=for-the-badge&logo=pandas&logoColor=white)
![Seaborn](https://img.shields.io/badge/Seaborn-Visualization-4c72b0?style=for-the-badge&logo=python&logoColor=white)

## 📌 Introdução
Este projeto consiste em uma análise exploratória de dados (EDA) focada em **Marketing Digital e Comportamento do Usuário**. 

O objetivo principal é entender não apenas o volume de tráfego de um site, mas a **qualidade** desse tráfego. Através da manipulação de dados brutos, buscamos responder perguntas cruciais de negócio: *Qual canal traz mais usuários? Quem retém mais a atenção? Qual o melhor horário para postar conteúdo?*

> **Nota:** Este projeto foi desenvolvido como prática de análise de dados com Python, baseando-se no case "Website Data Analysis" do canal *The iScale*, com personalizações e análises estratégicas adicionais focadas em Business Intelligence.

---

## 💼 Contexto do Negócio
Imagine uma empresa que investe pesado em diversos canais de marketing (Redes Sociais, Google, E-mail, Vídeos), mas não tem clareza sobre o retorno real desses investimentos.

O problema central é a **"Ilusão do Volume"**:
* Muitos gestores olham apenas para o número de visitas (Sessões).
* Porém, visitas que não geram engajamento (usuários que entram e saem em segundos) são custos, não lucros.

**O desafio:** Transformar uma tabela bruta de logs de acesso (com datas, horas e categorias) em insights acionáveis para otimizar a estratégia de conteúdo, focando em reter o usuário e não apenas atraí-lo.

---

## 🛠️ Metodologia e Ferramentas
Para resolver esse problema, foi utilizado o ecossistema Python para Ciência de Dados. O fluxo de trabalho seguiu as etapas de um projeto real de Analytics:

1.  **Coleta e Carregamento (ETL):** Importação de dados brutos em formato `.csv`.
2.  **Limpeza de Dados (Data Cleaning):**
    * Tratamento de cabeçalhos inconsistentes.
    * Conversão de tipos de dados (Casting) para `datetime` e `float`.
    * Remoção de valores nulos e dados irrelevantes.
3.  **Engenharia de Atributos (Feature Engineering):**
    * Extração da hora do dia (`Hour`) a partir do timestamp completo para análise de sazonalidade horária.
    * Criação da métrica de "Sessões Não Engajadas" para comparação de qualidade.
4.  **Análise Exploratória (EDA):**
    * Análise de Séries Temporais (Tendências diárias).
    * Comparação categórica entre canais de aquisição.
    * Análise de Correlação com Mapas de Calor (Heatmaps).

**Tech Stack:**
* **Python:** Linguagem base.
* **Pandas:** Manipulação e agregação de dados.
* **Matplotlib & Seaborn:** Visualização de dados estática e estatística.

---

## 🔍 Principais Insights de Negócio

### 1. Qualidade vs. Quantidade
Descobrimos que, embora as Redes Sociais tragam volume, o **Organic Video** retém a atenção do usuário **3x mais**.
![Tempo de Engajamento](images/tempo_engajamento_por_canal.png)

### 2. O Mito da "Diluição de Qualidade"
Nossa análise estatística (`Pearson R=0.31`) provou que **aumentar o tráfego NÃO reduz a qualidade**. Horários de pico trazem usuários altamente engajados, validando o investimento em escala.
![Correlação Volume x Qualidade](images/correlacao_volume_vs_qualidade.png)

### 3. Sazonalidade e Timing
O "horário nobre" do site é surpreendente: picos de acesso ocorrem à **Meia-Noite**, sugerindo um comportamento noturno do público-alvo.
![Heatmap de Horários](images/heatmap_trafego_hora_canal.png)

---

## 🚀 Acesse o Projeto Completo

Quer ver o código passo a passo, a limpeza dos dados e a geração dos gráficos? Clique no botão abaixo para acessar o Notebook.

[![Acessar Notebook](https://img.shields.io/badge/Acessar_Notebook_Completo-Jupyter-F37626?style=for-the-badge&logo=jupyter&logoColor=white)](/notebooks/01_analise_exploratoria.ipynb)

*(Caso o botão não funcione, navegue até o arquivo `.ipynb` na lista de arquivos acima)*