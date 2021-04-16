---
title: Produksjonsparametere i Produksjonsutførelse
description: Dette emnet gir informasjon om oppsettet av produksjonsparametere i Produksjonsutførelse.
author: johanhoffmann
ms.date: 06/16/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: JmgProdParameters
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: Manufacturing
ms.author: johanho
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: Version 1611
ms.openlocfilehash: 30bbcd0365fada4554dc2f7d12b40abc9b22ac63
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 04/01/2021
ms.locfileid: "5814614"
---
# <a name="production-parameters-in-manufacturing-execution"></a>Produksjonsparametere i Produksjonsutførelse

[!include [banner](../includes/banner.md)]

Dette emnet gir informasjon om oppsettet av produksjonsparametere i Produksjonsutførelse.

Modulen **Produksjonsutførelse** er tiltenkt brukt hovedsakelig av produksjonsselskaper. Den kan brukes til å registrere tids- og vareforbruk for produksjonsjobber eller prosjekter. Før du begynner å bruke produksjonsutførelse for jobbregistreringer, må du definere forskjellige produksjonsparametere som definerer hvordan og når registreringer posteres i løpet av produksjonsprosessen. Innstillingene for produksjonsparametere påvirker lagerstyring, produksjon, administrasjon og kostnadsberegningen.

Du bør nøye vurdere alle innstillingene på siden **Produksjonsparametere** før arbeidere begynner å gjøre registreringer på produksjonsjobber. Klikk på **Produksjonskontroll** &gt; **Oppsett** &gt; **Produksjonsutførelse** &gt; **Standarder for produksjonsordre**. Hvis firmaet ditt bruker multisite-funksjonaliteten, vil du kanskje definere forskjellige produksjonsparametere for hvert område. Parameterne for integrasjon med **Produksjon**-modulen defineres i følgende kategorier på siden **Produksjonsparametere**:

- **Generelt** – generelle parameterinnstillinger for produksjonsjobber i produksjonsutførelse.
- **Start** - Parametere som brukes når produksjonsoperasjoner startes.
- **Operasjoner** – Parametere som brukes på produksjonsoperasjoner og tilbakemeldinger for operasjoner i løpet av produksjonsprosessen.
- **Ferdigmeld** – Parametere som brukes når varer rapporteres som ferdigmeldt i den siste operasjonen til en produksjonsordre.
- **Antallsvalidering** – Parametere som brukes for validering av start- og tilbakemeldingsantall på produksjonsordrer.

## <a name="types-of-production-jobs"></a>Typer produksjonsjobber
På **Operasjoner**-fanen velger du typene produksjonsjobber som krever registrering på siden **Jobbregistrering**.

Vanligvis foretar arbeidere registreringer i oppsettjobber og prosessjobber. Hvis finplanlegging blir brukt, kan du imidlertid velge andre jobbtyper som ansatte må gjøre registreringer på når produksjonsordrer blir behandlet. Du kan for eksempel kreve registreringer for transportjobber.

> [!IMPORTANT]
> Kontroller at alle relevante jobbtyper velges. Ellers kan det være at jobber ikke er tilgjengelig for registrering på siden **Jobbregistrering**. Valgene skal samsvare med valgene i kolonnen **Jobbstyring** i **Oppsett** -fanen på siden **Rutegrupper** (**Produksjonskontroll** &gt; **Oppsett** &gt; **Ruter** &gt; **Rutegrupper**).

Hvis **Jobbstyring** velges i rutegruppen, rapporteres jobbtypen som ferdigmeldt på produksjonsordren når jobben er rapportert ferdigmeldt i produksjonsutførelse. Når alle jobbtyper som **Jobbstyring** er valgt for, er rapportert som fullført for en operasjon, rapporterer Produksjonsutførelse operasjonen som fullført.

> [!NOTE]
> Noen jobbtyper kan rapporteres manuelt gjennom produksjonsjournaler. I dette tilfellet velger du **Jobbstyring** for jobben, men ikke velg jobbtypen for registrering i **Operasjoner**-fanen på siden **Produksjonsparametere** i produksjonsutførelse.

