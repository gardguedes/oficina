# Desafio: Criar um esquema conceitual do zero.

## Descrição do Desafio
Criar o esquema conceitual para o contexto de oficina.

## Narrativa
Objetivo: Sistema de controle e gerenciamento de execução de ordens de serviço em uma oficina mecânica.

- Clientes levam veículos à oficina mecânica para serem consertados ou para passarem por revisões  periódicas;
- Cada veículo é designado a uma equipe de mecânicos que identifica os serviços a serem executados e preenche uma OS com data de entrega;
- A partir da OS, calcula-se o valor de cada serviço, consultando-se uma tabela de referência de mão-de-obra;
- O valor de cada peça também irá compor a OS;
- O cliente autoriza a execução dos serviços;
- A mesma equipe avalia e executa os serviços;
- Os mecânicos possuem código, nome, endereço e especialidade;
- Cada OS possui: n°, data de emissão, um valor, status e uma data para conclusão dos trabalhos;
- Uma OS pode ser composta por vários serviços e um mesmo serviço pode estar contido em mais de um OS;
- Uma OS pode ter vários tipos de peça e uma peça pode estar presente em mais de uma OS.

## Entidades
- Ordem de serviço
- Cliente
- Veículo
- Equipe
- Mecânicos
- Mão-de-obra
- Peças
- Fornecedor

## Considerações e Decisões de Modelagem
- Avaliando a narrativa e o objetivo do desafio, como cada Ordem de Serviço (OS) pode ter vários serviços e peças, optei por criar as entidades SERVIÇO e PEÇAS para ter informações separadas dos itens e seus respctivos valores.
- Outra entidade considerada foi EQUIPE, pois vários mecânicos podem compor uma equipe, que atenderá um ou mais OS. Sendo assim necessário estabeler esses relacionamentos, entre mecânicos, equipe e OS.
- Por fim, acrescentei a entidade FORNECEDOR que se relaciona com PEÇAS. Pois essas serão adquiridas de várias origens, sendo possível ter mais de um fornecedor para um peça e várias peças com o mesmo fornecedor.

## Resolução do Desafio
![Modelo conceitual do banco de oficina mecânica](https://github.com/user-attachments/assets/97efb115-b786-4cac-8bea-d53de21ead67)
