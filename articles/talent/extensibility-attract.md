---
title: Utvidelsesmulighet i Attract
description: Dette emnet beskriver hvordan du kan utvide programmet Microsoft Dynamics 365 Talent – Attract ved hjelp av Microsoft Power Platform.
author: andreabichsel
manager: AnnBe
ms.date: 03/18/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-talent
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Talent, Core
ms.custom: 7521
ms.assetid: 3b953d5f-6325-4c9e-8b9b-6ab0458a73f8
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2018-10-15
ms.dyn365.ops.version: Talent October 2018 update
ms.openlocfilehash: ddc6593431585ed79cc15f7ede5daf856f11b959
ms.sourcegitcommit: e89bb3e5420a6ece84f4e80c11e360b4a042f59d
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 11/17/2020
ms.locfileid: "4527248"
---
# <a name="extensibility-in-attract"></a>Utvidelsesmulighet i Attract

[!include [banner](includes/banner.md)]

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

Microsoft Dynamics 365 Talent er bygd på toppen av Common Data Service og kan utvides på forskjellige måter ved hjelp av Microsoft Power Platform og funksjonene som tilbys i Common Data Service. Derfor kan du konfigurere og tilpasse systemet ved hjelp av Microsoft Power Apps og Microsoft Power Automate. Du kan også få ekstra analyse om personer ved hjelp av Microsoft Power BI. Dessuten gjør nye egendefinerte aktiviteter, for eksempel Power Apps og webinnhold-aktivitet (iframe), ansettelsesprosessen mer fleksibel enn noen gang. Ved hjelp av disse aktivitetene kan du tilpasse ansettelsesprosessen til dine forretningsbehov og prosesser, og du kan forsikre deg om at både ansettelsesteamet og kandidatene får en sømløs, tilpasset opplevelse.

## <a name="extending-option-sets-in-attract"></a>Utvide alternativsett i Attract

