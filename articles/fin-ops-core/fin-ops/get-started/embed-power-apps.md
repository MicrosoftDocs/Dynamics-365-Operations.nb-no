---
title: Bygge inn lerretsapper fra Power Apps
description: Dette emnet forklarer hvordan du bygger inn lerretsapper fra Microsoft Power Apps i klienten for å øke produktets funksjonalitet.
author: jasongre
ms.date: 04/22/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: FormRunConfigurationAddPAControl, FormRunConfigurationEditPAControl
audience: Application User, Developer, IT Pro
ms.reviewer: sericks
ms.search.region: Global
ms.author: jasongre
ms.search.validFrom: 2018-02-28
ms.dyn365.ops.version: Platform update 14
ms.openlocfilehash: 18146ce5ab081b3a6376bf412805016b04da6a11
ms.sourcegitcommit: ab3f5d0da6eb0177bbad720e73c58926d686f168
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 04/26/2021
ms.locfileid: "5944685"
---
# <a name="embed-canvas-apps-from-power-apps"></a>Bygge inn lerretsapper fra Power Apps

[!include [banner](../includes/banner.md)]
[!include [banner](../includes/preview-banner.md)]

Microsoft Power Apps er en tjeneste som lar utviklere og ikke-tekniske brukere lage egendefinerte forretningsprogrammer for mobilenheter, nettbrett og nettet uten å måtte skrive kode. Finance and Operations-apper støtter integrasjon med Power Apps. Lerretsapper som du, organisasjon din eller det videre økosystemet utvikler, kan bygges inn i Finance and Operations-apper for å øke produktets funksjonalitet. Du kan for eksempel bygge en lerretsapp fra Power Apps for å supplere en Finance and Operations-app med informasjon som hentes fra et annet system.

