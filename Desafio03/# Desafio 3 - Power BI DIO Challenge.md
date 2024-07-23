# Desafio 3 - Power BI DIO Challenge

dados carregados
- Renomeado os cabeçalhos para melhor compreensão dos dados
- Identificado colaborador James sem gerente, ou seja, Super_ssn nulo
- Identificado que o colaborador James é gerente dos outros dois gerentes, no caso, o Franklin, e a Jennifer
- Ficou entendido que o James é o superior máximo, então, ele foi definido como seu próprio gerente, ou seja, o campo Super_ssn foi preenchido com seu próprio Ssn

- Foi criado uma nova tabela, usando a mescla da tabela employee com a propria tabela employee, com intuito de separar apenas os gerentes, para isso, na primeira referência da tabela, foi selecionada a coluna Ssn, e na segunda referência, a coluna Super_ssn, onde a mescla era executada a partir da segunda referência, retornando assim, apenas os gerentes.

Foram excluidas as colunas desnecessárias, ficando apenas os nomes e o campo Ssn, no qual ficou definida como chave estrangeira do campo Super_ssn na tabela employee.

Sendo assim, é possivel verificar em um gráfico de árvore, os colaboradores que são gerentes e seus respectivos subordinados.

Foi verificado que cada departamento tem 1 gerente responsável, dado que está sendo exibido em uma **TreeMap**

Feita a junção da localidade do departamento com o nome do departamento, deixando-os como únicos.

Foi usado a mesclagem de employee com a propria tabela employee, para definir para cada employee qual é o seu gerente responsável.

* Foi utilizado a mescla que busca a referência do registro na outra tabela e retorna os dados no mesmo registro
* Não é possivel utilizar a atribuição pois, diferente da mescla, ela retorna os dados em uma nova linha, onde as colunas referente a primeira tabela ficqm com __valores null__

Criado gráfico de horas dos colaboradores por projeto, além de outro gráfico com as horas totais usadas em cada projeto.

Criado um gráfico com salários de cada colaborador, que indica o James com o salário mais alto, confirmando ser o encarregado superior da empresa.