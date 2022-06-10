---
title: Integrere Customer Voice i e-handelsområdesider
description: Dette emnet beskriver hvordan du integrerer Microsoft Dynamics 365 Customer Voice på Dynamics 365 Commerce-ehandelsnettsteder.
author: samjarawan
ms.date: 05/17/2022
ms.topic: article
audience: Application User, Developer, IT Pro
ms.reviewer: v-chgriffin
ms.search.region: Global
ms.author: samjar
ms.search.validFrom: 2019-10-31
ms.openlocfilehash: 272ec1a59ed45b2d2336dcfea16051d27011360f
ms.sourcegitcommit: 48d094d083c1bd45c3d72f8b666926b48ec7ae35
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 05/18/2022
ms.locfileid: "8767955"
---
# <a name="integrate-customer-voice-into-e-commerce-site-pages"></a>Integrere Customer Voice i e-handelsområdesider

[!include [banner](../includes/banner.md)]

Dette emnet beskriver hvordan du integrerer Microsoft Dynamics 365 Customer Voice på Dynamics 365 Commerce-ehandelsnettsteder.

Du kan integrere [Customer Voice](https://dynamics.microsoft.com/customer-voice/overview/) på e-handelsområdet for å samle inn, analysere og spore tilbakemeldinger fra kunder i sanntid. For å komme i gang med integreringen må du opprette en konto og velge en Customer Voice-prosjektmal for tilbakemeldingstypen du vil samle inn.

## <a name="integrate-the-customer-voice-service"></a>Integrere Customer Voice-service

Hvis du vil opprette en Customer Voice-konto, kan du gå til [Customer Voice](https://dynamics.microsoft.com/customer-voice/overview/) og følge ledetekstene.

Når du oppretter en Customer Voice-konto og logger på, er neste trinn å velge en prosjektal for tilbakemeldingstypen du vil samle inn.

Følg denne fremgangsmåten for å velge en Customer Voice-prosjektmal.

1. Gå til [siden for Customer Voice-prosjektmalen](https://customervoice.microsoft.com/Pages/ProjectPage.aspx).
1. Velg **Kom i gang**.
1. Velg prosjektmalen for tilbakemeldingstypen du vil samle inn, og velg deretter **Neste**.
1. Velg et innebyggingsformat under **Velg et innebyggingsformat** i kategorien **Send**. Feltet **Innebygd kode** viser koden som må bygges inn i Commerce-områdebygger.

Eksemplene i dette emnet bruker prosjektmalen for **Periodisk kundeundersøkelse** og **Knapp**-innebyggingsformat.

Illustrasjonen nedenfor viser den prosjektmalsiden **Periodisk kundeundersøkelse**, der alternativet for **Knapp**-innebyggingsformatet er valgt, og innebyggingskode for dette alternativet vises i feltet **Innebygd kode**. Tre separate handlinger kreves for å bygge inn den angitte koden på områdesidene, som beskrevet i delene nedenfor.

![Customer Voice Periodisk kundeundersøkelse-siden med Knapp-alternativet valgt.](media/customer-voice-integration-1.png)

### <a name="embed-the-external-script-url"></a>Bygge inn den eksterne skript-URLen

På alle områdesider som skal ha en Customer Voice-undersøkelse, må du bygge inn den eksterne skript-URL-adressen som Customer Undersøker angav i innebyggingskoden. Den beste måten å bygge inn skriptet på flere områdesider på, er å opprette et fragment i områdekonfiguratoren som inneholder den eksterne skript-URL-adressen, og deretter legge til skriptet i de riktige sidemalene. Når du har publisert en oppdatert mal, vil den innebygde eksterne skriptkoden ligne på følgende eksempel på de berørte områdesidene.

```html
<script src=https://mfpembedcdnmsit.azureedge.net/mfpembedcontmsit/Embed.js type="text/javascript"></script>
```

Hvis du vil ha mer informasjon om fragmenter, kan du se [Arbeide med fragmenter](work-with-fragments.md).

> [!NOTE]
> Du trenger bare å legge til URLen i fragmentet. Den eksterne skriptmodulen legger til den andre skriptkoden.

Følg denne fremgangsmåten for å bygge inn den eksterne skript-URLen i et fragment.

1. I områdekonfiguratoren oppretter du et fragment som er basert på [Ekstern skriptmodul](script-module.md).
1. I det nye fragmentet velger du sporet **Standard eksternt skript**.
1. I ruten **Standard eksterne skript**-egenskaper i feltet **Skriptkilde** angir du den eksterne skript-URL-adressen, som vist i eksemplet nedenfor.

    ![Ekstern skript-URL i Skriptkilde-feltet for det nye fragmentet.](media/customer-voice-integration-2.png)

1. Velg **Lagre**, og velg deretter **Fullfør redigering**.
1. Velg **Publiser** for å publisere fragmentet.

Det nye fragmentet som inneholder den innebygde eksterne skriptblokken, er nå klar til å legges til i den aktuelle sidemalen.

### <a name="embed-the-external-style-sheet-code"></a>Bygge inn den eksterne stilarkkoden

På alle områdesider som skal ha en Customer Voice-undersøkelse, må du nå bygge inn den eksterne stilarkkoden som Customer Undersøker angav i innebyggingskoden. Som i forrige avsnitt, er sen beste måten å bygge inn den eksterne stilarkkoden på flere områdesider på, å opprette et fragment i områdekonfiguratoren som inneholder stilarkkoden, og deretter legge til skriptet i de riktige sidemalene. Den innebygde eksterne stilarkkoden vil ligne på følgende eksempelkode.

```typescript
<link rel="stylesheet" type="text/css" href=https://mfpembedcdnmsit.azureedge.net/mfpembedcontmsit/Embed.css />
```

Følg denne fremgangsmåten for å bygge inn den eksterne stilarkkoden i et fragment.

1. I områdekonfiguratoren oppretter du et fragment som er basert på [Modul for metakoder](metatags-module.md).
1. Velg sporet **Standard metakoder** i fragmentet.
1. I ruten **Standard metakoder**-egenskaper i feltet **Metakoder** angir du stilarkkoden, som vist i eksemplet nedenfor.

    ![Ekstern stilarkkode i metakodefeltet for det nye fragmentet.](media/customer-voice-integration-3.png)

1. Velg **Lagre**, og velg deretter **Fullfør redigering**.
1. Velg **Publiser** for å publisere fragmentet.

Det nye fragmentet som inneholder den innebygde eksterne stilarkkoden, er nå klar til å legges til i den aktuelle sidemalen.

### <a name="embed-the-inline-script-code"></a>Bygge inn den innebygde skriptkoden 

På alle områdesider som skal ha en Customer Voice-undersøkelse, må du nå bygge inn den innebygde skriptkoden som Customer Voice angav i innebyggingskoden. Som i de forrige delene er den beste måten å bygge inn den innebygde skriptkoden på flere områdesider på, å opprette et fragment i områdekonfiguratoren som inneholder stilarkkoden, og deretter legge til skriptet i de riktige sidemalene.

I følgende eksempel på linjeskriptkode er **SURVEY\_KEY** en plassholder. Verdien for **SURVEY\_KEY** bør samsvare med den faktiske undersøkelsesnøkkelen som Customer Voice angav i innebygd kode. Den siste linjen kaller koden for å gjengi undersøkelsesknappen etter ett sekund, for å sikre at skriptene har nok tid til å lastes. Avhengig av undersøkelsen du valgte, kan det være at du også må legge til eller oppdatere andre metadata, for eksempel firmanavnet.

```html
function renderSurveyButton() {
    var se = new SurveyEmbed("SURVEY_KEY","https://customervoice.microsoft.com/","https://mfpembedcdnmsit.azureedge.net/mfpembedcontmsit/","true");

    var context = {
        "First Name":"",
        "Last Name": "",
        "locale": "en-us",
        "companyname": "Adventure Works"
    };
    se.renderButton(context);
}

setTimeout(renderSurveyButton, 4000);
```

Følg denne fremgangsmåten for å bygge inn den innebygde skriptkoden i et fragment.

1. I områdekonfiguratoren oppretter du et fragment som er basert på [Innebygd skriptmodul](script-module.md).
1. I det nye fragmentet velger du sporet **Standard innebygd skript**.
1. I ruten **Standard innebygd skript**-egenskaper i feltet **Innebygd skript** angir du den innebygde skriptkoden, som vist i eksemplet nedenfor.

    ![Innebygd skriptiode i Innebygd skript-feltet for det nye fragmentet.](media/customer-voice-integration-4.png)

1. Velg **Lagre**, og velg deretter **Fullfør redigering**.
1. Velg **Publiser** for å publisere fragmentet.

Det nye fragmentet som inneholder den integrerte innebygde skriptkoden, er nå klar til å legges til i den aktuelle sidemalen.

## <a name="add-fragments-to-a-template"></a>Legge til fragmenter i en mal

Når du er ferdig med å lage fragmentene som inneholder den innebygde Customer Voice-koden, må du legge dem til i sidemalene som er tilknyttet områdesidene der du vil bruke dem. I illustrasjonen nedenfor er de tre eksempelfragmentene lagt til i en PDP-mal (product details page).

![Eksempel på fragmenter som er lagt til en PDP-mal.](media/customer-voice-integration-5.png)

Når den oppdaterte malen er publisert, vil Customer Voice-kundeundersøkelsen vises på alle sider som styres av malen.

Hvis du vil ha informasjon om maler, kan du se [Arbeide med maler](work-with-templates.md).

## <a name="configure-content-security-policy"></a>Konfigurere sikkerhetspolicy for innhold

Som standard tillater ikke innholdssikkerhetspolicy (CSP) kall til andre tjenester med mindre tilleggskonfigurasjon er utført. Når du har publisert de oppdaterte malene, er det derfor sannsynlig at undersøkelsen ikke vil bli lastet inn på de relevante områdesidene. Hvis du vil vise CSP-relaterte feil, åpner du webleserens utviklerverktøy (F12) og går deretter til en side som inneholder undersøkelsen. De CSP-relaterte feilene vises i konsollutdataene.

For å konfigurere CSP i områdebyggeren for å reparere feilene, følger du disse trinnene.

1. Gå til **Områdeinnstillinger \> Tillegg**.
1. I kategorien **Innholdssikkerhetspolicy** legger du til `https://customervoice.microsoft.com/` i direktivet **child-src**.
1. Legg til `https://customervoice.microsoft.com/` i **frame-src**-direktivet.
1. Legg til `https://mfpembedcdnmsit.azureedge.net` og **.azureedge.net** i direktivet **img-src**.

Hvis du vil ha mer informasjon, se [Innholdssikkerhetspolicy](manage-csp.md).

## <a name="additional-resources"></a>Tilleggsressurser

[Ekstern skriptmodul](script-module.md)

[Modul for metakoder](metatags-module.md)

[Innebygd skriptmodul](script-module.md)

[Innholdssikkerhetspolicy](manage-csp.md)

[Arbeide med fragmenter](work-with-fragments.md)

[Arbeide med maler](work-with-templates.md)