Hvis du vil vite mer om innebygging av lerretsapper, kan du se den korte videoen [Slik bygger du inn lerretsapper](https://www.youtube.com/watch?v=x3qyA1bH-NY).

## <a name="adding-an-embedded-canvas-app-from-power-apps-to-a-page"></a>Legge til en innebygd lerretsapp fra Power Apps på en side

### <a name="overview"></a>Oversikt

Før du bygger inn en lerretsapp fra Power Apps i klienten, må du først finne eller lage en app med ønskede visuelle effekter og/eller funksjonalitet. Dette emnet inneholder ikke en detaljert beskrivelse av prosessen for bygging av apper. Hvis du ikke har brukt Power Apps, se [Power Apps-dokumentasjonen](/powerapps/).

Det finnes to måter å få tilgang til en bestemt lerretsapp på en side når du er klar til å bygge inn appen. Du kan velge den metoden som passer best til ditt scenario. Den første måten er via **Power Apps**-knappen som er lagt til i standardhandlingsruten. Apper du legger til ved hjelp av denne fremgangsmåten, vises som elementer på **Power Apps**-menyknappen. Når du velger et av disse elementene, vises en siderute som inneholder den innebygde appen. Du kan også bygge inn en app direkte på en side som en ny fane, hurtigfane eller blad eller som en ny inndeling i et arbeidsområde.

Når du konfigurerer den innebygde lerretsappen, kan du velge ett felt du vil sende som kontekst til appen. Dette trinnet gjør at appen kan svare på grunnlag av dataene som vises nå.

> [!NOTE]
> Du kan for øyeblikket ikke bruke denne mekanismen til å bygge inn modelldrevne apper.  

### <a name="details"></a>Detaljer

Fremgangsmåten nedenfor viser hvordan du bygger inn en lerretsapp fra Power Apps i nettklienten.

1. Gå til siden der du vil bygge inn lerretsappen. Denne siden er siden som inneholder data som må sendes til appen som inndata.
2. Åpne **Legg til en app fra Power Apps**-ruten:

    - Klikk på **Alternativer**, og velg deretter **Tilpass denne siden**. Under **Sett inn**-menyen velger du **Power Apps**. Velg til slutt området der du vil legge til appen. Hvis du vil bygge inn appen under Power Apps-menyknappen, velger du handlingsruten. Hvis du vil bygge inn appen direkte på siden, velger du den aktuelle fanen, hurtigfanen, bladet eller delen (hvis du er koblet til et arbeidsområde).
    - Hvis appen åpnes ved hjelp av Power Apps-menyknappen, kan du også klikke på **Power Apps**-menyknappen i standardhandlingsruten, og deretter velger du **Legg til en app**.

3. Konfigurer den innebygde appen:

    - Feltet **Navn** angir teksten for knappen eller fanen som inneholder den innebygde appen. Ofte vil du kanskje gjenta navnet på appen i dette feltet.
    - **App-ID**-feltet angir GUIDen (globalt unik identifikator) for lerretsappen du vil bygge inn. Hvis du vil hente denne verdien, finner du appen på [make.powerapps.com](https://make.powerapps.com), og deretter ser du i feltet **App-ID** under **Detaljer**.
    - For **Inndatakontekst for appen** kan du også velge feltet som inneholder dataene du vil sende til appen som inndata. Hvis du vil ha mer informasjon om hvordan appen får tilgang til data sendt fra Finance and Operations-apper, kan du se delen senere i dette emnet som heter [Bygge en app som benytter data som sendes fra Finance and Operations-apper](#building-a-canvas-app-that-uses-data-that-is-sent-from-finance-and-operations-apps). 
        - Fra og med versjon 10.0.19 blir også den gjeldende juridiske enheten sendt som kontekst til lerretsappen via URL-parameteren **cmp**. Dette vil ikke ha noen innvirkning på mållerretsappen før appen benytter seg av denne informasjonen. 
    - Velg **programstørrelsen** som samsvarer med apptypen du bygger inn. Velg **Tynn** for apper bygget for mobilenheter, og **Bred** for apper bygget for nettbrett. Dette sørger for at tilstrekkelig mengde plass blir tildelt til den innebygde appen.
    - Hurtigfanen **Juridiske enheter** gir muligheten til å velge hvilke juridiske enheter appen er tilgjengelig for. Standardpraksis er å gjøre appen tilgjengelig for alle juridiske enheter. Dette alternativet er bare tilgjengelig når funksjonen [Lagrede visninger](saved-views.md) er deaktivert. 

4. Når du har bekreftet at konfigurasjonen er riktig, klikker du **Sett inn** for å bygge inn PowerApp på siden. Du blir bedt om å oppdatere leseren for å vise den innebygde appen.

## <a name="sharing-an-embedded-app"></a>Dele en innebygd app

Når du har bygd inn en lerretsapp på en side og bekreftet at det fungerer med enhver datakontekst sendt fra siden, kan det hende at du vil dele appen med andre brukere i systemet. Følg disse trinnene for å dele en innebygd lerretsapp.

1. [Del lerretsappen](/powerapps/maker/canvas-apps/share-app) med de riktige brukerne, slik at de får tilgang til appen i Power Apps. 

2. Kontroller at de angitte brukerne har de riktige tilpasningene, slik at den innebygde appen vises når disse brukerne viser siden. Du kan bruke en av følgende tilnærminger:

    - Anbefalt: Bruk [Lagrede visninger](saved-views.md)-funksjonen for å opprette og publisere en visning som inneholder den innebygde appen. Denne fremgangsmåten sikrer at alle brukere som har sikkerhetsroller som er målrettet av den publiserte visningen, vil se appen i Finance and Operations-apper. 
    - Hvis du ikke har aktivert funksjonen for lagrede visninger, kan du få systemadministrator til å pushe en personalisering som inkluderer den innebygde appen for alle brukere eller et delsett av brukere. Du kan også eksportere personlige tilpasninger for siden og sende dem til én eller flere brukere. Hver av disse brukerne kan deretter importere tilpasningene. Tilpasning-verktøylinjen inneholder handlinger som lar deg eksportere og importere tilpasninger. 
    
> [!NOTE]
> Hvis lerretsappen er delt med eksterne brukere, kan ikke disse brukerne bruke den innebygde appen i Finance and Operations-apper. De kan imidlertid få tilgang til appen direkte i Power Apps. Eksterne brukere inkluderer gjester og brukere som ikke hører til i Microsoft 365 Azure Directory der Finance and Operations-appen distribueres.

Se [Tilpasse brukeropplevelsen](personalize-user-experience.md) for mer informasjon om tilpassing av funksjonene i produktet og hvordan de brukes.

## <a name="building-a-canvas-app-that-uses-data-that-is-sent-from-finance-and-operations-apps"></a>Bygge en lerretsapp som bruker data som sendes fra Finance and Operations-apper

Når du bygger en lerretsapp som skal bygges inn i en Finance and Operations-app, er en viktig del av prosessen å bruke inndataene fra denne Finance and Operations-appen. Fra Power Apps-utviklingsopplevelsen kan inndataene sendt fra en Finance and Operations-app åpnes ved hjelp av variabelen **Param ("EntityId")**. I tillegg, fra og med versjon 10.0.19, blir også den gjeldende juridiske enheten sendt til lerretsappen via **Param("cmp")**-variabelen. 

I appens OnStart-funksjon kan du for eksempel sette inndataene fra Finance and Operations-apper til en variabel som ser slik ut:

``` Power Apps
If(!IsBlank(Param("EntityId")), Set(FinOpsInput, Param("EntityId")), Set(FinOpsInput, ""));

If(!IsBlank(Param("cmp")), Set(FinOpsInput, Param("cmp")), Set(FinOpsLegalEntity, ""));
```

## <a name="viewing-a-canvas-app"></a>Vise en lerretsapp

Hvis du vil vise en innebygd lerretsapp på en side i Finance and Operations-apper, går du til en side med en innebygd app. Husk at apper kan åpnes ved hjelp av **Power Apps**-knappen i standardhandlingsruten. De kan også vises direkte på siden som en ny fane eller hurtigfane eller et blad eller som en ny inndeling i et arbeidsområde. Når brukere først prøver å laste inn en app på en side, blir de bedt om å logge på. Dette trinnet sikrer at brukerne har de nødvendige tillatelsene til å bruke appen.

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

### <a name="developer-modeling-a-canvas-app-on-a-form"></a>[Utvikler] Modellere en lerretsapp på et skjema

Mens dette emnet fokuserer på å bygge inn lerretsapper innen personalisering, har utviklerne også muligheten til å legge til en lerretsapp i et skjema ved hjelp av Visual Studio-utviklingserfaringen. Du gjør dette ved å legge til en PowerAppsHostControl i skjemaet. Metadataegenskapene som er tilgjengelige for kontrollen, har de samme egenskapene som tilpasningserfaringen.


### <a name="developer-specifying-where-an-app-can-be-embedded"></a>[Utvikler] Angi hvor en app kan bygges inn

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


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
