🛒 Projeto — Dashboard Gerencial de E-commerce (Power BI)
=========================================================

📌 Visão Geral
--------------

Este projeto consiste na construção de um dashboard gerencial em Power BI a partir de bases de vendas e clientes, com foco em análise de performance comercial e perfil da base de consumidores.

O objetivo é transformar dados brutos em um painel analítico que permita exploração interativa e suporte à tomada de decisão.

* * *

## 🖼️ Preview

<img title="" src="https://raw.githubusercontent.com/LuizHViras/Cientista_de_Dados_-_DNC/refs/heads/main/01%20-%20Introdução%20a%20Análise%20de%20Dados/05%20-%20Desafio%20-%20Preveja%20Resultados%20E-commerce/Imagens/Prints%20Dash%20Final/Visão%20Compras.png" alt="Visão Compras">

<img title="" src="https://raw.githubusercontent.com/LuizHViras/Cientista_de_Dados_-_DNC/refs/heads/main/01%20-%20Introdução%20a%20Análise%20de%20Dados/05%20-%20Desafio%20-%20Preveja%20Resultados%20E-commerce/Imagens/Prints%20Dash%20Final/Visão%20Cliente.png" alt="Visão Cliente">

<img title="" src="https://raw.githubusercontent.com/LuizHViras/Cientista_de_Dados_-_DNC/refs/heads/main/01%20-%20Introdução%20a%20Análise%20de%20Dados/05%20-%20Desafio%20-%20Preveja%20Resultados%20E-commerce/Imagens/Prints%20Dash%20Final/Relacionamentos%20Tabelas.png" alt="Relacionamento Tabelas">

***

🧩 Modelagem e Preparação dos Dados
-----------------------------------

### 🔹 Bases utilizadas

* **Base Compra**

* **Base Cliente**

* **Base UF** (Origem: https://pt.wikipedia.org/wiki/Unidades_federativas_do_Brasil ; Acesso em: 15/02/2026)

### 🔹 Tratamento realizado (Power Query)

* Padronização dos nomes das colunas

* Ajuste de tipos de dados

* Correção de inconsistências (ex: “Mobil” → “Mobile”)

* Ajuste de campos geográficos para uso em mapas

### 🔹 Enriquecimento do modelo

Foi adicionada uma tabela auxiliar de **UF (Unidades Federativas)** para melhorar análises geográficas.

### 🔹 Tabelas Dimensão criadas

* d Canal Venda

* d Nome Departamento

* d Faixa Renda

* d UF

### 🔹 Estrutura do Modelo

* Relacionamento entre compras e clientes via `Cliente Log`

* Modelo orientado a dimensões para melhor performance e organização

* Separação clara entre fatos e dimensões

* * *

📊 Dashboard — Visão Compras
----------------------------

Página destinada ao acompanhamento da performance de vendas.

### KPIs (Cards)

* Quantidade de Compras

* Valor Total (Sem Frete)

* Valor Total (Com Frete)

* Última Compra

* * *

### Visualizações

#### 📈 Gráfico de Linha

* Eixo X: Data

* Eixo Y: KPI selecionada

* Objetivo: análise temporal e identificação de tendência

#### 📊 Gráfico de Colunas

* Canal de venda vs KPI

* Objetivo: comparação de performance entre canais

#### 🍩 Gráfico de Rosca

* Distribuição por bandeira

* Objetivo: visualizar participação relativa dos meios de pagamento

#### 🗺️ Mapa

* Estado da venda

* Tamanho da bolha proporcional à KPI selecionada

* Objetivo: identificar concentração geográfica das vendas

* * *

### Interatividade

Foi criado um **parâmetro de seleção de medidas**, permitindo alternar dinamicamente entre:

* Preço

* Preço com Frete

* Valor do Frete

* Quantidade de Compras

Essa abordagem reduz poluição visual e melhora a experiência do usuário.

* * *

👥 Dashboard — Visão Cliente
----------------------------

Página focada em perfil e distribuição da base de clientes.

### KPIs (Cards)

* Quantidade de Clientes

* Média de Renda

* Média de Idade

* * *

### Transformações

* Criação da coluna **Faixa de Renda** para segmentação dos clientes.

* * *

### Visualizações

#### 📈 Gráfico de Linha

* Idade vs Quantidade de Clientes

* Objetivo: observar distribuição etária

#### 📊 Gráfico de Colunas

* Faixa de renda vs Quantidade de Clientes

* Objetivo: identificar concentração econômica da base

#### 🗺️ Mapa

* Localização dos clientes por estado

* Objetivo: análise geográfica da base cadastrada

* * *

🎨 Decisões de Layout e Design
------------------------------

* Paleta consistente entre páginas (Branco, Azul e Azul Petróleo)

* Cards posicionados no topo para leitura executiva rápida

* Área dedicada para filtros

* Mesma identidade visual entre as duas visões para consistência

* * *

🔎 Principais Técnicas Aplicadas
--------------------------------

* Power Query para limpeza e padronização

* Modelagem dimensional

* Criação de medidas DAX

* Parâmetro de seleção de métricas

* Uso de visualizações orientadas ao tipo de análise

* Storytelling visual por páginas

* * *

📈 Resultado Final
------------------

O dashboard permite:

* Monitorar performance de vendas

* Comparar canais e categorias

* Identificar concentração geográfica

* Analisar perfil etário e econômico dos clientes

* Explorar dados com filtros dinâmicos

* * *

🧠 Aprendizados do Projeto
--------------------------

* Organização de modelos com tabelas dimensão

* Importância da padronização de dados antes da análise

* Uso de parâmetros para reduzir complexidade visual

* Estruturação de dashboards por contexto de negócio 
