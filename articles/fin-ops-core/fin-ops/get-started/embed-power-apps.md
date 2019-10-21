---
title: Bygge inn PowerApps-apper
description: Dette emnet beskriver hvordan du bygger inn PowerApps i klienten for å øke produktets funksjonalitet.
author: jasongre
manager: AnnBe
ms.date: 09/20/2019
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
ms.openlocfilehash: 37faf2a7a880c384f6f01d06ef5c9f28055d5006
ms.sourcegitcommit: 3ba95d50b8262fa0f43d4faad76adac4d05eb3ea
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 09/27/2019
ms.locfileid: "2191184"
---
# <a name="embed-powerapps-apps"></a>Bygge inn PowerApps-apper

[!include [banner](../includes/banner.md)]

Platform update 14 støtter integrering med Microsoft PowerApps, som er en tjeneste for utviklere og ikke-tekniske brukere for å lage egendefinerte forretningsprogrammer for mobile enheter, nettbrett og Internett uten å skrive kode. PowerApps utviklet av deg, din organisasjon eller det videre økosystemet kan deretter bygges i Finance and Operations-apper for å øke produktets funksjonalitet. Du kan for eksempel bygge en PowerApp for å utfylle Finance and Operations-apper med informasjon som hentes fra et annet system.

Hvis du vil vite mer om innebygging av PowerApps, kan du se den korte videoen [Slik bygger du inn PowerApps](https://www.youtube.com/watch?v=x3qyA1bH-NY).

## <a name="adding-an-embedded-powerapp-to-a-page"></a>Legge til en innebygd PowerApp på en side

### <a name="overview"></a>Oversikt

Før du bygger inn en PowerApp i klienten, må du først finne eller lage en PowerApp med ønskede visuelle effekter og/eller funksjonalitet. Vi beskriver ikke den detaljerte prosessen for å bygge en PowerApp her. Emnet [Innføring i PowerApps](https://docs.microsoft.com/powerapps/getting-started) er et godt utgangspunkt hvis du har erfaring med PowerApps.

Når du er klar til å bygge inn en bestemt PowerApp, kan du velge blant to måter å få tilgang til PowerApp på, på en side, uansett hvilken måte som passer deg best. Den første måten er via PowerApps-knappen som er lagt til i standardhandlingsruten. PowerApps som er lagt til med denne mekanismen, vises som menyelementer på PowerApps-menyknappen. Når disse menyelementene er valgt, åpnes hvert av dem sideruter som inneholder den innebygde PowerApp. Du kan også velge å vise en PowerApp direkte på en side som en ny fane, hurtigfane, blad eller som en ny inndeling i et arbeidsområde.

Når du konfigurerer din innebygde PowerApp, kan du velge ett felt du vil sende som inndata i PowerApp. Dette gjør at PowerApp kan svare på grunnlag av dataene som vises nå.

### <a name="details"></a>Detaljer

Fremgangsmåten nedenfor viser hvordan du bygger inn en PowerApp i webklienten.

1. Gå til siden der du vil bygge inn PowerApp. Dette er den samme siden som inneholder data som skal sendes til PowerApp som inndata.
2. Åpne ruten **Sett inn en PowerApp**:

    - Klikk **Alternativer**, og velg deretter **Tilpasse dette skjemaet**. Velg **PowerApp** under menyen **Sett inn**. Velg til slutt området der du vil legge til PowerApp. Hvis du vil bygge inn PowerApp under PowerApps-menyknappen, velger du handlingsruten. Hvis du vil bygge inn PowerApp direkte på siden, velger du den aktuelle fanen, hurtigfanen, bladet eller delen (hvis du er koblet til et arbeidsområde).
    - Hvis PowerApp åpnes ved hjelp av PowerApps-menyknappen, kan du også klikke på **PowerApps**-menyknappen i standardhandlingsruten, og deretter velger du **Sett inn en PowerApp**.

3. Konfigurer den innebygde PowerApp:

    - Feltet **Navn** angir teksten for knappen eller fanen som inneholder den innebygde PowerApp. Ofte vil du kanskje gjenta navnet på PowerApp i dette feltet.
    - **Program-ID** er GUID-en for PowerApp som du vil bygge inn. Hvis du vil hente denne verdien, finner du PowerApp på [web.powerapps.com](https://web.powerapps.com), og gå deretter til feltet **Program-ID** under **Detaljer**.
    - For **Inndata for PowerApp** kan du også velge feltet som inneholder dataene du vil sende til PowerApp som inndata. Se delen senere i dette emnet, kalt [Bygge en PowerApp som bruker data fra Finance and Operations-apper](#building-a-powerapp-that-leverages-data-sent-from-finance-and-operations-apps) for mer informasjon om hvordan PowerApp får tilgang til dataene som sendes fra Finance and Operations-apper.
    - Velg **programstørrelsen** som samsvarer med typen PowerApp du bygger inn. Velg **Tynn** for PowerApps som er bygget for mobile enheter, og **Bred** for PowerApps som er bygget for nettbrett. Dette sørger for at tilstrekkelig mengde plass blir tildelt til den innebygde PowerApp.
    - Hurtigfanen **Juridiske enheter** gir muligheten til å velge hvilke juridiske enheter PowerApp er tilgjengelig for. Standarden er å vise PowerApp i alle juridiske enheter.

4. Når du har bekreftet at konfigurasjonen er riktig, klikker du **Sett inn** for å bygge inn PowerApp på siden. Du blir bedt om å oppdatere leseren for å vise den innebygde PowerApp.

## <a name="sharing-an-embedded-powerapp"></a>Deling av en innebygd PowerApp

Når du har bygd inn en PowerApp på en side og bekreftet at det fungerer med enhver datakontekst sendt fra siden, kan det hende at du vil dele denne innebygde PowerApp med andre brukere i systemet. Dette kan gjøres på to forskjellige måter ved hjelp av tilpassingsfunksjonene i produktet:

- Det anbefalte scenariet er via systemadministratoren, som kan overføre en tilpassing til alle brukere eller en undergruppe av brukere.
- Du kan også eksportere sidens tilpassinger, sende dem til én eller flere brukere, og få hver av disse brukerne til å importere de endringene. Med Behandle-alternativet på tilpassingsverktøylinjen kan du eksportere og importere tilpasninger.

Se [Tilpasse brukeropplevelsen](personalize-user-experience.md) for mer informasjon om tilpassing av funksjonene i produktet og hvordan de brukes.

## <a name="building-a-powerapp-that-leverages-data-sent-from-finance-and-operations-apps"></a>Lage en PowerApp som bruker data som sendes fra Finance and Operations-apper

En viktig del av å bygge en PowerApp som bygges i Finance and Operations-apper, er å bruke inndataene fra Finance and Operations-apper. I PowerApp kan man få tilgang til de inndataene ved hjelp av variabelen Param("EntityId").

I funksjonen OnStart for PowerApp kan du for eksempel sette inndataene fra Finance and Operations-apper til en variabel som ser slik ut:

```
If(!IsBlank(Param("EntityId")), Set(FinOpsInput, Param("EntityId")), Set(FinOpsInput, ""));
```

## <a name="viewing-an-embedded-powerapp"></a>Vise en innebygd PowerApp

Hvis du vil vise en innebygd PowerApp på en side i Finance and Operations-apper, går du til en side med en innebygd PowerApp. Husk at PowerApps kan nås via PowerApps-knappen i standardhandlingsruten, eller kan vises direkte på siden som en ny fane, hurtigfane, blad eller som en ny inndeling i et arbeidsområde. Når en bruker først gang prøver å laste inn en PowerApp på en side, vil han eller hun bli bedt om å logge på PowerApps for å sikre at brukeren har de nødvendige tillatelsene til å bruke PowerApp.

## <a name="editing-an-embedded-powerapp"></a>Redigere en innebygd PowerApp

Når en PowerApp har blitt innebygd på en side, må du kanskje gjøre noen endringer i konfigurasjonen av den PowerApp. Du vil for eksempel kanskje endre etiketten som er knyttet til den innebygde PowerApp, eller det har blitt opprettet en ny versjon av en PowerApp og du må oppdatere program-IDen for å henvise til den siste PowerApp.

Følg denne fremgangsmåten for å redigere konfigurasjonen av en innebygd PowerApp:

1. Gå til ruten **Rediger en PowerApp**.

    - Hvis den innebygde PowerApp-en er tilgjengelig via PowerApps-menyknappen, høyreklikker du på PowerApps-menyknappen og velger **Tilpass**. Velg PowerApp du vil konfigurere, fra rullegardinlisten **Velg PowerApp**.
    - Hvis den innebygde PowerApp vises direkte på siden, velger du **Alternativer**, og deretter velger du **Tilpass dette skjemaet**. Ved hjelp av verktøyet **Velg** klikker du den innebygde PowerApp.

2. Gjør nødvendige endringer i konfigurasjonen av PowerApps, og klikk deretter på **Lagre**.

## <a name="removing-an-embedded-powerapp"></a>Fjerne en innebygd PowerApp

Når en PowerApp er innebygd på en side, er det to måter å fjerne den på om nødvendig:

- Gå til ruten **Rediger en PowerApp** ved hjelp av instruksjonene fra delen [Redigere en innebygd PowerApp](#editing-an-embedded-powerapp) tidligere i dette emnet. Bekreft at ruten viser informasjon for den innebygde PowerApp som du vil fjerne, og klikk deretter **Slett**.
- En innebygd PowerApp er lagret som personlige data, og derfor fjernes også alle innebygde PowerApps på den siden når du fjerner personlige data. Legg merke til at fjerning av personlige data på siden er permanent og ikke kan angres. Hvis du vil fjerne dine personlige data på en side, velger du **Alternativer** og klikk deretter **Tilpass dette skjemaet**. Velg **Fjern** under menyen **Administrer**. Når du har oppdatert leseren, er alle tidligere tilpassinger for denne siden fjernet. Se [Tilpasse brukeropplevelsen](personalize-user-experience.md) for mer informasjon om hvordan du optimaliserer sider ved hjelp av tilpassing.

## <a name="appendix"></a>Tillegg

### <a name="developer-control-over-where-a-powerapp-can-be-embedded"></a>Utviklerkontroll over hvor en PowerApp kan bygges inn

Som standard kan brukerne bygge inn PowerApps på alle sider, enten under PowerApps-menyknappen, eller direkte på siden som en fane, hurtigfane, blad eller ny inndeling i et arbeidsområde. Om nødvendig kan utviklere imidlertid også konfigurere denne funksjonen for å tillate bare innebygging av PowerApps på bestemte sider ved å implementere følgende metoder:

- **isPowerAppPersonalizationEnabled** – Hvis denne metoden returnerer USANN for en bestemt side, vises ikke PowerApps-menyknappen lenger og brukere kan ikke bygge inn PowerApps hvor som helst på denne siden, inkludert som en fane.
- **isPowerAppTabPersonalizationEnabled** – Hvis denne metoden returnerer USANN for en bestemt side, kan brukere ikke bygge inn PowerApps direkte på siden som en fane, hurtigfane eller panoramainndeling. Brukere kan fortsatt bygge inn PowerApps med PowerApps-menyknappen hvis innebygging er tillatt på siden.

Eksemplet nedenfor viser en ny klasse for de to metodene for å konfigurere hvor PowerApps kan bygges inn.

```
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