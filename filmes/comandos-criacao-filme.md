# Comandos SQL - Referência
<!-- __________________________________ -->

## Modelagem física

### Criar banco de dados

```sql

CREATE DATABASE filmes CHARACTER SET utf8mb4;

```

<!-- ____________________________ -->

### Criar a tabela de filmes

```sql
CREATE TABLE filmes(
    id INT NOT  NULL PRIMARY KEY AUTO_INCREMENT,
    nome VARCHAR(45) NOT NULL
    lancamento YEAR(4) NOT NULL
)
```

<!-- ___________________________ -->

### Criar a tabela de genêros

```sql
CREATE TABLE generos(
    id INT NOT  NULL PRIMARY KEY AUTO_INCREMENT,
    genero VARCHAR(45) NOT NULL
)
```

<!-- ___________________________ -->

### Adicionar linha tabela de filmes

```sql
ALTER TABLE filmes ADD genero_id INT NOT NULL
AFTER lancamento;  

```
<!-- ____________________________ -->

### Criação da chave estrangeira (relacionamento entre tabelas)

```sql
ALTER TABLE filmes
    # CONSTRAINT é uma restrição definida no relacionamento
    ADD CONSTRAINT fk_filmes_generos

    # A chave estrangeira deve fazer referência a chave primária 
    FOREIGN KEY(genero_id) REFERENCES generos(id)

```


