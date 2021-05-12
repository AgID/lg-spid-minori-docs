Limitazione dell'accesso ai servizi in rete
===========================================

Per impedire l'accesso a un servizio della società dell'informazione non
destinato ai minori o non conforme all'età prevista, evitando che il SP riceva
dati personali del minore, è necessario che la verifica sia effettuata dall'IdP
e non dal SP.

A tale scopo è possibile utilizzare le estensioni SAML che seguono negli esempi
all'interno dell'*authRequest*.

Alcuni esempi:

a. Per indicare che il servizio è riservato a chi ha 17 anni

   .. code-block:: xml

      <samlp:Extensions>
        <spid:AgeLimit>
          <spid:MinAge>17</spid:MinAge>
          <spid:MaxAge>17</spid:MaxAge>
        </spid:AgeLimit>
      </samlp:Extensions>

b. Per indicare che il servizio è riservato a chi ha compiuto quattordici anni e non ne ha ancora compiuti 18:

   .. code-block:: xml

      <samlp:Extensions>
        <spid:AgeLimit>
          <spid:MinAge>14</spid:MinAge>
          <spid:MaxAge>17</spid:MaxAge>
        </spid:AgeLimit>
      </samlp:Extensions>

Il valore "99" in MaxAge indica l'assenza di un limite superiore.

In questo modo, gli IdP che rilasciano identità digitali ai minorenni, ricevono
le informazioni necessarie per limitare l'accesso a una età o ad una specifica
fascia d'età.

L'IdP, previa autenticazione, effettua quindi la verifica di congruenza (età
effettiva/età richiesta) e stabilisce se portare a termine con successo il
processo di autenticazione. Nel caso in cui l'età del soggetto non sia congrua
con la richiesta pervenuta dall'SP, l'IdP informa l'utente con il messaggio

.. epigraph::

    "Spiacente %Nome%, ma non hai l'età richiesta da %SP% per accedere al
    servizio"

dove "*%Nome%*" è il nome proprio del soggetto autenticato e "*%SP%*" è
l'indicazione del SP o del servizio a cui si sta tentando di accedere.

Risultati attesi
----------------

1. Impedire, fin dalla progettazione e per impostazione predefinita, che un
   minore possa accedere a un servizio non destinato ai minori.

2. Consentire processi di autenticazione anonimi e basati esclusivamente sul
   controllo dell'età.

3. Evitare che il SP debba necessariamente conoscere la data di nascita del
   minore.

Rischi residui
--------------

Non si rilevano rischi residui.

Contromisure
~~~~~~~~~~~~

N.A.

.. forum_italia::
   :topic_id: 23778
   :scope: document
