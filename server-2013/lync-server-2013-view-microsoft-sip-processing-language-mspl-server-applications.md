﻿---
title: "Lync Server 2013: Visualizza app server MSPL (MS SIP Processing Language)"
TOCTitle: Visualizzare le applicazioni server MSPL (Microsoft SIP Processing Language)
ms:assetid: b7df1323-b6bd-4925-8fe6-5241c91fe51b
ms:mtpsurl: https://technet.microsoft.com/it-it/library/Gg182575(v=OCS.15)
ms:contentKeyID: 49301767
ms.date: 08/24/2015
mtps_version: v=OCS.15
ms.translationtype: HT
---

# Visualizzare le applicazioni server MSPL (Microsoft SIP Processing Language) in Lync Server 2013

 

_**Ultima modifica dell'argomento:** 2014-09-26_

Un'applicazione server MSPL (Microsoft SIP Processing Language) è un'applicazione script in cui viene utilizzato un linguaggio di script anziché API Microsoft Lync 2010. Il linguaggio MSPL garantisce un controllo più granulare sui comportamenti dei proxy e dei filtri, oltre a funzionalità per l'invio di messaggi specifici ad applicazioni SIP basate sulle transazioni. MSPL viene utilizzato in particolare per filtrare ed eseguire il routing di messaggi SIP. Le applicazioni MSPL vengono eseguite nello stesso processo del modulo UserServices, mentre un programma basato su API Lync 2010 viene eseguito in un processo separato.

È possibile utilizzare la pagina **Applicazione server** nel gruppo **Topologia** del Pannello di controllo di Lync Server per visualizzare un elenco delle applicazioni server MSPL eseguite nei Front End Server nell'ambiente Lync Server 2013. L'elenco mostra gli script disponibili per ogni pool e indica se sono abilitati o critici. Gli script vengono eseguiti nell'ordine in cui sono elencati.

Tali script includono i seguenti:

  - ClientVersionFilter fornisce all'amministratore un metodo per specificare la versione dei client supportati da un pool. Il filtro della versione client controlla la versione del client e può impedire l'accesso al client o visualizzare un messaggio all'utente per segnalare che sta utilizzando un client non supportato. Il filtro della versione client può inoltre essere configurato per la visualizzazione di un messaggio contenente l'URL della versione scaricabile più recente del client.

  - TranslationService converte un numero composto da un utente in numero in formato E.164 in base alle regole di normalizzazione definite dall'amministratore. Per informazioni dettagliate, vedere [Regole di conversione in Lync Server 2013](lync-server-2013-translation-rules.md).

  - IncomingFederation impone la convalida di federazione a livello di tenant per i messaggi tra tenant e in arrivo da distribuzioni esterne.

  - UserServices è il componente di un Front End Server per funzione di registrazione SIP, presenza e conferenze. Offre funzionalità altamente integrate di messaggistica istantanea, presenza e per conferenze basate sul proxy SIP.

  - InterClusterRouting è responsabile per il routing delle chiamate al pool della funzione di registrazione primario del chiamante. Per informazioni dettagliate, vedere [Componenti VoIP per Front End Server per Lync Server 2013](lync-server-2013-front-end-server-voip-components.md).

  - IIMFilter (Intelligent IM Filter) blocca i messaggi contenenti URL con collegamento ipertestuale o tramite cui vengono tentati trasferimenti di file. Verifica inoltre la versione client per conto del server. Viene applicato ai trasferimenti di file avviati utilizzando Lync Server o Communicator. Per impostazione predefinita, i collegamenti ipertestuali vengono disabilitati con l'aggiunta di un carattere di sottolineatura prima del primo carattere del collegamento. Un amministratore può modificare questo comportamento in modo da bloccare il collegamento e, in tal caso, i messaggi contenenti URL con collegamento ipertestuale o tramite cui vengono tentati trasferimenti di file vengono bloccati dal server e non possono raggiungere le destinazioni previste. IIMFilter viene installato in tutti i server che eseguono Lync Server, a eccezione dei server proxy e dei server di archiviazione.

  - UserPinService viene utilizzato per verificare i numeri di identificazione personale (PIN) degli utenti per le conferenze telefoniche con accesso esterno.

  - DefaultRouting è l'applicazione di routing predefinita per i server che eseguono Lync Server. È abilitata per impostazione predefinita e viene installata in tutti i server Standard Edition ed Enterprise Edition.

  - ExumRouting esegue il routing delle chiamate al server di messaggistica unificata di Exchange Server appropriato. ExumRouting determina il server di messaggistica unificata di Exchange appropriato per il routing della chiamata quando è presente un nuovo messaggio vocale da recapitare. Gestisce inoltre altri aspetti relativi all'integrazione della messaggistica unificata di Exchange, ad esempio il routing all'operatore automatico e l'accesso del sottoscrittore.

  - OutboundRouting determina il gateway che esegue il routing di una chiamata a un numero di telefono in base al numero composto e all'autorizzazione di composizione dell'utente. Gestisce inoltre un nuovo routing delle chiamate se un gateway non è in grado di elaborare una chiamata.

  - L'agente QoE riceve i rapporti relativi ai dati QoE (Quality of Experience) dagli endpoint tramite richieste SIP SERVICE e invia i dati alla coda di destinazione nel Monitoring Server o a consumer di terze parti con HTTP POST. Per informazioni dettagliate, vedere [Distribuzione del monitoraggio in Lync Server 2013](lync-server-2013-deploying-monitoring.md).

  - OutgoingFederation impone la convalida di federazione a livello di tenant per i messaggi indirizzati a una distribuzione esterna di destinazione.

  - AcpRouting opera come proxy e indirizza al gateway del provider di servizi di audioconferenza le richieste INVITE destinate a un provider di servizi di audioconferenza.

Gli script eseguiti nei server perimetrali includono i seguenti:

  - IIMFilter

  - OptionsHandler risponde alle richieste OPTIONS in arrivo con **200 OK** se la richiesta è destinata al server corrente. Questo script viene utilizzato per la convalida della topologia.

## Vedere anche

#### Attività

[Abilitare o disabilitare un'applicazione server MSPL (Microsoft SIP Processing Language)](lync-server-2013-enable-or-disable-a-microsoft-sip-processing-language-mspl-server-application.md)  
[Contrassegnare un'applicazione MSPL (Microsoft SIP Processing Language) come critica o non critica](lync-server-2013-mark-a-microsoft-sip-processing-language-mspl-application-as-critical-or-not-critical.md)

