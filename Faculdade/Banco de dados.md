## Módulo 1

Para criar uma tabela num banco de dados relacional (SQL), é necessário seguir algumas regras, como:

* Devem ser usados nomes diferentes das palavras reservadas
* Informar tipo de dados
* Tamanho
* Constraints
---
### Tipos de dados:

Alguns tipos de dados mais famosos do banco PostgreSQL:

| Tipo| Descrição |
| --- | --- |
| CHAR | De tamanho fixo, guarda apenas um caractere |
| VARCHAR(n) | É possível definir o tamanho limite dentro de parênteres () após a definição do tipo |
| INTEGER | Tipo numérico que guarda números entre 2³¹ negativo e positivo |

---
### Constraints:

Constraints (Restrições) são palavras-chave que definem uma regra para alguma coluna da tabela, entre as principais existem:

* Primary Key
* Foreing Key
* Unique
* Not Null
* Check

#### Primary Key

Também é possível usar constraints compostas, como a Primary key:

```sql 
constraints product_id_pk PRIMARY KEY (id, name)
```

---

Exemplo de criação de uma tabela Products com uma primary key ID:

```sql
CREATE TABLE product 
(
	id LONG NOT NULL,
	name VARCHAR(60) NOT NULL,
	unit_price DOUBLE,
	CONSTRAINT product_id_pk PRIMARY KEY (id)
)
```