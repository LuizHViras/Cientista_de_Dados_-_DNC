📦 Análise de Estoque – LLC Eletronics
======================================

📊 Visão Geral
--------------

Neste projeto, desenvolvi uma solução completa em Excel para **estruturação, consolidação e análise de estoque** da empresa fictícia **LLC Eletronics**.

O cenário inicial consistia em dados distribuídos em múltiplas planilhas, sem integração, dificultando:

* controle de entradas e saídas

* visibilidade do saldo por produto

* identificação de inconsistências

* análise gerencial

A solução entregue foi um **dashboard interativo**, permitindo análise rápida e suporte à tomada de decisão.

* * *

🧠 Abordagem
============

A construção foi baseada em três pilares:

* **Modelagem estruturada dos dados**

* **Automação de cálculos**

* **Visualização analítica**

A arquitetura foi organizada em camadas:

1. **Base de dados** → tabelas estruturadas

2. **Resumo** → consolidação e cálculos

3. **Pivot** → agregações analíticas

4. **Dashboard** → visualização e interação

* * *

🗂️ Estrutura dos Dados
=======================

As planilhas originais foram transformadas em tabelas estruturadas:

* `tb_Entrada` → (Data, SKU, Produto, Quantidade)
  
  <img title="Tabela Entrada" src="https://raw.githubusercontent.com/LuizHViras/Cientista_de_Dados_-_DNC/refs/heads/main/02%20-%20Excel%20Intermediario/03%20-%20Desafio%20-%20Organize%20os%20Dados%20de%20um%20Negocio%20com%20Excel/Imagens/Tabela%20Entrada.png" alt="Tabela Entrada">

* `tb_Saida` → (Data, SKU, Produto, Quantidade)
  
  <img title="Tabela Saida" src="https://raw.githubusercontent.com/LuizHViras/Cientista_de_Dados_-_DNC/refs/heads/main/02%20-%20Excel%20Intermediario/03%20-%20Desafio%20-%20Organize%20os%20Dados%20de%20um%20Negocio%20com%20Excel/Imagens/Tabela%20Saida.png" alt="Tabela Saida">

* `tb_Cadastro` → (SKU, Produto, Descrição, Categoria, Preço)
  
  <img title="Tabela Cadastro" src="https://raw.githubusercontent.com/LuizHViras/Cientista_de_Dados_-_DNC/refs/heads/main/02%20-%20Excel%20Intermediario/03%20-%20Desafio%20-%20Organize%20os%20Dados%20de%20um%20Negocio%20com%20Excel/Imagens/Tabela%20Cadastro.png" alt="Tabela Cadastro">

Essa abordagem garante:

* escalabilidade

* consistência

* atualização automática
  
  

* * *

🔄 Consolidação do Estoque
==========================

Criada a aba **Resumo Estoque** (`tb_Resumo`) com base no cadastro de produtos.
Cálculos principais:

--------------------

**Quantidade de Entradas**

=SOMASES(tb_Entrada[Quantidade]; tb_Entrada[SKU]; [@SKU])

**Quantidade de Saídas**

=SOMASES(tb_Saida[Quantidade]; tb_Saida[SKU]; [@SKU])

**Saldo Atual**

=[@Qntd Entradas] - [@Qntd Saídas]

**Valor em Estoque**

=[@Saldo Atual] * [@Preço]

<img title="Tabela Resumo Estoque" src="https://raw.githubusercontent.com/LuizHViras/Cientista_de_Dados_-_DNC/refs/heads/main/02%20-%20Excel%20Intermediario/03%20-%20Desafio%20-%20Organize%20os%20Dados%20de%20um%20Negocio%20com%20Excel/Imagens/Tabela%20Resumo%20Estoque.png" alt="Tabela Resumo Estoque">

* * *

🔗 Relacionamento de Dados
==========================

Para garantir consistência:

* A coluna **SKU** foi definida como chave principal

* Aplicada **validação de dados** baseada na `tb_Cadastro`

* Utilizado `PROCX` para buscar:
  
  * Categoria
  
  * Preço

Isso evita inconsistências e elimina preenchimento manual redundante.

* * *

🚨 Classificação de Estoque
===========================

Criação da coluna **Status do Produto** com base no saldo:

| Condição  | Status           |
| --------- | ---------------- |
| Saldo < 0 | Estoque Negativo |
| Saldo = 0 | Obsoleto         |
| 1 a 20    | Crítico          |
| 21 a 100  | OK               |
| > 100     | Excesso          |

* * *

🎨 Formatação e Usabilidade
===========================

* Formatação condicional aplicada ao **Saldo Atual**:
  
  * 🔴 negativo
  
  * 🔵 zero
  
  * 🟢 positivo

* Valores financeiros formatados em **R$ (contábil)**

* Congelamento de linhas e colunas

* Padronização visual da tabela

* * *

📊 Camada Analítica (Tabelas Dinâmicas)
=======================================

Foram criadas três tabelas dinâmicas com objetivos distintos:

<img title="Tabelas Dinamicas" src="https://raw.githubusercontent.com/LuizHViras/Cientista_de_Dados_-_DNC/refs/heads/main/02%20-%20Excel%20Intermediario/03%20-%20Desafio%20-%20Organize%20os%20Dados%20de%20um%20Negocio%20com%20Excel/Imagens/Tabelas%20Dinamicas.png" alt="Tabelas Dinamicas">

* * *

`din_Saldo_Atual`
-----------------

**Análise operacional por categoria**

* Entradas

* Saídas

* Saldo

* * *

`din_Status_Estoque`
--------------------

**Distribuição dos produtos por status**

* Contagem de SKUs

* Classificação de risco

* * *

`din_Preco_Medio`
-----------------

**Análise financeira**

* Preço médio por categoria

* * *

📈 Dashboard Interativo
=======================

Criada a aba **Dashboard**, contendo visualizações conectadas às tabelas dinâmicas.

<img title="Dashboard - Controle Estoque" src="https://raw.githubusercontent.com/LuizHViras/Cientista_de_Dados_-_DNC/refs/heads/main/02%20-%20Excel%20Intermediario/03%20-%20Desafio%20-%20Organize%20os%20Dados%20de%20um%20Negocio%20com%20Excel/Imagens/Dashboard%20-%20Controle%20Estoque.png" alt="Dashboard - Controle Estoque">
🎛️ Filtros interativos

-----------------------

* Categoria

* Status do Estoque

* * *

📌 KPIs principais
------------------

* 💰 **Valor Total em Estoque**

* ⚠️ **% de SKUs Críticos**

* ❌ **Quantidade de SKUs Negativos**

* * *

📊 Visualizações
----------------

### Controle de Estoque

* Comparação entre:
  
  * entradas
  
  * saídas
  
  * saldo

* Segmentado por categoria

* * *

### Status do Estoque

* Distribuição de produtos por:
  
  * negativo
  
  * crítico
  
  * ok
  
  * excesso

* * *

### Preço Médio

* Comparação de preços entre categorias

* * *

🧩 Principais Insights Possíveis
================================

O dashboard permite identificar rapidamente:

* categorias com maior volume de estoque

* concentração de produtos em estado crítico

* presença de inconsistências (estoque negativo)

* diferenças de preço entre categorias
