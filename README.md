# DESAFIO-OFICINA
Projeto DIO - Modelo conceitual de uma Oficina

Objetivo:
Criar um esquema conceitual para o contexto de oficina de veículos.

Narrativa:
Sistema de controle e gerenciamento de execução de ordens de serviço em uma oficina mecânica
Clientes levam veículos à oficina mecânica para serem consertados ou para passarem por revisões  periódicas
Cada veículo é designado a uma equipe de mecânicos que identifica os serviços a serem executados e preenche uma OS com data de entrega.
A partir da OS, calcula-se o valor de cada serviço, consultando-se uma tabela de referência de mão-de-obra
O valor de cada peça também irá compor a OSO cliente autoriza a execução dos serviços
A mesma equipe avalia e executa os serviços
Os mecânicos possuem código, nome, endereço e especialidade
Cada OS possui: n°, data de emissão, um valor, status e uma data para conclusão dos trabalhos.


Modelo conceitual:
Entidade Cliente: Com os atributos ID do cliente, nome e endereço.
Entidade Veículo: Com os atributos ID do veículo, modelo, placa e uma chave estrangeira para o cliente.
Entidade Mecânico: Com os atributos ID do mecânico, código, nome, endereço e especialidade.
Entidade Ordem de Serviço (OS): Com os atributos Número da OS, data de emissão, valor total, status, data de conclusão e chaves estrangeiras para o cliente e o veículo.
Entidade Serviço: Com os atributos ID do serviço, descrição, valor e tipo de mão-de-obra.
Entidade Peça: Com os atributos ID da peça, descrição e valor.
Relacionamentos:

Cliente e Veículo: Um cliente pode ter muitos veículos (1:N).
Veículo e Ordem de Serviço: Uma ordem de serviço está associada a um veículo (1:1).
Cliente e Ordem de Serviço: Uma ordem de serviço está associada a um cliente (1:1).
Mecânico e Serviço: Um mecânico pode executar muitos serviços (1:N).
Ordem de Serviço e Serviço: Uma ordem de serviço pode conter muitos serviços (1:N).
Ordem de Serviço e Peça: Uma ordem de serviço pode incluir muitas peças (1:N).

![MECÂNICA](https://github.com/matheusalx/DESAFIO-OFICINA/assets/15674874/6edd5d2a-8e06-4b26-a9b5-92c50725b463)
