# 🌧️ Simulazione Allagamento Pluviale

#### Procedura per la Simulazione di Allagamenti Pluviali

Questa sezione descrive il processo per eseguire una simulazione di allagamento pluviale, causato da eventi meteorici di pioggia intensa e di breve durata. Tali eventi generano criticità nella gestione del deflusso delle acque superficiali, causando allagamenti particolarmente intensi in aree urbane depresse, come sottopassi.

## RAINFALL - SIMULAZIONE ALLAGAMENTO PLUVIALE

Il Wizard offre una procedura guidata dove l'utente definisce i seguenti dati e parametri di input:



<details>

<summary>Nome Simulazione</summary>

L'utente può modificare il nome assegnato automaticamente alla simulazione. Si consiglia di utilizzare caratteri standard e numeri senza spazi o simboli.

<img src="../../.gitbook/assets/COAST_NAME.png" alt="" data-size="original">



</details>

<details>

<summary>Definizione e caratterizzazione dell'Evento Pluviale -“<em>Pluvial scenario</em>” (1-RAIN)</summary>

IIl primo step, 1-RAIN, richiede la definizione e caratterizzazione dell'evento di pioggia da simulare in termini di intensità e durata.

L'utente può definire l'intensità di pioggia in mm in tre modi diversi:

1. **Uniforme su tutta l'area del dominio attivata**: Intensità (mm) costante su tutta l'area.
2. **Localizzata in una sottoarea con intensità non uniforme (disegno)**: Intensità variabile associata a un poligono disegnato dall'utente tramite lo strumento “_Rain_”  presente anche nella [barra-superiore.md](../../saferplaces-interfaccia-gui-web/barra-superiore.md "mention")
3. **Non uniforme (caricamento)**: Intensità variabile caricando un file raster in formato GeoTIFF, ad esempio da un prodotto RADAR METEO o MODELLO METEO FORECAST.
4. **Generato da prodotto satellitare**: Intensità (mm) determinata da un prodotto satellitare specifico.

L'utente può definire la durata dell'evento pluviale in ore (h) tramite il box "Total duration of the rainfall event".

<figure><img src="../../.gitbook/assets/image (66).png" alt=""><figcaption><p>1 - RAIN </p></figcaption></figure>

</details>

<details>

<summary>Modello Infiltrazione del terreno (2-INFILTRATION)</summary>

Gli utenti possono attivare il modulo di infiltrazione nel terreno durante l'esecuzione della simulazione.

Il Modulo di Infiltrazione si basa sul Modello Green-Ampt e utilizza dati di input dai layer definiti nello [step-3-tasso-di-infiltrazione-raster-geotiff.md](../../gemello-digitale-e-attivazione-nuovo-servizio/creazione-digital-twin-e-attivazione-del-servizio-nellarea-di-interesse/step-3-tasso-di-infiltrazione-raster-geotiff.md "mention") e [step-4-litologia-raster-geotiff.md](../../gemello-digitale-e-attivazione-nuovo-servizio/creazione-digital-twin-e-attivazione-del-servizio-nellarea-di-interesse/step-4-litologia-raster-geotiff.md "mention")

<figure><img src="../../.gitbook/assets/image (67).png" alt=""><figcaption><p>2 - INFILTRATION</p></figcaption></figure>

</details>

<details>

<summary>Vasche di Accumulo (3-STORAGE)</summary>

Nella piattaforma SaferPlaces, come misura per mitigare il rischio, è possibile inserire Vasche di Accumulo (Storage Tanks) nel dominio di calcolo. Queste vasche aiutano a ridurre il volume d'acqua che inonda una specifica area o sotto-bacino durante la simulazione.

Gli Storage Tanks si possono posizionare come elementi puntiformi usando lo strumento "_Draw storage tank_", disponibile sia nel Wizard che nel pannello.

Per generare una Storage Tank, cliccare su "NEW". Questo permette di posizionare le vasche e assegnare a ognuna la capacità volumetrica in m³.

Nel riquadro "Select Storage Tanks to simulate", l'utente può selezionare o rimuovere le Vasche di Accumulo presenti. Con "REMOVE ALL" si deselezionano tutte le vasche selezionate.

<figure><img src="../../.gitbook/assets/image (69).png" alt=""><figcaption><p>3 - storage</p></figcaption></figure>

</details>

<details>

<summary>Modello di calcolo (4-MODEL)</summary>

In questa sezione del Wizard l'utente ha la possibilità di:

1. Selezionare il modello di Allagamento (Hazard)
2. Attivare il calcolo del Dannno Economico (Damage)

I modelli di allagamento Pluviale disponibili sono:&#x20;

[safer\_rain.md](../modelli-di-allagamento-hazard-saferplaces/safer_rain.md "mention") - Modello Raster-based filling and spilling

[untrim.md](../modelli-di-allagamento-hazard-saferplaces/untrim.md "mention") - Modello Idrodinamico 2D

