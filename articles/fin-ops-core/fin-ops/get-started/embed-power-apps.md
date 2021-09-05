---
title: Bygge inn lerretsapper fra Power Apps
description: Dette emnet forklarer hvordan du bygger inn lerretsapper fra Microsoft Power Apps i klienten for å øke produktets funksjonalitet.
author: jasongre
ms.date: 08/09/2021
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
ms.openlocfilehash: 37ef6101a5a69e9c820347dd6f61c987467d40b3
ms.sourcegitcommit: b9c2798aa994e1526d1c50726f807e6335885e1a
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 08/13/2021
ms.locfileid: "7344535"
---
# <a name="embed-canvas-apps-from-power-apps"></a>Bygge inn lerretsapper fra Power Apps

[!include [banner](../includes/banner.md)]
[!include [banner](../includes/preview-banner.md)]

Microsoft Power Apps er en tjeneste som lar utviklere og ikke-tekniske brukere lage egendefinerte forretningsprogrammer for mobilenheter, nettbrett og nettet uten å måtte skrive kode. Finance and Operations-apper støtter integrasjon med Power Apps. Lerretsapper som du, organisasjon din eller det videre økosystemet utvikler, kan bygges inn i Finance and Operations-apper for å øke produktets funksjonalitet. Du kan for eksempel bygge en lerretsapp fra Power Apps for å supplere en Finance and Operations-app med informasjon som hentes fra et annet system.