Et **Alternativsett** (plukkliste) er et type felt som kan inkluderes i en enhet. Det definerer et sett med alternativer. Når et alternativsett vises i et skjema, brukes en rullegardinlistekontroll.  I Attract finnes det flere felt som er alternativsett.  Vi introduserer muligheten til å utvide alternativsettene og begynner med Avslag-årsaksfeltet, Ansettelsestype-feltet og Ansiennitetstype-feltet.   Du kan også legge til lokaliserte visningsetiketter for alternativene du legger til. Hvis du vil ha mer informasjon, se [Tilpasse alternativsettetiketter](https://docs.microsoft.com/powerapps/developer/common-data-service/customize-labels-support-multiple-languages).

> [!NOTE]
> Jobbposteringen til LinkedIn-funksjonaliteten krever bruk av feltet **Ansettelsestype** og **Ansiennitetstype** på siden **Jobbdetaljer**. Standardverdiene i disse feltene støttes av LinkedIn og vises når jobben posteres. Hvis du posterer jobber i LinkedIn og endrer de eksisterende alternativsettverdiene for disse feltene, vil jobben derfor fortsatt posteres, men LinkedIn vil ikke vise de egendefinerte **Ansettelsestype**- og **Ansiennitetstype**-verdiene.  

Nedenfor finner du trinnene for å oppdatere **Avvisningsårsak**-feltet med verdier som er spesifikke for din virksomhet.  

1. Hvis du vil vise **Avvisningsårsak**-alternativsettet, går du til [nettstedet for Power Apps-administrasjon](https://admin.powerapps.com).
2. Du kan bli bedt om å logge på kontoen. Oppgi bruker-ID-en og passordlegitimasjonen du bruker til å logge på Dynamics 365 og/eller Office 365, og klikk deretter **Neste**.
3. I **Miljøer**-fanen velger du miljøet du vil administrere, og dobbeltklikker for å gå til **Detaljer**-kategorien.
4. På **Detaljer**-kategorien velger du **Administrasjonssenter for Dynamics 365**.
5. Velg forekomsten du vil endre, og velg **Åpne**.
6. Gå til **Innstillinger** og deretter **Tilpasninger**, og velg **Tilpass systemet**.
7. Finn enheten du vil vise alternativsettet for, ved å velge **Enheter** og vise gruppen. I dette eksemplet vil det være **Stillingssøknadenhet**.
8. Gå til feltet som du vil utvide alternativsettet for, ved å velge **Felt**-alternativet. I dette eksemplet vil det være **msdyn_rejectionreason**. Dobbeltklikk på feltet.
9. I **Alternativsett**-feltet velger du **Rediger**.
10. Velg **+**-ikonet.
11. Angi en **Etikett**.  (Dette må være en unik verdi – ingen duplikater).
12. Velg **Lagre**.
13. Velg **Publiser** øverst på siden.

## <a name="take-advantage-of-the-microsoft-power-platform"></a>Dra nytte av Microsoft Power Platform 

Fordi alle dataene fra Attract ligger i Common Data Service, kan du bruke verktøy fra Microsoft Power Platform til å ta dine unike forretningsbehov til Attract.

### <a name="power-apps"></a>Power Apps

Du kan bruke Power Apps til å opprette programmer som koble til Attract-dataene, og som bruker uttrykk som uttrykkene i Microsoft Excel, til å legge til logikk. Apper du lager med Power Apps, kan kjøre på Internett, og på Apple iOS og Google Android-enheter.

Du kan for eksempel forenkle universitetsmesser for rekrutteringspersoner ved å bygge en enkel app som lar dem skanne CVer og legge kandidater til en stilling i Attract. Du kan også bygge en app som bidrar til å dekke organisasjonens samsvarsbehov. Hvis du vil ha mer informasjon om Power Apps og hvordan den brukes til å bygge apper, kan du se [Integrere data i Common Data Service](https://docs.microsoft.com/powerapps).

### <a name="microsoft-power-automate"></a>Microsoft Power Automate 

Du kan bruke Microsoft Power Automate til å opprette automatisert arbeidsflyt som kjører på toppen av Attract-data. Du kan enkelt koble til hundrevis av populære apper og tjenester uten å måtte skrive kode. Ved å bygge flyter som samhandler med Attract-jobben, kandidaten og søknadsenheter i Common Data Service, kan du automatisere forskjellige handlinger. Når en kandidat for eksempel har godtatt et tilbud, kan en varsling sendes til et jobbintroduksjonsteam, eller nyhetene kan kunngjøres på Twitter. Hvis du vil ha mer informasjon om flyter, se [dokumentasjonen for Microsoft Power Automate](https://docs.microsoft.com/flow/).

### <a name="power-bi"></a>Power BI

Med Power BI kan du lage og vise egendefinerte rapporter og instrumentbord som gir deg større innsikt i Attract-dataene. Hvis du vil ha mer informasjon om Power BI og hvordan du kan bygge interaktive rapporter og instrumentbord, se [Power BI-dokumentasjonen](https://docs.microsoft.com/power-bi/).

### <a name="custom-activities"></a>Egendefinert aktiviteter 

Du kan legge til egendefinerte aktiviteter, for eksempel Power Apps-apper og webinnhold-aktiviteter (iframe), på nivået av jobbprosessmalen eller mens du oppretter en ny jobb. Disse aktivitetene lar deg tilpasse ansettelsesprosessen og hente forretningslogikk som er unik for organisasjonen, til Attract.

#### <a name="power-apps-activity"></a>Power Apps-aktivitet 

Power Apps-aktiviteten lar personen som oppretter en jobb eller jobbprosessmal, bygge inn en Power Apps-app i ansettelsesflyten. Når du har opprettet og publisert appen, kan du angi app-ID-en i aktivitetskonfigurasjonene. Ved hjelp av en Power Apps-app kan du lese og skrive data til Common Data Service. Du kan også koble appen til en flyt. Du har for eksempel en app som rekrutteringspersoner bruker til å fylle ut et skjema når de gjør telefonintervjuer. I dette tilfelle kan du koble appen til en flyt som vurderer om en søker kan tas videre i jobbsøknadsprosessen. Denne typen aktivitet kan bare vises av medlemmer av ansettelsesteamet. Hvis du vil ha mer informasjon om hvordan du konfigurerer Power Apps-aktiviteten, kan du se [Aktiviteter i ansettelsesprosesser](./activities-attract.md).

> [!NOTE]
> Power Apps-aktiviteten er bare tilgjengelig med tillegget for omfattende ansettelse.

#### <a name="web-content-iframe-activity"></a>Webinnhold-aktivitet (iframe)

Webinnhold-aktivitet (iframe) lar deg bygge inn en egendefinert webløsning som du har opprettet i ansettelsesprosessen eller kandidatportalen. Du kan lese og skrive data direkte fra Common Data Service. Du kan også tilpasse løsningen slik at den utløser flyter eller utnytter Microsoft Azure-funksjoner. Hvis du vil ha mer informasjon om hvordan du konfigurerer webinnhold-aktiviteten, kan du se [Aktiviteter i ansettelsesprosesser](./activities-attract.md).

> [!NOTE]
> Webinnhold-aktiviteten er bare tilgjengelig med tillegget for omfattende ansettelse.
