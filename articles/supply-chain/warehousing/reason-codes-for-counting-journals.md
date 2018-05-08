---
title: "Årsakskoder for lagertelling"
description: "Dette emnet beskriver hvordan du konfigurerer og bruker årsakskoder for tellingsoppgaver."
author: Mirzaab
manager: AnnBe
ms.date: 03/15/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: InventCountingReasonCodePolicy
audience: Application User
ms.reviewer: bis
ms.search.scope: Core, Operations
ms.custom: 1705903
ms.assetid: 427e01b3-4968-4cff-9b85-1717530f72e4
ms.search.region: Global
ms.author: mirzaab
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 8.0.0
ms.translationtype: HT
ms.sourcegitcommit: a8b5a5af5108744406a3d2fb84d7151baea2481b
ms.openlocfilehash: fe01425fa236655731e6e0723f3a1e57c05035cc
ms.contentlocale: nb-no
ms.lasthandoff: 04/13/2018

---

# <a name="reason-codes-for-inventory-counting"></a>Årsakskoder for lagertelling

[!include [banner](../includes/banner.md)]

Med årsakskoder kan du analysere resultatene av tellingen og eventuelle avvik som oppstår under denne prosessen. Du kan angi årsaken for å gjøre tellingen, for eksempel en skadet pall eller en lagerjustering som er basert på lagereksempler.

## <a name="recommendation"></a>Anbefaling

Før du definerer systemet, anbefaler vi at du definerer en strategi for å arbeide med årsakskoder. Du kan for eksempel prøve å svare på følgende spørsmål:

- Skal årsakskoder være obligatoriske på lagre?
- Skal årsakskoder være obligatoriske eller valgfrie for noen varer?
- Hvor mange årsakskoder trenger du?
- Hvordan skal brukerne av strekkodeskannere bruke årsakskoder? Skal årsakskodene være forhåndsvalgt, være obligatoriske eller ikke redigerbare?
- Trenger lagermedarbeidere annen årsakskodevirkemåte på mobile skannere? Hvis svaret er Ja, kan du opprette flere menyelementer og tilordne dem til forskjellige personer.

## <a name="where-reason-codes-apply"></a>Der bruke årsakskoder brukes

Du kan opprette flere årsakskodepolicyer, og hver årsakskodepolicy kan ha to årsakskodepolicyer for telling. Policyene for årsakskoder for telling kan brukes på lagernivå eller varenivå.

## <a name="set-up-reason-code-policies"></a>Definere policyer for årsakskoder

1. Velg **Lagerstyring** \> **Oppsett** \> **Lager** \> **Årsakskodepolicyer for telling**, og opprett en ny policy for årsakskoder.
2. I feltet **Årsakskodetype for telling** velger du **Obligatorisk** eller **Valgfritt** for å angi om valg av en årsakskode skal være en valgfri eller obligatorisk handling i én av følgende opptellingsjournaler:

    - Syklustelling (mobilenhet)
    - Spottelling (mobilenhet)
    - Terskeltelling (mobilenhet)
    - Justering inn (mobil enhet)
    - Justering ut (mobil enhet)
    - Opptellingsjournal (rik klient)

Du kan også definere årsakskoder for individuelle lagre og for produkter. Årsakskodeoppsettet for produkter kan se bort fra oppsettet for lagrene.

## <a name="mandatory-reason-codes"></a>Obligatoriske årsakskoder

Hvis **Obligatorisk**-parameteren er angitt i konfigurasjonen av årsakskoder for lagre eller varer, kan ikke opptellingsjournalen fullføres og lukkes før en årsakskode er angitt.

### <a name="set-up-reason-codes-for-warehouses"></a>Definere årsakskoder for lagre

1. Velg **Lagerstyring** \> **Oppsett** \> **Lageroppdeling** \> **Lagre**.
2. I **Lager**-kategorien i feltet **Årsakskodepolicy for telling**, velger du ett av følgende alternativer:

    - **Tom** -parameteren som er definert for varen, brukes til å bestemme om opptellingsjournalene er obligatoriske for produktet.
    - **Obligatorisk** – en årsakskode kreves alltid på opptellingsjournaler for lageret.
    - **Valgfri** – en årsakskode kreves ikke på opptellingsjournaler for lageret.

### <a name="set-up-reason-codes-for-products"></a>Definere årsakskoder for produkter

1. Velg **Behandling av produktinformasjon** \> **Produkter** \> **Frigitte produkter**.
2. I **Produkt**-kategorien velger du **Årsakskodepolicy for telling**, og deretter velger du ett av følgende alternativer:

    - **Tom** -parameteren som er definert for lageret, brukes til å bestemme om opptellingsjournalene er obligatoriske for produktet.
    - **Obligatorisk** – en årsakskode kreves alltid på opptellingsjournaler for produktet. Denne innstillingen overstyrer en årsakskodeinnstilling på lagernivå.
    - **Valgfri** – en årsakskode kreves ikke på opptellingsjournaler for produktet. Denne innstillingen overstyrer en årsakskodeinnstilling på lagernivå.

