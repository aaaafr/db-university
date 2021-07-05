<!-- Modellizzare la struttura di una tabella per memorizzare tutti i dati riguardanti una università:
- sono presenti diversi dipartimenti, ciascuno con i propri corsi di laurea;
- ogni corso di laurea è formato da diversi corsi;
- ogni corso può essere tenuto da diversi insegnanti e prevede più appelli d'esame;
- ogni studente è iscritto ad un corso di laurea;
- per ogni appello d'esame a cui lo studente ha partecipato, è necessario memorizzare il voto ottenuto, anche se non sufficiente -->


# UNIVERSITÀ


## DIPARTIMENTI
- id      BINGINT PRIMARY KEY UNIQUE NOTNULL INDEX
- dipartimenti_id      BIGINT FKEY
- nome    VARCHAR(50) NOTNULL
- desc    TEXT NULL
- luogo   VARCHAR(50) NULL
- servizi VARCHAR(255) NULL


## LAUREA
- id       BINGINT PRIMARY KEY UNIQUE NOTNULL INDEX
- nome     VARCHAR(50) NOTNULL
- desc     TEXT NULL
- sede     VARCHAR(50) NULL



## CORSI
- id     BINGINT PRIMARY KEY UNIQUE NOTNULL INDEX
- corsi_id  BIGINT FKEY
- nome   VARCHAR(50) NOTNULL
- desc   TEXT NULL
- cfu    TINYINT NOT NULL
- aule   VARCHAR(20) NULL

## INSEGNANTI
- id        BINGINT PRIMARY KEY UNIQUE NOTNULL INDEX
- nome      VARCHAR(20) NOTNULL
- cognome   VARCHAR(20) NOTNULL
- studi     VARCHAR(100) NOTNULL

## APPELLI
- id      BINGINT PRIMARY KEY UNIQUE NOTNULL INDEX
- nome    VARCHAR(50) NOTNULL
- data    DATE NOTNULL
- ora     TIME NULL
- luogo   VARCHAR(50) NULL

## STUDENTI
- id          BINGINT PRIMARY KEY UNIQUE NOTNULL INDEX
- nome        VARCHAR(50) NOTNULL  
- cognome     VARCHAR(50) NOTNULL
- matricola   VARCHAR(50) NOTNULL


## VOTI
- id             BINGINT PRIMARY KEY UNIQUE NOTNULL INDEX
- valutazione    TINYINT NOTNULL


