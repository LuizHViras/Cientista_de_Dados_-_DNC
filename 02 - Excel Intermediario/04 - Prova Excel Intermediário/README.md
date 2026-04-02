Prova 2: Excel Intermediário
============================

🎯 Objetivo
-----------

Avaliar domínio de Excel aplicado à análise de dados:

* Funções de agregação e busca
* Validação e padronização
* Modelagem de dados
* Tabelas e gráficos dinâmicos
* Boas práticas operacionais

****

🧠 Questões e Respostas
-----------------------

### 1.

**Enunciado:**  
Na aba Resumo Estoque, é necessário calcular o total de entradas de um produto com base no SKU registrado na célula A2, utilizando os dados da aba Entrada. Qual das fórmulas abaixo calcula corretamente o total de entradas para esse SKU?

**Alternativas:**

A) =SOMASE(Entrada!D:D;Entrada!B:B;A2)

=SOMASES(Entrada!D:D;Entrada!B:B;A2) ✅

C) =SOMASES(Entrada!B:B;A2;Entrada!D:D)

D) =PROCV(A2;Entrada!B:D;3;0)

* * *

### 2.

**Enunciado:**  
Na aba Resumo Estoque, é necessário calcular o Valor em Estoque de cada produto utilizando as quantidades da aba Entrada, as quantidades da aba Saída e o Preço da aba Cadastro. Sabendo que o SKU está na célula A2, qual fórmula calcula corretamente o Valor em Estoque?

**Alternativas:**

A) =(SOMASE(Entrada!A:A;A2;Entrada!C:C)-SOMASE(Saida!A:A;A2;Saida!C:C))*PROCV(A2;Cadastro!A:E;5;FALSO) ✅

B) =(SOMASE(Entrada!A:A;A2;Entrada!C:C)-SOMASE(Saida!A:A;A2;Saida!C:C))*PROCV(A2;Cadastro!A:E;4;FALSO)

C) =(SOMASE(Entrada!A:A;A2;Entrada!C:C)-SOMASE(Saida!A:A;A2;Saida!C:C))*PROCV(A2;Cadastro!A:E;5;VERDADEIRO)

D) =(SOMASE(Entrada!A:A;A2;Entrada!C:C)-SOMASE(Saida!A:A;A2;Saida!B:B))*PROCV(A2;Cadastro!A:E;5;FALSO)

* * *

### 3.

**Enunciado:**  
Em uma planilha de análise de estoque, a formatação condicional foi aplicada para destacar valores negativos automaticamente. Qual é a característica correta desse recurso?

**Alternativas:**

A) Ele modifica permanentemente os valores das células para refletir a condição aplicada.

B) Ele substitui a necessidade de fórmulas para identificar inconsistências nos dados.

C) Ele impede que valores fora do intervalo definido sejam inseridos na planilha.

D) Ele altera apenas a aparência das células com base em regras, sem modificar os dados originais. ✅

* * *

### 4.

**Enunciado:**  
Uma planilha utiliza validação de dados com lista suspensa para selecionar categorias de produtos. Qual é o principal benefício dessa prática em bases utilizadas para análise e relatórios?

**Alternativas:**

A) Reduz o tamanho do arquivo do Excel ao limitar o número de valores possíveis.

B) Garante padronização das informações inseridas, evitando variações que podem comprometer análises. ✅

C) Permite calcular automaticamente totais e médias por categoria.

D) Substitui a necessidade de utilizar tabelas dinâmicas para análise de dados.

* * *

### 5.

**Enunciado:**  
Na aba Resumo Estoque, é necessário criar a coluna Status do Produto com base no Saldo Atual (F2), utilizando as seguintes regras: Obsoleto → saldo = 0; Estoque Negativo → saldo < 0; Crítico → saldo entre 1 e 20; OK → saldo entre 21 e 100; Excesso → saldo > 100. Qual das fórmulas abaixo classifica corretamente os produtos de acordo com essas condições?

