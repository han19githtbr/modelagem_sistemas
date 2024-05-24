## Diagrama DER

```mermaid
CREATE TABLE Aluno (
    ra INT PRIMARY KEY,
    nome VARCHAR(100),
    email VARCHAR(100),
    telefone VARCHAR(20)
);


CREATE TABLE Livro (
    isbn VARCHAR(13) PRIMARY KEY,
    nome VARCHAR(100),
    autor VARCHAR(100),
    paginas INT
);


CREATE TABLE Colaborador (
    cpf VARCHAR(11) PRIMARY KEY,
    nome VARCHAR(100),
    email VARCHAR(100),
    cargo VARCHAR(50)
);


CREATE TABLE Emprestimo (
    id INT PRIMARY KEY AUTO_INCREMENT,
    dataEmprestimo DATE,
    dataDevolucao DATE,
    livroIsbn VARCHAR(13),
    colaboradorCpf VARCHAR(11),
    raAluno INT,
    FOREIGN KEY (livroIsbn) REFERENCES Livro(isbn),
    FOREIGN KEY (colaboradorCpf) REFERENCES Colaborador(cpf),
    FOREIGN KEY (raAluno) REFERENCES Aluno(ra)
);
```
