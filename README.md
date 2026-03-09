# estudos-sql-server
Repositório de práticas de SQL do curso de ADS - Procedures e Modelagem.
# 📊 Sistema de Gestão de Contratos - SQL Server

Este repositório contém scripts de banco de dados desenvolvidos durante o curso **SQL Impressionador** da **Hashtag Treinamentos**. O foco aqui é demonstrar a aplicação prática de conceitos de banco de dados em cenários reais de negócios.

## 🚀 O que este projeto faz?

O projeto simula o fluxo de registro de contratos em um banco de dados relacional. Ele utiliza uma **Stored Procedure** que:
1. Recebe nomes de clientes e gerentes (em vez de IDs complexos).
2. Localiza automaticamente os IDs correspondentes nas tabelas de dimensão.
3. Garante a inserção correta na tabela de fatos (`fContratos`) com a data atual do sistema.

## 🛠️ Tecnologias Utilizadas
* **Banco de Dados:** SQL Server
* **Linguagem:** T-SQL (Stored Procedures, Variables, DML)
* **Versionamento:** Git & GitHub

## 📖 Como utilizar
Para registrar um novo contrato, basta executar a procedure passando os parâmetros:

```sql
EXEC prRegistraContrato 
    @gerente = 'Lucas Sampaio', 
    @cliente = 'Gustavo Barbosa', 
    @valor = 5000;
