---
title: Elektroniske finanskonsolideringer
description: Denne artikkelen beskriver elektroniske finanskonsolideringer i Økonomimodul.
author: aprilolson
ms.date: 12/07/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: twheeloc
ms.search.region: Global
ms.author: aolson
ms.search.validFrom: 2018-5-31
ms.dyn365.ops.version: 8.0.1
ms.openlocfilehash: 5843ac78adf32e738d9882c7f4e9e04a79200700
ms.sourcegitcommit: bdee5e642d417a13abdb778c14ec5f2dbbf8dee7
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 12/09/2022
ms.locfileid: "9838286"
---
# <a name="online-financial-consolidations"></a>Elektroniske finanskonsolideringer

[!include [banner](../includes/banner.md)]

Denne artikkelen beskriver elektroniske finanskonsolideringer i Økonomimodul. Før du leser denne artikkelen, må du lese artikkelen [Oversikt over finanskonsolideringer og valutaomveksling](financial-consolidations-currency-translation.md).

Når du har fullført oppsettet, du angir detaljer om konsolideringer på siden **Konsolider [Online]**. Når du er ferdig, kan du klikke **OK** eller **Parti** for å behandle konsolideringen.

## <a name="criteria"></a>Vilkår
I kategorien **Vilkår** på siden **Konsolider [Online]** definerer du kontoene, periodene og typen data som konsolideres.

![Kategorien Kriterier.](./media/criteria-consolidate-online.png "Kategorien Kriterier")

Her er en forklaring på feltene i denne kategorien:

- **Beskrivelse** – Angi en nøyaktig beskrivelse av perioden som du konsoliderer.
- **Hovedkonto** – Bruk feltene i denne delen til å definere hovedkontoene som skal behandles.

    - **Fra** og **Til** – Angi et kontoområde som skal behandles. Hvis du lar disse feltene stå tomme, vil alle kontoer fra alle firmaer bli flyttet til det konsoliderte selskapet. Hvis du konsoliderer fire firmaer og hvert firma har en annen kontoplan, vil derfor alle kontoer fra alle fire firmaer opprettes i det konsoliderte selskapet.
    - **Bruk konsolideringskonto** – Hvis du setter dette alternativet til **Ja**, blir feltet **Velg konsolideringskonto fra** tilgjengelig. I dette feltet velger du om alle kontoer skal konsolideres til konsolideringskontoen som er angitt på siden **Hovedkontoer**, eller om du vil velge kontoen fra én av konsolideringskontogruppene.
    - **Konsolideringskontogruppe** – Velg gruppen du vil bruke for hovedkontotilordningen for konsolideringen.

- **Konsolideringsperiode** – Bruk feltene i denne delen til å definere konsolideringsperioden.

    - **Fra** og **Til** – Angi et datoområde for konsolidering. Hvis du lar disse feltene stå tomme, behandles konsolideringen for alle perioder som er definert i Finans for firmaet. Vi anbefaler ikke at du ikke lar disse feltene stå tomme.
    - **Velg konsolideringsbeløpet fra** – Bruk dette feltet til å angi om regnskapsvalutabeløpene eller rapporteringsvalutabeløpene fra kildefirmaene skal brukes til å oppdatere regnskapsvalutabeløpene i konsolideringsfirmaet.

        - Velg **Regnskapsvaluta** for å bruke regnskapsvalutabeløpene fra kildefirmaene til å oppdatere regnskapsvalutabeløpene i konsolideringsfirmaet. Når denne verdien er valgt, bruker du feltet **Konsolider regnskapsvaluta** til å definere hvordan regnskapsvalutaene i konsolideringsfirmaet skal beregnes.
        - Velg **Rapporteringsvaluta** for å bruke rapporteringsvalutabeløpene fra kildefirmaene til å beregne regnskapsvalutabeløpene i konsolideringsfirmaet.

            - Hvis rapporteringsvalutaen fra kildefirmaet er den samme som regnskapsvalutaen for konsolideringsfirmaet, kopieres rapporteringsvalutabeløpene fra kildefirmaet til konsolideringsfirmaet.
            - Hvis rapporteringsvalutaen fra kildefirmaet er forskjellig fra regnskapsvalutaen til konsolideringsfirmaet, omregnes verdiene ved hjelp av utvekslingsinformasjonen som er definert i fanen **Valutaomregning** på denne siden, for å beregne verdiene i konsolideringsfirmaet.

    - **Konsolider regnskapsvaluta** – Dette feltet er bare tilgjengelig hvis feltet **Velg konsolideringsbeløp fra** er satt til **Regnskapsvaluta**. Bruk det til å angi om regnskapsvalutabeløpene fra kildefirmaene skal omregnes via valutakurser eller kopieres til konsolideringsfirmaet. Velg **Bruk valutaomregning** til å bruke valutakursinformasjonen som er definert i fanen **Valutaomregning** til å beregne saldoene i konsolideringsregnskapet. Velg **Bruk regnskapsvalutabeløp** for å kopiere regnskapsvalutabeløpene fra kildefirmaene til konsolideringsfirmaet.

        - Hvis regnskapsvalutaen fra kildefirmaet er den samme som regnskapsvalutaen for konsolideringsfirmaet, kopieres valutabeløpene fra kildefirmaet til konsolideringsfirmaet.
        - Hvis regnskapsvalutaen fra kildefirmaet er forskjellig fra regnskapsvalutaen til konsolideringsfirmaet, omregnes verdiene ved hjelp av utvekslingsinformasjonen som er definert i fanen **Valutaomregning**, for å beregne verdiene i konsolideringsfirmaet.

    - **Inkluder faktiske beløp** – Sett dette alternativet til **Ja** for å konsolidere de faktiske dataene.
    - **Inkluder budsjettbeløp** – Sett dette alternativet til **Ja** for å konsolidere data fra budsjettregisteret.
    - **Bygg saldoer på nytt under konsolideringsprosessen** – Vi anbefaler ikke at du setter dette alternativet til **Ja**. I stedet gjenoppbygging saldoer som en egen satsvis jobb.

