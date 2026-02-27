Aula — Primeiras Análises - Excel
==========================================================



Este documento reúne os principais conceitos, funções e recursos trabalhados na aula, com foco em **organização, sumarização e visualização de dados**. O objetivo é consolidar o entendimento prático do Excel como ferramenta de análise, indo além do uso mecânico das fórmulas.

* * *

➕ Função SOMA e a diferença para a soma manual
----------------------------------------------

A função **SOMA** é utilizada para somar valores numéricos de forma automática dentro de um intervalo ou entre valores específicos.

`SOMA(valor1; [valor2]; …)`

**Diferença para soma manual:**

* Soma manual (`=A1+A2+A3`) é **estática** e frágil: qualquer alteração no intervalo exige edição da fórmula.

* `SOMA(A1:A10)` é **dinâmica**, escalável e reduz erros humanos.

* A função permite trabalhar com **intervalos grandes**, células não consecutivas e atualização automática ao inserir novos dados.

* * *

➕ Função SOMA.SE
----------------

A função **SOMA.SE** permite somar valores **com base em um critério**, sendo essencial para análises segmentadas.

`SOMA.SE(intervalo; critério; [intervalo_soma])`

Exemplo:

`SOMA.SE(A2:A10; "SP"; B2:B10)`

Nesse caso:

* `A2:A10` → intervalo onde o critério é avaliado

* `"SP"` → critério

* `B2:B10` → valores que serão somados

* * *

🔢 Função CONT.SE
-----------------

A função **CONT.SE** conta quantas células atendem a um determinado critério.

`CONT.SE(intervalo; critério)`

Exemplo:

`CONT.SE(A2:A10; "Aprovado")`

* * *

🔢 Função CONT.VALORES
----------------------

A função **CONT.VALORES** conta células **não vazias**, independentemente do tipo de dado.

`CONT.VALORES(valor1; [valor2]; …)`

Exemplo:

`CONT.VALORES(A2:A10)`

Diferença importante:

* `CONT` → conta apenas números

* `CONT.VALORES` → conta qualquer conteúdo (texto, número, data)

* * *

🔍 Função PROCV
---------------

A função **PROCV** é utilizada para buscar um valor em uma tabela e retornar uma informação relacionada.

`PROCV(valor_procurado; matriz_tabela; núm_coluna; [procurar_intervalo])`

Exemplo:

`PROCV(101; A2:C10; 3; FALSO)`

Funcionamento:

* Busca o valor **na primeira coluna** da tabela

* Retorna o valor correspondente de outra coluna

* `FALSO` garante correspondência exata

Limitação importante:

* Só busca da **esquerda para a direita**

* Depende da estrutura da tabela

* * *

📅 Funções ANO e MÊS
--------------------

Essas funções extraem partes específicas de uma data.

### ANO

`ANO(data)`

Exemplo:

`ANO("15/03/2024") → 2024`

### MÊS

`MÊS(data)`

Exemplo:

`MÊS("15/03/2024") → 3`



* * *

🧹 Remover duplicadas e sumarização de dados
--------------------------------------------

O recurso **Remover Duplicatas** elimina registros repetidos com base em uma ou mais colunas.

Uso comum:

* Limpeza de bases

* Garantir unicidade (ex: clientes, IDs)

Fluxo típico trabalhado na aula:

1. Remover duplicadas para garantir dados únicos

2. Utilizar `SOMA.SE`, `CONT.SE` e `CONT.VALORES`

3. Gerar tabelas resumidas e métricas consolidadas

Esse processo simula uma **pré-agregação**, muito comum antes de análises mais avançadas.

* * *

📊 Gráficos
-----------

### Gráfico de Barras

* Comparação entre categorias

* Ideal para ranking e volumes

### Gráfico de Linha

* Evolução ao longo do tempo

* Muito usado para séries temporais

### Gráfico de Pizza

* Representação proporcional

* Uso recomendado apenas com poucos elementos

### Gráfico de Mapa

* Visualização geográfica

* Análise por região, estado ou país

Os gráficos servem para **comunicar insights**, não apenas para “embelezar” dados.

* * *

📑 Tabela Dinâmica
------------------

A **Tabela Dinâmica** permite resumir grandes volumes de dados rapidamente, sem fórmulas complexas.

Principais recursos:

* Agrupamento automático

* Soma, contagem, média

* Segmentação por filtros

Uso típico:

* Análises exploratórias

* Consolidação rápida de métricas

* Base para dashboards

* * *

📈 Gráfico Dinâmico
-------------------

O **Gráfico Dinâmico** é a representação visual da tabela dinâmica.

Vantagens:

* Atualização automática

* Interatividade

* Facilidade para análise gerencial

É a ponte entre **análise** e **comunicação de resultados**.
