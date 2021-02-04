====================================
La Carta di identità elettronica CIE
====================================


La Carta d'identità elettronica (CIE) è il documento di identità rilasciato dai Comuni italiani su richiesta dei cittadini che ne certifica l'identità fisica e digitale.  È considerata una piattaforma abilitante ai sensi del `Piano Triennale per l'informatica nella Pubblica Amministrazione <https://docs.italia.it/italia/piano-triennale-ict/pianotriennale-ict-doc/it/2019-2021/index.html>`__ dal momento che consente l'attivazione di servizi basati sull'utilizzo del microprocessore a radio frequenza di cui è dotata. Nello specifico, per il tramite della CIE e del PIN che ciascun cittadino riceve, metà alla richiesta, metà con la carta, è possibile accedere ai servizi erogati in rete dalle PP.AA. e dai soggetti privati con i massimi livelli di sicurezza.
 
Lo schema di autenticazione con CIE si basa su un modello diverso da quello utilizzato per l'accesso in rete mediante la Carta Nazionale dei Servizi “CNS”.

Con la CNS, infatti, l'utente utilizza la carta come contenitore della coppia di chiavi di autenticazione TLS. Il middleware CNS consente l'autenticazione verso il sito dell'erogatore del servizio, sul quale ricade interamente l'onere della verifica della validità della catena di certificati della CA Autenticazione del Ministero dell'Interno.

Lo schema di autenticazione “Entra con CIE” è, invece, basato su un sistema di *Single Sign-On* (SSO) che consente a chi rilascia l'identitá digitale (Identity provider) di inviare le credenziali di autorizzazione dell'utilizzatore finale al fornitore di servizi (Service Provider), sollevando quest'ultimo dall'onere di gestione delle identità digitali. Il vantaggio da parte dell'utilizzatore che fa richiesta di autenticazione è altrettanto tangibile, in quanto tale schema di identificazione consente di avere un'unica chiave di accesso superando, in questo modo, il modello tradizionale di autenticazione basato su password specifiche per ogni servizio. Di seguito viene riportato il tipico flusso di funzionamento.

.. figure:: ../../media/schema_autenticazione.png
   :alt: Schema di autenticazione Entra con CIE.
   :width: 15cm
   :name: schema-autenticazione

   Schema di autenticazione Entra con CIE.

1.	il cittadino richiede a un Service Provider la fruizione di un servizio digitale;

2.	il Service Provider invia all'Identity Provider una richiesta di autenticazione del cittadino;

3.	l'Identity Provider richiede al cittadino di utilizzare la sua CIE per autenticarsi avvicinandola a un lettore RF collegato a un PC o direttamente al proprio dispositivo mobile dotato di interfaccia NFC e inserendo il PIN. Viene, inoltre, verificata, la validità del certificato digitale associato al cittadino;

4.	l'Identity Provider reindirizza l'utente verso il Service Provider inviando a quest'ultimo l'esito di avvenuta autenticazione e gli attributi identificativi dell'utente;

5.	il Service Provider, in caso di esito positivo, concede l'accesso al servizio richiesto.

Il set di dati che vengono inviati al Service Provider sono i seguenti:

   -	nome;

   -	cognome;

   -	data di nascita;

   -	codice fiscale.


Il processo di autenticazione è garantito mediante la verifica di validità (autenticità e scadenza) del certificato digitale presente a bordo della CIE che viene letto dal microprocessore della carta ed inviato presso la CA Autenticazione (cfr. `DM del 23 dicembre 2015 recante “Modalità tecniche di emissione della Carta d'Identità elettronica” <http://www.gazzettaufficiale.it/eli/id/2015/12/30/15A09809/sg>`__).

La procedura suindicata garantisce la correttezza delle informazioni sia al Ministero dell'Interno - cui è riservata l'emissione della Carta di identità elettronica (cfr. `D.L. 78/2015, art.10 <https://www.gazzettaufficiale.it/eli/id/2015/06/19/15G00093/sg>`__ ) – che alle pubbliche amministrazioni e ai soggetti erogatori di servizi pubblici e privati che consentono l'accesso tramite CIE. 

La CIE, inoltre, è stata riconosciuta dal Cooperation Network eIDAS (electronic IDentification Authentication and Signature) come strumento di identificazione digitale e di accesso ai servizi online erogati nei paesi dell'Unione Europea compatibile con il Level of Assurance 4 (high), in conformità con quanto previsto dal `Regolamento UE n° 910/2014 sull'identità digitale <https://eur-lex.europa.eu/legal-content/IT/TXT/?uri=CELEX%3A32014R0910>`__. 

Lo schema di autenticazione con la CIE supera, dunque, il modello precedente basato sulla CNS, dal momento che:

- è fruibile anche in ambiente “mobile”;

- offre una “user experience” migliore ed uniforme dal momento che consente di fornire in ogni caso d'uso le giuste istruzioni all'utente (es. PIN bloccato, carta scaduta, postazione non configurata);

- è pienamente rispondente alle prescrizioni del GDPR dal momento che prevede il consenso da parte dell'utente all'invio degli attributi richiesti dal servizio;

- è utilizzabile come schema di autenticazione in conformità al regolamento eIDAS;

- offre l'opportunità di conservare in modo semplice la prova dell'avvenuta autenticazione da parte del Ministero dell'Interno che consegna la CIE e i relativi codici al titolare previa identificazione da parte di operatori qualificati dei Comuni e degli Uffici consolari.

