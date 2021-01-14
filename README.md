# Attivita_progettuale
Repository dedicata al lavoro svolto durante l'attività progettuale interna, per il corso di laurea in Ingegneria Informatica dell'Università degli Studi di Modena e Reggio Emilia (dipartimento di Ingegneria).
Il lavoro è suddiviso in due cartelle:
- ChessEngine1 --> il progetto Python contenuto implementa un prototipo di motore scacchistico. Le features implementate sono:
    - Generatore ad oggetti, legale e incrementale
    - Esploratore che utilizza Minimax, Perft, Alphabeta con ordinamento delle mosse, Iterative Deepening e Tabella di Trasposizione
    - Valutatore che presenta una funzione di valutazione a tabelle e una funzione di valutazione "pigra"
- ChessEngine1.1 --> il progetto Python contenuto implementa una variante non completa del motore sudetto; infatti presenta:
    - Generatore a liste (si ispira alle bitboards), pseudo-legale e incrementale
    - Esploratore che utilizza Minimax, Alphabeta con ordinamento delle mosse, Iterative Deepening
    - Valutatore che presenta una funzione di valutazione a tabelle e una funzione di valutazione "pigra"


Per quanto riguarda ChessEngine1, è composto dai seguenti moduli:
- algebraicnotationmodule.py è il modulo dedicato alla gestione delle coordinate algebriche , così da permettere una manipolazione più agevole dei vettori di movimento, oltre alla semplificazione di una serie di controlli sulla legalità delle mosse.

- movemodule.py è il modulo dedicato alla gestione delle mosse e dei diritti di arrocco.

- hashingalgorithm.py è il modulo che implementa gli algoritmi di hashing, in particolare quello di Zobrist.

- piecesmodule.py è il modulo che si occupa di mantenere lo stato interno e della generazione delle mosse, offrendo tutta una serie di servizi a GameTreeSearcher e Evaluator.

- evaluationmodule.py è il modulo che implementa le funzioni di valutazione.

- transpositionmodule.py è il modulo che implementa la gestione della Tabella di Trasposizione.

- gametreesearching.py è il modulo che implementa gli algoritmi di ricerca

- ucimanagermodule.py è il modulo che gestisce le comunicazioni da/verso l'esterno, implementando il protocollo UCI. All'accensione di motore, questo modulo costituisce il punto di partenza dell'esecuzione. Dopo aver ricevuto dall'esterno l'opportuna sequenza di comandi UCI, avvierà la ricerca attraverso un Python-Thread.


ChessEngine1.1 ha una struttura del tutto simile, anche se, internamente, i singoli moduli presentano delle differenze. Inoltre, il modulo deidcato allo stato interno e alla generazione delle mosse prende il nome di dictgenerataormodule.py
