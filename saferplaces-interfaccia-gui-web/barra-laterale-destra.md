---
icon: magnifying-glass
---

# Barra Laterale destra

A destra della schermata principale, troverai un pannello che elenca tutti i layer geospaziali ("layers") utilizzati per l'attivazione del  [gemello-digitale-digital-twin.md](../gemello-digitale-e-attivazione-nuovo-servizio/gemello-digitale-digital-twin.md "mention") e i layer relativi ai risultati delle [Broken link](broken-reference "mention").

I layers geospaziali del progetto sono organizzati nei seguenti gruppi di layers:

* DAMAGE - gruppo di layers dei risultati delle simulazioni di [modello-di-danno-economico-safer\_damage.md](../simulazioni-allagamento-pericolo-e-danno/modello-di-danno-economico-safer_damage.md "mention")
* COAST - gruppo di layers dei risultati delle simulazioni di [simulazione-allagamento-costiero.md](../simulazioni-allagamento-pericolo-e-danno/definizione-scenario-source-scenarios/simulazione-allagamento-costiero.md "mention")
* RIVER - gruppo di layers dei risultati delle simulazioni di [simulazione-allagamento-fluviale.md](../simulazioni-allagamento-pericolo-e-danno/definizione-scenario-source-scenarios/simulazione-allagamento-fluviale.md "mention")
* RAIN - gruppo di layers dei risultati delle simulazioni di [simulazione-allagamento-pluviale.md](../simulazioni-allagamento-pericolo-e-danno/definizione-scenario-source-scenarios/simulazione-allagamento-pluviale.md "mention")
* Digital Twin - gruppo di layer utilizzati e/o caricati nella fase di [creazione-digital-twin-e-attivazione-del-servizio-nellarea-di-interesse](../gemello-digitale-e-attivazione-nuovo-servizio/creazione-digital-twin-e-attivazione-del-servizio-nellarea-di-interesse/ "mention")
  * layer DTM - relativo al Modello Digitale del Terreno
  * layers di classe tessiturale  litologica (Sand e Clay)
  * layer di infiltrazione ottenuto riclassificando uso del suolo
  * layer foot print (sagoma) degli edifici - OSM o caricato da utente
* Bluespots - gruppo di layers che contiene i vettoriali shapefile di:
  * bluespots.labels - vettoriale delle depressioni dei sotto-bacini (watersheds.labels)
  * stream - veootoriale degli "streams" ovvero line di flusso che idrologicamente connettono i diversi "Bluespots"
  * watersheds.labels - vettoriale dei sotto-bacini idrologici
* Layer Mappe di Background
  * Google Map Hybrid o satellite
  * OSM
  * Stamen

<figure><img src="../.gitbook/assets/layers_destra.png" alt=""><figcaption></figcaption></figure>

Facendo clic con il pulsante destro del mouse su ciascun layer o relativo gruppo , l'utente può attivare alcune funzioni utili elencate nella figura&#x20;

<figure><img src="../.gitbook/assets/image (5).png" alt=""><figcaption><p>Funzioni layer barra destra</p></figcaption></figure>

In particolare è possibile:

* EXPAND ALL - espandere&#x20;
* COLLAPS ALL - collassare tutti i layer
* ZOOM TO LAYER - zoomare sul layer selezionato
* OPACITY - aumentare o diminuire la sua opacità
* REMOVE LAYER rimuovere layer dal progetto
* EXPORT - salvare su file il layer (Geotiff o Shapefile)
* UP/DOWN - spostare la sua posizione in alto/basso&#x20;
* PORPERTIES - ispezionare e modificare  le sue proprietà.

Attivando le PROPERTIES sul laye di interesse è possibile in particolare:

* SOURCE - visualizzare i metadati del layer&#x20;

<figure><img src="../.gitbook/assets/porperties_1.png" alt=""><figcaption></figcaption></figure>

* SYMBOLOGY - modificare la scala di colori del layer raster o vettoriale

<figure><img src="../.gitbook/assets/properties_symbology.png" alt=""><figcaption></figcaption></figure>

<figure><img src="../.gitbook/assets/properties_symbologiy_vector.png" alt=""><figcaption></figcaption></figure>



