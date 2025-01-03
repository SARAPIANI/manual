# 🌧️ Simulazione Allagamento Pluviale

In questa sezione si descrive la procedura per l'esecuzione di una simulazione di allagamento di tipo Pluviale, ovvero determinato da un evento meteorico di pioggia intensa e in genere di breve durata che genera una forte criticità nella gestione del deflusso delle acque superficiali con allagamenti in aree urbane particolarmente intensi in zone depresse (sottopassi).

## RAINFALL - SIMULAZIONE ALLAGAMENTO PLUVIALE

Il Wizard offre una procedura guidata dove l'utente definisce i seguenti dati e parametri di input:



<details>

<summary>Nome Simulazione</summary>

L'utente può modificare il nome della simulaizone editando liberamente il nome che viene assegnato automaticamente. Si consiglia di utilizzare un nome composto da caratteri standard e numeri senza uso dello spazio e/o simboli.

<img src="../../.gitbook/assets/COAST_NAME.png" alt="" data-size="original">



</details>

<details>

<summary>Definizione e caratterizzazione  dell'evento Pluviale -“<em>Pluvial scenario</em>” (1-RAIN)</summary>

Il primo step 1-RAIN richiede la definizione e caratterizzazione in termini di intensità e durata dell'evento meteorico di pioggia che si intende simulare.

L'utente ha la possibilità di definire l'intensità di pioggia in mm che intende simulare in tre diverse modailità:

1. Evento Pluviale di intensità (mm) UNIFORM su tutta l'area del dominio attivata
2. Evento Pluviale localizzato in una sottoarea con intensità (mm) NON-UNIFORM(draw) associata ad un poligono che disegnato dall'utente attraverso  lo strumento “_Rain_” presente nella [barra-superiore.md](../../saferplaces-interfaccia-gui-web/barra-superiore.md "mention")
3. Evento Pluviale di intensità (mm) NON UNIFORM (upload) caricando un file raster formato GeoTIFF - ad esempio fornito da prodotto RADAR METEO o MODELLO METEO FORECAST
4. Evento Pluviale con intensità (mm) generato dal prodotto satellitare @@@@

L'utente ha la possibilità di definire la durata temporale in ore (h) dell'evento meteo pluviale che intende simulare mediate il box "Total duration of the rainfall event"&#x20;

<img src="../../.gitbook/assets/1_RAIN.png" alt="" data-size="original">

</details>

<details>

<summary>Modello Infiltrazione del terreno (2-INFILTRATION)</summary>

L'utente ha la possibilità di attivare il modulo di infiltrazione nel terreno nell'esecuzione della simulazione.

Il Modulo di infiltrazione è basato sul Modello Green-Ampt ed utilizza come dato di input i layer definiti nello [step-3-tasso-di-infiltrazione-raster-geotiff.md](../../gemello-digitale-e-attivazione-nuovo-servizio/creazione-digital-twin-e-attivazione-del-servizio-nellarea-di-interesse/step-3-tasso-di-infiltrazione-raster-geotiff.md "mention") e [step-4-litologia-raster-geotiff.md](../../gemello-digitale-e-attivazione-nuovo-servizio/creazione-digital-twin-e-attivazione-del-servizio-nellarea-di-interesse/step-4-litologia-raster-geotiff.md "mention")

<img src="../../.gitbook/assets/2_INFILTRATION.png" alt="" data-size="original">

</details>

<details>

<summary>Vasche di Accumulo (3-STORAGE)</summary>

Come misura di mitigazione dell'hazard la piattaforma SaferPlaces consente all'utente di inserire nel dominio di calcolo delle Vasche di Accumulo (Storage Tanks) che permettono di ridurre il volume di acqua che allaga una specifica area o sotto-bacino del dominio oggetto della simulazione.

Gli Storage Tanks possono essere localizzato come elementi puntiformi mediante l'attivazione dello strumento “_Draw storage tank_”, presente sia nel Wizard che nella  [barra-superiore.md](../../saferplaces-interfaccia-gui-web/barra-superiore.md "mention").

Il tool di generazione delle Storage Tank (Vasche di Accumulo) si attiva cliccando sul Pulsante "NEW" e consente di localizzare le vasche e di associare a ciascuna vasca la capacità volumetrica in mc.

Nel riquadro denominato "Select Storage Tanks to simulate" l'utente ha la possibilità di selezionare e/o rimuvere le Vasche di Accumulo presenti nel dominio. Con il Pulsante "REMOVE ALL" si de-selezionano tutte le vasche presenti.

<img src="../../.gitbook/assets/3_STORAGE.png" alt="" data-size="original">

</details>

<details>

<summary>Modello di calcolo (4-MODEL)</summary>

In questa sezione del Wizard l'utente ha la possibilità di&#x20;

1. Selezionare il modello di Allagamento (Hazard)
2. Attivare il calcolo del Dannno Economico (Damage)

I modelli di allagamento Pluviale disponibili sono:&#x20;

[safer\_rain.md](../modelli-di-allagamento-hazard-saferplaces/safer_rain.md "mention") - Modello Raster-based filling and spilling

[untrim.md](../modelli-di-allagamento-hazard-saferplaces/untrim.md "mention") - Modello Idrodinamico 2D

L'opzione di default è sempre il modello [safer\_rain.md](../modelli-di-allagamento-hazard-saferplaces/safer_rain.md "mention")

