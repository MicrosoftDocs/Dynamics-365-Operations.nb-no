---
title: "Finansrapporter for råbalanse"
description: "Denne artikkelen beskriver standardrapportene for råbalanser. Den beskriver også byggeblokker som er knyttet til disse rapportene, og hvordan du kan endre rapporter som passer dine forretningskrav."
author: twheeloc
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, AX 7.0.0, Operations, UnifiedOperations
ms.custom: 12314
ms.assetid: 3b77d6f3-fd07-41a7-9ddb-1b22d1ae33fc
ms.search.region: Global
ms.author: jcart
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: Human Translation
ms.sourcegitcommit: 869151f2486b7a481e4694cfb6992d0ee2cfc008
ms.openlocfilehash: 86e8e91f2af474999d89bb63ac9e2afad7843c8a
ms.contentlocale: nb-no
ms.lasthandoff: 06/13/2017


---

# Finansrapporter for råbalanse
<a id="trial-balance-financial-reports" class="xliff"></a>

[!include[banner](../includes/banner.md)]


Denne artikkelen beskriver standardrapportene for råbalanser. Den beskriver også byggeblokker som er knyttet til disse rapportene, og hvordan du kan endre rapporter som passer dine forretningskrav. 

Standardrapporter for råbalanse
<a id="default-trial-balance-reports" class="xliff"></a>
-----------------------------

Tre råbalanserapporter er tilgjengelige i økonomisk rapportering i Microsoft Dynamics 365 for Finance and Operations, Enterprise edition.

| Standardrapport                                 | Resultat                                                                                                                                                                                        |
|------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Detaljert råbalanse – Standard               | Inneholder saldoinformasjon for alle kontoer, og inkluderer debet- og kreditsaldoer, og nettoen av disse, sammen med transaksjonsdato, bilag og journalbeskrivelse.                  |
| Råbalansesammendrag – Standard                | Inneholder saldoinformasjon for alle kontoer, herunder åpnings- og avslutningssaldo og debet- og kreditsaldoer, sammen med deres nettoforskjell.                                        |
| Sammendrag Råbalanse Årlig – Standard | Inneholder saldoinformasjon for alle kontoer, herunder åpnings- og avslutningssaldo og debet- og kreditsaldoer, sammen med deres nettoforskjell for gjeldende og forrige år. |

## Byggeblokker
<a id="building-blocks" class="xliff"></a>
Finansrapportene for råbalanse bruker byggeblokkene nedenfor.

| Standardrapport                                 | Raddefinisjon          | Kolonnedefinisjon                              |
|------------------------------------------------|-------------------------|------------------------------------------------|
| Detaljert råbalanse – Standard               | Råbalanse – standard | Detaljert råbalanse – Standard               |
| Råbalansesammendrag – Standard                | Råbalanse – standard | Råbalansesammendrag – standard                |
| Sammendrag Råbalanse Årlig – Standard | Råbalanse – standard | Årlig råbalansesammendrag – standard |

### Raddefinisjon
<a id="row-definition" class="xliff"></a>

Raddefinisjonen, råbalanse – standard, inneholder én rad som trekker inn alle hovedkontiene. Derfor kan alle generere rapporten uten å gjøre endringer. Når du viser rapporten, kan du drille ned i hver enkelt rad for å vise detaljer om hver konto. Du kan endre raddefinisjonen slik at den inneholder flere detaljer. Hvis du vil endre raddefinisjonen Råbalanse – standard slik at den inneholder rader for alle kontoer, kan du følge fremgangsmåten nedenfor.

1.  Klikk **Rediger**, og klikk deretter **Sett inn rader fra dimensjoner**. Kommandoen **Sett inn rader fra dimensjoner** lar deg velge dimensjonene som du vil ha i raddefinisjonen. Du skal bruke **Hovedkonto** for denne raddefinisjonen.
2.  Kontroller at **Hovedkonto** inneholder bare &-tegn, og klikk deretter **OK**.

Raddefinisjonen inneholder nå alle hovedkontoene for standard juridisk enhet.

### Kolonnedefinisjon
<a id="column-definition" class="xliff"></a>

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

 

Se også
<a id="see-also" class="xliff"></a>
--------

[Finansrapportering](financial-reporting-getting-started.md)

[Vis finansrapporter](view-financial-reports.md)

[Blogg for Dynamics-finansrapportering](http://blogs.msdn.com/b/dynamics_financial_reporting/)




