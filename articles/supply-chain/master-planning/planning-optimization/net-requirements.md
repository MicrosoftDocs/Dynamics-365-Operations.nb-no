---
title: Nettobehov og utligningsinformasjon med planleggingsoptimalisering
description: Dette emnet gir informasjon om beregnede nettobehov og utligningsinformasjon i planleggingsoptimalisering.
author: crytt
ms.date: 7/28/2021
ms.topic: article
ms.search.form: ReqTransOverview
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: crytt
ms.search.validFrom: 2021-07-28
ms.dyn365.ops.version: 10.0.20
ms.openlocfilehash: 77b04f417e5bd8d236fa53810f9cbfe5860d9dd7
ms.sourcegitcommit: b9c2798aa994e1526d1c50726f807e6335885e1a
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 08/13/2021
ms.locfileid: "7343244"
---
# <a name="net-requirements-and-pegging-information-with-planning-optimization"></a>Nettobehov og utligningsinformasjon med planleggingsoptimalisering

[!include [banner](../../includes/banner.md)]

Når du kjører hovedplanlegging i planleggingsoptimalisering, er det viktig at du forstår resultatet, hvordan eksisterende forsyning dekker behovet og hvorfor spesifikk forsyning ble generert. Du kan bruke siden **Nettobehov** til å få en bedre forståelse av de beregnede kravene som hovedplanleggingen produserer.

**Nettobehov**-siden viser nettobehov som planleggingsoptimaliseringen beregnes for produktet. Den viser også dekningsinnstillingene som ble brukt under hovedplanleggingens kjøring, en nedbrytning av behovstotaler etter transaksjonstype og utligningsinformasjon.

## <a name="open-the-net-requirements-page"></a>Åpne siden Nettobehov

Du kan åpne siden **Nettobehov** på en av følgende måter:

- Gå til **Behandling av produktinformasjon \> Produkter \> Frigitte produkter**. Velg eller åpne et produkt. I handlingsruten, i **Plan**-fanen og **Krav**-gruppen, velger du **Nettobehov**.
- Gå til **Salg og markedsføring \> Salgsordrer \> Alle salgsordrer**. Åpne en salgsordre. I hurtigfanen **Salgsordrelinjer** på verktøylinjen velger du **Produkt og forsyning \> Nettobehov**.
- Gå til **Hovedplanlegging \> Hovedplanlegging \> Planlagte ordrer**. Velg eller åpne en planlagt ordre. I handlingsruten, i **Vis**-fanen og **Krav**-gruppen, velger du **Kravprofil**.

## <a name="use-the-net-requirements-page"></a>Bruk siden Nettobehov

Siden **Nettobehov** består av øvre og nedre del. Handlingsruten på denne siden inneholder en **Oppdater**-knapp. Når denne knappen er valgt, vises en meny med kommandoer.

### <a name="select-a-master-plan-to-view"></a>Velg en hovedplan du vil vise

Før du går gjennom nettokravene for produktet, må du passe på å velge den relevante hovedplanen i **Plan**-feltet øverst på siden.

### <a name="upper-section"></a>Øvre del

Den øvre delen av siden inneholder følgende faner:

- **Oversikt** – Vis varebehovene for produktdimensjonene.
- **Varedekning** – Vis dekningsinnstillingene som ble brukt ved beregning av behov.
- **Sammendrag** – Vis en nedbryting av behovstotalene etter transaksjonstype.
- **Periode** – Vis mottak, avganger og fremtidig tilgjengelig lagerbeholdning for hver periode som er definert av periodemalen. Du kan også få en grafisk visning av fremtidig tilgjengelig lagerbeholdning.

### <a name="lower-section"></a>Nedre del

Den nedre delen av siden inneholder følgende faner:

- **Oversikt** – Vis listen over produktbehov som ble beregnet under hovedplanleggingen, sammen med feil og mottakstransaksjoner som samsvarer med behovene. Listen sorteres som standard etter behovsdato. Når du velger et behov, viser hurtigfanen **Utligning** i den nedre delen enten kilden for behovet eller transaksjonene som oppfyller behovet.
- **Generelt** – Vis detaljert informasjon om det valgte kravet.
- **Handling** – Vis handlingsmeldinger for behovene.

### <a name="the-action-pane"></a>Handlingsruten

Følgende kommandoer er tilgjengelige i handlingsruten:

- **Oppdater \> Hovedplanlegging** – Kjør hovedplanlegging direkte fra siden **Nettobehov**.
- **Oppdater \> Prognoseplanlegging** – Kjør prognoseplanlegging direkte fra siden **Nettobehov**. Planleggingsoptimalisering støtter ennå ikke denne operasjonen.
- **Oppdater \> Kontinuitetsplanlegging** – Kjør kontinuitetsplanlegging direkte fra siden **Nettobehov**. Planleggingsoptimalisering støtter ennå ikke denne operasjonen.

