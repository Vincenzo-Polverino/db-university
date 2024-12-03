"Modellare la struttura di un database per memorizzare tutti i dati riguardanti una università:
sono presenti diversi Dipartimenti (es.: Lettere e Filosofia, Matematica, Ingegneria ecc.);
ogni Dipartimento offre più Corsi di Laurea (es.: Civiltà e Letterature Classiche, Informatica, Ingegneria Elettronica ecc..)
ogni Corso di Laurea prevede diversi Corsi (es.: Letteratura Latina, Sistemi Operativi 1, Analisi Matematica 2 ecc.);
ogni Corso può essere tenuto da diversi Insegnanti;
ogni Corso prevede più appelli d'Esame;
ogni Studente è iscritto ad un solo Corso di Laurea;
ogni Studente può iscriversi a più appelli di Esame;
per ogni appello d'Esame a cui lo Studente ha partecipato, è necessario memorizzare il voto ottenuto, anche se non sufficiente. Pensiamo a quali entità (tabelle) creare per il nostro database e cerchiamo poi di stabilirne le relazioni. Infine, andiamo a definire le colonne e i tipi di dato di ogni tabella."



## Dipartimenti
id: INT | PRIMARY KEY |NONULL
nome: VARCHAR(100) | NONULL
descrizione: TEXT | NULL


## Corsi_Laurea
id: INT | PRIMARY KEY| NONULL
nome: VARCHAR(100) | NONULL
id_dipartimento: INT | FOREIGN KEY | NONULL
descrizione: TEXT | NULL


## Corsi
id: INT | PRIMARY KEY | NONULL
nome: VARCHAR(100) | NONULL
id_corso_laurea: INT | FOREIGN KEY | NONULL
descrizione: TEXT | NULL


## Insegnanti
id: INT | PRIMARY KEY | NONULL
cognome: VARCHAR(100) | NONULL
email: VARCHAR(100) | NONULL


## Appelli_Esame
id: INT | PRIMARY KEY | NONULL
id_corso: INT | FOREIGN KEY | NONULL
data: DATE | NONULL
luogo: VARCHAR(100) | NONULL


## Studenti
id: INT | PRIMARY KEY | NONULL
nome: VARCHAR(100) | NONULL
cognome: VARCHAR(100) | NONULL
data_nascita: DATE | NONULL
id_corso_laurea: INT | FOREIGN KEY | NONULL

