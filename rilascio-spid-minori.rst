Rilascio di SPID ai minori
==========================

Dall'analisi della normativa vigente emerge l'opportunità che il rilascio
dell'identità digitale SPID a favore del minore avvenga previa richiesta da
parte di chi esercita la responsabilità genitoriale, ferma restando la facoltà
del minore che abbia compiuto quattordici anni di esprimere autonomamente il
consenso al trattamento dei propri dati in relazione all'offerta di servizi
della società dell'informazione.

L'IdP che rilascia l'identità digitale al minore espone un apposito servizio
accessibile dal genitore attraverso credenziali SPID dallo stesso rilasciate,
che consente al genitore di gestire l'identità del minore (si pensi, ad
esempio, alla possibilità di revocare l'identità).

Per ottenere l'autorizzazione del genitore all'accesso ai servizi in rete da
parte del minore è prevista una notifica *push* da parte dell'IdP su richiesta
del minore.

Il genitore, al fine di fornire le suddette autorizzazioni, accetta, al momento
della richiesta dell'identità del minore, di ricevere notifiche *push*
dall'IdP.

Tali notifiche sono inviate esclusivamente se il minore conferma all'IdP la
volontà di richiedere l'autorizzazione al genitore. Nel caso in cui il minore
non confermi all'IdP la volontà di richiedere l'autorizzazione al genitore, la
procedura di autenticazione è interrotta.

Il genitore utilizza le proprie credenziali SPID per gestire l'identità del
minore fermo restando che l'IdP non avrà la necessità di entrare nella
federazione SPID in qualità di SP in quanto il genitore, per gestire l'identità
del minore, utilizza un'identità digitale rilasciata dal medesimo IdP presso il
quale il minore ottiene la propria identità digitale.

L'IdP predispone un servizio per consentire al genitore di chiedere il rilascio
dell'identità digitale per il minore. Tale servizio, accessibile con
credenziali SPID di livello 2, prevede l'inserimento dei dati identificativi
del minore (nome, cognome, codice fiscale, data di nascita).

Se il minore non presenta all'IdP un documento di identità (o il permesso di
soggiorno) in cui è riportato il nominativo del genitore, il genitore dichiara,
ai sensi dell'art. 46 del decreto del Presidente della Repubblica 28 dicembre
2000, n. 445, la sua qualità rispetto al minore con le modalità indicate
dall'IdP.

Il genitore fornisce il consenso al trattamento dei dati personali per il
rilascio e la gestione dell'identità digitale del minore nonché la delega
dell'eventuale genitore non richiedente alla gestione dell'identità del minore
da parte del genitore.

L'IdP genera, conseguentemente, un codice casuale di tre numeri in notazione
decimale (*seriale minore*) che, associato al *codice del genitore*, è univoco
nell'ambito di ogni IdP e costituisce il *codice di verifica* assegnato al
minore.

In particolare, il *codice del genitore* è composto dal risultato della
funzione CRC-32 applicato al codice fiscale del genitore (Ad esempio:
RSSMTT64A01G201K, produce il CRC 0x4DFCE69E, il *codice del genitore* sarà
4DFCE69E. Ipotizzando che il codice casuale sia 737, il *codice di verifica*
sarà 4DFCE69E737).

L'IdP associa ai dati del genitore il *codice di verifica* per il quale è stato
fornito il consenso al rilascio dell'identità e i dati identificativi del
minore forniti dal genitore. L'IdP consegna al genitore il *codice di verifica*
affinché lo stesso sia messo a disposizione del minore che lo utilizza per
effettuare il processo di rilascio dell'identità digitale, previa verifica
dell'identità personale e acquisizione del consenso al trattamento dei dati
personali anche da parte del minore che ha compiuto almeno quattordici anni.

