# Gestao De Contas Bancarias

Este projeto é uma aplicação de gestão de contas bancárias desenvolvida em Python utilizando SQLModel 
para a manipulação do banco de dados e Matplotlib para a geração de gráficos.

Funcionalidades
*Criar Conta:* Permite criar uma nova conta bancária.
*Desativar Conta:* Desativa uma conta bancária, desde que não possua saldo.
*Transferir Dinheiro:* Transfere saldo de uma conta para outra.
*Movimentar Dinheiro:* Registra entradas e saídas de dinheiro em uma conta.
*Total Contas:* Calcula o saldo total de todas as contas.
*Filtrar Histórico:* Filtra o histórico de movimentações entre duas datas.
*Gerar Gráfico:* Gera um gráfico de barras com o saldo de todas as contas ativas.

Estrutura do Projeto
Arquivos Principais
models.py: Define os modelos de dados e a estrutura do banco de dados.
view.py: Contém as funções principais para manipulação das contas e movimentações.
templates.py: Interface de usuário para interação com o sistema via linha de comando.

Modelos de Dados
Define as classes e enums que representam os dados no banco de dados

Enums:
Bancos: Enumeração dos bancos disponíveis (NUBANK, SANTANDER, INTER).
Status: Enumeração do status da conta (ATIVO, INATIVO).
Tipos: Enumeração dos tipos de movimentação (ENTRADA, SAIDA).

Classes:
Conta: Representa uma conta bancária com os atributos id, banco, status e valor.
Historico: Representa o histórico de movimentações com os atributos id, conta_id, conta, tipo, valor e data.

Funções Principais
Contém as funções para manipulação das contas e movimentações:

criar_conta(conta: Conta): Cria uma nova conta bancária.
listar_contas(): Lista todas as contas bancárias.
desativar_conta(id): Desativa uma conta bancária, desde que não possua saldo.
transferir_saldo(id_conta_saida, id_conta_entrada, valor): Transfere saldo de uma conta para outra.
movimentar_dinheiro(historico: Historico): Registra entradas e saídas de dinheiro em uma conta.
total_contas(): Calcula o saldo total de todas as contas.
buscar_historicos_entre_datas(data_inicio: date, data_fim: date): Filtra o histórico de movimentações entre duas datas.
criar_grafico_por_conta(): Gera um gráfico de barras com o saldo de todas as contas ativas.
