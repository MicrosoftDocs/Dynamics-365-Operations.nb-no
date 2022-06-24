---
title: Hovedplanlegging med forretningsavtaler
description: Denne artikkelen beskriver hvordan planleggingsoptimalisering kan finne leverandøren og/eller leveringstiden for en planlagt ordre, basert på den beste prisen eller leveringstiden som finnes i kjøpsavtaler.
author: t-benebo
ms.date: 06/29/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ReqCreatePlanWorkspace
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: benebotg
ms.search.validFrom: 2020-05-29
ms.dyn365.ops.version: AX 10.0.12
ms.openlocfilehash: 29f0f44289e44b21cb304bd1f423d63f9f58f2db
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 06/03/2022
ms.locfileid: "8873760"
---
# <a name="master-planning-with-purchase-trade-agreements"></a>Hovedplanlegging med forretningsavtaler

[!include [banner](../../includes/banner.md)]

Denne artikkelen beskriver hvordan planleggingsoptimalisering kan finne leverandøren og/eller leveringstiden for en planlagt ordre, basert på den beste prisen eller leveringstiden som finnes blant alle kjøpsavtaler som er spesifisert for et gitt produkt.

## <a name="turn-on-the-purchase-trade-agreements-for-planning-optimization-feature"></a>Slå på funksjonen Kjøpsavtaler for planleggingsoptimalisering

Før du kan bruke denne funksjonen, må den være aktivert i systemet. Administratorer kan bruke [Funksjonsbehandling](../../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md)-arbeidsområdet til å kontrollere funksjonsstatusen og aktivere den hvis den kreves. Funksjonen vises på følgende måte:

- **Modul:** *Hovedplanlegging*
- **Funksjonsnavn:** *Kjøpsavtaler for planleggingsoptimalisering*

## <a name="prepare-your-system-to-evaluate-purchase-trade-agreements-during-master-planning"></a>Gjør systemet ditt klart til å evaluere kjøpsavtaler under hovedplanlegging

Følg denne fremgangsmåten for å konfigurere systemet til å bruke planleggingsoptimalisering som evaluerer kjøpsavtaler.

1. Gå til **Hovedplanlegging \> Oppsett \> Parametere for hovedplanlegging**. I **Planlagte ordre**-fanen, i **Leverandør**-delen, angir du følgende verdier:

    - **Finn forretningsavtale** – sett dette alternativet til **Ja** for å ta med kjøpsavtaler i hovedplanlegging.
    - **Søkekriterium** – Velg faktoren du vil prioritere for hver kjøpsavtale: **Minimum leveringstid** eller **Laveste enhetspris**.

1. Gå til **Innkjøp og leverandører \> Oppsett \> Priser og rabatter \> Aktiver pris/rabatt**, og kontroller at **Leverandør**-alternativet er satt til **Ja**.
1. Gå til **Behandling av produktinformasjon \> Oppsett \> Dimensjons- og variantgrupper \> Lagringsdimensjonsgrupper**, og velg en lagringsdimensjonsgruppe som gjelder for produkter som hovedplanleggingen skal evaluere kjøpsavtaler for. Kontroller at det er merket av for alle relevante lagringsdimensjoner i denne gruppen i **For innkjøpspriser**-kolonnen. Gjenta dette trinnet for alle relevante lagringsdimensjonsgrupper.

## <a name="prepare-a-released-product-to-evaluate-purchase-trade-agreements-during-master-planning"></a>Gjør et frigitt produkt klart til å evaluere kjøpsavtaler under hovedplanlegging

Når systemet er klargjort som beskrevet i den forrige delen, bør du følge denne fremgangsmåten for å kontrollere at hvert produkt du vil bruke sammen med denne funksjonen, er riktig konfigurert.

1. Gå til **Behandling av produktinformasjon \> Produkter \> Frigitte produkter**, og åpne et målprodukt.
1. I **Kjøp**-hurtigfanen kontrollerer du at ingen leverandør er tilordnet i **Leverandør**-feltet.
1. I handlingsruten, i fanen **Planlegg** i **Dekning**-gruppen, velger du **Varedekning** for å åpne **Varedekning**-siden for det valgte produktet. Bekreft følgende innstillinger:

    - I **Generelt**-fanen kan du definere leverandøroverstyringer. Hvis du vil at planleggingsoptimalisering skal bruke kjøpsavtaler til å velge en leverandør, bør du hindre at leverandører overstyres, ved å fjerne **Bruk spesifikk innstilling**-merket.
    - I **Leveringstid**-fanen kan du definere overstyringer for leveringstid. Hvis du vil at planleggingsoptimalisering skal bruke kjøpsavtaler til å velge leveringstider, bør du forhindre overstyringer av leveringstid. Fjern merket i avmerkingsboksen for hver type leveringstid du vil velge ved hjelp av kjøpsavtaler (**Kjøp**, **Produksjon** og/eller **Overfør**).

