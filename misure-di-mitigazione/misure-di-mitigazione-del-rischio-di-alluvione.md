---
cover: ../.gitbook/assets/Asset 10.jpg
coverY: 0
layout:
  cover:
    visible: true
    size: hero
  title:
    visible: true
  description:
    visible: true
  tableOfContents:
    visible: true
  outline:
    visible: true
  pagination:
    visible: true
---

# 📔 Misure di mitigazione del rischio di alluvione

Saferplaces può essere utilizzato per testare l'efficacia di progetti e misure di mitigazione del rischio di allagamento sia in termini di riduzione dell'Hazard come estensione e magnitudo (profondità dell'acqua) sia in termini di protezioni passive e riduzione della vulnerabilità degli asset esposti.

<figure><img src="../.gitbook/assets/climate-resilience-models-cities.svg" alt=""><figcaption></figcaption></figure>

Le misure di mitigazione che si possono simulare sono:

●        [#barriere-fisiche](misure-di-mitigazione-del-rischio-di-alluvione.md#barriere-fisiche "mention"), come dune, argini o muri che possono contenere e limitare la portata delle inondazioni, in particolare quelle di origine fluviale e costiera

●      [#vasche-di-accumulo](misure-di-mitigazione-del-rischio-di-alluvione.md#vasche-di-accumulo "mention") ovvero vasche di stoccaggio dell'acqua in grado di ridurre il volume di acqua che allaga un sotto bacino.

●        [#sistemi-di-drenaggio-urbano-sostenibile-suds](misure-di-mitigazione-del-rischio-di-alluvione.md#sistemi-di-drenaggio-urbano-sostenibile-suds "mention"), come aree verdi, bacini di infiltrazione, uso del suolo permeabile, tetti verdi, zone umide urbane.



<details>

<summary>Barriere fisiche</summary>

Barriere fisiche come dune, argini o muri che possono contenere e limitare l'estensione spaziale e ridurre i battenti acqua associate agli scenari di allagamento.

Le barriere fisiche possono essere aggiunte al dominio di calcolo con lo **strumento "**_**Draw barrier**_**" della** [barra-superiore.md](../saferplaces-interfaccia-gui-web/barra-superiore.md "mention")che **permette di disegnare elementi lineari (polilinea) ed definire una altezza in m.**

Le barriere fisiche editate sono simulate modificando la quota del DTM e quindi determinano un effetto di contenimento dei fenomeni di allagamento.

&#x20;L'effetto è particolarmente evidente nella simulazione delle inondazioni costiere, dove barriere continue come le dune artificiali, se applicate lungo la linea di costa, possono proteggere una porzione significativa dell'entroterra.

<img src="../.gitbook/assets/barriere.jpg.webp" alt="" data-size="original">



</details>

<details>

<summary>Vasche di Accumulo</summary>

Le Vasche di accumulo sono una eficace misura di mitigazione per fli scenari di allagamento Pluviale e Fluviale.

Si tratta di inserire nel dominio di calcolo delle vasche di stoccaggio di tipo puntiforme con assegnata capacità volumetrica di contenere acqua nel proprio sotto-bacino di appartenenza.&#x20;

L'effetto che si ottiene è quello di ridurre la quantità di acqua se si accumula nelle depressioni e quindi ridurre gli effetti degli allagamenti.

L'utente utilizzando l**o strumento "**_**Draw storage tank**_**" della** [barra-superiore.md](../saferplaces-interfaccia-gui-web/barra-superiore.md "mention")**è in grado di disegnare e localizzare le vasche di accumulo all'interno del dominio, rappresentate da elementi puntiformi..**

Misure come vasche di accumulo "Storage Tank" possono essere simulate riducendo il volume d'acqua che scorre lungo la superficie e sono particolarmente rilevanti per le simulazioni di inondazioni pluviali.&#x20;

<img src="../.gitbook/assets/underground_tank.jpg" alt="" data-size="original">

</details>

<details>

<summary>Sistemi di drenaggio urbano sostenibile (SUDS)</summary>

Un ulteriore misura efficace di riduazione delle aree allagate è rappresentata dalla possibilità di modificare sia il ruscellamento superficiale delle acque  e sia la capacità del terreno di infiltrare ed immagazzinare acqua nel sottosuolo.

Si tratta  di piccole misure diffuse come come tetti verdi, la progettazione  di superfici permeabili e sistemi di infiltrazione.

Queste misure trovano applicazione in ambito urbano con la principale finalità di ridurre il rischio da allagamenti pluviali intensi e di breve durata.

La piattaforma Saferplaces consente di simulare queste misure mediante la modifica del [step-3-tasso-di-infiltrazione-rer-raster-geotiff.md](../gemello-digitale-e-attivazione-nuovo-servizio/creazione-digital-twin-e-attivazione-del-servizio-nellarea-di-interesse-solo-utenti-regione-er/step-3-tasso-di-infiltrazione-rer-raster-geotiff.md "mention") che si attiva con lo **strumento "**_**infiltration rate**_**" della** [barra-superiore.md](../saferplaces-interfaccia-gui-web/barra-superiore.md "mention")



</details>