Hvis du vil vite mer om innebygging av lerretsapper, kan du se den korte videoen [Slik bygger du inn lerretsapper](https://www.youtube.com/watch?v=x3qyA1bH-NY).

## <a name="adding-an-embedded-canvas-app-from-power-apps-to-a-page"></a>Legge til en innebygd lerretsapp fra Power Apps på en side

Før du bygger inn en lerretsapp fra Power Apps i klienten, må du først finne eller lage en app med ønskede visuelle effekter og/eller funksjonalitet. Dette emnet inneholder ikke en detaljert beskrivelse av prosessen for bygging av apper. Hvis du ikke har brukt Power Apps, se [Power Apps-dokumentasjonen](/powerapps/).

Det finnes tre måter å bygge inn en app på i en Finance and Operations-app. Du kan bruke fremgangsmåten som passer best til scenariet. 

- Bygg inn lerretsappen i **Power Apps**-knappen i den standard handlingsruten på en side. Apper du legger til på denne måten, vises som elementer på **Power Apps**-menyknappen, og appene åpnes i sideruter. 
- Bygg inn lerretsappen direkte på en eksisterende side som en ny kategoriside (pivotfane, hurtigfane, blad eller arbeidsområde).
- Opprett en ny fullsideopplevelse for lerretsappen fra instrumentbordet.

Når du konfigurerer den innebygde lerretsappen, kan du velge ett felt du vil sende som kontekst til appen. Dette trinnet gjør at appen kan svare på grunnlag av dataene som vises nå.

> [!NOTE]
> Du kan ikke bruke denne mekanismen til å bygge inn modelldrevne apper.

### <a name="embedding-a-canvas-app-on-an-existing-page"></a>Bygg inn en lerretsapp på en eksisterende side

Fremgangsmåten nedenfor viser hvordan du bygger inn en lerretsapp på en eksisterende side fra Power Apps.

1. Gå til siden der du vil bygge inn lerretsappen. Denne siden inneholder data som må sendes til appen som inndata.
2. Åpne **Legg til en app fra Power Apps**-ruten:

    - Hvis appen skal bygges inn direkte på siden, velger du **Alternativer** \> **Tilpass denne siden** \> **Mer**, og deretter følger du ett av disse trinnene:

        - Hvis funksjonen **Fullsideapper** er aktivert, velger du **Legg til en side** og velger deretter området der du vil legge til appen. Hvis du vil bygge inn appen i **Power Apps**-menyknappen, velger du handlingsruten. Hvis du vil bygge inn appen direkte på siden, velger du den aktuelle fanen, hurtigfanen, bladet eller delen (hvis du er koblet til et arbeidsområde). Deretter velger du en **Power Apps**-app i ruten **Legg til en app**.
        - Hvis funksjonen **Fullsideapper** er deaktivert, velger du **Legg til en app fra Power Apps** og velger deretter området der du vil legge til appen. Hvis du vil bygge inn appen i **Power Apps**-menyknappen, velger du handlingsruten. Hvis du vil bygge inn appen direkte på siden, velger du den aktuelle fanen, hurtigfanen, bladet eller delen (hvis du er koblet til et arbeidsområde).

    - Hvis appen åpnes ved hjelp av **Power Apps**-menyknappen, kan du også velge **Power Apps**-menyknappen i standardhandlingsruten, og deretter velger du **Legg til en app**.

3. Konfigurer den innebygde appen. Hvis du vil ha mer informasjon, kan du se delen [Konfigurer en lerretsapp](#configuring-a-canvas-app) senere i dette emnet.
4. Når du har bekreftet at konfigurasjonen er riktig, velger du **Sett inn**.

    - Hvis funksjonen **Lagrede visninger** er slått av, blir du bedt om å oppdatere webleseren for å se den innebygde appen.
    - Hvis funksjonen **Lagrede visninger** er aktivert, må du lagre visningen for at endringen skal vedvare.

### <a name="embedding-a-canvas-app-as-a-full-page-experience-from-the-dashboard"></a>Bygg inn en lerretsapp som en helsideopplevelse fra instrumentbordet

Det kan hende at du vil bygge inn en lerretsapp fra instrumentbordet hvis appen ikke er relatert til en eksisterende side, eller hvis du bare vil legge inn appen som en fullsideopplevelse i Finance and Operations-appen.

> [!NOTE]
> Du må aktivere funksjonen **Fullsideapper** i funksjonsadministrasjon for å gjøre denne funksjonen tilgjengelig. 

1. Åpne instrumentbordet.
2. Velg og hold siden nede (eller høyreklikk), velg **Tilpass**, og velg deretter **Legg til en side**.
3. I ruten **Legg til en side** velger du **Power Apps**.
4. Konfigurer den innebygde appen. Hvis du vil ha mer informasjon, kan du se delen [Konfigurer en lerretsapp](#configuring-a-canvas-app) senere i dette emnet.
5. Velg **Lagre** for å legge til appen på instrumentbordet som en ny flis.
6. Velg den nye flisen på instrumentbordet, og bekreft at lerretsappen vises som forventet.

### <a name="configuring-a-canvas-app"></a>Konfigurer en lerretsapp

Når du bygger inn en lerretsapp, må du angi følgende parametere:

- **Navn** – Angi teksten som skal vises for knappen eller fanen som skal inneholde den innebygde appen. Ofte vil du kanskje gjenta navnet på appen i dette feltet.
- **App-ID** – Angi GUID-en (globalt unik identifikator) for lerretsappen du vil bygge inn. Hvis du vil hente denne verdien, finner du appen på [make.powerapps.com](https://make.powerapps.com), og deretter ser du i feltet **App-ID** under **Detaljer**.
- **Inndatakontekst for app** – Du kan også velge feltet som inneholder dataene du vil sende til appen som inndata. Hvis du vil ha mer informasjon om hvordan appen får tilgang til data som er sendt fra Finance and Operations-apper, kan du se delen [Bygg en app som benytter data som sendes fra Finance and Operations-apper](#building-a-canvas-app-that-uses-data-that-is-sent-from-finance-and-operations-apps) senere i dette emnet.

    Fra og med versjon 10.0.19 blir også den gjeldende juridiske enheten sendt som kontekst til lerretsappen via URL-parameteren **cmp**. Denne virkemåten vil ikke påvirke lerretsappen før appen bruker denne informasjonen.

- **Appstørrelse** – Velg typen app du bygger inn. Velg **Tynn** for apper som er bygd for mobilenheter, eller **Bred** for apper som er bygd for nettbrett. Denne parameteren sørger for at nok plass blir tildelt til den innebygde appen.
- **Juridiske enheter** – Du kan velge de juridiske enhetene som appen skal være tilgjengelig for. Som standard er appen tilgjengelig for alle juridiske enheter. Dette alternativet er bare tilgjengelig når du bygger inn direkte på en eksisterende side, og funksjonen **[Lagrede visninger](saved-views.md)** er deaktivert.

## <a name="sharing-an-embedded-app"></a>Dele en innebygd app

Når du har bygd inn en lerretsapp på en side og bekreftet at den fungerer som den skal, kan det hende at du vil dele appen med andre brukere i systemet. Følg disse trinnene for å dele en innebygd lerretsapp.

1. [Del lerretsappen i Power Apps](/powerapps/maker/canvas-apps/share-app) med de aktuelle brukerne, slik at de kan få tilgang til appen direkte i Power Apps.
2. Del tilpasningene som er knyttet til den innebygde appen, med de ønskede brukerne. Du kan bruke en av følgende tilnærminger:

    - **Publiser visningen (anbefalt):** Hvis funksjonen **[Lagrede visninger](saved-views.md)** er aktivert, er den anbefalte og foretrukne tilnærmingen å opprette en visning som omfatter den innebygde appen, og deretter publisere visningen til de ønskede brukerne. Denne fremgangsmåten sikrer at alle brukere som har sikkerhetsroller som er målrettet av den publiserte visningen, vil se lerretsappen på siden.

        Du kan også publisere en lerretsapp som er innebygd som en helsideopplevelse fra instrumentbordet. Velg og hold (eller høyreklikk) flisen som er tilknyttet appen, på instrumentbordet, velg **Tilpass**, og velg deretter **Publiser side**. En opplevelse som ligner på *publiseringsvisninger* vises, og du kan velge sikkerhetsrollene du vil publisere til. Hvis funksjonen **Forbedret støtte for juridiske enheter for lagrede visninger**, i oppdatering 10.0.21 eller senere, er aktivert, kan du også publisere appen til de ønskede juridiske enhetene.

    - Hvis funksjonen **Lagrede visninger** er deaktivert, kan systemadministratoren gi en tilpasning som inkluderer lerretsappen, til det aktuelle settet med brukere via **Tilpasning**-siden. Du kan også eksportere personlige tilpasninger for siden og sende dem til én eller flere brukere. Hver av disse brukerne kan deretter importere tilpasningen. Tilpasning-verktøylinjen inneholder knapper som lar deg eksportere og importere tilpasninger.

> [!NOTE]
> Hvis lerretsappen er delt med eksterne brukere, kan ikke disse brukerne bruke den innebygde appen i Finance and Operations-apper. De kan imidlertid få tilgang til appen direkte i Power Apps. Eksterne brukere inkluderer gjester og brukere som ikke hører til i Microsoft 365 Azure Directory der Finance and Operations-appen distribueres.

Se [Tilpasse brukeropplevelsen](personalize-user-experience.md) for mer informasjon om tilpassing av funksjonene i produktet og hvordan de brukes.

## <a name="building-a-canvas-app-that-uses-data-that-is-sent-from-finance-and-operations-apps"></a>Bygge en lerretsapp som bruker data som sendes fra Finance and Operations-apper

Når du bygger en lerretsapp som skal bygges inn i en Finance and Operations-app, er en viktig del av prosessen å bruke inndataene fra denne Finance and Operations-appen. Fra Power Apps-utviklingsopplevelsen kan inndataene sendt fra en Finance and Operations-app åpnes ved hjelp av variabelen **Param ("EntityId")**. I tillegg, fra og med versjon 10.0.19, blir også den gjeldende juridiske enheten sendt til lerretsappen via **Param("cmp")**-variabelen. 

I appens OnStart-funksjon kan du for eksempel sette inndataene fra Finance and Operations-apper til en variabel som ser slik ut:

``` Power Apps
If(!IsBlank(Param("EntityId")), Set(FinOpsInput, Param("EntityId")), Set(FinOpsInput, ""));

If(!IsBlank(Param("cmp")), Set(FinOpsLegalEntity, Param("cmp")), Set(FinOpsLegalEntity, ""));
```

## <a name="viewing-a-canvas-app"></a>Vise en lerretsapp

Hvis du vil vise en innebygd lerretsapp på en side i Finance and Operations-apper, går du til en side med en innebygd app. Husk at apper kan åpnes ved hjelp av **Power Apps**-knappen i standardhandlingsruten. De kan også vises direkte på siden som en ny fane eller hurtigfane eller et blad eller som en ny inndeling i et arbeidsområde. Når brukere først prøver å laste inn en app på en side, blir de bedt om å logge på. Dette trinnet sikrer at brukerne har de nødvendige tillatelsene til å bruke appen.

## <a name="editing-an-embedded-app"></a>Redigere en innebygd app

Når en app har blitt innebygd på en side, må du kanskje gjøre noen endringer i konfigurasjonen av appen. Du vil for eksempel kanskje endre etiketten som er knyttet til den innebygde appen, eller det har blitt opprettet en ny versjon av en app og du må oppdatere program-IDen for å henvise til den siste versjonen.

Følg denne fremgangsmåten for å redigere konfigurasjonen av en innebygd app:

1. Gå til **Rediger appen**-ruten.

    - Hvis den innebygde appen er tilgjengelig via Power Apps-menyknappen, velger du og holder (eller høyreklikker på) Power Apps-menyknappen og velger **Tilpass**. Velg appen du vil konfigurere, fra rullegardinlisten **Velg en app**.
    - Hvis den innebygde appen vises direkte på siden, velger du **Alternativer**, og deretter velger du **Tilpass denne siden**. Ved hjelp av verktøyet **Velg** klikker du den innebygde appen.
    - Hvis den innebygde appen ble lagt til fra instrumentbordet, åpner du instrumentbordet, velger og holder (eller høyreklikker på) flisen som er knyttet til lerretsappen, velger **Tilpass** og velger deretter **Rediger side**.

2. Gjør nødvendige endringer i appkonfigurasjonen, og klikk deretter på **Lagre**.

## <a name="removing-an-app"></a>Fjerne en app

Når en app er innebygd på en side, er det noen måter å fjerne den på om nødvendig:

- Gå til ruten **Rediger en app** ved hjelp av instruksjonene fra delen [Redigere en innebygd app](#editing-an-embedded-app) tidligere i dette emnet. Bekreft at ruten viser informasjon for den innebygde app som du vil fjerne, og klikk deretter på **Slett**-knappen.
- Hvis den innebygde appen ble lagt til fra instrumentbordet, åpner du instrumentbordet, velger og holder (eller høyreklikker på) flisen som er knyttet til lerretsappen, velger **Tilpass** og velger deretter **Fjern side**. 
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
