# Pizzaria Project

Este projeto tem como objetivo projetar e construir um banco de dados relacional personalizado para uma nova pizzaria. O foco será na parte de backend, enquanto a criação do sistema de pedidos frontend será realizada por outra equipe.

## Descrição do Projeto
A pizzaria será um estabelecimento apenas para retirada e entrega, sem serviço de jantar. O cliente, Ben, deseja ter um banco de dados que permita capturar e armazenar todas as informações importantes geradas pelo negócio, com o intuito de monitorar o desempenho do negócio por meio de um painel de controle.
<br>
O projeto será dividido em três principais áreas de concentração:

1. Pedidos dos clientes
2. Controle de estoque
3. Dados dos funcionários

## Pedidos dos Clientes
Os pedidos dos clientes serão a base do sistema. Ben forneceu uma lista inicial de dados que deseja coletar para cada pedido:

- Nome do item
- Preço do item
- Quantidade
- Nome do cliente
- Endereço de entrega
<br>
Com base nessas informações, identificamos a necessidade de incluir outros campos, como ID do pedido, tamanho do item e categoria do produto (pizza, acompanhamento, sobremesa, bebida). O endereço de entrega também será dividido em diferentes partes, como endereço 1, endereço 2, cidade e código postal.

## Controle de Estoque
O controle de estoque é uma parte essencial para garantir o abastecimento adequado dos ingredientes.<br>
Ben deseja monitorar o estoque de forma eficiente, identificando quando é necessário fazer novos pedidos. Para isso, serão coletadas informações sobre os ingredientes utilizados em cada pizza, suas quantidades com base no tamanho da pizza e o nível atual de estoque.
<br><br>
Para simplificar o projeto, foi assumido que todos os fornecedores têm o mesmo prazo de entrega dos itens. Com base nas informações fornecidas por Ben sobre os ingredientes de cada pizza, incluindo pesos e quantidades necessárias, foi possível criar tabelas separadas para ingredientes e receitas, permitindo o cálculo preciso do custo de cada pizza.

## Dados dos Funcionários
Ben também gostaria de ter acesso aos dados dos funcionários e suas escalas de trabalho. Isso inclui informações como salários, horários de entrada e saída. Esses dados serão adicionados ao banco de dados e permitirão o cálculo dos custos com a mão de obra.

## Ferramentas Utilizadas
Para projetar o banco de dados, foi utilizada a ferramenta Quick Database Diagrams (Quick DBD), que permitiu visualizar e definir as tabelas, seus campos e relacionamentos. Posteriormente, o diagrama resultante foi exportado para um software de gerenciamento de banco de dados SQL(PostgreSQL).<br>
![diagrama](QuickDBD.png)
*diagram*

## Base de dados
Após a criação das tabelas, importamos os arquivos CSV de cada tabela, que continham as informações.
<br>
Construímos consultas (queries) que nos ajudaram a construir o painel de controle.

### Query 1 - Atividade de Pedidos

Consulta para o Painel de Controle 1 - Atividade de Pedidos
Para esse painel, precisamos dos seguintes dados:

- Total de pedidos
- Total de vendas
- Total de itens
- Valor médio do pedido
- Vendas por categoria
- Itens mais vendidos
- Pedidos por hora
- Vendas por hora
- Pedidos por endereço
- Pedidos para entrega ou retirada


### Query 2 - Gerenciamento de Estoque
Aqui está o que precisamos:

- Quantidade total por ingrediente
- Custo total dos ingredientes
- Custo calculado da pizza
- Porcentagem de estoque restante por ingrediente

<br>
Para obter essas informações, foram utilizadas duas consultas SQL. A primeira consulta calcula o custo dos ingredientes para cada item vendido. A segunda consulta relaciona os ingredientes com o estoque atual.

<br>
Outra consulta relacionada aos dados dos funcionários foi criada para calcular o custo da equipe com base nas informações de escalas de trabalho. 
<br>
Essas consultas são usadas para extrair os dados necessários das tabelas relacionadas e, em seguida, os dados podem ser utilizados para construir os painéis de controle desejados.

## Painéis de Controle 

![dashboard](dashboard.pdf)

## Conclusão
O projeto de construção do banco de dados para a pizzaria busca atender às necessidades de Ben, o cliente, fornecendo uma solução eficiente para armazenar e analisar os dados do negócio. Com a coleta e organização adequada dessas informações, será possível monitorar o desempenho do negócio, gerenciar o estoque de forma mais eficiente e analisar os custos da equipe, proporcionando uma base sólida para a tomada de decisões estratégicas.
