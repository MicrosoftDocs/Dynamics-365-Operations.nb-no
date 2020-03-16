---
title: Innebygg Power Apps
description: Dette emnet beskriver hvordan du bygger inn Power Apps i klienten for å øke produktets funksjonalitet.
author: jasongre
manager: AnnBe
ms.date: 12/02/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
ms.search.form: FormRunConfigurationAddPAControl, FormRunConfigurationEditPAControl
audience: Application User, Developer, IT Pro
ms.reviewer: sericks
ms.search.scope: Operations, Core
ms.search.region: Global
ms.author: jasongre
ms.search.validFrom: 2018-02-28
ms.dyn365.ops.version: Platform update 14
ms.openlocfilehash: 90422a34499dab7302ad7722cf84d40e1815991c
ms.sourcegitcommit: 3c1eb3d89c6ab9bd70b806ca42ef9df74cf850bc
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 02/12/2020
ms.locfileid: "3042948"
---
# <a name="embed-microsoft-power-apps"></a>Innebygg Microsoft Power Apps

[!include [banner](../includes/banner.md)]

Finance and Operations støtter integrering med Microsoft Power Apps, som er en tjeneste for utviklere og ikke-tekniske brukere for å lage egendefinerte forretningsprogrammer for mobilenheter, nettbrett og Internett uten å skrive kode. Power Apps utviklet av deg, din organisasjon eller det videre økosystemet kan deretter bygges i Finance and Operations-apper for å øke produktets funksjonalitet. Du kan for eksempel bygge en app fra Power Apps for å supplere en Finance and Operations-app med informasjon som hentes fra et annet system.

