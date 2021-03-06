﻿---
title: 'Lync Server 2013: Rapporto riepilogativo attività peer-to-peer'
TOCTitle: Rapporto riepilogativo attività peer-to-peer
ms:assetid: e829a21e-9dfa-46ba-9b5b-077c175d6586
ms:mtpsurl: https://technet.microsoft.com/it-it/library/Gg615041(v=OCS.15)
ms:contentKeyID: 49302335
ms.date: 08/24/2015
mtps_version: v=OCS.15
ms.translationtype: HT
---

# Rapporto riepilogativo attività peer-to-peer in Lync Server 2013

 

_**Ultima modifica dell'argomento:** 2015-03-09_

Il Rapporto riepilogativo attività peer-to-peer offre informazioni generali sulle sessioni di comunicazione peer-to-peer. Una sessione peer-to-peer coinvolge in genere due soli utenti e non richiede l'utilizzo dei servizi di conferenza di Lync Server. Una conferenza, invece, coinvolge più di due utenti e richiede l'utilizzo dei servizi di conferenza di Microsoft Lync Server 2013. Le attività relative alle conferenze sono riepilogate nel Rapporto riepilogativo conferenze.

Nel Rapporto riepilogativo attività peer-to-peer è possibile trovare risposte a domande come le seguenti:

  - Quanti messaggi istantanei peer-to-peer si scambiano quotidianamente gli utenti?

  - Gli utenti stanno sfruttando le funzionalità di condivisione applicazioni e trasferimento file di Lync Server?

  - Gli utenti si lamentano della lentezza della rete in periodi specifici del giorno. Quanti minuti sono dedicati alle sessioni audio e video peer-to-peer durante tali periodi?

## Accesso al Rapporto riepilogativo attività peer-to-peer

Il Rapporto riepilogativo attività peer-to-peer è accessibile dalla home page dei rapporti di monitoraggio. Per aprire il [Rapporto di messaggistica istantanea peer-to-peer in Lync Server 2013](lync-server-2013-peer-to-peer-im-report.md), fare clic su una delle metriche seguenti:

  - Totale sessioni di messaggistica istantanea peer-to-peer

  - Totale messaggi istantanei peer-to-peer

In modo analogo, è possibile aprire il Rapporto voce e video peer-to-peer facendo clic su una delle metriche seguenti:

  - Totale sessioni audio peer-to-peer

  - Totale minuti sessioni audio peer-to-peer

  - Totale sessioni audio peer-to-peer

  - Totale minuti sessioni audio peer-to-peer

## Utilizzo ottimale del Rapporto riepilogativo attività peer-to-peer

Nella parte inferiore del Rapporto riepilogativo attività peer-to-peer sono disponibili i totali per le metriche, come Totale sessioni di messaggistica istantanea peer-to-peer e Totale messaggi istantanei peer-to-peer. Questi valori offrono un rapido riepilogo delle informazioni dettagliate disponibili nel corpo del rapporto.

## Filtri

I filtri consentono di ottenere un set di dati più specifico o di visualizzare in modo diverso i dati restituiti. Il Rapporto riepilogativo attività peer-to-peer consente ad esempio di scegliere la modalità di raggruppamento dei dati. In questo caso le attività sono raggruppate per ora, giorno, settimana o mese.

Nella tabella seguente sono elencati i filtri che è possibile utilizzare con il Rapporto riepilogativo attività peer-to-peer.

### Filtri del Rapporto riepilogativo attività peer-to-peer

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th>Nome</th>
<th>Descrizione</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><strong>Da</strong></p></td>
<td><p>Data e ora di inizio per l'intervallo di tempo. Per visualizzare i dati in base all'ora, inserire sia la data che l'ora di inizio come segue:</p>
<p>7/17/2012 1:00 PM</p>
<p>Se non si specifica l'ora di inizio, il rapporto inizia automaticamente alla mezzanotte del giorno specificato. Per visualizzare i dati in base al giorno, immettere solo la data:</p>
<p>7/17/2012</p>
<p>Per visualizzare i dati in base alla settimana o al mese, immettere una data che rientra nella settimana o nel mese in base a cui deve essere effettuata la visualizzazione. Non è necessario immettere il primo giorno della settimana o del mese:</p>
<p>7/13/2012</p>
<p>Le settimane vengono calcolate sempre dal lunedì alla domenica.</p></td>
</tr>
<tr class="even">
<td><p><strong>A</strong></p></td>
<td><p>Data e ora di fine per l'intervallo di tempo. Per visualizzare i dati in base all'ora, inserire sia la data che l'ora di fine come segue:</p>
<p>7/17/2012 1:00 PM</p>
<p>Se non si specifica l'ora di fine, il rapporto termina automaticamente alla mezzanotte del giorno specificato. Per visualizzare i dati in base al giorno, immettere solo la data:</p>
<p>7/17/12012</p>
<p>Per visualizzare i dati in base alla settimana o al mese, immettere una data che rientra nella settimana o nel mese in base a cui deve essere effettuata la visualizzazione. Non è necessario immettere il primo giorno della settimana o del mese:</p>
<p>7/13/2012</p>
<p>Le settimane vengono calcolate sempre dal lunedì alla domenica.</p></td>
</tr>
<tr class="odd">
<td><p><strong>Intervallo</strong></p></td>
<td><p>Intervallo di tempo. Selezionare una delle opzioni seguenti:</p>
<ul>
<li><p>Orario (è possibile visualizzare un massimo di 25 ore)</p></li>
<li><p>Giornaliero (è possibile visualizzare un massimo di 31 giorni)</p></li>
<li><p>Settimanale (è possibile visualizzare un massimo di 12 settimane)</p></li>
<li><p>Mensile (è possibile visualizzare un massimo di 12 mesi)</p></li>
</ul>
<p>Se le date di inizio e fine superano il numero massimo di valori consentiti per l'intervallo selezionato, verrà visualizzato solo il numero massimo di valori, a partire dalla data di inizio. Se ad esempio si seleziona l'intervallo Giornaliero con 7/17/2012 come data di inizio e 2/28/2012 come data di fine, verranno visualizzati i dati dalla mezzanotte del 8/7/2012 12:00 AM alla mezzanotte del 9/7/2012 12:00 AM, ovvero i dati per un totale di 31 giorni.</p></td>
</tr>
</tbody>
</table>


