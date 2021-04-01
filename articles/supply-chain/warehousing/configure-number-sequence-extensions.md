---
title: Konfigurer nummerserier for lagerflyter
description: Dette emnet gir en oversikt over funksjonaliteten som inneholder nummerserieutvidelser for nummerskilt-IDer, bølgeetikett-IDer, container-IDer og fraktbrev-IDer.
author: GarmMSFT
manager: tfehr
ms.date: 06/10/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: WHSNumberSequenceExt
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2020-06-10
ms.dyn365.ops.version: 10.0.2
ms.openlocfilehash: 5de5f4695b4e4ccaaf050c3593d3f7ee0cc32ed8
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 02/15/2021
ms.locfileid: "5232941"
---
# <a name="configure-number-sequences-for-warehouse-flows"></a>Konfigurer nummerserier for lagerflyter

[!include [banner](../includes/banner.md)]

Funksjonen *Nummerserieutvidelser* legger til en ny konfigurasjonsside for oppretting av nummerserier. Den gjør det mulig med fleksibel konfigurering av GS1-regulerte IDer, inkludert GS1-prefikser og kontrollsifre (modulo 10), og fremtvinger lengdebegrensninger på eksisterende nummerserier.

Standard nummerseriesegmenter passer ikke for GS1-implementering, fordi det ikke beregnes kontrollsiffer, og selskapets GS1-prefiks må oppdateres manuelt.

Denne funksjonen legger til følgende funksjonalitet:

- Fraktbrev-ID-er kan genereres på forhånd.
- En unik nummerserie kan genereres for SSCC-numre (Serial Shipping Container Code).
- GS1-kompatible nummerserier kan opprettes for BOL- og SSCC-numre. Denne funksjonen legger til standardstøtte for nummerskilt-IDer, container-IDer, bølgeetikett-IDer og fraktbrev-IDer.
- Konfigurasjon av ID-numre for lisensplate er fleksibelt. Du kan for eksempel inkludere eller utelate app-ID-er (AI), for eksempel ledende nuller (00).

Denne funksjonaliteten gjør det mer effektivt å støtte etiketter med kartonger og justere nye numre som genereres av systemet.

## <a name="turn-on-the-number-sequence-extensions-feature"></a>Aktivere funksjonen for nummerserieutvidelser

Før du kan bruke funksjonen må den være aktivert i systemet. Administratorer kan bruke [Funksjonsbehandling](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md)-arbeidsområdet til å kontrollere funksjonsstatusen og aktivere den hvis den kreves. Funksjonen vises på følgende måte:

- **Modul:** *Lagerstyring*
- **Funksjonsnavn:** *Nummerserieutvidelser*

## <a name="set-up-the-feature"></a>Definere funksjonen

Følg denne fremgangsmåten for å definere nummerserieutvidelser i systemet.

1. Gå til **Lagerstyring \> Oppsett \> Lagerstyringsparametere**.
1. I fanen **Generelt** i feltet **GS1-firmaprefiks** angir du firmaets GS1-prefiks. Denne verdien vil påvirke alle nummerserier der GS1-prefikset er inkludert som et segment.
1. Hvis du vil generere BOL-numre for bølgeetiketter, merker du av for å **generere BOL-nummer ved utskrift av bølgeetiketter** i fanen **Rapporter**.

    > [!NOTE]
    > Denne avmerkingsboksen er bare tilgjengelig hvis funksjonaliteten for [bølgeetikettutskrift](configure-wave-label-printing.md) er slått på.

1. Gå til **Lagerstyring** \> **Oppsett** \> **Nummerserieutvidelser**
1. Velg **Opprett standardoppsett** i handlingsruten. En GS1-kompatibel BOL-nummerserie og tre typer SSCC-nummerserier opprettes. Alle disse nummerseriene tar lengden på firmaets GS1-prefiks med i betraktningen.

    Hvis du vil ha mer informasjon om hvordan du tilpasser disse standard nummerseriene og/eller legger til nye sekvenser, kan du se neste del. Du kan også fjerne noen av disse sekvensene hvis du ikke trenger dem.

1. Gå tilbake til **Lagerstyring \> Oppsett \> Lagerstyringsparametere**.
1. I fanen **Nummerserier** velger du en relevant nummerserieutvidelse som skal brukes til å generere numre for lisensplate-IDer, bølgeIDer, container-IDer (i dette tilfellet velge riktig **SSCC-18-nummer**-serie) og/eller Bol-IDer (i dette tilfellet velger du **BOL**-sekvensen). Som standard støttes nummerserieutvidelser bare for disse fire typene av IDer.