## <a name="bom-consumption-and-picking-list-journals"></a>Stykklisteforbruk og plukklistejournaler
Et konsekvent oppsett for stykklisteforbruk er viktig for å garantere at lagerstyring er effektivt. Hvis for eksempel parametere for stykklisteforbruk ikke er satt opp riktig i produksjonsutførselse, kan materialer trekkes fra lager to ganger eller ikke i det hele tatt.

På **Produksjonsparametere**-siden er automatisk stykklisteforbruk definert i tre trinn:

- Ved starten av en produksjon. Definer dette stadiet i **Start**-fanen.
- I løpet av produksjonsprosessen når en operasjon er fullført. Definer dette stadiet i **Operasjoner**-fanen.
- Når en produksjonsordre rapporteres som avsluttet. Definer dette stadiet i **Ferdigmeld**-fanen.

For hvert trinn i feltet **Automatisk stykklisteforbruk** kan du velge én av tre metoder for å plukke varer for en produksjonsordre:

- **Trekkprinsipp** – dette alternativet brukes sammen med et alternativ som er definert for stykklisten i **Produksjon**- modulen. Klikk på **Produksjonskontroll** &gt; **Felles** &gt; **Produksjonsordrer** &gt; **Alle produksjonsordrer**. På siden **Alle produksjonsordrer** velger du en produksjonsordre i listen, og deretter klikker du **Stykkliste** på handlingsruten. På **Stykkliste**-siden i **Oppsett**-fanen i **Trekkprinsipp**-feltet velger du ett av følgende alternativer:

  - **Start**
  - **Fullfør**
  - **Manuell**
  - Tom (ingen alternativer er valgt.)
  - **Tilgjengelig på lokasjon**

    Hvis **Trekkprinsipp** er valgt i feltet **Automatisk stykklisteforbruk** i **Start**-fanen i produksjonsutførelse, trekkes alt materiale som er satt til **Start** i stykklisten, fra lagerbeholdningen når operasjonen startes. Alternativet **Tilgjengelig på lokasjon** brukes for produkter som er aktivert for avanserte lagerprosesser. Hvis du velger dette trekkprinsippet, tømmes materiale når lagerarbeid for råvareplukking er fullført. Materiale tømmes også når en stykklistelinje som bruker dette trekkprinsippet, er frigitt til lageret og materialet er tilgjengelig på produksjonsinnleveringsstedet.

    > [!NOTE]
    > Hvis feltet **Trekkprinsipp** er satt til **Start** i Produksjonsutførelse, må du velge samme prinsipp på enten fanen **Operasjoner** eller fanen **Rapporter som fullført**. Dette kravet bidrar til å sikre at materialer trekkes fra inventar på stykkliste som bruker **Fullført** som trekkprinsipp på produksjonsordren. Hvis det samme trekkprinsippet ikke velges for verken **Operasjoner**-fanen eller **Ferdigmeld**-fanen, kan materialer bli trukket fra lager to ganger.

- **Alltid** – Hvis du velger dette alternativet for et stadium, trekkes materialene alltid fra lageret på dette stadiet. Materialer for produksjonen trekkes for eksempel fra når produksjonsordren startes. Denne innstillingen krever at **Aldri** velges på **Operasjoner**- og **Ferdigmeld**-fanen. Dette kravet bidrar til å forhindre at varer blir trukket fra lagerbeholdningen to ganger.
- **Aldri** – Hvis du velger dette alternativet for et stadium, skjer intet stykklisteforbruk på dette stadiet. Hvis du for eksempel velger **Aldri** i alle tre kategorier (**Start**, **Operasjoner**, og **Ferdigmeld**), må materialer trekkes fra lageret manuelt.

> [!IMPORTANT]
> Vurder konfigurasjonen av produksjonsparameterne nøye og forsikre deg om at parameterne som er valgt i de forskjellige fanene på **Produksjonsparametere**-siden, ikke motstrider hverandre.

Eksemplene nedenfor viser parameterinnstillinger som støtter ulike prinsipper for stykklisteforbruk. Parameterne er definert på **Produksjonsparametere**-siden i produksjonsutførelse.

### <a name="example-1-backflushing-on-operations"></a>Eksempel 1: Backflushing for operasjoner

Bruk innstillingene nedenfor hvis plukklistejournaler og vareforbruket for stykklisten må genereres når varer rapporteres som ferdigmeldt for en operasjon.