Il minore, ricevuto il *codice di verifica* dal proprio genitore, utilizza le
procedure di verifica dell'identità personale messe a disposizione dall'IdP per
completare la procedura di rilascio dell'identità. L'IdP, per verificare
l'esistenza dell'autorizzazione preventiva, richiede al minore il *codice di
verifica* in modo da poter verificare la presenza del consenso genitoriale
prima di acquisire i dati personali del minore. L'IdP verifica, quindi, la
corrispondenza dell'identità del minore con i dati precedentemente forniti dal
genitore, verificando implicitamente l'esistenza dell'autorizzazione del
genitore al rilascio dell'identità per quello specifico minore.

L'IdP, inoltre, se il minore ha compiuto almeno quattordici anni, acquisisce
anche da quest'ultimo il consenso al trattamento dei dati personali per il
rilascio e la gestione dell'identità digitale.

L'IdP, rilasciata l'identità, invia una e-mail informativa al genitore recante
l'indicazione del nome del minore.

Per ottenere l'autorizzazione del genitore all'accesso ai servizi in rete da
parte del minore, è prevista una notifica *push* da parte dell'IdP al genitore,
su richiesta del minore.

Quando il minore tenta di accedere a un servizio della società
dell'informazione, l'IdP, se ha già ottenuto l'autorizzazione all'accesso da
parte del genitore, autentica il minore. Nel caso in cui l'autorizzazione non
sia presente, invia al genitore una notifica *push* contenente:

-	il nome del minore, 
-	il nome del SP cui il minore ha tentato di accedere, 
-	la data e l'ora del tentativo di accesso e i dati personali richiesti dal SP.

Il genitore può autorizzare l'accesso allo specifico servizio indicando la
durata dell'autorizzazione che, in ogni caso, non potrà essere superiore a un
anno.

Almeno dieci giorni prima della scadenza di ogni autorizzazione, il genitore
riceve dall'IdP una notifica *push* per l'eventuale rinnovo
dell'autorizzazione.

Il genitore utilizza le proprie credenziali SPID per gestire l'identità del
minore, fermo restando che l'IdP non avrà la necessità di entrare nella
federazione SPID in qualità di SP in quanto il genitore, per gestire l'identità
del minore, utilizza un'identità digitale rilasciata dal medesimo IdP presso il
quale il minore ottiene la propria identità digitale.

L'IdP mette a disposizione del genitore una funzionalità che gli consente di
avere evidenza delle identità digitali destinate ai minori e oggetto della sua
autorizzazione al rilascio. Tale funzionalità, inoltre, consente al genitore di
visualizzare tutti i SP presso i quali ha autorizzato l'accesso del figlio con
possibilità di revoca delle singole autorizzazioni e, ove necessario, della
stessa identità digitale del minore.

Risultati attesi
----------------

1. Garantire che l'identità digitale sia rilasciata al minore esclusivamente
   previa richiesta del genitore.
2. Consentire al genitore di avere evidenza delle identità digitali rilasciate
   ai propri figli minori.
3. Consentire al genitore di gestire le identità digitali rilasciate ai propri
   figli minori con la possibilità di revocare le singole autorizzazioni
   all'accesso ai servizi della società dell'informazione o la stessa identità
   digitale del minore.
4. Garantire che nessun dato del minore sia fornito ai SP in assenza del
   consenso del genitore e del minore che ha compiuto almeno quattordici anni.
5. Informare il genitore in merito al rilascio dell'identità digitale al figlio
   minore.

Rischi residui
--------------

Un soggetto potrebbe dichiarare falsamente di esercitare la tutela di un minore.

Contromisure
~~~~~~~~~~~~

L'IdP verifica il reale stato di tutela del minore sulla carta di identità o
sul permesso di soggiorno.

Nel caso residuale dell'autocertificazione, la normativa prevede responsabilità
penali in capo al soggetto che effettua false dichiarazioni ai sensi del
decreto del Presidente della Repubblica 28 dicembre 2000, n. 445. Tale soggetto
potrà essere facilmente individuato e perseguito, in quanto, per effettuare la
dichiarazione di cui al punto 5, è necessario procedere a un'autenticazione
SPID.

.. forum_italia::
   :topic_id: 23776
   :scope: document
