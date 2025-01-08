# Controle Financeiro
Projeto para criação de controle financeiro pessoal com uso de Python e Banco de Dados (SQLITELY).

[1.Tabelas](#tabelas)

**Desenvolvedor**-Ronisio Xavier Junior  
**Início do Projeto** - Janeiro/2025.


## Tabelas

### 1.cartoes

> Tabela para armazenamento dos dados de cartões de crédito do usuário. 

|Campo|Tipo|Detalhe|
|---|---|---|
|**ID_CARTAO**|PK INTEGER|Chave autonumerada|
|**BANDEIRA** |TEXT |Bandeira do Cartão de Crédito Cadastrado|
|**PORTADOR** | TEXT | Nome do portador do cartão|
| **EMISSOR** | TEXT | Nome da instituição emissora do cartão|
|**LIMITE**   | REAL |Valor do limite do cartão|

### 2.categoria

> Tabela para cadastramento de categorias e subcategorias de gastos.

|Campo|Tipo|Detalhe|
|---|---|---|
|ID_CATEGORIA| PK INTEGER| Chave autonumerada|
|CATEGORIA|TEXT| Categoria de Gasto |
|SUB_CATEGORIA| TEXT | Subcategoria do gasto|

### 3.desp_cartoes

> Tabela para cadastramento de despesas realizadas no cartão de crédito.

|Campo|Tipo|Detalhe|
|---|---|---|
|ID_DESP_CARTOES|PK INTEGER| Chave autonumerada|
|DT_DESP_CARTOES|TEXT|Data da realização da despesa|
|VALOR|REAL|Valor da despesa.|
|VENCIMENTO|TEXT| Data do vencimento|
|PARCELA | TEXT | Identificação da parcela|
|CREDOR | TEXT | Credor |
|DESCRICAO | TEXT | Descricao do Gasto|
|ID_CATEGORIA | FK INTEGER | Chave estrangeira - Categoria |
|ID_CARTAO | FK INTEGER | Chave estrangeira - Subcategoria |


### 4.desp_debito_cta

> Tabela para cadastramento de despesas realizadas em conta-corrente.

|Campo|Tipo|Detalhe|
|---|---|---|
|ID_DESP_CTA|PK INTEGER| Chave autonumerada|
|DT_DESP_CTA|TEXT|Data da realização da despesa|
|VALOR|REAL|Valor da despesa.|
|VENCIMENTO|TEXT| Data do vencimento|
|PARCELA | TEXT | Identificação da parcela|
|CREDOR | TEXT | Credor |
|DESCRICAO | TEXT | Descricao do Gasto|
|ID_CATEGORIA | FK INTEGER | Chave estrangeira - Categoria |

### 5.orcamento

> Tabela para cadastramento dos valores orçados para cada categoria


|Campo|Tipo|Detalhe|
|---|---|---|
|ID_ORCAMENTO|PK INTEGER|Chave Primária autonumerada|
|ID_CATEGORIA|FK INTEGER|Chave estrangeira - Categoria|
|MES_REF|INTEGER|Identificação do mês|
|ANO_REF|INTEGER|Identificação do ano|


