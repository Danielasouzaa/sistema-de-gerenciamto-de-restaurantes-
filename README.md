# Sistema de Gerenciamento de Restaurante

## Descrição

O Sistema de Gerenciamento de Restaurante é um projeto desenvolvido para gerenciar as operações de um restaurante. O sistema permite a gestão de clientes, mesas, pedidos e itens de pedido.

## Estrutura do Banco de Dados

O banco de dados é chamado `RestauranteDB` e possui as seguintes tabelas:

### Tabela Clientes

Armazena informações dos clientes.

- `id_cliente` (INT, AUTO_INCREMENT, PRIMARY KEY): Identificador único do cliente.
- `nome` (VARCHAR(100)): Nome do cliente.
- `telefone` (VARCHAR(15)): Número de telefone do cliente.
- `email` (VARCHAR(100)): Endereço de e-mail do cliente.

### Tabela Mesas

Gerencia as mesas do restaurante.

- `id_mesa` (INT, AUTO_INCREMENT, PRIMARY KEY): Identificador único da mesa.
- `numero_mesa` (INT): Número da mesa.
- `capacidade` (INT): Capacidade da mesa (número de pessoas).

### Tabela Pedidos

Armazena informações sobre os pedidos realizados.

- `id_pedido` (INT, AUTO_INCREMENT, PRIMARY KEY): Identificador único do pedido.
- `id_cliente` (INT, FOREIGN KEY): Referência ao cliente que fez o pedido.
- `id_mesa` (INT, FOREIGN KEY): Referência à mesa onde o pedido foi feito.
- `data_pedido` (DATETIME): Data e hora do pedido.
- `total` (DECIMAL(10, 2)): Valor total do pedido.

### Tabela Itens_Pedido

Gerencia os itens de cada pedido.

- `id_item` (INT, AUTO_INCREMENT, PRIMARY KEY): Identificador único do item.
- `id_pedido` (INT, FOREIGN KEY): Referência ao pedido ao qual o item pertence.
- `descricao_item` (TEXT): Descrição do item.
- `quantidade` (INT): Quantidade do item no pedido.
- `preco_unitario` (DECIMAL(10, 2)): Preço unitário do item.

## Como Usar

1. Clone o repositório:
    ```bash
    git clone https://github.com/seu_usuario/seu_repositorio.git
    ```

2. Acesse o diretório do projeto:
    ```bash
    cd seu_repositorio
    ```

3. Importe o banco de dados `RestauranteDB` para seu sistema de gerenciamento de banco de dados preferido (por exemplo, MySQL).

4. Utilize as tabelas criadas para inserir, consultar, atualizar e deletar dados conforme necessário.

## Contribuições

Contribuições são bem-vindas! Se você encontrar algum problema ou tiver sugestões de melhoria, sinta-se à vontade para abrir uma issue ou enviar um pull request.

## Licença

Este projeto está licenciado sob a [Licença MIT](LICENSE).

