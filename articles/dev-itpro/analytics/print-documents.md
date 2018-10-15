---
title: Dokumentutskrift
description: I Microsoft Dynamics 365 for Finance and Operations kan du skrive ut dokumenter med en lokal skriver eller en enhet som er koblet til nettverket. Denne artikkelen gir en oversikt over hvordan dokumenter skrives ut.
author: TJVass
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-platform
ms.technology: 
audience: IT Pro, Application User
ms.reviewer: sericks
ms.search.scope: Operations, Core
ms.custom: 69161
ms.assetid: 7815bddd-c4f4-4bc3-a29b-315458065374
ms.search.region: Global
ms.author: tjvass
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 821d8927211d7ac3e479848c7e7bef9f650d4340
ms.openlocfilehash: 4fd20022ff91fedb6d0323e82fbe3c1acae38e48
ms.contentlocale: nb-no
ms.lasthandoff: 08/13/2018

---

# <a name="document-printing"></a>Dokumentutskrift

[!include [banner](../includes/banner.md)]

I Microsoft Dynamics 365 for Finance and Operations kan du skrive ut dokumenter med en lokal skriver eller en enhet som er koblet til nettverket. Denne artikkelen gir en oversikt over hvordan dokumenter skrives ut.

## <a name="printing-overview"></a>Oversikt over utskrift

Microsoft Dynamics 365 for Finance and Operation gir integrerte tjenester og klientprogrammer som gjør det enkelt å generere, lagre og distribuere dokumenter som støtter forretningsaktiviteten. I Finance and Operations kan du skrive ut dokumenter med en lokal skriver eller en enhet som er koblet til nettverket. I tillegg kan du eksportere Finance and Operations-sider og -rapporter direkte fra klienten, som PDF-filer eller Microsoft Office-dokumenter. Til slutt lar den distribuerte arbeidsmengden deg skrive ut forretningsdokumenter direkte fra en mobil enhet ved hjelp av nettverksressurser. Selv om utskriftskravene kan variere, må alle bransjer vanligvis lage papirkopier av forretningsdokumenter i Finance and Operations. Å skrive ut dokumenter på nettverksenheter fra vertsbaserte programmer gir et unikt sett med utfordringer. Her er noen eksempler:

- Skriverdrivere er kanskje ikke tilgjengelige på brukerens enheten.
- Brukerens enhet er kanskje ikke koblet til firmanettverket.

Ved hjelp av en dedikert vert og følgende enkle trinn, kan administratorer konfigurere distribusjoner slik at brukere kan skrive ut direkte fra forretningsprogrammer på nettverksenheter.

### <a name="printing-scenarios-in-finance-and-operations-applications"></a>Utskriftsscenarioer i Finance and Operations-programmer

Tabellen nedenfor beskriver tre primære utskriftsscenarioer i Finance and Operations-programmer.

| Scenario                        | Mål                                                      | Løsning |
|---------------------------------|-----------------------------------------------------------|----------|
| 1. Skrive ut det du ser        | Skriv ut det som vises i webleseren.             | Det genereres en "utskriftsvennlig" versjon av websiden for leseren. |
| 2. Interaktiv utskrift         | Skriv ut et presisjonsdokument på en lokalt tilkoblet enhet. | Du kan eksportere en PDF-versjon av rapporten, og laste den ned til leseren. |
| 3. Skrive ut på en nettverksenhet | Send et presisjonsdokument til en domeneskriverenhet.     | En presisjonsdokument blir sendt til et klientprogram som kjører på en server som ligger på kundens domene. |

Fordi løsningen varierer, vil Finance and Operations avhengig av scenarioet, tilby innebygde tjenester og verktøy som kan hjelpe brukerne med å oppnå målene.

- **Scenario 1** støttes av webleserens gjengivelse av HTML5-klienten.
- **Scenario 2** bruker klientprogrammer og tjenester for Microsoft Office 365.
- **Scenario 3** krever støtte fra klientprogrammer og tjenester som Microsoft Azure er vert for.

I tillegg til plattformen som er distribuert til Azure-abonnementet, gir Finance and Operations kunder et integrert, førsteparts Azure-program som gjør det enklere for dem å bruke domene-vertsbaserte enheter til å skrive ut dokumenter.

## <a name="service-overview"></a>Serviceoversikt
Mens dokumenter som produseres av de vertsbaserte programmene venter på å skrives ut på en enhet som er koblet til nettverket, lagres de i Azure blob-lageret. [Dokumentrutingsagenten](install-document-routing-agent.md) bruker Azure-godkjenning til å opprette en sikker kanal til Azure-tjenestene.

**Utførelsessekvens**

1. Rapporten genereres av Microsoft SQL Server Reporting Services (SSRS) og lagres i Azure blob-lageret. Tilknyttede skriverinnstillinger lagres sammen med dokumentet.
2. Dokumentrutingsagenten spør Azure Service Bus-køen om aktive jobber.
3. Dokumentet lastes ned av dokumentrutingsagenten og sendes i kø til nettverksskriveren.

Den klientbaserte løsningen lar kundene administrere skalaen for utskriftsbehovene deres. Kunder som har store utskriftsmengder, kan installere mange dokumentrutingsagenter for å øke antallet samtidige utskriftsoperasjoner. Noen kunder trenger også svært få installasjoner av dokumentrutingsagenten for å håndtere forventede utskriftsbehov.

### <a name="service-components-for-network-printing"></a>Servicekomponenter for nettverksutskrift

Diagrammet nedenfor viser de grunnleggende komponentene som bidrar til å støtte nettverksutskriftsoperasjoner.

[![Servicekomponenter for nettverksutskrift\_2016](./media/service-components-for-network-printing_2016.png)](./media/service-components-for-network-printing_2016.png)

Legg merke til at én enkelt skriver kan registreres med flere dokumentrutingsagenter. Hvis du vil løse skriverinnstillingene, bruker den vertsbaserte tjenesten nettverksbanen som entydig identifiserer hver nettverksskriver. Resultatet er at selv om en skriver er registrert av flere klienter, vises den som et enkelt valg i listen over skrivere som er tilgjengelige, i Finance and Operations.
