#Comandos sql
criando um banco de dados

create database empresa;

Selecionando o banco de dados
Use empresa;

Criando uma tabela

create table clientes(
id int primary key,
nome varchar(200),
email varchar(100)
);

Inserindo valores
insert into clientes (id, nome, email) values(1, 'Maria silveira santos', 'Mariasilveria@gmail.com');

Selecionando todos os clientes
select \* from clientes;

Atualizando dados

update clientes set nome = 'João silva matos' where id = 1;
