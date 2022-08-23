---
title: MVA-oppgave for Norge
description: Denne artikkelen forklarer hvordan du setter opp og generere MVA-oppgaven for juridiske enheter som har en primær postadresse i Norge.
author: EricWangChen
ms.date: 03/21/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: kfend
ms.search.region: Norway
ms.author: wangchen
ms.search.validFrom: 2017-06-30
ms.dyn365.ops.version: July 2017 update
ms.openlocfilehash: 06614aead2b46825b51bb2ab900c22012ec5dabf
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 08/12/2022
ms.locfileid: "9286638"
---
# <a name="vat-statement-for-norway"></a>MVA-oppgave for Norge

[!include [banner](../includes/banner.md)]

Denne artikkelen inneholder landsspesifikk informasjon om hvordan du setter opp MVA-oppgaven (merverdiavgift) for juridiske enheter som har en primæradresse i Norge. Hvis du vil ha mer informasjon om generell MVA-rapportering, kan du se [MVA-rapportering for Europa](emea-vat-reporting.md).

> [!NOTE]
> Som en del av moderniseringen av mva-systemer innførte skatteetaten i Norge et nytt format for mva-rapportering for perioder som starter på eller etter 1. januar 2022. Mva-oppgaver for perioder før denne datoen og rettelser i disse mva-oppgavene må rapporteres i formatet som er beskrevet i denne artikkelen. Hvis du vil ha mer informasjon om det nye mva-oppgaveformatet, kan du se [Mva-oppgave med direkte innsending til Altinn](emea-nor-vat-return.md).

## <a name="set-up-sales-tax-authorities"></a>Definere skattemyndigheter
Hvis du vil generere en mva-oppgave i det riktige formatet for en bestemt skattemyndighet, må du definere rapportoppsettet for skattemyndighetene.

1. På siden **Skattemyndigheter** i feltet **Rapportoppsett** velger du **Norsk rapportformat**.
2. Velg samme skattemyndighetene for utligningsperioden for merverdiavgift som skal brukes for mva-kodene.

## <a name="set-up-sales-tax-reporting-codes"></a>Definer mva-rapporteringskoder
Følgende eksempel viser hvordan du kan definere mva-rapporteringskodene til å generere mva-oppgaven.

For brukere i juridiske enheter i Norge, kan den følgende mva-rapporteringskoder opprettet og tilordnet til mva-koder.

| Rapporteringskode | Beskrivelse                                                                        | Velg koden for rapportering i dette feltet i oppsettkategorien for rapporten eller Rapportoppsett - kreditnota-kategorien på siden for mva-koder |
|--------------|--------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------|
| 11             | Samlet omsetning utenfor merverdiavgiftsloven                                          | **Avgiftspliktig salg** eller **Avgiftsfritt salg**, avhengig av hvilken type mva |
| 31             | Innenlands omsetning og uttak, og beregnet avgift, 25 %, basis                   | **Avgiftspliktig salg** |
| 32             | Innenriks omsetning og uttak, og beregnet avgift 25 %, beregnet avgift               | **Utgående merverdiavgift** |
| 41             | Innenlands omsetning og uttak, og beregnet avgift, 15 %, basis                    | **Avgiftspliktig salg** |
| 42             | Innenriks omsetning og uttak, og beregnet avgift 15 %, beregnet avgift                | **Utgående merverdiavgift** |
| 51             | Innenlands omsetning og uttak, og beregnet avgift, 10 %, basis                   | **Avgiftspliktig salg** |
| 52             | Innenriks omsetning og uttak, og beregnet avgift 10 %, beregnet avgift               | **Utgående merverdiavgift** |
| 61             | Innenlands omsetning og uttak fritatt for merverdiavgift, basis                                 | **Avgiftspliktig salg** |
| 71             | Innenlands omsetning med omvendt avgiftsplikt, basis     | **Avgiftspliktig import** |
| 72             | Innenlands omsetning med omvendt avgiftsplikt, beregnet avgift | **Use tax** |
| 81             | Utførsel av varer og tjenester fritatt for merverdiavgift, basis               | **Avgiftsfritt salg** |
| 91             | Innførsel av varer, og beregnet avgift, 25 %, basis                                    | **Avgiftspliktig import** |
| 92             | Innførsel av varer, og beregnet avgift, 25 %, beregnet avgift                                | **Use tax**         |
| 93             | Motregning for 92                                                                  | **Motregning av use tax**         |
| 101            | Innførsel av varer, og beregnet avgift, 15 %, basis                                    | **Avgiftspliktig import** |
| 102            | Innførsel av varer, og beregnet avgift, 15 %, beregnet avgift                                | **Use tax** |
| 103            | Motregning for 102                                                                 | **Motregning av use tax** |
| 111            | Innførsel av varer som det ikke skal beregnes merverdiavgift av, basis                                          | **Avgiftsfritt kjøp** |
| 121            | Tjenester kjøpt fra utlandet, og beregnet avgift, 25 %, basis        | **Avgiftspliktig import** |
| 122            | Tjenester kjøpt fra utlandet, og beregnet avgift, 25 %, beregnet avgift    | **Use tax** |
| 123            | Motregning for 122                                                                 | **Motregning av use tax** |
| 131            | Innenlands kjøp av varer og tjenester, og beregnet avgift, 25 %, basis       | **Avgiftspliktig import** |
| 132            | Innenlands kjøp av varer og tjenester, og beregnet avgift, 25 %, beregnet avgift   | **Use tax** |
| 133            | Motregning for 132                                                                 | **Motregning av use tax** |
| 142            | Fradragsberettiget innenlandsk inngående avgift, 25%, beregnet. avgift                                     | **Inngående merverdiavgift** |
| 152            | Fradragsberettiget innenlandsk inngående avgift, 15%, beregnet. avgift                                     | **Inngående merverdiavgift** |
| 162            | Fradragsberettiget innenlandsk inngående avgift, 10%, beregnet. avgift                                     | **Inngående merverdiavgift** |
| 172            | Fradragsberettiget innførselsavgift, 25%, beregnet. avgift                                             | **Motregning av use tax** hvis du ikke bruker rapporteringskodene 93, 123 eller 133. |
| 182            | Fradragsberettiget innførselsavgift, 15%, beregnet. avgift                                             | **Motregning av use tax** hvis du ikke bruker rapporteringskode 103. |