- **Budsjettmodeller** – Hvis du har valgt å konsoliderer budsjettdata, kan du bruke feltene i denne delen til å definere budsjettmodellene.

    - **Fra** og **Til** – Angi modellområdet som skal brukes.
    - **Budsjettsatstype** – Velg typen budsjettsats som skal brukes for omregning av valuta i budsjettdata.

## <a name="financial-dimensions"></a>Finansdimensjoner
I kategorien **Finansdimensjoner** kan du angi hvilke dimensjoner som skal inkluderes i konsolideringsfirmaet. Hvis du vil velge en dimensjon, kan du angi feltet **Spesifikasjon** til **Dimensjon** og deretter definere rekkefølgen på dimensjonen i konsolideringsfirmaet.

![Kategorien Finansdimensjoner.](./media/financial-dimensions-cons.png "Kategorien Finansdimensjoner")

Uavhengig av hvilken rekkefølge du definerer, blir **Hovedkonto** alltid det første segmentet.

## <a name="legal-entities"></a>Juridiske enheter
I kategorien **Juridiske enheter** kan du angi hvilke firmaer som skal inkluderes i konsolideringsfirmaet. Du kan også definere eierskapsprosenten for disse firmaene. Hvis du angir mindre enn 100 prosent eierskap, blir den angitte prosenten rullet opp til konsolideringsfirmaet. For eventuelle oversettelsesforskjeller brukes feltet **Kontotypen for konverteringsavvik** til å velge hovedkontoen fra oppsettet på siden **Kontoer for automatiske transaksjoner**.

![Kategorien Juridiske enheter.](./media/legal-entities-cons.png "Kategorien Juridiske enheter")

![Siden Kontoer for automatiske transaksjoner.](./media/accounts-for-automatic-cons.png "Siden Kontoer for automatiske transaksjoner")

## <a name="elimination"></a>Eliminering
I kategorien **Eliminering** har du tre alternativer for behandling av elimineringer:

- Velg elimineringsregelen, og deretter i feltet **Forslagsalternativer** velger du **Bare forslag**. Dette alternativet behandler elimineringen i løpet av konsolideringsprosessen, men bokfører ikke alt i ett trinn. Du kan også postere journalen senere.
- Velg elimineringsregelen, og deretter i feltet **Forslagsalternativer** velger du **Bare poster**. Dette alternativet behandler elimineringen i løpet av konsolideringsprosessen, og bokfører alt i ett trinn.
- Kjør et elimineringsforslag separat fra konsolideringsprosessen ved hjelp av elimineringsjournalen.

![Kategorien Eliminering.](./media/elimination-cons-onl.png "Kategorien Eliminering")

Hvis du vil ha mer informasjon om elimineringer, kan du se [Elimineringsregler](./elimination-rules.md).

## <a name="currency-translation"></a>Valutaveksling
I kategorien **Valutaveksling** definerer du juridisk enhet, konto, valutakurstype og -sats. Hvis konsolideringsfirmaet er tildelt andre hovedkontoer enn kildefirmaet, må konsolideringsfirmaets hovedkonto angis i feltene **Fra dato** og **Til dato**, ikke kildefirmaets hovedkontoer. For hver rad i juridisk enhet og hovedkontoer er tre alternativer tilgjengelige i feltet **Bruk valutakurs fra**:

- **Konsolideringsdato** – Datoen som er definert i **Konsolideringsperiode til**-feltet i fanen **Kriterier** for konsolideringen, brukes til å få valutakursen. Denne satsen tilsvarer spotkursen eller kursen ved månedsslutt. Du ser en forhåndsvisning av satsen, men du kan ikke redigere den.
- **Transaksjonsdato** – Datoen for hver transaksjon brukes til å velge en valutakurs. Dette alternativet brukes oftest for anleggsmidler og omtales ofte som en historisk kurs. Du får ikke en forhåndsvisning av satsen, fordi det vil være mange satser for de ulike transaksjonene i kontoområdet.
- **Brukerdefinert sats** – Når du velger dette alternativet, kan du angi valutakursen som du vil bruke. Dette alternativet kan være nyttig for gjennomsnittlige valutakurser eller hvis du konsoliderer mot en fast valutakurs.

![Kategorien Valutaveksling.](./media/currency-translation-cons-online.png "Kategorien Valutaveksling")

## <a name="additional-resources"></a>Tilleggsressurser

Hvis du vil ha mer informasjon om konsolidering og valutavekslinger, kan du se den overordnede artikkelen i denne artikkelen, [Oversikt over finanskonsolideringer og valutaomveksling](./financial-consolidations-currency-translation.md).

For informasjon om situasjoner der du kan generere konsoliderte regnskapsoppgjør, kan du se [Generere konsoliderte regnskapsoppgjør](./generating-consolidated-financial-statements.md).


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