L'opzione di default è sempre il modello , che non prevede la definizione di ulteriori parametri "Setting".&#x20;

Nel caso si selezioni il modello [untrim.md](../modelli-di-allagamento-hazard-saferplaces/untrim.md "mention") occorre definire i seguenti parametri "Settings" cliccando sul task dedicato.&#x20;

* Slider - Durata della Simulazione in ore (h) -Tmax - Max time of simulation
* Slider - Coefficiente di scabrezza Manning  -Manning Coefficient
* Slider - Cella di calcolo in numero di pixel -nl - The number of pixel for each element side&#x20;
* Slider - Tempo di integrazione numerico  (min) -Delta T - Time simulation step
* Slider - Frequenza Stampa Output  (min) -Ti - Time shoot interval

L'attivazione del modello di calcolo del Danno Economico procede spuntando il check-box "Apply Damage"

<figure><img src="../../.gitbook/assets/Screenshot 2026-05-26 180148 (1).png" alt=""><figcaption></figcaption></figure>

<figure><img src="../../.gitbook/assets/Screenshot 2026-05-26 180136.png" alt=""><figcaption></figcaption></figure>

</details>

<details>

<summary>Note (5-NOTE)</summary>

In questa sezione del Wizard, l'utente, tramite il pulsante EDIT, ha la possibilità di aggiungere o togliere dettagli descrittivi alle note riassuntive sulla simulazione, che ha appena creato, che vengono scritte di default.&#x20;

<figure><img src="../../.gitbook/assets/image (72).png" alt=""><figcaption></figcaption></figure>

</details>

<details>

<summary>Definizione dei parametri del modello di calcolo, da definirsi in: Modello di calcolo (4-MODEL)</summary>

**Modello SaferPlaces:** Per il modello di calcolo SaferPlaces, non è necessaria la definizione di ulteriori parametri. Nelle simulazioni pluviali, il codice si attiva automaticamente.

&#x20;Nel caso delle simulazioni Pluviali si attiva automaticamente il codice [safer\_rain.md](../modelli-di-allagamento-hazard-saferplaces/safer_rain.md "mention"), in cui non ci sono impostazioni da scegliere

<figure><img src="../../.gitbook/assets/Screenshot 2026-05-27 113242.png" alt=""><figcaption></figcaption></figure>

**Modello UNTRIM:** Se si sceglie il modello idrodinamico UNTRIM, è fondamentale specificare diversi parametri di simulazione tramite gli slider:

* **Durata della Simulazione (ore):** Selezionare una durata pari o superiore all'evento di pioggia; ad esempio, se la pioggia dura 2 ore, la simulazione deve essere di almeno 2 ore.
* **Coefficiente di Manning (adimensionale):** Un coefficiente di attrito uniforme ipotizzato nel dominio di calcolo. Valore consigliato: 0.2.
* **nl (m):** Dimensione della cella definita dal numero di pixel in metri. Per esempio, scegliendo 50 con una risoluzione Lidar di 2 m si ottiene una cella di 100 m. Per Lidar a risoluzione 1-2 m, si consigliano valori tra 20 e 50. La dimensione della cella influisce sul numero totale di celle, che a sua volta incide sul tempo di calcolo. Si consiglia di mantenere le celle sotto le 20.000 per tempi di calcolo gestibili (3 minuti per ogni ora di simulazione).
* **Delta T - Passo di Integrazione Numerico (sec):** Si consiglia un passo di integrazione di 6 secondi.
* **Ti - Intervallo di Tempo per gli Output (min):** Definire l'intervallo per la produzione degli output.

<figure><img src="../../.gitbook/assets/UNtrim_impostazioni.png" alt=""><figcaption></figcaption></figure>



</details>

<details>

<summary>Attivazione Calcolo del danno economico - DAMAGE</summary>

Nella sezione "Model" della procedura guidata, è possibile attivare il calcolo del danno economico per ogni edificio inserito.

Il calcolo del danno economico viene eseguito inizialmente con le seguenti ipotesi:

1. Tutti gli edifici sono considerati residenziali, utilizzando una curva di vulnerabilità residenziale.
2. Valore dell'edificio fissato a 1000 euro/mq.

<img src="../../.gitbook/assets/image (49).png" alt="" data-size="original">



</details>

<details>

<summary>RUN SIMULAZIONE</summary>

Cliccando sul pulsante RUN l'utente attiva l'esecuzione della simulazione creata.\
Dopo il lancio, il Pannello di Controllo visualizzerà l'esecuzione del processo con lo stato di avanzamento.

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

Part 1

{% embed url="https://drive.google.com/file/d/17EsakehC2pH7954xikSBDWlIpLVDqbPr/view?usp=sharing" %}

Part2



{% embed url="https://drive.google.com/open?id=17HtQzcBDqB26EA3jnpWu_scpBxEe4PZj&usp=drive_fs" %}