1. Lukk **Varedekning**-siden for å gå tilbake til detaljsiden for det valgte produktet.
1. I handlingsruten, på **Planlegg**-fanen, går du til **Prognose**-gruppen og velger **Forsyningsprognose** for å åpne **Forsyningsprognose**-siden. Kontroller at ingen rader som vises her, har en verdi i **Leverandørkonto**-kolonnen.
1. Lukk **Forsyningsprognose**-siden for å gå tilbake til detaljsiden for det valgte produktet.
1. På handlingsruten, i fanen **Kjøp** i **Forretningsavtaler**-gruppen, velger du **Vis forretningsavtaler**. Kontroller at alle de aktuelle kjøpsavtalene vises. Du må også kontrollere at **Ignorer leveringstid**-alternativet er satt til **Nei** for hver avtale der du vil at planleggingsoptimalisering skal bruke leveringstiden som er angitt for den avtalen.
1. I handlingsruten, i fanen **Planlegg** i **Ordreinnstillinger**-gruppen, velger du **Standard ordreinnstillinger** for å åpne **Standard ordreinnstillinger**-siden for det valgte produktet. I **Bestilling**-hurtigfanen viser du verdien i **Leveringstid for innkjøp**-feltet. Hvis ingen overstyring av leveringstid for varedekning er definert, vil planleggingsoptimalisering bruke denne verdien når den velger forretningsavtaler der alternativet **Ignorer leveringstid** er satt til **Ja**. Derfor bør du justere denne verdien slik du ønsker.
1. Gjenta denne fremgangsmåten for hvert relevant produkt.

> [!NOTE]
> Støtte for planleggingsoptimalisering for kjøpsavtaler med flere valutaer. Når du søker etter en forretningsavtale ved hjelp av alternativet **Laveste enhetspris**, vil systemet vurdere forretningsavtalelinjer med ulike valutaer, forutsatt at det er definert en valutakurs mellom forretningsavtalelinjevalutaen og regnskapsvalutaen for den juridiske enheten. Hvis ikke blir forretningsavtalelinjen ignorert, og du vil få en feilmelding under hovedplanleggingen. Hovedplanleggingen vil derfor inkludere informasjon fra alle relevante forretningsavtalelinjer der prisene kan omregnes til regnskapsvalutaen. Det er viktig å merke seg at det ikke tas hensyn til avrundingsregler i løpet av priskonverteringen på forretningsavtalen.

## <a name="examples-of-how-planning-optimization-finds-vendor-and-lead-times"></a>Eksempler på hvordan planleggingsoptimalisering finner leverandør- og leveringstider

Følgende tabell viser eksempler på hvordan ulike innstillinger for et frigitt produkt og de tilknyttede kjøpsavtalene påvirker verdiene som blir funnet for det resulterende bestillingsforslaget. Verdiene i **uthevet** skrift i de to kolonnene lengst til høyre, er verdiene som velges ved hjelp av planleggingsoptimalisering. Verdiene **_fet og kursiv_** i de andre kolonnene er innstillingene som produserte disse resulterende verdiene for hver rad.

| Frigitt produkt: Leverandør | Standard ordreinnstillinger: Leveringstid | Varedekning: Overstyr leverandør | Varedekning: Overstyr leveringstid | Forretningsavtale: Leverandør | Forretningsavtale: Leveringstid | Forretningsavtale: Ignorer leveringstid | Resulterende leverandør | Resulterende leveringstid |
| --- | --- | --- | --- | --- | --- | --- | --- | --- |
| ***US001** _ | _*_1_*_ | Nei | Nei | US003 | 3 | Nei | _ *US001** | **1** |
| US001 | 1 | ***Ja: US002** _ | _*_Ja: 2_*_ | US003 | 3 | Nei | _ *US002** | **2** |
| *(Tom)* | 1 | Nei | Nei | ***US003** _ | _*_3_*_ | Nei | _ *US003** | **3** |
| *(Tom)* | ***1** _ | Nei | Nei | _*_US003_*_ | 3 | Ja | _ *US003** | **1** |
| *(Tom)* | ***1** _ | _*_Ja: US002_*_ | Nei | US003 | 3 | Nei | _ *US002** | **1** |
| *(Tom)* | ***1** _ | _*_Ja: US002_*_ | Nei | US003 | 3 | Nei | _ *US002** | **1** |
| *(Tom)* | 1 | Nei | Ja: 2 | ***US003** _ | _*_3_*_ | Nei | _ *US003** | **3** |
| *(Tom)* | 1 | Nei | ***Ja: 2** _ | _*_US003_*_ | 3 | Ja | _ *US003** | **2** |

## <a name="additional-resources"></a>Tilleggsressurser

[Kjøpsavtaler](../../procurement/purchase-agreements.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
