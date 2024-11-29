# Projeto_final

## Proposta
### Struct Data

Dados do Usuario: id, nome, email;

Dados da tarefa: id, id_usuario, descricao_tarefa, nome_do_setor, prioridade["baixa", "media", "alta"], \
    data_de_cadastro, status["a fazer"(Default), "fazendo", "pronto"];

Um usuario pode cadastrar uma ou mais tarefas, porém a tarefa é cadastrada por somente um usuario.


### Manage

#### Passos

- Cadastra tarefa;

- Gerenciar a mesma (Se selecionada);

- ["Alterar status", "Prioridades", NULL];

#### Apresentação

Apresentada em três colunas para usuario;

Não é *nescessario*(Não é obrigatorio) o uso de ["login", "sessão", "niveis"];

#### cors

As cores possiveis para utilização são:

| RGB             | Hexadecimal | Cor Exibida   |
|-----------------|-------------|---------------|
| rgb(255, 255, 255) | #FFFFFF     | <span style="color: #FFFFFF;">Branco</span> |
| rgb(0, 86, 179)   | #0056b3     | <span style="color: #0056b3;">Azul Claro</span> |
| rgb(0, 0, 0)      | #000000     | <span style="color: #000000;">Preto</span> |

---

## Projeto

### Banco

#### Estrutura Conceitual de Dados

##### Entidade: Usuário
A tabela **Usuário** armazena informações dos usuários do sistema.

| **Campo** | **Tipo**     | **Descrição**               |
|-----------|--------------|-----------------------------|
| id        | INT (PK)     | Identificador único do usuário |
| nome      | VARCHAR(255) | Nome do usuário             |
| email     | VARCHAR(255) | Endereço de e-mail do usuário |

##### Entidade: Tarefa
A tabela **Tarefa** armazena informações sobre as tarefas cadastradas.

| **Campo**        | **Tipo**     | **Descrição**                                      |
|------------------|--------------|----------------------------------------------------|
| id               | INT (PK)     | Identificador único da tarefa                      |
| id_usuario      | INT (FK)     | Identificador do usuário que cadastrou a tarefa (chave estrangeira) |
| descricao_tarefa| TEXT         | Descrição detalhada da tarefa                      |
| nome_do_setor   | VARCHAR(255) | Nome do setor relacionado à tarefa                 |
| prioridade      | ENUM('baixa', 'media', 'alta') | Prioridade da tarefa          |
| data_de_cadastro| DATETIME     | Data de cadastro da tarefa                         |
| status          | ENUM('a fazer', 'fazendo', 'pronto') | Status da tarefa              |

##### Relacionamento entre as Entidades
- **Usuário** e **Tarefa** possuem um relacionamento **1 para N** (um para muitos), onde um usuário pode ter várias tarefas, mas cada tarefa é associada a apenas um usuário.
- A tabela **Tarefa** possui uma chave estrangeira **`id_usuario`** que referencia a chave primária **`id`** da tabela **Usuário**.


###### Observações:
- **Usuário** pode cadastrar várias **Tarefas**.
- Cada **Tarefa** está associada a um único **Usuário**.



