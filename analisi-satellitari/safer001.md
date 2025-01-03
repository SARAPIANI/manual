---
description: >-
  Estrazione automatica della maschera relativa all'estensione delle aree
  allagate in condizione post-evento.
---

# 🛠️ Safer001

Attivanto sulla barra in alto Lo strumento “_Satellite_”  si attiva la funzione , denominata Safer001, che consente all'utente di generare automaticamente la  maschera delle aree allagate all'interno del dominio di calcolo attivato.&#x20;

L'area allagata farà riferimento ad uno specifico evento temporale della durata di qualche giorno e verrà prodotta analizzando immagini sia SAR che Ottiche da Copernicus Sentinel e COSMO SKY MED.

&#x20;Il pannello di apertura richiede all'utente di inserire i quattro parametri di input richiesti dal modulo Safer001:

\- _from date_: data dell'evento di alluvione,

\- _lag (days)_: n° di giorni consecutivi all'evento, in cui il sistema deve verificare la disponibilità dei dati,

\- _bbox_: bounding box o area di interesse,

\- _DEM_: il miglior DEM disponibile sarà passato al modulo Safer001.

<figure><img src="../.gitbook/assets/image (40).png" alt=""><figcaption><p>Safer001 - Estrazione automatica della maschera di acqua alluvionale</p></figcaption></figure>



