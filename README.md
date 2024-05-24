## Diagrama DER

```mermaid
Aluno
-----
ra (PK)
nome
email
telefone

Livro
-----
isbn (PK)
nome
autor
paginas

Colaborador
-----------
cpf (PK)
nome
email
cargo

Empréstimo
----------
id (PK)
dataEmprestimo
dataDevolucao
livroIsbn (FK) -> Livro.isbn
colaboradorCpf (FK) -> Colaborador.cpf
raAluno (FK) -> Aluno.ra

```
