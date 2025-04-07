# Desafio Backend NestJS – XBRI

## Objetivo: 

Construir uma API baseada no modelo TDD para um marketplace de venda de pneus, permitindo que usuários (vendedores e compradores) gerenciem seus anúncios e realizem compras.

## Requisitos

### Usuário (User):

Campos: 

- nome
- e-mail
- senha (hash), 
- tipo de usuário (comprador ou vendedor)

Validações:

- O e-mail deve ser único.
- A senha deve ter no mínimo 8 caracteres.
- O tipo de usuário deve ser "comprador" ou "vendedor".

### Produto (Tire):

Campos: 

- nome do pneu, 
- marca
- tamanho (ex: 205/55R16)
- preço, 
- quantidade disponível
- ID do vendedor.

Validações:

- O tamanho deve seguir o formato padrão de pneus (ex: 205/55R16).
- O preço deve ser maior que zero.
- Apenas vendedores podem criar produtos.

### Pedido (Order):

Campos: 

- ID do comprador
- ID do produto
- quantidade
- preço total
- status (pendente, pago, enviado, concluído).

Validações:

- Não permitir pedidos com quantidade maior que o estoque disponível.
- Atualizar o estoque do produto após a criação do pedido.

## Funcionalidades obrigatórias

### Cadastro e autenticação de usuários:
- Endpoint para registrar um novo usuário.
- Endpoint para login com geração de token JWT.

### Gerenciamento de produto:

CRUD de produtos (apenas para vendedores) com as opções a seguir:
- Criar 
- listar
- atualizar
- deletar produtos.

### Gerenciamento de pedidos:

- Criar um pedido para um produto.
- Listar pedidos do comprador ou vendedor.
- Atualizar o status do pedido (apenas pelo vendedor).

### Marketplace público:

- Listar todos os produtos disponíveis (com paginação, filtro por marca e tamanho).

### Testes obrigatórios

- Cadastro e autenticação de usuários.
- Criação e validação de produtos.
- Lógica de criação de pedidos, incluindo validação de estoque.

Cobertura mínima: 80%.