## <a name="example-scenario"></a>Eksempelscenario

Dette eksemplet viser hvordan utligningsinformasjon presenteres på **Nettobehov**-siden.

### <a name="prerequisites"></a>Forutsetninger

Før du arbeider gjennom scenarioet må du klargjøre følgende forutsetninger:

1. Du må arbeide på et system der standard eksempeldata er tilgjengelige, og du må sette den juridiske enheten til *USMF*.
2. I dette eksemplet brukes produkt *1000*, som er en del av USMF-eksempeldataene. Kontroller at dette produktet er tilgjengelig, og at det er konfigurert på følgende måte:

    - **Standard ordretype:** *Bestilling*
    - **Lagerbeholdning:** *10,00*

3. Opprett en salgsordre for et antall på *25,00* og en enhetspris på *1000*. Bruk lagringsdimensjonene der lagerbeholdningen er plassert.
4. Kjøre hovedplanlegging for *DynPlan*-hovedplanen.

### <a name="review-the-calculated-requirements"></a>Se gjennom det beregnede behovet

Deretter åpner du siden **Nettobehov** for produkt *1000* for å gå gjennom hvordan beregnede krav samsvarer med hverandre.

1. Gå til **Behandling av produktinformasjon \> Produkter \> Frigitte produkter**.
1. Velg produktet som har **varenummerverdien** *1000*.
1. I handlingsruten, i **Plan**-fanen og **Krav**-gruppen, velger du **Nettobehov**.
1. På siden **Nettobehov** angir du **Plan**-feltet til *DynPlan*.
1. I fanen **Oversikt** nederst på siden kontrollerer du at følgende krav vises som rader i rutenettet:

    | Referanse | Behovsantall | Akkumulert |
    |---|---|---|
    | Beholdning | 10,00 | 10,00 |
    | Bestillingsforslag | 15.00 | 25.00 |
    | Salgsordre | –25,00 | (Tom) |

    > [!NOTE]
    > **Behovsantall**-feltet representerer det totale antallet som behovet enten krever (hvis verdien er negativ) eller forsyning (hvis verdien er positiv). **Akkumulert**-feltet representerer det totale mottaks- og avgangsantallet som har akkumulert gjennom den valgte perioden.

1. Velg *Beholdning*-kravlinjen for lagerbeholdning, og gå deretter gjennom behovene som dekkes av denne forsyningen, i hurtigfanen **Utligning**. Raden nedenfor skal vises der.

    | Referanse | Behovsantall | Dekket antall |
    |---|---|---|
    | Salgsordre | –25,00 | -10,00 |

    Den eksisterende lagerbeholdningen dekker delvis behovet som kommer fra salgsordren.

    ![Utligningsinformasjon for lagerbeholdningen](media/pegging-on-hand.png "Utligningsinformasjon for lagerbeholdningen")

1. Velg *Planlagte bestillinger*-kravlinjen for lagerbeholdning, og gå deretter gjennom behovene som dekkes av denne forsyningen, i hurtigfanen **Utligning**. Raden nedenfor skal vises der.

    | Referanse | Behovsantall | Dekket antall |
    |---|---|---|
    | Salgsordre | –25,00 | –15,00 |

    Fordi salgsordren allerede er delvis dekket, oppretter systemet et bestillingsforslag for det gjenstående uoppdagede antallet.

    ![Utligningsinformasjon for bestillingsforslaget](media/pegging-planned-purchase-order.png "Utligningsinformasjon for bestillingsforslaget")

1. Velg *Salgsordre*-kravlinjen for lagerbeholdning, og gå deretter gjennom behovene som dekkes av dette behovet, i hurtigfanen **Utligning**. Radene nedenfor skal vises der.

    | Referanse | Behovsantall | Dekket antall |
    |---|---|---|
    | Beholdning | 10,00 | 10,00 |
    | Bestillingsforslag | 15.00 | 15.00 |

    ![Utligningsinformasjon for salgsordren](media/pegging-planned-purchase-order.png "Utligningsinformasjon for salgsordren")

> [!NOTE]
> Siden planleggingsoptimalisering ennå ikke støtter noen funksjoner, er ikke behovstypene *Sikkerhetslager* og *Utløpte satsvise* inkludert på siden **Nettobehov**. Hvis du vil ha mer informasjon, se [Tilpassingsanalyse av planleggingsoptimalisering](planning-optimization-fit-analysis.md).
>
> Hvis du bruker den innebygde hovedplanleggingsmotoren, støttes partikontrollerte produkter. For partikontrollerte produkter vises utløpte lagerbeholdning på **Nettobehov**-siden, men den trenger ikke å utlignes med behovskrav. Utløpte lagerbeholdningslinjer av denne typen vises som *Utløpt parti*-kravlinjer på siden **Nettobehov**.

[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
