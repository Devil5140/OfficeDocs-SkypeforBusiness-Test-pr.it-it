﻿---
title: "Lync Server 2013: Crea/modifica configuraz. di registraz. dettagli chiamata"
TOCTitle: "Lync Server 2013: Crea/modifica configuraz. di registraz. dettagli chiamata"
ms:assetid: c830be5a-2a82-468d-9c46-d3fec0f79fd0
ms:mtpsurl: https://technet.microsoft.com/it-it/library/JJ721878(v=OCS.15)
ms:contentKeyID: 49887749
ms.date: 08/24/2015
mtps_version: v=OCS.15
ms.translationtype: HT
---

# Creare o modificare una raccolta di impostazioni di configurazione di registrazione dettagli chiamata

 

_**Ultima modifica dell'argomento:** 2015-03-09_

La registrazione dettagli chiamata consente di tenere traccia dell'utilizzo di elementi quali le sessioni di messaggistica istantanea peer-to-peer, le chiamate telefoniche VoIP (Voice over Internet Protocol) e le conferenze telefoniche. Questi dati relativi all'utilizzo includono informazioni sull'utente chiamante e sull'utente chiamato, sulla data della chiamata e sulla durata della conversazione.

Quando si installa Microsoft Lync Server 2013, viene creata automaticamente una singola raccolta globale di impostazioni di configurazione di registrazione dettagli chiamata. Gli amministratori possono inoltre creare impostazioni personalizzate nell'ambito del sito che, se utilizzate, hanno la precedenza sulle impostazioni globali. Se ad esempio si creano impostazioni dell'ambito del sito Redmond, verranno utilizzate tali impostazioni e non le impostazioni globali per la gestione della registrazione dettagli chiamata nel sito Redmond.