| Kategori                | Felt                          | Innstilling                             |
|--------------------|--------------------------------|-------------------------------------|
| Start              | Oppdater start online           | **Status** eller **Status + antall** |
| Start              | Automatisk stykklisteforbruk      | **Aldri**                           |
| Operations         | Automatisk stykklisteforbruk      | **Alltid**                          |
| Ferdigmeld | Automatisk stykklisteforbruk      | **Aldri**                           |
| Ferdigmeld | Oppdater ferdig rapport online | **Status + antall**               |

### <a name="example-2-backflushing-on-production"></a>Eksempel 2: Backflushing på produksjon

Bruk innstillingene nedenfor hvis plukklistejournaler med vareforbruket for stykklisten må genereres når varer rapporteres som ferdigmeldt på produksjonsordren.

| Kategori                | Felt                          | Innstilling                             |
|--------------------|--------------------------------|-------------------------------------|
| Start              | Oppdater start online           | **Status** eller **Status + antall** |
| Start              | Automatisk stykklisteforbruk      | **Aldri**                           |
| Operations         | Automatisk stykklisteforbruk      | **Aldri**                           |
| Ferdigmeld | Automatisk stykklisteforbruk      | **Alltid**                          |
| Ferdigmeld | Oppdater ferdig rapport online | **Status + antall**               |

### <a name="example-3-flushing-principle"></a>Eksempel 3: Trekkprinsipp

Bruk innstillingene nedenfor hvis plukklistejournaler med vareforbruket for stykklisten må genereres i henhold til trekkprinsippinnstillingen for stykklistevarene.

| Kategori                | Felt                          | Innstilling                |
|--------------------|--------------------------------|------------------------|
| Start              | Oppdater start online           | **Status + antall**  |
| Start              | Automatisk stykklisteforbruk      | **Trekkprinsipp** |
| Operations         | Automatisk stykklisteforbruk      | **Trekkprinsipp** |
| Ferdigmeld | Automatisk stykklisteforbruk      | **Aldri**              |
| Ferdigmeld | Oppdater ferdig rapport online | **Status + antall**  |

### <a name="example-4-deduction-of-materials-during-startup-of-a-production-order"></a>Eksempel 4: Fradrag av materialer under oppstart av en produksjonsordre

Bruk innstillingene nedenfor hvis plukklistejournaler og vareforbruket for stykklisten må genereres når varer rapporteres når en produksjon startes.

| Kategori                | Felt                          | Innstilling                             |
|--------------------|--------------------------------|-------------------------------------|
| Start              | Oppdater start online           | **Status + antall**               |
| Start              | Automatisk stykklisteforbruk      | **Alltid**                          |
| Operations         | Automatisk stykklisteforbruk      | **Aldri**                           |
| Ferdigmeld | Automatisk stykklisteforbruk      | **Aldri**                           |
| Ferdigmeld | Oppdater ferdig rapport online | **Status** eller **Status + antall** |

Basert på valgene som er beskrevet tidligere i denne delen, posteres plukklistejournaler på ulike stadier i produksjonsordeprosessen:

- Når en operasjon startes
- Når antallstilbakemelding rapporteres for en operasjon
- Når varer rapporteres som ferdigmeldt på produksjonsordren

### <a name="example-5-manual-bom-consumption"></a>Eksempel 5: Manuell stykklisteforbruk

Du kan bruke følgende innstillinger hvis materialene alltid skal trekkes fra beholdningen manuelt. I så fall posteres ikke plukklistejournaler.


|        Kategori         |             Felt              |         Innstilling         |
|--------------------|--------------------------------|-------------------------|
|       Start        |      Oppdater start online      | <strong>Status</strong> |
|       Start        |   Automatisk stykklisteforbruk    | <strong>Aldri</strong>  |
|     Operations     |   Automatisk stykklisteforbruk    | <strong>Aldri</strong>  |
| Ferdigmeld |   Automatisk stykklisteforbruk    | <strong>Aldri</strong>  |
| Ferdigmeld | Oppdater ferdig rapport online | <strong>Status</strong> |



[!INCLUDE[footer-include](../../includes/footer-banner.md)]