Neste gang et nytt nummer genereres for en av disse nummerseriene, blir den nye logikken brukt.

> [!NOTE]
> Hvis du ikke velger en nummerserieutvidelse for lisensplate-IDer, brukes de gjeldende reglene for å generere lisensplate-IDer. Hvis ikke brukes den valgte nummerserien. De andre IDene vil bruke en vanlig nummerserie til du bruker en nummerserieutvidelse for dem.

## <a name="create-and-edit-number-sequences"></a>Opprette og redigere nummerserier

I den forrige delen genererte du et standard sett med nummerserier. Denne delen forklarer hvordan hver nummerserie defineres. Den forklarer også hvordan du oppretter egendefinerte sekvenser og hvordan du redigerer standard eller egendefinerte sekvenser.

Følg denne fremgangsmåten for å opprette og redigere nummerserier.

1. Gå til **Lagerstyring** \> **Oppsett** \> **Nummerserieutvidelser**.
1. Velg **Ny** i handlingsruten.
1. I feltet **Nummerserieutvidelser** angir du et navn på den nye sekvensen. Angi en beskrivelse i **Beskrivelse**-feltet.
1. I hurtigfanen **Segmenter** bruker du knappene på verktøylinjen til å sette inn nummereringsformatet ved å legge til, slette og ordne segmenter. I **Segment**-feltet for hver rad tilordner du en segmenttype for å definere formålet med og innholdet i segmentet. Tabellen nedenfor inneholder en beskrivelse av typer segmenter som er tilgjengelige.

    | Segmenttype | beskrivelse |
    |---|---|
    | Konstant | Denne segmenttypen legger til samme konstanttekst for hvert genererte tall i sekvensen. I **Verdi**-feltet legger du inn teksten som kreves. **Lengde**-feltet oppdateres automatisk til lengden på teksten du har angitt i **Verdi**-feltet. |
    | Nummerserie | I **Verdi**-feltet angir du et nummertegn (*\#*) for hvert tegn som skal vises i den genererte rekkefølgen. Selve nummerserien kan generere lengre numre, men bare tegn som er lengst til høyre, vil bli vist. **Lengde**-feltet oppdateres automatisk til antall nummertegn du har angitt i **Verdi**-feltet.<p>Hvis du vil overholde GS1-kravene for SSCC-18-numre, må du kontrollere at lengden på dette segmentet er 16 minus lengden på GS1-prefikset.</p> |
    | GS1-prefiks | Denne segmenttypen legger til verdien som er angitt i feltet **GS1-firmaprefiks** på siden for **Lagerstyringsparametere**. **Verdi**-feltet viser verdien som er angitt på siden **Lagerstyringsparametere**, og feltet **Lengde** viser antall tegn i verdien. Både **Verdi**-feltet og **Lengde**-feltet er skrivebeskyttet. |
    | Program-ID | I **Verdi**-feltet angir du en programidentifikatoren, som angitt av den relevante GS1-policyen for denne typen nummerserie. Skriv for eksempel *00* for SSCC eller *420* for BOL. **Lengde**-feltet oppdateres automatisk til lengden på identifikatoren du har angitt i **Verdi**-feltet. |
    | Emballasjetype | For varer som kan identifiseres tydelig, legger denne segmenttypen til en feltverdi fra den aktuelle enhetsseriegruppen (fra siden **Sekvensgrupper for enhet**). (Denne virkemåten samsvarer med den eksisterende logikken for nummerskilt-IDer.) For lisensplater som inneholder flere lagerenheter (SKUer), legger denne segmenttypen til *0* (null) som standard. For denne segmenttypen er feltet **Verdi** alltid satt til *P*, og feltet **Lengde** alltid satt til *1*.|
    | Kontrollsiffer | Denne segmenttypen legger til et kontrollsiffer, som er en modulus 10-beregning. (Denne virkemåten samsvarer med den eksisterende logikken for nummerskilt-IDer.) For denne segmenttypen er **Verdi**-feltet alltid satt til et cirkumflekstegn (*^*), og **Lengde**-feltet er alltid satt til *1*. |

1. Hvis du vil vise et eksempel på det endelige tallformatet, kontrollerer du **Format**-feltet nederst i hurtigfanen **Segmenter**.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]