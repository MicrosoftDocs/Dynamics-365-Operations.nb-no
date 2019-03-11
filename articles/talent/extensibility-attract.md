---
title: Utvidelsesmuligheter i Attract
description: Dette emnet beskriver hvordan du kan utvide programmet Microsoft Dynamics 365 for Talent - Attract ved hjelp av Microsoft Power-plattformen.
author: josaw
manager: AnnBe
ms.date: 10/15/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-talent
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Talent, Core
ms.custom: 7521
ms.assetid: 3b953d5f-6325-4c9e-8b9b-6ab0458a73f8
ms.search.region: Global
ms.author: rschloma
ms.search.validFrom: 2018-10-15
ms.dyn365.ops.version: Talent October 2018 update
ms.openlocfilehash: d9e1dd3a67c5f64b5d05f0f171226085138e0b44
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 01/29/2019
ms.locfileid: "305609"
---
# <a name="extensibility-in-attract"></a>Utvidelsesmuligheter i Attract

[!include[banner](../includes/banner.md)]

Microsoft Dynamics 365 for Talent er bygd på toppen av Common Data Service (CDS) for Apps-plattformen, og kan utvides på forskjellige måter ved hjelp av Microsoft Power-plattformen og funksjonene som tilbys i Common Data Service for Apps. Derfor kan du konfigurere og tilpasse systemet ved hjelp av Microsoft PowerApps og Microsoft Flow. Du kan også få ekstra analyse om personer ved hjelp av Microsoft Power BI. Dessuten gjør nye egendefinerte aktiviteter, for eksempel PowerApps og webinnhold-aktivitet (iframe), ansettelsesprosessen mer fleksibel enn noen gang. Ved hjelp av disse aktivitetene kan du tilpasse ansettelsesprosessen til dine forretningsbehov og prosesser, og du kan forsikre deg om at både ansettelsesteamet og kandidatene får en sømløs, tilpasset opplevelse.

## <a name="take-advantage-of-the-microsoft-power-platform"></a>Dra nytte av Microsoft Power Platform 

Fordi alle dataene fra Attract ligger i Common Data Service for Apps, kan du bruke verktøy fra Microsoft Power-plattformen til å ta dine unike forretningsbehov til Attract.

### <a name="powerapps"></a>PowerApps

Du kan bruke PowerApps til å opprette programmer som koble til Attract-dataene, og som bruker uttrykk som uttrykkene i Microsoft Excel, til å legge til logikk. Apper du lager med PowerApps, kan kjøre på Internett, og på Apple iOS og Google Android-enheter.

Du kan for eksempel forenkle universitetsmesser for rekrutteringspersoner ved å bygge en enkel app som lar dem skanne CVer og legge kandidater til en stilling i Attract. Du kan også bygge en app som bidrar til å dekke organisasjonens samsvarsbehov. Hvis du vil ha mer informasjon om PowerApps og hvordan den brukes til å bygge apper, se [Integrere data i Common Data Service for Apps](https://docs.microsoft.com/en-us/powerapps).

### <a name="microsoft-flow"></a>Microsoft Flow 

Du kan bruke Microsoft Flow til å opprette automatisert arbeidsflyt som kjører på toppen av Attract-data. Du kan enkelt koble til hundrevis av populære apper og tjenester uten å måtte skrive kode. Ved å bygge flyter som samhandler med Attract-jobben, kandidaten og søknadsenheter i Common Data Service for Apps, kan du automatisere forskjellige handlinger. Når en kandidat for eksempel har godtatt et tilbud, kan en varsling sendes til et jobbintroduksjonsteam, eller nyhetene kan kunngjøres på Twitter. Hvis du vil ha mer informasjon om flyter, se [dokumentasjonen for Microsoft Flow](https://docs.microsoft.com/en-us/flow/).

### <a name="power-bi"></a>Power BI

Med Power BI kan du lage og vise egendefinerte rapporter og instrumentbord som gir deg større innsikt i Attract-dataene. Hvis du vil ha mer informasjon om Power BI og hvordan du kan bygge interaktive rapporter og instrumentbord, se [Power BI-dokumentasjonen](https://docs.microsoft.com/en-us/power-bi/).

### <a name="custom-activities"></a>Egendefinert aktiviteter 

Du kan legge til egendefinerte aktiviteter, for eksempel PowerApps-apper og webinnhold-aktiviteter (iframe), på nivået av jobbprosessmalen eller mens du oppretter en ny jobb. Disse aktivitetene lar deg tilpasse ansettelsesprosessen og hente forretningslogikk som er unik for organisasjonen, til Attract.

#### <a name="powerapps-activity"></a>PowerApps-aktivitet 

PowerApps-aktiviteten lar personen som oppretter en jobb eller jobbprosessmal, bygge inn en PowerApps-app i ansettelsesflyten. Når du har opprettet og publisert appen, kan du angi app-ID-en i aktivitetskonfigurasjonene. Ved hjelp av en PowerApps-app kan du lese og skrive data til Common Data Service for Apps. Du kan også koble appen til en flyt. Du har for eksempel en app som rekrutteringspersoner bruker til å fylle ut et skjema når de gjør telefonintervjuer. I dette tilfelle kan du koble appen til en flyt som vurderer om en søker kan tas videre i jobbsøknadsprosessen. Denne typen aktivitet kan bare vises av medlemmer av ansettelsesteamet. Hvis du vil ha mer informasjon om hvordan du konfigurerer PowerApps-aktiviteten, kan du se [Aktiviteter i Attract](./activities-attract.md).

> [!NOTE]
> PowerApps-aktiviteten er bare tilgjengelig med tillegget for omfattende ansettelse.

#### <a name="web-content-iframe-activity"></a>Webinnhold-aktivitet (iframe)

Webinnhold-aktivitet (iframe) lar deg bygge inn en egendefinert webløsning som du har opprettet i ansettelsesprosessen eller kandidatportalen. Du kan lese og skrive data direkte fra Common Data Service for Apps. Du kan også tilpasse løsningen slik at den utløser flyter eller utnytter Microsoft Azure-funksjoner. Hvis du vil ha mer informasjon om hvordan du konfigurerer webinnhold-aktiviteten, kan du se [Aktiviteter i Attract](./activities-attract.md).

> [!NOTE]
> Webinnhold-aktiviteten er bare tilgjengelig med tillegget for omfattende ansettelse.