**Alternativas:**

A) =SES(F2<0;"Estoque Negativo"; F2=0;"Obsoleto"; E(F2>=1;F2<=20);"Crítico"; E(F2>=21;F2<=100);"OK"; F2>100;"Excesso") ✅

B) =SE(F2<=0;"Obsoleto"; SE(E(F2>=1;F2<=20);"Crítico"; SE(E(F2>=21;F2<=100);"OK"; "Excesso")))

C) =SES(F2<0;"Estoque Negativo"; F2=0;"Obsoleto"; F2<=20;"Crítico"; F2<=100;"OK"; F2>=100;"Excesso")

D) =SES(F2<0;"Estoque Negativo"; F2=0;"Obsoleto"; F2<=20;"Crítico"; F2>=100;"Excesso"; F2<=100;"OK")

* * *

### 6.

**Enunciado:**  
Qual é a principal finalidade de uma Tabela Dinâmica no Excel ao trabalhar com bases de dados estruturadas?

**Alternativas:**

A) Alterar automaticamente os valores da base de dados original para facilitar a análise.

B) Permitir reorganizar e resumir grandes volumes de dados em diferentes perspectivas sem alterar a base original. ✅

C) Substituir completamente o uso de fórmulas para cálculos em planilhas.

D) Impedir a edição de dados após a criação da análise.

* * *

### 7.

**Enunciado:**  
Uma Tabela Dinâmica foi criada a partir da aba Resumo Estoque para analisar o estoque por categoria de produto. O objetivo é identificar quanto dinheiro está imobilizado em estoque em cada categoria. Qual configuração da Tabela Dinâmica permite obter corretamente essa análise?

**Alternativas:**

A) Colocar SKU em Linhas e Categoria em Valores utilizando a agregação Contagem.

B) Colocar Valor em Estoque em Linhas e Categoria em Valores utilizando a agregação Média.

C) Colocar Categoria em Linhas e Valor em Estoque em Valores utilizando a agregação Soma. ✅

D) Colocar Preço em Valores utilizando a agregação Soma e Categoria em Filtros.

* * *

### 8.

**Enunciado:**  
Ao criar gráficos a partir de uma Tabela Dinâmica para compor um painel analítico, qual característica diferencia esse tipo de gráfico de um gráfico criado diretamente a partir de um intervalo comum de dados?

**Alternativas:**

A) O gráfico dinâmico impede que novos dados sejam adicionados à base original.

B) O gráfico dinâmico elimina a necessidade de atualizar os dados da planilha.

C) O gráfico dinâmico substitui completamente a Tabela Dinâmica utilizada na análise.

D) O gráfico dinâmico permanece conectado à Tabela Dinâmica e se atualiza automaticamente quando os dados da análise são atualizados.✅

* * *

### 9.

**Enunciado:**  
Em uma planilha grande utilizada para análise de dados, qual é a principal finalidade do recurso Congelar Painéis no Excel?

**Alternativas:**

A) Impedir que células específicas sejam editadas por outros usuários.

B) Permitir que determinadas linhas ou colunas permaneçam visíveis ao rolar a planilha. ✅

C) Bloquear o cálculo automático das fórmulas da planilha.

D) Fixar permanentemente os dados de uma tabela para evitar alterações.

* * *

### 10.

**Enunciado:**  
Ao trabalhar com diferentes planilhas contendo cadastro de produtos, entradas e saídas, qual prática é fundamental para garantir que os dados possam ser relacionados corretamente em análises no Excel?

**Alternativas:**

A) Manter todas as informações do produto repetidas em cada planilha para evitar o uso de fórmulas de busca.

B) Consolidar todas as informações em uma única planilha para reduzir a quantidade de abas no arquivo.

C) Utilizar um identificador único (como SKU) presente em todas as tabelas para permitir o relacionamento entre os dados. ✅

D) Utilizar cores e formatações diferentes para identificar visualmente os produtos em cada planilha.
