# Desafio: Preveja os resultados de um e-commerce utilizando o Power BI

### Preveja os resultados de um e-commerce utilizando o Power BI

> Você irá aplicar os seus conhecimentos de Excel e PowerBI para construir um painel gerencial de um e-commerce que seja capaz de direcionar a uma análise de negócio para que a empresa defina as estratégias com o objetivo de aumentar as suas vendas. Também deverá estabelecer recomendações sobre como a empresa pode melhorar seus resultados.

### 🚨 Antes de iniciar, atente-se ao formato de entrega deste desafio!

1. Nomeie o seu dashboard com seu RID e o número do desafio. Exemplo: RID1234_Desafio01
2. No PowerBI, vá em Salvar Como > Arquivo .**pbix**
3. Submeta o arquivo .pbix em um drive
4. Altere as configurações do arquivo para deixá-lo público.
5. Copie o link após alterar a permissão de acesso.
6. Submeta o link do arquivo (e não da pasta do drive!) na plataforma.

**Contexto**
------------

Neste desafio, você deverá construir um painel gerencial para um e-commerce que almeja estudar as suas vendas e assim, traçar a melhor estratégia para alavancar seus resultados.Você receberá duas bases de dados, uma com dados das vendas e outra com informações dos clientes. Com isso, crie duas páginas para que os analistas possam visualizar as métricas.Crie as determinadas métricas: Quantidade total e valor total de vendas, Contagem e valor total de vendas por data, quantidade e valor total por categoria e crie os filtros necessários para fornecer ao usuário a melhor experiência. Lembrem-se do storytelling e de um bom layout para ser atrativo.

## **Detalhamento das tabelas:**

| Coluna            | Descrição                                      | Base         |
| ----------------- | ---------------------------------------------- | ------------ |
| idcompra          | numero de identificação da compra              | base compra  |
| idcanalvenda      | Canal de venda                                 | base compra  |
| bandeira          | Qual foi a bandeira que a compra foi realizada | base compra  |
| Data              | Data da compra                                 | base compra  |
| Preço             | Preço da compra                                | base compra  |
| Preço_com_frete   | Preço da compra + frete                        | base compra  |
| Nome_Departamento | Departamento do produto                        | base compra  |
| estado            | Estado da compra                               | base compra  |
| cliente_Log       | Identificação do cliente                       | base compra  |
| cliente_Log       | Identificação do cliente                       | Base cliente |
| Idade             | Idade do cliente                               | Base cliente |
| uf_nascimento     | Cidade de nascimento                           | Base cliente |
| Renda             | renda do cliente                               | Base cliente |

Dica de como deverá ficar
-------------------------

Utilize as imagens abaixo como base para se inspirar na construção e organização do seu dashboard

<img title="" src="https://dncgroupbr.notion.site/image/https%3A%2F%2Fs3-us-west-2.amazonaws.com%2Fsecure.notion-static.com%2F3ff02d3f-182f-4901-97c2-b2e0faebaf2f%2FUntitled.png?table=block&id=b49e2ef1-79e3-4825-a8b9-5a87302c8b24&spaceId=6a055055-52ec-4ebb-a697-63027c951344&width=1420&userId=&cache=v2" alt="">

<img title="" src="https://dncgroupbr.notion.site/image/https%3A%2F%2Fs3-us-west-2.amazonaws.com%2Fsecure.notion-static.com%2F4afc2ca3-5bc0-4974-81d0-483d09230119%2FUntitled.png?table=block&id=05cd389b-e22a-455b-92d9-227a466c3070&spaceId=6a055055-52ec-4ebb-a697-63027c951344&width=2000&userId=&cache=v2" alt="">

**Como começar?**
-----------------

Com base no contexto fornecido, é necessário criar dashboards para permitir que a equipe de negócios desenvolva planos de ação com o objetivo de aumentar o número de usuários cadastrados e impulsionar o crescimento da empresa.

