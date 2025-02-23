## Relacionamentos
Cliente - Veículo: Um cliente pode ter vários veículos (1:N). Um veículo pertence a um único cliente.

Veículo - Ordem de Serviço (OS): Um veículo pode ter várias ordens de serviço (1:N). Cada OS é associada a um único veículo.

Ordem de Serviço (OS) - Equipe: Cada OS é atribuída a uma equipe de mecânicos (N:1). Uma equipe pode ser responsável por várias ordens de serviço.

Equipe - Mecânico: Cada equipe é composta por vários mecânicos (1:N). Um mecânico pertence a uma única equipe.

Ordem de Serviço (OS) - Serviço: Cada OS pode ter múltiplos serviços associados a ela (N:M). Para isso, existe uma tabela associativa chamada Serviço-OS que armazena os serviços executados em uma OS.

Ordem de Serviço (OS) - Peça: Cada OS pode ter várias peças associadas (N:M). A tabela Peça-OS é uma tabela associativa que contém as peças usadas em uma OS, incluindo a quantidade e o valor de cada uma.

## Modelo ER

Cliente: Entidade que contém informações dos clientes da oficina.
Veículo: Entidade que contém informações dos veículos que os clientes trazem para a oficina.
Ordem de Serviço (OS): Cada OS contém informações sobre os serviços solicitados, com a data de emissão, status e valor total.
Equipe: Entidade que agrupa os mecânicos que irão trabalhar nas ordens de serviço.
Mecânico: Entidade que representa os mecânicos da oficina, com suas especialidades e dados pessoais.
Serviço: Cada tipo de serviço (ex: troca de óleo, revisão) que a oficina oferece.
Peça: Cada peça utilizada nas ordens de serviço.
Serviço-OS: Relacionamento entre a OS e os serviços realizados.
Peça-OS: Relacionamento entre a OS e as peças utilizadas.

## Diagrama ER:
Entidade Cliente: Contém os atributos id_cliente, nome, endereco, telefone, email.
Entidade Veículo: Contém os atributos id_veiculo, placa, modelo, ano_fabricacao, cor, id_cliente.
Entidade Ordem de Serviço (OS): Contém os atributos id_os, numero_os, data_emissao, data_conclusao, valor_total, status, id_veiculo, id_equipe.
Entidade Equipe: Contém os atributos id_equipe, nome_equipe, id_mecanico.
Entidade Mecânico: Contém os atributos id_mecanico, codigo, nome, endereco, especialidade.
Entidade Serviço: Contém os atributos id_servico, descricao, valor.
Entidade Peça: Contém os atributos id_peca, descricao, valor.
Entidade Serviço-OS: Relacionamento entre OS e Serviço.
Entidade Peça-OS: Relacionamento entre OS e Peça.
