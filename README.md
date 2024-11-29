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

#### Estrutura conceitual

+----------------+       +------------------+
|    Usuário     |       |     Tarefa       |
+----------------+       +------------------+
| id             |<----- | id_usuario       |
| nome           |       | id               |
| email          |       | descricao_tarefa |
+----------------+       | nome_do_setor    |
                         | prioridade       |
                         | data_de_cadastro |
                         | status           |
                         +------------------+

