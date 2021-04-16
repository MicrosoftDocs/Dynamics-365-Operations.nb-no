---
title: Generere rapporter om lov om Affordable Care
description: I ACA-rapporteringen genereres skjema 1095-B og 1095-C til støtte for **Employer Mandate**-delen av Affordable Care Act.
author: andreabichsel
ms.date: 02/03/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Human Resources
ms.custom: 7521
ms.assetid: 3b953d5f-6325-4c9e-8b9b-6ab0458a73f8
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: AX 7.0.0, Human Resources
ms.openlocfilehash: 055de1f0ff3f8fd4fadba0a685fd703b9d19d918
ms.sourcegitcommit: 3cdc42346bb653c13ab33a7142dbb7969f1f6dda
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 03/31/2021
ms.locfileid: "5806000"
---
# <a name="generate-aca-reports"></a>Generere ACA-rapporter

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

I ACA-rapporteringen genereres skjema 1095-B og 1095-C til støtte for **Employer Mandate**-delen av Affordable Care Act.

> [!NOTE]
> ACA-rapportering er bare aktivert for juridiske enheter i USA.

## <a name="getting-started"></a>Komme i gang

Hvis du vil spore informasjon for 1095-B- og 1095-C-skjemaer, må du først opprette én eller flere Affordable Care-dekningsgrupper. Affordable Care-dekningsgrupper indikerer følgende:

- Tilbud om dekning for en ansatt
- Den ansattes del av den månedlige bonusen med lavest kostnad, hvis kostnaden er over den føderale fattigdomsgrensen
- Safe Harbor som brukes av arbeidsgiveren, dersom det er aktuelt

Ved å bruke Affordable Care-grupper kan du behandle informasjonen for disse feltene uten å måtte endre hver ansattpost der betingelsene er de samme. Du kan enkelt tilordne Affordable Care-dekningsgrupper til én eller flere ansatte ved hjelp av **Massetilordning**-funksjonen på siden.

## <a name="maintaining-multiple-versions-of-a-coverage-group"></a>Vedlikeholde flere versjoner av en dekningsgruppe

Du kan vedlikeholde flere versjoner av en hvilken som helst dekningsgruppe. Ved hjelp av denne funksjonaliteten kan du foreta endringer uten å måtte opprette en ny gruppe og tilordne ansatte på nytt. 

Når du har opprettet ACA-dekningsgrupper, kan du massetildele gruppene til ansatte ved hjelp av alternativet **Massetilordning**. Du kan også enkeltvis angi om du vil spore og rapportere ACA-informasjon, og tilordne en ansatt til en Affordable Care-dekningsgruppe.

Du trenger ikke å spore noe ACA-dekningsinformasjon, for eksempel for deltidsansatte. I dette tilfellet angir du **Rapportdekning**-feltet til **Nei**. Selv om du må tilordne hver ansatt med sporbar ACA-informasjon til en Affordable Care-dekningsgruppe, kan du fremdeles endre følgende alternativer for måneder med forskjellige verdier:

- **Tilbud om dekning**
- **Ansattdel av kostnad**
- **Safe harbor**

Hvis du vil angi unntak for Affordable Care-dekningsgruppenes verdier, velger du på koblingen for **Affordable Care-dekning** på siden **Arbeiderdetaljer** under delen **Mer informasjon** i kategorien **Ansettelse**.

## <a name="reporting-health-care-coverage"></a>Rapportere helsedekning

I tillegg til å spore helseforsikringsdekning som tilbys heltidsansatte, må tilleggsinformasjon rapporteres på 1095-C hvis arbeidsgiveren arbeidsgiversponset selvforsikret helsedekning som den ansatte dekkes under (uavhengig av om de jobber fulltid eller deltid). Hver ansatt (inkludert avhengige) som er dekket av arbeidsgiver-sponsede fordelsplaner, må tas med i rapporten for månedene de var dekket. 

Du kan angi om hver fordelsplan må rapporteres eller ikke, ved å merke av for **ACA-rapporterbar**.

Dessuten, hvis ansatte har valgt å dekke noen av sine avhengige under en fordel, kan du angi datoene den avhengige ble dekket, for hver ansatt, på siden **Vedlikehold fordeler**. Du angir at den avhengige dekkes inn under fordelen ved å velge **Rediger**-knappen i handlingsruten på hurtigfanen **Avhengige**.

På siden **Behandling for dekningsdato for avhengig** kan du angi datoene da den avhengige ble dekket av fordelen. Når det angis datoer på denne siden, merkes det automatisk av for **Dekket** på **Vedlikehold fordeler**-siden.

## <a name="generate-1095-b-and-1095-c-forms"></a>Generere 1095-B- og 1095-C-skjemaer

Du kan også generere 1095-B- og 1095-C-skjemaer fra produktet, og levere dem til alle ansatte. Systemet kan også generere 1095-C-skjemaer elektronisk og overføringsfilene 1094-C IRS.  

Når du genererer skjemaet 1095-C, skriver du inn i det aktuelle skatteåret og angir om personnumre skal maskeres. Hvis du skriver ut 1095-C-skjemaer for mer enn 500 ansatte, får du mer enn én PDF-fil. Det anbefales at du øker **Maksimal filstørrelse** i **Parametere for dokumentstyring**-vinduet til 150 MB.

## <a name="viewing-information"></a>Vise informasjon

Du kan bruke siden **Affordable Care-dekning for arbeidere** hvis du vil se hvilke ansatte som er tilordnet til hver dekningsgruppe, hvilke ansatte som ikke trenger å være med i en rapport, og hvilke ansatte som ikke er tilordnet.

Hvis noen av standardverdiene fra Affordable Care-dekningsgruppen har blitt overstyrt, vises en stjerne ved siden av verdien som ble endret. Hvis verdiene for alle tolv månedene er de samme, og ikke har blitt overstyrt, skrives verdien ut i **Alle 12 måneder**-kolonnen.

Du kan også bruke forespørselsvinduet til å forstå hvilke ansatte som er flagget som ikke ACA-rapporteringsbare. Du trenger ikke å spore om dekningen ble tilbudt dem, og du trenger ikke å utstede en 1095-C til dem på slutten av året. Velg **Ikke ACA-rapporterbar** i **Filtrer etter**-feltet for å generere en liste over alle ansatte som ikke vil motta 1095-C.

I tillegg kan du vise alle ansatte som ikke er tilordnet (**ACA-rapportens dekningsfelt** er tomt), eller som er knyttet til en Affordable Care-dekningsgruppe som er utløpt for året som er valgt i **År**-feltet.

Du kan eksportere lister over ansatte som ble generert ved hjelp av noen av alternativene for filtrering til Excel.

Hvis du må rapportere dekkede personer fordi du gir selvforsikret dekning, kan du vise avhengige som dekkes av fordelsplaner, som er merket som **ACA-rapporterbar**. Velg **Vis avhengig dekning** i handlingsruten.

> [!NOTE]
> Bare fordelsplaner som er merket som **ACA-rapporterbare**, vises i forespørselsvinduet.


[!INCLUDE[footer-include](../includes/footer-banner.md)]