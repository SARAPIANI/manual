# 🛠️ Definizione Scenario - Source Scenarios

La piattaforma SaferPlaces rappresenta un avanzato strumento di analisi integrata, che sfrutta modelli matematici e algoritmi di elaborazione rapida sia di tipo raster-based che di Intelligenza Artificiale. Questa combinazione tecnologica permette di fornire risultati accurati e dettagliati in tempi molto contenuti. Gli utenti della piattaforma possono ottenere, infatti, una rapida mappatura dell'estensione dell'Hazard, ovvero la pericolosità associata ad eventi alluvionali.

Inoltre, vengono fornite informazioni essenziali sul livello di profondità dell'acqua (Water Depth) all'interno delle aree colpite da allagamenti. Questo dato è cruciale per progettare e implementare misure di mitigazione e intervento. Ulteriormente, la piattaforma offre una valutazione dettagliata del Danno Economico potenziale per ciascun edificio situato nelle zone a rischio. Questa stima è calcolata considerando il valore dell'asset immobiliare, espresso in euro per metro quadrato, insieme alla vulnerabilità specifica di ogni edificio. Tale vulnerabilità è descritta attraverso la Curva di Danno (Damage Function), che misura l'impatto economico in funzione delle caratteristiche strutturali e della resistenza del bene immobiliare coinvolto.

Grazie a queste funzionalità, SaferPlaces si pone come una risorsa indispensabile per enti pubblici e privati interessati a ridurre al minimo le perdite economiche e aumentare la resilienza dei territori nei confronti di eventi calamitosi. La capacità di effettuare analisi dettagliate e mirate consente di prendere decisioni informate, pianificare efficacemente strategie di risposta e proporre interventi di lungo termine per la protezione dell'ambiente e delle infrastrutture urbane.



Per procedere con le simulazioni, accedi alla scheda "Source Scenario" situata in alto nella barra laterale sinistra dell'interfaccia.

{% hint style="danger" %}
Il primo elemento delle attività nel pannello a sinistra è denominato _Source Scenarios_ (scenari sorgente) ed è utilizzato per eseguire simulazioni di alluvione.
{% endhint %}

<figure><img src="../../.gitbook/assets/Screenshot 2024-10-10 at 00.12.02.png" alt=""><figcaption></figcaption></figure>

Sono stati sviluppati modelli innovativi ed efficienti per tutte e tre le fonti di allagamento:

* [Pluviale](simulazione-allagamento-pluviale.md) - RAINFALL Determinato da pioggie intense per assegnata durata :cloud\_rain:
* [Fluviale](simulazione-allagamento-fluviale.md) - RIVER Determinato da rilasci volumetrici per Breccia/Rottura Arginale o Sormonto :wavy\_dash:
* [Costiero](simulazione-allagamento-costiero.md) -COASTAL  Determinato dal livello del mare come combinazione di Storm Surge, Marea e Onda. :ocean:

{% hint style="info" %}
Una guida passo-passo aiuterà l'utente a inserire tutte le informazioni necessarie per calcolare il rischio di alluvione e i relativi danni. L'utente potrà creare uno scenario climatico che rifletta le condizioni storiche, attuali o future.
{% endhint %}