1. Importe as duas bases para o Power BI
2. Crie uma coluna na base cliente de faixa de rendas, clusterizando entre os seguintes valores
   1. Até 10000
   2. Até 7500
   3. Até 5000
   4. Até 2500
   5. Até 1750
3. Crie 2 páginas: Visão do clientes e Visão Compra

🎯 Etapas de Desenvolvimento
============================

**Para te ajudar nesse processo, o PO do projeto pediu alguns gráficos para ter visibilidade do processo:**

**Etapa 01) Tipo de gráfico: Cartões**
--------------------------------------

Primeiro passo é analisar as tabelas recebidos no Excel, olhe as colunas, entenda os valores que possuem nela e a definição para o negócio

1. Crie um card de quantidade de vendas
2. Crie um card de valor total de vendas sem frete ($)
3. Crie um card de valor total de vendas com frete ($)
4. Crie um card de quantidade de clientes
5. Crie um card de média de renda dos clientes

**Etapa 02) Tipo de gráfico: Gráfico de linhas**
------------------------------------------------

1. Contagem de vendas por mês
2. Valor total de vendas por mês

**Etapa 03) Tipo de gráfico: Gráfico de Barras**
------------------------------------------------

1. Quantidade de vendas por categoria
2. Valor total de vendas por categoria
3. Distribuição de idades dos clientes
4. Distribuição de renda dos clientes

**Etapa 04) Filtro**
--------------------

1. Bandeira
2. Estado
3. Canal de venda
4. Departamento
5. Idade
6. Faixa de renda
7. Estado de nascimento

📝 Critérios de Avaliação
=========================

Os critérios de avaliação mostram como você será avaliado em relação ao seu desafio.

## **Critérios de Avaliação:**

| ****Critérios****           | **Atendeu às Especificações**                                                                                                                                                                                                        | ****Pontos**** |
| --------------------------- | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ | -------------- |
| **Tipo de gráfico: Cartão** | Elabore 5 gráficos tipo cartão utilizando as simbologias de moeda para representar indicadores financeiros                                                                                                                           | 20             |
| **Tipo de gráfico: Linhas** | Crie 2 gráficos de linhas, onde o eixo x deve ser uma série temporal (datas), representando tendências ao longo do tempo                                                                                                             | 30             |
| **Tipo de gráfico: Barras** | Crie 4 gráficos de barras: 2 gráficos comparando vendas por categoria (um em quantidade de vendas e outro em valor de vendas), 1 histograma de idades dos clientes, e 1 gráfico de barras para a distribuição de rendas dos clientes | 30             |
| **Filtro**                  | Crie filtros interativos para as seguintes categorias: bandeira, estado, canal de venda, departamento, idade, faixa de renda, e estado de nascimento                                                                                 | 20             |

📆 Entrega
==========

As informações necessárias para resolução do desafio estão no arquivo e também nessa instrução.

### 🚨 Atente-se ao formato de entrega deste desafio!

1. Nomeie o seu dashboard com seu RID e o número do desafio. Exemplo: RID1234_Desafio01
2. No PowerBI, vá em Salvar Como > Arquivo .**pbix**
3. Submeta o arquivo .pbix em um drive
4. Altere as configurações do arquivo para deixá-lo público.
5. Copie o link após alterar a permissão de acesso.
6. Submeta o link do arquivo (e não da pasta do drive!) na plataforma.

<img title="" src="https://file.notion.so/f/f/6a055055-52ec-4ebb-a697-63027c951344/c0a7cc62-ced2-4edb-84a2-c7ae96440337/EnviarDesafio.gif?table=block&id=0893e436-0a1e-4bef-ae05-a08db9043edf&spaceId=6a055055-52ec-4ebb-a697-63027c951344&expirationTimestamp=1771041585664&signature=Zqz8zswvL0DPkZYYCe4RfXTGAtwl3EBTIiFLriITG1A" alt="">