## Metriche

Nella tabella seguente sono indicate le informazioni fornite nel Rapporto riepilogativo attività peer-to-peer.

### Metriche del Rapporto riepilogativo attività peer-to-peer

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th>Nome</th>
<th>Elemento utilizzabile per eseguire l'ordinamento?</th>
<th>Descrizione</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><strong>Orario</strong></p>
<p><strong>Giornaliero</strong></p>
<p><strong>Settimanale</strong></p>
<p><strong>Mensile</strong></p></td>
<td><p>No</p></td>
<td><p>Indica l'intervallo di tempo selezionato sulla barra degli strumenti dei filtri. Ove applicabile, è possibile fare clic su un determinato intervallo di tempo per visualizzare informazioni dettagliate relative a tale intervallo. Se ad esempio si sta utilizzando l'intervallo giornaliero e si fa clic su 17/07/2012, verranno visualizzate le attività di registrazione degli utenti per tale data, suddivise per ore.</p></td>
</tr>
<tr class="even">
<td><p><strong>Totale sessioni peer-to-peer</strong></p></td>
<td><p>No</p></td>
<td><p>Numero totale di sessioni peer-to-peer condotte, indipendentemente dal tipo.</p></td>
</tr>
<tr class="odd">
<td><p><strong>Totale sessioni di messaggistica istantanea peer-to-peer</strong></p></td>
<td><p>No</p></td>
<td><p>Numero totale di sessioni di messaggistica istantanea condotte. Se si fa clic su questo elemento, verrà visualizzato il Rapporto di messaggistica istantanea peer-to-peer relativo al periodo di tempo selezionato.</p></td>
</tr>
<tr class="even">
<td><p><strong>Totale messaggi istantanei peer-to-peer</strong></p></td>
<td><p>No</p></td>
<td><p>Numero totale di messaggi istantanei inviati in sessioni peer-to-peer. Se si fa clic su questo elemento, verrà visualizzato il Rapporto di messaggistica istantanea peer-to-peer relativo al periodo di tempo selezionato.</p></td>
</tr>
<tr class="odd">
<td><p><strong>Totale sessioni audio peer-to-peer audio</strong></p></td>
<td><p>No</p></td>
<td><p>Numero totale di chiamate audio peer-to-peer. Se si fa clic su questo campo, verrà visualizzato il Rapporto voce e video peer-to-peer relativo al periodo di tempo selezionato.</p></td>
</tr>
<tr class="even">
<td><p><strong>Totale minuti sessioni audio peer-to-peer</strong></p></td>
<td><p>No</p></td>
<td><p>Quantità totale di tempo impiegato in sessioni audio peer-to-peer. Se si fa clic su questo elemento, verrà visualizzato il Rapporto di messaggistica istantanea peer-to-peer relativo al periodo di tempo selezionato.</p></td>
</tr>
<tr class="odd">
<td><p><strong>Media minuti sessioni audio peer-to-peer</strong></p></td>
<td><p>No</p></td>
<td><p>Quantità media di tempo impiegato in sessioni audio peer-to-peer. Il valore viene calcolato dividendo il tempo totale per il numero totale delle sessioni audio.</p></td>
</tr>
<tr class="even">
<td><p><strong>Totale sessioni video peer-to-peer</strong></p></td>
<td><p>No</p></td>
<td><p>Numero totale di videochiamate peer-to-peer. Si noti che le sessioni video vengono conteggiate anche come sessioni audio. Ogni sessione video viene conteggiata come una sessione video e una sessione audio. Se si fa clic su questo elemento, verrà visualizzato il Rapporto di messaggistica istantanea peer-to-peer relativo al periodo di tempo selezionato.</p></td>
</tr>
<tr class="odd">
<td><p><strong>Totale minuti sessioni video peer-to-peer</strong></p></td>
<td><p>No</p></td>
<td><p>Quantità totale di tempo impiegato in sessioni video peer-to-peer. Se si fa clic su questo elemento, verrà visualizzato il Rapporto di messaggistica istantanea peer-to-peer relativo al periodo di tempo selezionato.</p></td>
</tr>
<tr class="even">
<td><p><strong>Media minuti sessioni video peer-to-peer</strong></p></td>
<td><p>No</p></td>
<td><p>Quantità media di tempo impiegato in sessioni video peer-to-peer. Il valore viene calcolato dividendo il tempo totale per il numero totale delle sessioni video.</p></td>
</tr>
<tr class="odd">
<td><p><strong>Totale sessioni di trasferimento di file peer-to-peer</strong></p></td>
<td><p>No</p></td>
<td><p>Numero totale di sessioni peer-to-peer che includono trasferimenti di file.</p></td>
</tr>
<tr class="even">
<td><p><strong>Totale sessioni di condivisione applicazioni peer-to-peer</strong></p></td>
<td><p>No</p></td>
<td><p>Numero totale di sessioni peer-to-peer che includono la condivisione di applicazioni.</p></td>
</tr>
</tbody>
</table>