## <a name="set-up-the-sales-tax-period-code"></a>Definere koden for mva-perioden
Opprett en liste over perioder på siden **Mva-utligningsperioder**. I feltet **Kode for merverdiavgiftsperiode** angir du periodekoder i henhold til innsendingsperiodene. Disse periodekodene må være rettet inn mot verdiene som angitt av skattemyndighetene. Verdiene i dette feltet brukes når det genereres en XML-fil.

Her er et eksempel for rapportering hver andre måned.

|             Periode               | Kode for merverdiavgiftsperiode |
|----------------------------------|-----------------------|
| Første periode – januar/februar  | 014                   |
| Andre periode – mars/april      | 024                   |
| Tredje periode – mai/juni          | 034                   |
| Fjerde periode – juli/august      | 044                   |
| Femte periode – september/oktober | 054                   |
| Sjette periode – november/desember | 064                   |

## <a name="configure-the-er-model-and-format-for-the-report"></a>Konfigurere ER modellen og formatet for rapporten
Hvis du vil kontrollere eller endre rapporteringsformatene, må du bruke elektronisk rapporteringsfunksjonalitet (ER). Du kan finne MVA-oppgaveformatet for juridiske enheter som har en primæradresse i Norge i på siden **Konfigurasjoner** (**Organisasjonsstyring** > **Elektronisk rapportering** > **Konfigurasjoner**). I treet for ER-modeller utvider du noden **MVA-deklarerasjonsmodell** og velger deretter **MVA-deklarasjon (NO)**.

Du kan bruke utformingen for å vise eller endre konfigurasjonen du valgte i modelltreet. For mer informasjon, se [Elektronisk rapportering](../../fin-ops-core/dev-itpro/analytics/general-electronic-reporting.md).

> [!NOTE]
> Samme MVA-deklarasjonsmodell brukes for Østerrike, Tsjekkia, Estland, Finland, Latvia, Litauen og Norge. Denne modellen samler avgiftsdata som kreves for MVA-deklarerasjonen.

## <a name="generate-the-vat-statement"></a>Generere MVA-oppgaven
1. På siden **Rapporter merverdiavgift for utligningsperioden** angir du verdier i feltene **Utligningsperiode**, **Fra-dato**, og **Mva-betalingsversjon**.
2. Klikk **OK**.
3. I feltet **Formattilordning** velger du ett av følgende alternativer:

    - **VAT-deklarasjon (NO)** – Generer en XML-fil.
    - **Mva-rapport (NO)** – Skriv ut rapporten i Microsoft Excel.

4. Før XML-filen kan opprettes, må du angi verdier i følgende felt:

    - **Meldingstype** – Velg **Hoved**, **Tillegg** eller **Korrigering**.
    - **KID-nummer**
    - **Bransjetype**
    - **Forklaring**
  
### <a name="create-a-report-after-a-sales-tax-payment-update"></a>Opprette en rapport etter en mva-betalingsoppdatering
1. På siden **MVA-betalinger** velger du aktuelle bilag og klikker deretter **Eksporter MVA-fil**.
2. I feltet **Formattilordning** velger du ett av følgende alternativer for å angi typen utdatafil:

    - **VAT-deklarasjon (NO)** – Generer en XML-fil.
    - **Mva-rapport (NO)** – Skriv ut rapporten i Microsoft Excel.

> [!NOTE]
> Du kan kombinere flere mva-betalinger og skrive ut én kombinert rapport/XML-fil som inneholder summerte data for alle valgte oppføringer. Du kan kombinere bare poster som er knyttet til en utligningsperiode, og som har samme verdier for **Fra-dato** og **Til-dato**. Du kan for eksempel kombinere en **Originalversjon**-post med dens **Rettelser/Siste rettelser**-post.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