### <a name="use-reason-codes-in-counting-journals"></a>Bruke årsakskoder i opptellingsjournaler

I en opptellingsjournal kan du legge til årsakskoder for tellinger av følgende typer:

- Syklustelling
- Spottelling
- Terskeltelling
- Justering inn
- Justering ut

Årsakskoder legges til i journallinjene i opptellingsjournaler av typen **Opptellingsjournal**.

1. Velg **Lagerstyring** \> **Loggoppføringer** \> **Vareopptelling** \> **Opptelling**.
2. I linjedetaljene i opptellingsjournalen i feltet **Årsakskode for telling**, velger du et alternativ.

### <a name="view-the-counting-history-as-its-recorded-by-reason-codes"></a>Vise historikken opptelling slik det er registrert etter årsakskoder

- Velg **Lagerstyring** \> **Forespørsler og rapporter** \> **Opptellingslogg**, og deretter i **Årsakskode for telling**-feltet kan du vise opptellingsloggen som er registrert via en årsakskode.

### <a name="use-a-reason-code-for-a-quantity-adjustment"></a>Bruke en årsakskode for en antallsjustering

1. På **Lagerbeholdning**-siden velger du **Juster antall**. Du kan åpne **Lagerbeholdning**-siden på flere måter. Velg for eksempel **Lagerstyring** \> **Forespørsler og rapporter** \> **Lagerbeholdning**.
2. Velg **Juster antall**, og deretter i **Årsakskode for telling**, velger en årsakskode.

### <a name="configure-reason-codes-for-mobile-device-menu-items"></a>Konfigurere årsakskoder for menyelementer i mobilenheter

Du kan konfigurere årsakskoder for alle antall på et menyelement i en mobilenhet. Konfigurasjonen av menyelementet på mobilenheten omfatter følgende informasjon:

- Om årsakskoden vises for mobilenhetsmedarbeideren under opptelling.
- Standard årsakskode som vises på et menyelement for mobilenhet.
- Om brukeren kan redigere årsakskoden.

### <a name="set-up-reason-codes-on-a-mobile-device"></a>Definere årsakskoder på en mobilenhet

1. Velg **Lagerstyring** \> **Oppsett** \> **Mobilenhet** \> **Menyelementer på mobilenheten**.
2. I kategorien **Syklustelling** velger **Syklustelling**.
3. I feltet **Standard årsakskode for telling** angir du standard årsakskode som skal registreres når tellingen er utført, ved hjelp av menyelementet på mobilenheten.
4. I feltet **Vis årsakskode for telling** velger du **Linje** for å vise årsakskoden når hvert avvik er registrert. Velg eventuelt **Skjul** hvis ikke årsakskoden skal vises.
5. Sett **Rediger årsakskode for telling** til **Ja** eller **Ne***. Hvis du setter dette alternativet til **Ja**, kan medarbeideren redigere årsakskoden når den vises på mobilenheten under opptelling.

> [!NOTE]
> **Syklustelling**-knappen kan aktiveres på et menyelement for mobilenhet der telling kan utføres. Eksempel omfatter menyelementene for spottelling, brukerstyrt arbeid og systemstyrt arbeid.

## <a name="cycle-count-approvals"></a>Godkjenninger av syklustelling

Før en telling er godkjent, kan brukeren endre årsakskoden som er knyttet til opptellingen. Når tellingen er godkjent, oppføres årsakskoden på opptellingsjournallinjene.

### <a name="modify-cycle-count-approvals"></a>Endre godkjenninger av syklustelling

1. Velg **Lagerstyring** \> **Syklustelling** \> **Syklustellingsarbeid venter på gjennomgang**.
2. Velg **Syklustelling**, og deretter i **Årsakskode**-feltet, velger du en ny årsakskode.

### <a name="modify-the-mobile-device-menu-item-for-adjustment-in-and-adjustment-out"></a>Endre menyelementet for mobilenhet for justering inn og justering ut

1. Velg **Lagerstyring** \> **Oppsett** \> **Mobilenhet** \> **Menyelementer på mobilenheten**, og velg deretter **Justering inn og ut**.
2. Sett alternativet **Bruk eksisterende arbeid** til **Ja**.
3. I feltet **Arbeidsopprettelsesprosess** velger du **Justering inn**.

Følgende felt vil bli lagt til menyelementet for mobilenhet når **Justering inn** eller **Justering ut** er valgt under arbeidsopprettingen:

- Standard årsakskode for telling
- Vis årsakskode for telling
- Rediger årsakskode for telling

