---
title: Definere kommunikasjon for detaljhandelskanal (Commerce Data Exchange)
description: "Denne artikkelen inneholder en oversikt over Commerce Data Exchange og komponentene. Det forklarer delen som spiller hver komponent i overføring av data mellom Microsoft Dynamics 365 for operasjoner og kanaler for detaljhandel."
author: josaw1
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
audience: Application User
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 27021
ms.assetid: 179b1629-ac90-4cfb-b46a-5bda56c4f451
ms.search.region: global
ms.search.industry: Retail
ms.author: josaw
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
translationtype: Human Translation
ms.sourcegitcommit: 29938d962db42a521dd8dc03b8e45e0e34410e4d
ms.openlocfilehash: d3b36ec2a3f859215d93dd7ebf1f1ecfb2731c59
ms.lasthandoff: 03/31/2017


---

# <a name="define-retail-channel-communications-commerce-data-exchange"></a>Definere kommunikasjon for detaljhandelskanal (Commerce Data Exchange)

Denne artikkelen inneholder en oversikt over Commerce Data Exchange og komponentene. Det forklarer delen som spiller hver komponent i overføring av data mellom Microsoft Dynamics 365 for operasjoner og kanaler for detaljhandel.

<a name="overview"></a>Oversikt
--------

Commerce Data Exchange er et system som overfører data mellom Dynamics 365 for operasjoner og retail-kanaler, for eksempel Internett-butikker eller murstein og mørtel butikker. Databasen som lagrer data for en retail-kanalen er atskilt fra Dynamics-365 for databasen for operasjoner. Kanaldatabasen inneholder bare dataene som kreves for detaljhandelstransaksjoner. Hoveddata er konfigurert i Dynamics 365 for operasjoner og distribuert til kanaler. Transaksjonsdata som er opprettet i punktet salg (POS) system eller den elektroniske lagre, og deretter lastet opp til Dynamics 365 for operasjoner. Datadistribusjon er asynkron. Fremgangsmåten for å samle inn og pakke data ved kilden skjer med andre ord separat fra fremgangsmåten for å motta og bruke data på målet. Når det gjelder enkelte scenarier, for eksempel pris og beholdningsoppslag, må data hentes i sanntid. For å støtte disse scenariene, inneholder Commerce Data Exchange også en tjeneste som muliggjør kommunikasjon i sanntid mellom Dynamics 365 for operasjoner og en kanal. 

[![oppdatert-retail-grafikk](./media/updated-retail-graphic.png)](./media/updated-retail-graphic.png)  

## <a name="async-service"></a>Async Service
Microsoft SQL Server-endringssporing på Dynamics-365 for operasjoner databasen brukes til å bestemme dataendringer som må sendes til kanaler. Basert på en distribusjonsplan, Dynamics 365 for operasjoner pakker som data og lagrer den i sentral lagring (Azure blob storage). En egen partiprosess bruker Commerce Data Exchange: Async-klientbiblioteket til å sette inn denne datapakken i kanaldatabasen. 

[![Async Service](./media/async-300x239.png)](./media/async.png)

### <a name="retail-scheduler"></a>Detaljhandel Planlegger

Planleggerjobber er mekanismen for distribusjon av data til og fra lokasjoner. Jobber består av deljobber, som angir tabellene og tabellfeltene som inneholder dataene du vil distribuere. Dynamics 365 for operasjoner inneholder forhåndsdefinerte Oppgaveplanlegging-jobber og deljobber som oppfyller kravene til replikering av de fleste organisasjoner. Følgende typer forhåndsdefinerte jobber opprettes:

-   **Last ned jobber** – nedlasting jobber sender data som er endret fra Dynamics 365 for operasjoner til kanalen databaser. Endringer i poster spores ved hjelp av SQL Server-endringssporing.
-   **Last opp jobber (P jobber)** – opplasting jobber trekke salgstransaksjoner fra en kanal i Dynamics-365 for databasen for operasjoner. P-jobber laster opp data trinnvis. Når en P-jobb kjører, kontrollerer Async-klientbiblioteket replikeringstelleren for poster som allerede er mottatt fra en lokasjon. En post lastes opp bare hvis replikeringstelleren er større enn den største verdien som blir funnet. P-jobber oppdaterer ikke dataene som ble lastet opp tidligere.

Distribusjonsplan brukes til å kjøre dataoverføring, enten manuelt eller ved å planlegge en satsvis jobb i Dynamics 365 for operasjoner. En distribusjonsplan kan inneholde én eller flere kanaldatagrupper, og én eller flere planleggerjobber.

## <a name="realtime-service"></a>Realtime-tjenesten
Commerce Data Exchange: Real-time Service er en integrert tjeneste som gir kommunikasjon i sanntid mellom Dynamics 365 for operasjoner og kanaler for detaljhandel. Real-time Service kan individuelle POS-datamaskiner og Internett-butikker til å hente bestemte data fra Dynamics 365 for operasjoner i sanntid. Selv om de fleste viktige operasjoner kan utføres i databasen for lokale kanaler, krever direkte tilgang til data som er lagret i Dynamics 365 for operasjoner i følgende scenarier:

-   Utstedelse og innløsing av gavekort
-   Innløsing av fordelspoeng
-   Utstedelse og innløsing av kreditnotaer
-   Opprettelse og oppdatering av kundeposter
-   Opprettelse, oppdatering og fullføring av salgsordrer
-   Mottak av beholdning mot en bestilling eller overføringsordre
-   Utføring av lageropptellinger
-   Henting av salgstransaksjoner på tvers av butikker og fullføring av returtransaksjoner

[![Real-time Service](./media/rts.png)](./media/rts.png) 

Det opprettes en forhåndsdefinert Real-time Service-profil.


