# Esame
### PROVA "C"
### Creazione Database ed inserimento Dummydatas


- ## 1 Creazione della tabella

Per creare la tabella Compagni viene usato il comando ***SQL CREATE TABLE IF NOT EXISTS*** specificando il tipo di dato che ospiterà ogni campo:

```sql
CREATE TABLE IF NOT EXISTS Compagni (
    ID INTEGER PRIMARY KEY,
    NOME TEXT,
    COGNOME TEXT,
    EMAIL TEXT
);
```
***NOME, COGNOME*** e ***EMAIL*** sono campi di tipo testuale  ***TEXT***, inserisco anche un campo ID di tipo ***INTEGER*** con chiave primaria che garantisce la natura univoca dei dati.
Spefificando invece ***IF NOT EXISTS*** si evita la possibilità di creare più tabelle identiche.

Lo script SQL è salvato in un file ***create_table.sql***.

Viene creato quindi il database ***database.db*** da riga di comando che conterrà la tabella ***Compagni*** tramite l'istruzione:
> sqlite3 database.db < create_table.sql

- ## 2 Inserimento dati

I dati vengono inseriti nella tabella tramite il comando SQL ***INSERT INTO*** specificando poi la tabella e i campi ***Compagni (NOME, COGNOME, EMAIL)***, seguono i valori ***VALUES ('Andrea', 'Alvigini', 'andreaalvigini@gmail.com'), ...***.

Anche in questo caso lo script SQL viene salvato in un file dall'estensione .sql  ***insert_dummy_data.sql*** eseguito poi da terminale.

Di seguito il codice:
```sql
INSERT INTO
    Compagni (NOME, COGNOME, EMAIL)
VALUES
    ('Andrea', 'Alvigini', 'andreaalvigini@gmail.com'),
    ('Greta', 'Di Fabio', 'gretadifabio@gmail.com'),
    ('Gianluca', 'Ciceri', 'gianlucaciceri@gmail.com'),
    ('Davide', 'Rivolta', 'daviderivolta@gmail.com'),
    ('Alessandro','De Giacobbi','alessandro@gmail.com'),
    ('Cristopher','Thompson','christopher@gmail.com'),
    ('Giorgio', 'Bruzzone', 'giorgio@gmail.com'),
    ('Simone', 'Rizzo', 'simonerizzo@gmail.com'),
    ('Tiziano', 'Gessa', 'tiziano@gmail.com'),
    ('Emanuele', 'Cappanera', 'emanuelecappanera@gmail.com');
```
Il file ***database.db*** conterrà la tabella ***Compagni*** con i dati corrispettivi per i campi ***NOME, COGNOME*** e ***EMAIL*** per ogni compagno.
