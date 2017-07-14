---
title: Definere kommunikasjon for detaljhandelskanal (Commerce Data Exchange)
description: "Denne artikkelen inneholder en oversikt over Commerce Data Exchange og komponentene. Den forklarer rollen hver komponent har i overføringen av data mellom Microsoft Dynamics 365 for Retail og detaljhandelskanaler."
author: josaw1
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-365-retail
ms.technology: 
audience: Application User
ms.search.scope: AX 7.0.0, Operations, Core, Retail
ms.custom: 27021
ms.assetid: 179b1629-ac90-4cfb-b46a-5bda56c4f451
ms.search.region: global
ms.search.industry: Retail
ms.author: josaw
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0, Retail July 2017 update
ms.translationtype: Human Translation
ms.sourcegitcommit: 298ac47e2253f8add1aa3938dda15afe186afbeb
ms.openlocfilehash: 68252e52da47b89166627edbf2aa530e762354c6
ms.contentlocale: nb-no
ms.lasthandoff: 06/20/2017


---

# Definere kommunikasjon for detaljhandelskanal (Commerce Data Exchange)
<a id="define-retail-channel-communications-commerce-data-exchange" class="xliff"></a>

[!include[banner](../includes/banner.md)]


Denne artikkelen inneholder en oversikt over Commerce Data Exchange og komponentene. Den forklarer rollen hver komponent har i overføringen av data mellom Microsoft Dynamics 365 for Retail og detaljhandelskanaler.

Oversikt
<a id="overview" class="xliff"></a>
--------

Commerce Data Exchange er et system som overfører data mellom Dynamics 365 for Retail og detaljhandelskanaler, for eksempel nettbutikker eller fysiske butikker. Databasen som lagrer data for en detaljhandelskanal, er atskilt fra Microsoft Dynamics 365 for Retail-databasen. Kanaldatabasen inneholder bare dataene som kreves for detaljhandelstransaksjoner. Hoveddata konfigureres i Dynamics 365 for Retail og distribueres til kanaler. Transaksjonsdata opprettes i salgsstedssystemet eller nettbutikken, og lastes deretter opp til Dynamics 365 for Retail. Datadistribusjon er asynkron. Fremgangsmåten for å samle inn og pakke data ved kilden skjer med andre ord separat fra fremgangsmåten for å motta og bruke data på målet. Når det gjelder enkelte scenarier, for eksempel pris og beholdningsoppslag, må data hentes i sanntid. For å støtte disse scenariene har Commerce Data Exchange også en tjeneste som muliggjør sanntidskommunikasjon mellom Dynamics 365 for Retail og en kanal. 

[![oppdatert-detaljhandel-grafikk](./media/updated-retail-graphic.png)](./media/updated-retail-graphic.png)  

## Async Service
<a id="async-service" class="xliff"></a>
Microsoft SQL Server-endringssporing for Dynamics 365 for Retail-databasen brukes til å finne ut hvilke dataendringer som må sendes til kanaler. Dynamics 365 for Retail pakker disse dataene og lagrer dem i sentral lagerplass (Azure BLOB-lager) basert på en distribusjonsplan. En egen partiprosess bruker Commerce Data Exchange: Async-klientbiblioteket til å sette inn denne datapakken i kanaldatabasen. 

[![Async Service](./media/async-300x239.png)](./media/async.png)

### Detaljhandel Planlegger
<a id="retail-scheduler" class="xliff"></a>

Planleggerjobber er mekanismen for distribusjon av data til og fra lokasjoner. Jobber består av deljobber, som angir tabellene og tabellfeltene som inneholder dataene du vil distribuere. Dynamics Dynamics 365 for Retail inneholder forhåndsdefinerte planleggerjobber og deljobber som oppfyller replikeringskravene til de fleste organisasjoner. Følgende typer forhåndsdefinerte jobber opprettes:

-   **Nedlastingsjobber** – Nedlastingsjobber sender data som er endret, fra Dynamics 365 for Retail til kanaldatabaser. Endringer i poster spores ved hjelp av SQL Server-endringssporing.
-   **Opplastingsjobber (P-jobber)** – Opplastingsjobber trekker salgstransaksjoner fra en kanal til Dynamics 365 for Retail-databasen. P-jobber laster opp data trinnvis. Når en P-jobb kjører, kontrollerer Async-klientbiblioteket replikeringstelleren for poster som allerede er mottatt fra en lokasjon. En post lastes opp bare hvis replikeringstelleren er større enn den største verdien som blir funnet. P-jobber oppdaterer ikke dataene som ble lastet opp tidligere.

Distribusjonsplanen brukes til å kjøre dataoverføringen, enten manuelt eller ved å planlegge en satsvis jobb i Dynamics 365 for Retail. En distribusjonsplan kan inneholde én eller flere kanaldatagrupper, og én eller flere planleggerjobber.

## Sanntidstjeneste
<a id="realtime-service" class="xliff"></a>
Commerce Data Exchange: Real-time Service er en integrert tjeneste som sørger for sanntidskommunikasjon mellom Dynamics 365 for Retail og detaljhandelskanaler. Real-time Service gjør at individuelle datamaskiner på salgssteder og nettbutikker kan hente bestemte data fra Dynamics 365 for Retail i sanntid. Selv om de fleste viktige operasjoner kan utføres i den lokale kanaldatabasen, krever følgende scenarier direkte tilgang til dataene som er lagret i Dynamics 365 for Retail:

-   Utstedelse og innløsing av gavekort
-   Innløsing av fordelspoeng
-   Utstedelse og innløsing av kreditnotaer
-   Opprettelse og oppdatering av kundeposter
-   Opprettelse, oppdatering og fullføring av salgsordrer
-   Mottak av beholdning mot en bestilling eller overføringsordre
-   Utføring av lageropptellinger
-   Henting av salgstransaksjoner på tvers av butikker og fullføring av returtransaksjoner

[![Sanntidstjeneste](./media/rts.png)](./media/rts.png) 

En forhåndsdefinert Real-time Service-profil opprettes.




