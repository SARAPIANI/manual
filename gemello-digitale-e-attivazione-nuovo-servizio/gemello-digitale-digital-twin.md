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

# 📔 Gemello Digitale - Digital Twin

Per avviare un nuovo progetto o servizio sulla piattaforma Saferplaces, è necessario generare un Digital Twin dell'area di interesse.

{% content-ref url="creazione-digital-twin-e-attivazione-del-servizio-nellarea-di-interesse/" %}
[creazione-digital-twin-e-attivazione-del-servizio-nellarea-di-interesse](creazione-digital-twin-e-attivazione-del-servizio-nellarea-di-interesse/)
{% endcontent-ref %}

La Digital Twin è costituita dai seguenti dati geospaziali:

<details>

<summary>Modello digitale del Terreno (DTM) - LIDAR</summary>

La piattaforma SaferPlaces consente agli utenti di selezionare diversi strati DTM disponibili con varie risoluzioni spaziali.

Durante la fase di attivazione, i livelli DTM sono ordinati in ordine decrescente di risoluzione.

Gli utenti possono scegliere tra i DTM partendo dalla più alta risoluzione spaziale (LIDAR) fino a prodotti regionali o nazionali con risoluzione più bassa.

In alternativa, se gli utenti dispongono dei propri dati DTM, possono caricarli direttamente utilizzando l'opzione UPLOAD e utilizzare i dati per creare il Gemello Digitale.

La piattaforma è ottimizzata per lavorare con dati DEM LIDAR ad alta risoluzione.

I DTM pre-caricati e disponibili a livello nazionale sono:

* LIDAR Ministero dell'Ambiente - [Piano Nazionale di Telerilevament](https://sim.mase.gov.it/portalediaccesso/mappe/#/viewer/new)o
* DTM [TINITALY](https://tinitaly.pi.ingv.it/Download_Area1_1.html)
* LIDAR Regione Emilia Romagna
* LIDAR Regione Veneto
* DTM Regionionali

\


</details>

<details>

<summary>Footprint Edifici - Shapefile Vettoriale</summary>

Il contorno (footprint) degli edifici è un dato utilizzato per calcolare il Danno Economico associato agli eventi di allagamento.

Questo layer geospaziale, in formato vettoriale shapefile, viene acquisito automaticamente dal set di dati di [Open Street Map](https://osmbuildings.org/?lat=43.94654\&lon=12.63075\&zoom=16.0\&tilt=30).\
In alternativa, l'utente può caricare informazioni specifiche direttamente sulla piattaforma utilizzando l'opzione UPLOAD.

</details>

<details>

<summary>Tasso di infiltrazione</summary>

Questo layer rappresenta la capacità di infiltrazione del suolo, collegata alla classificazione dell'uso del suolo. In particolare, l'uso del suolo urbanizzato o industriale avrà un tasso di infiltrazione vicino allo zero, mentre il suolo agricolo o le aree verdi avranno un tasso vicino a uno.

Nella creazione del Digital Twin, Saferplaces utilizza il layer di uso del suolo a 10 m fornito da ESA ([The European Space Agency (ESA) WorldCover 10 m 2021](https://esa-worldcover.org/)) .

Per l'area della Regione Emilia Romagna si utilizza il mosaico dell'uso del suolo da CORINE LAND COVER.

Se sono disponibili informazioni più dettagliate, gli utenti possono caricare uno shapefile vettoriale con le classi di uso del suolo utilizzando la funzione UPLOAD.

\


</details>

<details>

<summary>Litologia</summary>

La litologia del suolo, definita dalle classi tessiturali (Sabbia, Argilla e Limo), influisce sulla capacità e velocità di infiltrazione dell'acqua, riducendo così il run-off superficiale e contribuendo a mitigare gli allagamenti.

Questa informazione è un input per il modello di infiltrazione di Green-Ampt, implementato in strumenti specifici.

Il dato tessiturale è integrato nella piattaforma Saferplaces, con copertura globale e risoluzione spaziale di 100 m, ed è fornito da [OpenLandMap](https://opengeohub.org/about-openlandmap/).

Per la Regione Emilia Romagna, sono disponibili classi tessiturali fornite dal [Servizio Geologico](https://mappegis.regione.emilia-romagna.it/gstatico/documenti/dati_pedol/tessitura_pianura.pdf). Inoltre, se l'utente dispone di dati più dettagliati, può utilizzare la funzione UPLOAD per caricare uno shapefile vettoriale con le classi di uso del suolo.

</details>

<details>

<summary>Dati Climatici</summary>

Nella fase di attivazione del servizio è possibile acquisire automaticamente i dati climatici dei dataset presenti in [Copernicus CDS.](https://cds.climate.copernicus.eu)

</details>

<details>

<summary>Immagini Satellitari</summary>

Le funzioni si processamento dei dati satellitari consentono di estrarre automaticamente le aree allagate analizzando le immagini [Copernicus Sentinel](https://dataspace.copernicus.eu/explore-data/data-collections) sia ottiche che SAR.

</details>

{% hint style="danger" %}
Per la creazione del nuovo progetto e del Digital Twin, i dati di input essenziali includono il DTM e il "Footprint" degli edifici.

Il DTM è l'input principale e cruciale richiesto dai modelli di pericolosità da alluvione di SaferPlaces.

Il wizard di attivazione richiede all'utente di selezionare tra i dati disponibili o di caricare i propri per:

* DTM
* EDIFICI
* INFILTRAZIONE
* LITOLOGIA

I dati climatici e le immagini satellitari vengono caricati in background durante l'attivazione del progetto.
{% endhint %}

