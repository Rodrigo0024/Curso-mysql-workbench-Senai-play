Markdown# 💾 Comandos SQL Essenciais

Este README serve como uma referência rápida e prática dos comandos SQL mais comuns para a **criação, manipulação e gerenciamento de dados** em um banco de dados, utilizando o exemplo de um banco de dados chamado `empresa`.

---

## 🏗️ 1. Criação e Gerenciamento do Banco de Dados (DDL)

| Ação                      | Comando SQL                      |
| :------------------------ | :------------------------------- |
| **Criar Banco de Dados**  | `CREATE DATABASE nome_do_banco;` |
| **Selecionar/Usar BD**    | `USE nome_do_banco;`             |
| **Apagar Banco de Dados** | `DROP DATABASE nome_do_banco;`   |

### Exemplo de Criação e Seleção

```sql
-- Criando um banco de dados
CREATE DATABASE empresa;

-- Selecionando o banco de dados
USE empresa;
📋 2. Estrutura de Tabelas (DDL)Criando uma Tabela (clientes)SQLCREATE TABLE clientes(
    id INT PRIMARY KEY,
    nome VARCHAR(200),
    email VARCHAR(100)
);
Alterando a Estrutura (Adicionar Coluna)SQL-- Alterando colunas: adiciona a coluna 'sobre'
ALTER TABLE clientes ADD COLUMN sobre VARCHAR(100);
Apagando a TabelaSQL-- Apaga a tabela clientes
DROP TABLE clientes;
✏️ 3. Manipulação de Dados (DML)Inserindo ValoresO email de exemplo foi alterado para fins de demonstração.SQLINSERT INTO clientes (id, nome, email)
VALUES (1, 'Maria silveira santos', 'contato@exemplo.com');
Selecionando Dados (Consultas)SQL-- Selecionando todos os clientes
SELECT * FROM clientes;
Atualizando DadosSQL-- Atualizando o nome do cliente onde o id é 1
UPDATE clientes SET nome = 'João silva matos' WHERE id = 1;
Apagando DadosComandoDescriçãoTRUNCATE TABLEApaga todos os dados e reseta o contador de ID (se houver).DROP DATABASEApaga o banco de dados inteiro.Exemplo:SQL-- Apaga todos os dados da tabela, inclusive os IDs
TRUNCATE TABLE clientes;
SQL-- Apaga o banco de dados (CUIDADO!)
DROP DATABASE empresa;
```