Nel caso si selezioni il modello [untrim.md](../modelli-di-allagamento-hazard-saferplaces/untrim.md "mention") occorre definire i seguenti parametri "Settings" cliccando sul task dedicato.&#x20;

* Slider - Durata della Simulazione in ore (h) -Tmax - Max time of simulation
* Slider - Coefficiente di scabrezza Manning  -Manning Coefficient
* Slider - Cella di calcolo in numero di pixel -nl - The number of pixel for each element side&#x20;
* Slider - Tempo di integrazione numerico  (min) -Delta T - Time simulation step
* Slider - Frequenza Stampa Output  (min) -Ti - Time shoot interval

L'attivazione del modello di calcolo del Danno Economico procede spuntando il check-box "Apply Damage"

<img src="../../.gitbook/assets/4_MODEL.png" alt="" data-size="original">

</details>

<details>

<summary>Definizione dei parametri del modello di calcolo</summary>

Modello SaferPlaces - Nel caso si sia selezionato il modello di calcolo SaferPlaces non è necessario specificare ulteriori parametri di calcolo. Nel caso delle simulazioni Pluviali si attiva automaticamente il codice [safer\_rain.md](../modelli-di-allagamento-hazard-saferplaces/safer_rain.md "mention")\


<img src="../../.gitbook/assets/image (50).png" alt="" data-size="original">

Modello UNTRIM - Nel caso si sia selezionato il modello idrodinamico [untrim.md](../modelli-di-allagamento-hazard-saferplaces/untrim.md "mention") occorre specificare alcuni parametri molto importati di simulazione selezionando con gli slider i valori.

* Durata della Simulazione in ore (h) - il valore da selezionare corrisponde alla durata dell'evento che si vuole simulare, ad esempio se l'evento pioggia dura 2h la durata della simulazione deve essere maggiore o uguale alla durata dell'evento
* Manning Coefficient (adim) - coefficiente di attrito di Manning che viene ipotizzato uniforme nel dominio di calcolo. Valore Consigliato 0.2
* nl (m) - Dimensione della cella di calcolo quadrata definita come numero dei pixel in metri. Ad esempio se si seleziona 50 e il lidar del dominio ha una risoluzione di 2 m allora la dimensione della cella è pari a 100m. In questo caso nel caso di Lidar a risoluzione 1/2 si consigli un valore tra 20 e 50. La dimensione della cella di calcolo influisce sul numero totale delle celle di calcolo in funzione anche della estensione del dominio. Il numero totale influisce a sua volta sul tempo di calcolo. Si consiglia rimanere al di sotto delle 20000 celle nell'intero dominio per avere tempi di calcolo contenuti (3 minuti per ogni ora di simulazione )
* Delta T - Passo di imntegrazione numerico (sec) - Si consiglia di selezionare il passo di integrazione pari a 6 secondi.
* Ti - Time Shot Interval (min) - Qui si definisce l'intervallo temporale di produzione degli output
*

![](<../../.gitbook/assets/image (51).png>)

![](<../../.gitbook/assets/image (52).png>)



</details>

<details>

<summary>Attivazione Calcolo del danno economico - DAMAGE</summary>

Nella procedura guidata alla pagina "Model" è possibile attivare il calcolo del danno economico per ciascun edificio inserito.



Il calcolo del Danno Economico viene eseguito in prima analisi applicando le seguenti ipotesi:

1. Tutti gli edifici cono considerati residenziali con un curva di vulnerabilità residenziale
2.  Valore dell'edificio pari a 1000 euro/mq\


    <figure><img src="../../.gitbook/assets/image (49).png" alt=""><figcaption></figcaption></figure>



</details>

<details>

<summary>Inserimento metadati e descrizione della  simulazione generata (5- NOTE)</summary>

Cliccando sul pulsante EDIT l'utente può attivare una casella di testo dove inserire metadati e dettagli descrittivi della simulazione che ha appena creato.

<img src="../../.gitbook/assets/5_NOTE_RUN.png" alt="" data-size="original">

</details>

<details>

<summary>RUN SIMULAZIONE</summary>

Cliccando sul pulsante RUN l'utente attiva l'esecuzione della simulazione creata.\
Dopo l'avvio sul pannello Control Panel si aggiungerà l'esecuzione del processo attivato con indicazione dello stato di avanzamento.

<img src="../../.gitbook/assets/control_panel.png" alt="" data-size="original">

</details>

## Esempio di simulazione pluviale pioggia uniforme con SAFER

{% embed url="https://drive.google.com/open?id=1uLE_G6aEek9T6H49Zs5TXAfltNfbtoVb&usp=drive_fs" %}

## Esempio di simulazione pluviale pioggia non uniforme con SAFER

{% embed url="https://drive.google.com/open?id=1PnqEcQY3OxSbL4zjLkJH9tE2ihTJObsg&usp=drive_fs" %}



## Esempio di simulazione pluviale con Storage Tank



{% embed url="https://drive.google.com/open?id=1aRcVm58KGtN7-KWEy9y06h-qdiCVclN8&usp=drive_fs" %}

## Esempio di simulazione pluviale con Modifica Infiltrazione



{% embed url="https://drive.google.com/open?id=1uAfjjMyb7TrVAHRHZaQdvY-CEnOUBUjG&usp=drive_fs" %}

## #Esempio di simulazione pluviale - Modello UNTRIM



