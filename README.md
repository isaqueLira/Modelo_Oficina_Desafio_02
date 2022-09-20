# Desafio de Projeto 02 DIO - Modelo Oficina

### Projeto 02 do Bootcamp Database Experience da DIO.

## Obejetivo:
Criar o esquema conceitual para o contexto de oficina com base na narrativa fornecida.

## Narrativa:
* Sistema de Controle e gerenciamento de execução de **Ordens de Serviço** em uma **Oficina Mecânica**
* Clientes leva veículos à oficina mecânica para serem consertados ou para passarem por revisões períodicas
* Cada veículos é designado a uma equipe de mecânicos que identifica os serviços a serem executados e preenche uma OS com data de entrega
* A partir da OS, calcula-se o valor de cada serviço, consultando-se uma tabela de referência de mão-de-obra
* O valor de cada peça também irá compor a OS se o cliente autorizar a execução dos serviços
* A mesma equipe avalia e executa os serviços
* Os mecânicos possuem código, nome, endereço e especialidade
* Cada OS possui número, data de emissão, um valor, status e uma data para conclusão dos trabalhos.

## Interpretações:
* Os Clientes serão uma **Entidade** que possuem o **Relacionamento de Possuir** uma ou mais **Entidade Veículo**
* O Veículo (que terá o código do seu Poossuídor) solicitará uma OS descrevendo o Motivo (Nessa etapa será possível filtrar se será conserto ou revisões períodicas) que será um atributo da OS inicial
* A OS inicial será preenchida pela Equipe que possuem Mecânicos
* A OS de Execução será o resultado da OS inicial com a adição dos Serviços e/ou Peças
* A OS de Execução deverá ser Aprovada pelo Cliente, e a aprovação ficará no atributo Status (que poderá ser: Aguardando Aprovação, Aprovado e Encaminhado para Execução, em Execução, Finalizado, Cancelado, Reprovado)

