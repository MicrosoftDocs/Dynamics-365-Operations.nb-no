---
title: "Finansrapporter for råbalanse"
description: "Denne artikkelen beskriver standardrapportene for råbalanser. Den beskriver også byggeblokker som er knyttet til disse rapportene, og hvordan du kan endre rapporter som passer dine forretningskrav."
author: twheeloc
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
audience: Application User
ms.reviewer: annbe
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 12314
ms.assetid: 3b77d6f3-fd07-41a7-9ddb-1b22d1ae33fc
ms.search.region: Global
ms.author: jcart
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: Human Translation
ms.sourcegitcommit: fd3392eba3a394bd4b92112093c1f1f9b894426d
ms.openlocfilehash: ff868bcc202d74f94b6e2f9047a34d83e2ac149f
ms.contentlocale: nb-no
ms.lasthandoff: 04/25/2017


---

# <a name="trial-balance-financial-reports"></a>Finansrapporter for råbalanse

[!include[banner](../includes/banner.md)]


Denne artikkelen beskriver standardrapportene for råbalanser. Den beskriver også byggeblokker som er knyttet til disse rapportene, og hvordan du kan endre rapporter som passer dine forretningskrav. 

<a name="default-trial-balance-reports"></a>Standardrapporter for råbalanse
-----------------------------

Tre råbalanserapporter er tilgjengelige i Finansrapportering i Microsoft Dynamics AX 7.

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

 

<a name="see-also"></a>Se også
--------

[Finansrapportering](financial-reporting-getting-started.md)

[Vis finansrapporter](view-financial-reports.md)

[Blogg for Dynamics-finansrapportering](http://blogs.msdn.com/b/dynamics_financial_reporting/)




