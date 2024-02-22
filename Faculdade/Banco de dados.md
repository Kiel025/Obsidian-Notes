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

```sql
select last_name "Ultimo nome", 
	department_id "Codigo do Depto",
	job_id "Codigo do cargo" 
from employees 
where 
	department_id in (
	select department_id from departments where location_id= 1 700
	);
```

```sql
select first_name,
	job_id,
	salary
from employees
where salary > (select avg(salary) from employees);
```

```sql
select employee_id, manager_id, first_name, last_name
from employees
where employee_id
```

## Cursores e Procedures
* PL/SQL é uma linguagem de programação da Oracle feita para processar as informações do banco de dados junto com o SQL
* Cursores são áreas compostas de linhas e colunas (matriz) na memória usadas para armazenar as informações vindas de uma query que retornam 0 ou mais linhas
* Stored Procedure é um subprograma armazenado no servidor

#### PL/SQL

Estrutura do PL/SQL

```plsql
DECLARE /* (Opcional)
+ Declara variáveis, cursores, constantes, tabelas, estruturas, exceptions */

BEGIN /* (Obrigatório)
+ SQL statements
+ PL/SQL statements */ 

EXCEPTION /* (Opcional)
+ Ações que deverão ser executadas quando ocorrer erros */

END; /* (Obrigatório) */
```