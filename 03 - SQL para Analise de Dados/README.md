📊 SQL para Análise de Dados
-------------------------------------

* * *

🎯 Visão Geral
---------------------

Este módulo aborda o uso de **SQL (Structured Query Language)** como ferramenta central para **extração, manipulação e análise de dados em bancos relacionais**, além da conexão com práticas de **Business Intelligence (BI)**.

O objetivo não é só escrever queries, mas **gerar informação acionável** para tomada de decisão.

***

🧩 Fundamentos do SQL
-----------------------------

### 🔹 O que é SQL?

SQL é a linguagem padrão para interação com bancos de dados relacionais, essencial para extrair valor dos dados armazenados. Após modelar tabelas e relacionamentos, ela permite:

* Consultar dados

* Filtrar informações

* Agregar métricas

* Relacionar tabelas

* Preparar dados para análise e visualização
  
  ***

### 🔹 Estrutura de uma Query SQL

    SELECT coluna
    FROM tabela
    WHERE condição
    ORDER BY coluna
    LIMIT n

**Ordem lógica de execução:**

1. FROM
2. WHERE
3. GROUP BY
4. HAVING
5. SELECT
6. ORDER BY
7. LIMIT

***

🔍 1. Consultas Básicas
-----------------------

### 🔹 Seleção de dados

    SELECT
        nome,
        preco
    FROM produtos;

### 🔹 Filtragem

    SELECT *
    FROM pedidos
    WHERE valor > 100;

### 🔹 Ordenação

    SELECT *
    FROM produtos
    ORDER BY preco DESC;

### 🔹 Limitação

    SELECT *
    FROM produtos
    LIMIT 10;

* * *

📊 3. Agregações e Análise
--------------------------

 Funções de agregação permitem transformar dados brutos em métricas:

| Função | Descrição |
| ------ | --------- |
| COUNT  | Contagem  |
| SUM    | Soma      |
| AVG    | Média     |
| MAX    | Máximo    |
| MIN    | Mínimo    |

### Exemplo:

    SELECT
        user_id,
        COUNT(*)
    FROM compras
    GROUP BY user_id;

### 🔹 GROUP BY

Agrupa dados para análise:

```
SELECT
    categoria,
    SUM(valor)
FROM vendas
GROUP BY categoria;
```

### 🔹 HAVING (filtro pós-agrupamento)

    SELECT
        categoria,
        SUM(valor)
    FROM vendas
    GROUP BY categoria
    HAVING SUM(valor) > 1000;

👉 Diferença crítica:

* WHERE → antes da agregação
* HAVING → depois da agregação

* * *

🔗 4. Relacionamento entre Tabelas (JOINs)
------------------------------------------

### Conceito central

Relacionar dados de diferentes tabelas usando **chaves**:

* **Primary Key (PK)** → identifica registros únicos
* **Foreign Key (FK)** → conecta tabelas

📌 Exemplo do material (_página 19_):  
Tabela `compras` usa `user_id` para identificar o cliente correspondente.

* * *

### Tipos de JOIN

| Tipo       | Descrição                           |
| ---------- | ----------------------------------- |
| INNER JOIN | Apenas correspondências             |
| LEFT JOIN  | Tudo da esquerda + correspondências |
| RIGHT JOIN | Tudo da direita + correspondências  |
| FULL JOIN  | Tudo de ambas                       |

### Exemplo:

    SELECT
        c.nome,
        cp.valor
    FROM clientes c
    INNER JOIN compras cp
    ON c.id = cp.user_id;

### ⚠️ Erro comum

JOIN sem condição → **cartesian explosion** (multiplica linhas)

* * *

🧠 5. Joins Avançados e Modelagem Mental
----------------------------------------

### 🔹 Joins subsequentes

Encadeamento de múltiplas tabelas:

```
SELECT *
FROM pedidos p
JOIN clientes c
    ON p.cliente_id = c.id
JOIN produtos pr
    ON p.produto_id = pr.id;
```

* * *

🏗️ 6. CTEs (Common Table Expressions)
--------------------------------------

### 🔹 O que são

CTEs são consultas temporárias reutilizáveis que melhoram:

* Legibilidade
* Organização
* Manutenção

```
WITH vendas_por_cliente AS (
    SELECT
        cliente_id,
        SUM(valor) AS total
    FROM vendas
    GROUP BY cliente_id
)

SELECT *
FROM vendas_por_cliente
WHERE total > 1000;
```

### 🔹 Quando usar

* Queries complexas
* Reuso de lógica
* Melhorar legibilidade

* * *

🔤 7. Funções SQL
-----------------

### 🔹 Operadores Comuns

* `=`, `>`, `<`, `>=`, `<=`
* `BETWEEN`
* `IN`
* `LIKE`

### 🔹 Texto

* `UPPER()`, `LOWER()`
* `CONCAT()`
* `TRIM()`

### 🔹 Datas

* `DATE()`
* `EXTRACT()`
* `CURRENT_DATE`

### 🔹 Numéricas

* `ROUND()`
* `ABS()`

* * *

🧪 8. Análises Mais Avançadas
--------------------

### Casos comuns:

* Top N produtos (Ordenação + filtro)
* Análise temporal (Fltro + decomposição da data)
* Métricas por segmento (Filtro)
* Ranking (Agrupamento + ordenação)

* * *

📊 9. Boas Práticas em Análise
-------------------------------

----------------------------

### 🔹 Filtragem eficiente

Evite analisar datasets inteiros sem necessidade.

### 🔹 Combinação de filtros

Exemplo:

* Data + preço + avaliação

### 🔹 Iteração

* Explorar → filtrar → analisar → refinar

### 🔹 Exportação

* Use CSV/Excel quando necessário para análises complementares

📊 10. Métricas de Negócio
--------------------------------------

Exemplos de métricas de negócio:

* Receita por período
* Produtos mais vendidos
* Clientes ativos
* Ticket médio
* Conversão
1. analista

* * *

🚀 Conclusão
------------

SQL não é só linguagem, é ferramenta estratégica e, com ele, as possibilidades são praticamente infinitas.

Dominar SQL significa:

* Entender dados
* Conectar informações
* Gerar insights
* Influenciar decisões