Hvis du vil vite mer om innebygging av Power Apps, kan du se den korte videoen [Slik bygger du inn Power Apps](https://www.youtube.com/watch?v=x3qyA1bH-NY).

## <a name="adding-an-embedded-app-from-power-apps-to-a-page"></a>Legge til en innebygd app fra Power Apps på en side

### <a name="overview"></a>Oversikt

Før du bygger inn en app fra Power Apps i klienten, må du først finne eller lage en app med ønskede visuelle effekter og/eller funksjonalitet. Vi beskriver ikke den detaljerte prosessen for å bygge apper her. Emnet [Innføring i Power Apps](https://docs.microsoft.com/powerapps/getting-started) er et godt utgangspunkt hvis du har erfaring med Power Apps.

Når du er klar til å bygge inn en bestemt app, kan du velge blant to måter å få tilgang til appen på, på en side, uansett hvilken måte som passer deg best. Den første måten er via Power Apps-knappen som er lagt til i standardhandlingsruten. Apper som er lagt til med denne mekanismen, vises som menyelementer på Power Apps-menyknappen. Når disse menyelementene er valgt, åpnes hvert av dem sideruter som inneholder den innebygde appen. Du kan også velge å bygge inn en app direkte på en side som en ny fane, hurtigfane, blad eller som en ny inndeling i et arbeidsområde.

Når du konfigurerer den innebygde appen, kan du velge ett felt du vil sende som kontekst til appen. Dette gjør at appen kan svare på grunnlag av dataene som vises nå.

### <a name="details"></a>Detaljer

Fremgangsmåten nedenfor viser hvordan du bygger inn en app fra Power Apps i nettklienten.

1. Gå til siden der du vil bygge inn appen. Dette er den samme siden som inneholder data som skal sendes til appen som inndata.
2. Åpne **Legg til en app fra Power Apps**-ruten:

    - Klikk på **Alternativer**, og velg deretter **Tilpass denne siden**. Under **Sett inn**-menyen velger du **Power Apps**. Velg til slutt området der du vil legge til appen. Hvis du vil bygge inn appen under Power Apps-menyknappen, velger du handlingsruten. Hvis du vil bygge inn appen direkte på siden, velger du den aktuelle fanen, hurtigfanen, bladet eller delen (hvis du er koblet til et arbeidsområde).
    - Hvis appen åpnes ved hjelp av Power Apps-menyknappen, kan du også klikke på **Power Apps**-menyknappen i standardhandlingsruten, og deretter velger du **Legg til en app**.

3. Konfigurer den innebygde appen:

    - Feltet **Navn** angir teksten for knappen eller fanen som inneholder den innebygde appen. Ofte vil du kanskje gjenta navnet på appen i dette feltet.
    - **Program-ID** er GUID-en for appen som du vil bygge inn. Hvis du vil hente denne verdien, finner du appen på [web.powerapps.com](https://web.powerapps.com), og går deretter til feltet **Program-ID** under **Detaljer**.
    - For **Inndatakontekst for appen** kan du også velge feltet som inneholder dataene du vil sende til appen som inndata. Se avsnittet senere i dette emnet med tittelen [Bygge en app som bruker data sendt fra Finance and Operations-apper](#building-an-app-that-leverages-data-sent-from-finance-and-operations-apps) for detaljert informasjon om hvordan appen kan få tilgang til dataene sendt fra Finance and Operations-apper.
    - Velg **programstørrelsen** som samsvarer med apptypen du bygger inn. Velg **Tynn** for apper bygget for mobilenheter, og **Bred** for apper bygget for nettbrett. Dette sørger for at tilstrekkelig mengde plass blir tildelt til den innebygde appen.
    - Hurtigfanen **Juridiske enheter** gir muligheten til å velge hvilke juridiske enheter appen er tilgjengelig for. Standardpraksis er å gjøre appen tilgjengelig for alle juridiske enheter. Dette alternativet er bare tilgjengelig når funksjonen [Lagrede visninger](saved-views.md) er deaktivert. 

4. Når du har bekreftet at konfigurasjonen er riktig, klikker du **Sett inn** for å bygge inn PowerApp på siden. Du blir bedt om å oppdatere leseren for å vise den innebygde appen.

## <a name="sharing-an-embedded-app"></a>Dele en innebygd app

Når du har bygd inn en app på en side og bekreftet at det fungerer med enhver datakontekst sendt fra siden, kan det hende at du vil dele denne med andre brukere i systemet. Dette kan gjøres på to forskjellige måter ved hjelp av tilpassingsfunksjonene i produktet:

- Det anbefalte scenariet er via systemadministratoren, som kan overføre en tilpassing til alle brukere eller en undergruppe av brukere.
- Du kan også eksportere sidens tilpassinger, sende dem til én eller flere brukere, og få hver av disse brukerne til å importere de endringene. Tilpasning-verktøylinjen inneholder handlinger som lar deg eksportere og importere tilpasninger.

Se [Tilpasse brukeropplevelsen](personalize-user-experience.md) for mer informasjon om tilpassing av funksjonene i produktet og hvordan de brukes.

## <a name="building-an-app-that-leverages-data-sent-from-finance-and-operations-apps"></a>Bygge en app som benytter data som sendes fra Finance and Operations-apper

En viktig del av bygging av en app fra Power Apps, som skal bygges inn i en Finance and Operations-app, er å bruke inndataene fra denne applikasjonen. Fra Power Apps-utviklingsopplevelsen kan inndataene sendt fra en Finance and Operations-app åpnes ved hjelp av variabelen Param ("EntityId").

I appens OnStart-funksjon kan du for eksempel sette inndataene fra Finance and Operations-apper til en variabel som ser slik ut:

```powerapps
If(!IsBlank(Param("EntityId")), Set(FinOpsInput, Param("EntityId")), Set(FinOpsInput, ""));
```

## <a name="viewing-an-app"></a>Vise en app

Hvis du vil vise en innebygd app på en side i Finance and Operations-apper, går du til en side med en innebygd app. Husk at apper kan nås via Power Apps-knappen i standardhandlingsruten, eller kan vises direkte på siden som en ny fane, hurtigfane, blad eller som en ny inndeling i et arbeidsområde. Når en bruker først gang prøver å laste inn en app på en side, vil han eller hun bli bedt om å logge på for å sikre at brukeren har de nødvendige tillatelsene til å bruke appen.

## <a name="editing-an-embedded-app"></a>Redigere en innebygd app

Når en app har blitt innebygd på en side, må du kanskje gjøre noen endringer i konfigurasjonen av appen. Du vil for eksempel kanskje endre etiketten som er knyttet til den innebygde appen, eller det har blitt opprettet en ny versjon av en app og du må oppdatere program-IDen for å henvise til den siste versjonen.

Følg denne fremgangsmåten for å redigere konfigurasjonen av en innebygd app:

1. Gå til **Rediger appen**-ruten.

    - Hvis den innebygde appen er tilgjengelig via Power Apps-menyknappen, høyreklikker du på Power Apps-menyknappen og velger **Tilpass**. Velg appen du vil konfigurere, fra rullegardinlisten **Velg en app**.
    - Hvis den innebygde appen vises direkte på siden, velger du **Alternativer**, og deretter velger du **Tilpass denne siden**. Ved hjelp av verktøyet **Velg** klikker du den innebygde appen.

2. Gjør nødvendige endringer i appkonfigurasjonen, og klikk deretter på **Lagre**.

## <a name="removing-an-app"></a>Fjerne en app

Når en app er innebygd på en side, er det to måter å fjerne den på om nødvendig:

- Gå til ruten **Rediger en app** ved hjelp av instruksjonene fra delen [Redigere en innebygd app](#editing-an-embedded-app) tidligere i dette emnet. Bekreft at ruten viser informasjon for den innebygde app som du vil fjerne, og klikk deretter på **Slett**-knappen.
- Fordi den innebygde appen lagres som tilpasningsdata, vil fjerning av sidetilpasningen også fjerne alle innebygde apper på denne siden. Legg merke til at fjerning av personlige data på siden er permanent og ikke kan angres. Hvis du vil fjerne tilpasningene dine på en side, velger du **Alternativer**, velger deretter **Tilpass denne siden**, og velger til slutt **Tøm**-knappen. Når du har oppdatert leseren, er alle tidligere tilpassinger for denne siden fjernet. Se [Tilpasse brukeropplevelsen](personalize-user-experience.md) for mer informasjon om hvordan du optimaliserer sider ved hjelp av tilpassing.

## <a name="appendix"></a>Tillegg

### <a name="developer-control-over-where-an-app-can-be-embedded"></a>Utviklerkontroll over hvor en app kan bygges inn

Som standard kan brukerne bygge inn apper på alle sider, enten under Power Apps-menyknappen, eller direkte på siden som en fane, hurtigfane, blad eller ny inndeling i et arbeidsområde. Om nødvendig kan utviklere imidlertid også konfigurere denne funksjonen for å tillate bare innebygging av apper på bestemte sider ved å implementere følgende metoder:

- **isPowerAppPersonalizationEnabled** – Hvis denne metoden returnerer USANN for en bestemt side, vises ikke Power Apps-menyknappen lenger og brukere kan ikke bygge inn apper hvor som helst på denne siden, inkludert som en fane.
- **isPowerAppTabPersonalizationEnabled** – Hvis denne metoden returnerer USANN for en bestemt side, kan brukere ikke bygge inn apper direkte på siden som en fane, hurtigfane eller panoramainndeling. Brukere kan fortsatt bygge inn apper med Power Apps-menyknappen hvis innebygging er tillatt på siden.

Følgende eksempel viser en ny klasse for de to metodene for å konfigurere der apper kan bygges inn.

```powerapps
[ExtensionOf(classStr(FormRunConfigurationPowerAppsConfiguration))]

public final class ClassTest_Extension
{
    public static boolean isPowerAppPersonalizationEnabled(str pageName)
    {
        var result = next isPowerAppPersonalizationEnabled(pageName);
        return result;
    }
    
    public static boolean isPowerAppTabPersonalizationEnabled(str pageName)
    {
        var result = next isPowerAppTabPersonalizationEnabled(pageName);
        return result;
    }
}
```
