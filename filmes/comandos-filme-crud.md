# Inserir genêros

```sql
INSERT INTO generos (genero)
    VALUES('Ação'), ('Terror'), ('Romance'), ('Ficção Científica');
```

## Inserir filmes

```sql
    INSERT INTO filmes (titulo, lancamento, genero_id)
    VALUES('Velozes e furiosos 3', 2006,1);
    INSERT INTO filmes (titulo, lancamento, genero_id)
    VALUES('Fale comigo', 2022,2);
    INSERT INTO filmes (titulo, lancamento, genero_id)
    VALUES('La La Land', 2017,3);
    INSERT INTO filmes (titulo, lancamento, genero_id)
    VALUES('Interestelar', 2014,4);

```