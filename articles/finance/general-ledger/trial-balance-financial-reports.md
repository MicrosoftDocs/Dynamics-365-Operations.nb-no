---
title: Finansrapporter for råbalanse
description: Denne artikkelen beskriver standardrapportene for råbalanser. Den beskriver også byggeblokker som er knyttet til disse rapportene, og hvordan du kan endre rapporter som passer dine forretningskrav.
author: jcart1106
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: LedgerTrialBalanceListPage
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.custom: 12314
ms.assetid: 3b77d6f3-fd07-41a7-9ddb-1b22d1ae33fc
ms.search.region: Global
ms.author: jcart
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 5fd4512b02070415b6228c91b66635815dbacaa2
ms.sourcegitcommit: 3ba95d50b8262fa0f43d4faad76adac4d05eb3ea
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 09/27/2019
ms.locfileid: "2175557"
---
# <a name="trial-balance-financial-reports"></a>Finansrapporter for råbalanse

[!include [banner](../includes/banner.md)]

Denne artikkelen beskriver standardrapportene for råbalanser. Den beskriver også byggeblokker som er knyttet til disse rapportene, og hvordan du kan endre rapporter som passer dine forretningskrav. 

<a name="default-trial-balance-reports"></a>Standardrapporter for råbalanse
-----------------------------

Tre råbalanserapporter er tilgjengelige i Finansrapportering.

| Standardrapport                                 | Resultat                                                                                                                                                                                        |
|------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Detaljert råbalanse – Standard               | Inneholder saldoinformasjon for alle kontoer, og inkluderer debet- og kreditsaldoer, og nettoen av disse, sammen med transaksjonsdato, bilag og journalbeskrivelse.                  |
| Råbalansesammendrag – Standard                | Inneholder saldoinformasjon for alle kontoer, herunder åpnings- og avslutningssaldo og debet- og kreditsaldoer, sammen med deres nettoforskjell.                                        |
| Sammendrag Råbalanse Årlig – Standard | Inneholder saldoinformasjon for alle kontoer, herunder åpnings- og avslutningssaldo og debet- og kreditsaldoer, sammen med deres nettoforskjell for gjeldende og forrige år. |

## <a name="building-blocks"></a>Byggeblokker
Finansrapportene for råbalanse bruker byggeblokkene nedenfor.

| Standardrapport                                 | Raddefinisjon          | Kolonnedefinisjon                              |
|------------------------------------------------|-------------------------|------------------------------------------------|
| Detaljert råbalanse – Standard               | Råbalanse – standard | Detaljert råbalanse – Standard               |
| Råbalansesammendrag – Standard                | Råbalanse – standard | Råbalansesammendrag – standard                |
| Sammendrag Råbalanse Årlig – Standard | Råbalanse – standard | Årlig råbalansesammendrag – standard |

### <a name="row-definition"></a>Raddefinisjon

Raddefinisjonen, råbalanse – standard, inneholder én rad som trekker inn alle hovedkontiene. Derfor kan alle generere rapporten uten å gjøre endringer. Når du viser rapporten, kan du drille ned i hver enkelt rad for å vise detaljer om hver konto. Du kan endre raddefinisjonen slik at den inneholder flere detaljer. Hvis du vil endre raddefinisjonen Råbalanse – standard slik at den inneholder rader for alle kontoer, kan du følge fremgangsmåten nedenfor.

1.  Klikk **Rediger**, og klikk deretter **Sett inn rader fra dimensjoner**. Kommandoen **Sett inn rader fra dimensjoner** lar deg velge dimensjonene som du vil ha i raddefinisjonen. Du skal bruke **Hovedkonto** for denne raddefinisjonen.
2.  Kontroller at **Hovedkonto** inneholder bare &-tegn, og klikk deretter **OK**.

Raddefinisjonen inneholder nå alle hovedkontoene for standard juridisk enhet.

### <a name="column-definition"></a>Kolonnedefinisjon

Hver rapport for råbalanse bruker en annen kolonnedefinisjon. Disse kolonnedefinisjonene inneholder ulike typer kolonner for å angi ulike nivåer av detaljer og økonomiske data.

-   **Detaljert råbalanse – standard kolonnetyper:**
    -   **DESC** – Beskrivelsen fra raddefinisjonen.
    -   **ACCT** – Kontokoder
    -   **ATTR (3)** – Attributter:
        -   Transaksjonsdato
        -   Bilag
        -   Journalbeskrivelse
    -   **FD** – Økonomiske data som inneholder bare debet
    -   **FD** – Økonomiske data som inneholder bare kredit
    -   **CALC** – Nettodifferansen
-   **Råbalansesammendrag – standard kolonnetyper:**
    -   **ACCT** – Kontokoder
    -   **DESC** – Beskrivelsen fra raddefinisjonen.
    -   **ATTR** – Et attributt:
        -   Bilag
    -   **FD** – Økonomiske data for starsaldo
    -   **FD** – Økonomiske data som inneholder bare debet
    -   **FD** – Økonomiske data som inneholder bare kredit
    -   **CALC** – Nettodifferansen
    -   **CALC** – Avslutningssaldo
-   **Årlig råbalansesammendrag – standard:**
    -   **ACCT** – Kontokoder
    -   **DESC** – Beskrivelsen fra raddefinisjonen.
    -   **ATTR** – Et attributt
        -   Bilag
    -   **FD** – Økonomiske data for startsaldo for inneværende år
    -   **FD** Økonomiske data som inneholder bare debet for inneværende år
    -   **FD** – Økonomiske data som inneholder bare kredit for inneværende år
    -   **CALC** – Nettodifferansen
    -   **CALC** – Avslutningssaldo
    -   **FD** – Økonomiske data som inneholder bare debet for forrige år
    -   **FD** – Økonomiske data som inneholder bare kredit for forrige år



<a name="additional-resources"></a>Tilleggsressurser
--------

[Finansrapportering](financial-reporting-getting-started.md)

[Vise finansrapporter](view-financial-reports.md)

[Blogg for Dynamics-finansrapportering](https://blogs.msdn.com/b/dynamics_financial_reporting/)