Per creare impostazioni di configurazione di registrazione dettagli chiamata, è possibile utilizzare il Pannello di controllo di Lync Server oppure il cmdlet [New-CsCdrConfiguration](https://docs.microsoft.com/en-us/powershell/module/skype/New-CsCdrConfiguration). Per modificare impostazioni esistenti, è possibile utilizzare il Pannello di controllo di Lync Server oppure il cmdlet [Set-CsCdrConfiguration](https://docs.microsoft.com/en-us/powershell/module/skype/Set-CsCdrConfiguration). Se si utilizza il Pannello di controllo di Lync Server per creare o modificare impostazioni, saranno disponibili le opzioni seguenti:


<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th>Impostazione dell'interfaccia utente</th>
<th>Parametro di PowerShell</th>
<th>Descrizione</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p>Nome</p></td>
<td><p>Identity</p></td>
<td><p>Identificatore univoco delle impostazioni di configurazione di registrazione dettagli chiamata che si desidera creare. Queste impostazioni possono essere create solo nell'ambito del sito.</p></td>
</tr>
<tr class="even">
<td><p>Abilita monitoraggio registrazioni dettagli chiamata</p></td>
<td><p>EnableCDR</p></td>
<td><p>Indica se la registrazione dettagli chiamata è abilitata o meno.</p></td>
</tr>
<tr class="odd">
<td><p>Abilita eliminazione registrazioni dettagli chiamata</p></td>
<td><p>EnablePurging</p></td>
<td><p>Indica se le registrazioni dettagli chiamata saranno eliminate periodicamente dal relativo database.</p></td>
</tr>
<tr class="even">
<td><p>Mantieni registrazioni dettagli chiamata per durata massima (giorni)</p></td>
<td><p>KeepCallDetailForDays</p></td>
<td><p>Indica per quanti giorni le registrazioni dettagli chiamata verranno mantenute nel relativo database. Le eventuali registrazioni antecedenti al numero di giorni specificato verranno eliminate automaticamente. Si noti che questa operazione verrà eseguita soltanto se è stata abilitata l'eliminazione.</p></td>
</tr>
<tr class="odd">
<td><p>Mantieni dati delle segnalazioni errori per durata massima (giorni)</p></td>
<td><p>KeepErrorReportForDays</p></td>
<td><p>Indica per quanti giorni verranno mantenuti i rapporti sugli errori di registrazione dettagli chiamata. Gli eventuali rapporti antecedenti al numero di giorni specificato verranno eliminati automaticamente. I rapporti sugli errori di registrazione dettagli chiamata sono rapporti di diagnostica caricati da applicazioni client.</p></td>
</tr>
</tbody>
</table>



> [!NOTE]
> I nuovi cmdlet New-CsCdrConfiguration e Set-CsCdrConfiguration includono ulteriori opzioni non disponibili nel Pannello di controllo di Lync Server. Per ulteriori informazioni, vedere nella Guida gli argomenti relativi a <A href="https://docs.microsoft.com/en-us/powershell/module/skype/New-CsCdrConfiguration">New-CsCdrConfiguration</A> e <A href="https://docs.microsoft.com/en-us/powershell/module/skype/Set-CsCdrConfiguration">Set-CsCdrConfiguration</A>.



## Per creare impostazioni di configurazione di registrazione dettagli chiamata tramite il Pannello di controllo di Lync Server

1.  Nel Pannello di controllo di Lync Server fare clic su **Monitoraggio e archiviazione**.

2.  Nella scheda **Registrazione dettagli chiamata** fare clic su **Nuovo**.

3.  Nella finestra di dialogo **Seleziona un sito** selezionare il sito in cui devono essere create le nuove impostazioni di configurazione. Se la finestra di dialogo è vuota, è stata già assegnata una raccolta di impostazioni di configurazione di registrazione dettagli chiamata a tutti i siti. Ogni sito è limitato a una sola raccolta di questo tipo. In tal caso, è possibile eliminare e quindi ricreare le impostazioni oppure modificare semplicemente le impostazioni esistenti.

4.  Nella finestra di dialogo **Nuova impostazione di registrazione dettagli chiamata** selezionare le opzioni desiderate e quindi fare clic su **Commit**.

## Per modificare impostazioni di configurazione di registrazione dettagli chiamata esistenti tramite il Pannello di controllo di Lync Server

1.  Nel Pannello di controllo di Lync Server fare clic su **Monitoraggio e archiviazione**.

2.  Fare doppio clic sulla raccolta di impostazioni da modificare oppure selezionarla. Fare clic su **Modifica** e quindi su **Mostra dettagli**. Si noti che è possibile modificare solo una raccolta per volta. Per applicare le stesse modifiche a più raccolte, utilizzare Lync Server Management Shell.

3.  Nella finestra di dialogo **Modifica impostazione di registrazione dettagli chiamata** selezionare le opzioni desiderate e quindi fare clic su **Commit**.

## Per creare impostazioni di configurazione di registrazione dettagli chiamata tramite i cmdlet di Lync Server Management Shell

Le impostazioni di configurazione di registrazione dettagli chiamata possono essere create anche utilizzando Windows PowerShell e il cmdlet **New-CsCdrConfiguration**. È possibile eseguire questo cmdlet da Lync Server 2013 Management Shell o da una sessione remota di Windows PowerShell. Per informazioni dettagliate sull'utilizzo di Windows PowerShell remoto per la connessione a Lync Server, vedere l'articolo "Avvio rapido: gestione di Microsoft Lync Server 2010 con PowerShell remoto" nel blog su Windows PowerShell per Lync Server all'indirizzo [http://go.microsoft.com/fwlink/p/?linkId=255876](http://go.microsoft.com/fwlink/p/?linkid=255876).

## Per creare una nuova raccolta di impostazioni di configurazione di registrazione dettagli chiamata

  - Il comando seguente crea una nuova raccolta di impostazioni di configurazione di registrazione dettagli chiamata applicate al sito Redmond:
    
        New-CsCdrConfiguration -Identity "site:Redmond"

## Per creare una raccolta di impostazioni di configurazione di registrazione dettagli chiamata che disabilitano la registrazione dettagli chiamata

  - Poiché nel comando precedente non sono stati specificati parametri, eccetto il parametro obbligatorio Identity, la nuova raccolta di impostazioni di configurazione utilizzerà i valori predefiniti per le relative proprietà. Per creare impostazioni basate su valori di proprietà diversi, è sufficiente includere il parametro appropriato e il valore corrispondente. Per creare ad esempio una raccolta di impostazioni di configurazione di registrazione dettagli chiamata che consentano per impostazione predefinita di disabilitare la registrazione dettagli chiamata, utilizzare un comando simile al seguente:
    
        New-CsCdrConfiguration -Identity "site:Redmond" -EnableCDR $False

## Per specificare più valori di proprietà quando si crea una nuova raccolta di impostazioni di configurazione di registrazione dettagli chiamata

  - È possibile modificare più valori di proprietà includendo più parametri. Il comando seguente ad esempio configura le nuove impostazioni in modo da mantenere le registrazioni dettagli chiamata per 30 giorni e i rapporti sugli errori per 90 giorni:
    
        New-CsCdrConfiguration -Identity "site:Redmond" -KeepCallDetailForDays 30 -KeepErrorReportForDays 90

Per ulteriori informazioni, vedere l'argomento della Guida relativo al cmdlet [New-CsCdrConfiguration](https://docs.microsoft.com/en-us/powershell/module/skype/New-CsCdrConfiguration).

