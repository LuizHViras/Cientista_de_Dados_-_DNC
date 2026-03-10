Desafio: Organize os dados de um negócio com Excel
==========

**Contexto - Introdução**
-------------------------

Você acaba de ingressar como analista de dados na LLC Eletronics e recebeu sua primeira missão: **estruturar e apresentar uma análise completa do estoque** da empresa.

Atualmente, o controle de estoque está espalhado em planilhas separadas, dificultando o acompanhamento. Sua entrega será um **painel visual, consolidado e estratégico**, que permitirá ao time de operações tomar decisões com base em dados.

> ⚠️ Estoque negativo representa quando há mais saídas do que entradas de um produto. Isso pode indicar erro de registro, venda sem reposição ou problemas logísticos.

###### 💡Dicas:

- A melhor maneira de dar doublecheck no sistema é utilizando as planilhas no Excel.

- Se você fechar o arquivo sem salvar, segue o caminho para recuperação: C:\Users\NOME DO USUARIO\AppData\Local\Temp\Microsoft Vá manualmente até essa pasta em até 15 minutos, caso contrário, poderá perder tudo.

A planilha contém três abas:

* `Cadastro`: produtos com SKU, nome, descrição, categoria e preço.
* `Entrada`: registros de entrada no estoque por produto e data.
* `Saída`: registros de saída do estoque por produto e data.

🎯 Etapas de Desenvolvimento
============================

Para te ajudar nesse processo, dono do mercado sugeriu dividir essa tarefa em 4 etapas:

### Etapa 01 – Relacionamento entre dados

1. Crie uma nova aba chamada `Resumo Estoque`.
2. Liste em três colunas (SKU, Categoria e Preço) da aba `Cadastro`.
3. Para cada produto, calcule em cada coluna:
   * Some o total de entradas;
   * Some o total de saídas;
   * Saldo atual = entradas − saídas;
   * Valor em estoque = saldo × preço.

###### 💡Dica:  Use SOMASES e PROCV

### Etapa 02 – Classificação por status de estoque

Adicione uma coluna chamada **Status do Produto** utilizando o Saldo Atual, aplicando a seguinte lógica:

* `Obsoleto`: estoque 0;
* `Estoque Negativo`: saldo < 0;
* `Crítico`: saldo entre 1 e 20;
* `OK`: saldo entre 21 e 100;
* `Excesso`: saldo acima de 100.

###### 💡Dica:  Utilize funções como SES (IFS), E, OU

### Etapa 03 – Formatação condicional

Aplique formatação condicional destacando em **vermelho** os valores em estoque **negativos**.

* Destaque também:
  * Colunas de valor (formate como moeda R$).
  * Valores em verde positivos
  * Valores igual a zero em azul

### Etapa 04 – Validação e estrutura

* Crie listas suspensas com validação de dados na coluna Categoria.
* Congele a primeira linha e a primeira coluna da aba `Resumo Estoque`.
* Organize visualmente a aba: alinhe colunas, ajuste larguras e padronize os títulos.

### **Etapa 05) Tabela dinâmica**

Crie uma Tabela Dinâmica em uma nova aba chamada `Painel`, com as seguintes análises:

* Valor total em estoque por categoria;
* Quantidade de SKUs por categoria;
* Preço médio por categoria.
* Quantidade de Total de Saídas por categoria

###### 💡Dica: Use a aba Resumo Estoque como fonte e certifique-se de atualizar os dados caso altere qualquer fórmula.

### **Etapa 06) Gráficos interativos**

Com base na Tabela Dinâmica da etapa anterior, crie os **seguintes três gráficos analíticos**:

###### 💡Dica: Todos esses dados já existem na Tabela Dinâmica. Use rótulos claros, cores consistentes e organize os gráficos de forma visualmente limpa na aba Painel.

📝 Critérios de Avaliação
=========================

Os critérios de avaliação são as conclusões das etapas propostas de acordo com os critérios abaixo.
