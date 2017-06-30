---
title: Konvertere regnskaps- eller rapporteringsvalutaer
description: 
author: RobinARH
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: RobinARH
ms.search.scope: Core, AX 7.0.0, Operations, UnifiedOperations
ms.custom: 78223
ms.assetid: 31c56f9a-9c64-40a2-90e3-1969a760614b
ms.search.region: Global
ms.author: aolson
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: Human Translation
ms.sourcegitcommit: d421b161216d700f7819f1da8c0ca8ad089b5670
ms.openlocfilehash: 728af2fff6317c17e47d48ea07dbeb57068fbf3f
ms.contentlocale: nb-no
ms.lasthandoff: 05/25/2017


---

# <a name="convert-accounting-or-reporting-currencies"></a>Konvertere regnskaps- eller rapporteringsvalutaer

[!include[banner](../includes/banner.md)]




Et firma som må endre regnskapsvalutaen eller rapporteringsvalutaen, har to alternativer. Det første alternativet er å opprette et nytt firma, og starte på nytt. Det andre alternativet er å kjøre konverteringsprosessen for regnskaps- og rapporteringsvaluta. Dette er en svært tidkrevende prosess som endrer hver transaksjon i systemet. Det kreves også noe oppsett før prosessen kan kjøres.

## <a name="preparing-the-legal-entity-for-currency-conversion"></a>Klargjøre den juridiske enheten for valutaomregning
Før du kan konvertere den juridiske enhetens valuta, må du tilbakestille alle beløp for revaluering av utenlandsk valuta for kunde- og leverandørkontoer og lukke tidligere regnskapsår. Du må også klargjøre databasen for konverteringen, og deretter gjøre de nødvendige endringene i kontoen for den juridiske enheten som gjennomgår valutaomregningen. Når du har fullført en valutaomregning, må du fullføre noen tilleggsprosedyrer. Du må avstemme avrundingsdifferansene i omregnede beløp, beregne forretningsstatistikk på nytt, journalføre finanstransaksjonene, begrense tilgangen til konverteringsverktøyet og revaluere beløp i utenlandsk valuta for kunde- og leverandørkonti.

## <a name="setting-up-accounts-for-automatic-transactions"></a>Konfigurere kontoer for automatiske transaksjoner
Under valutaomregningsprosessen posteres fortjeneste eller tap eller øredifferanser, til kontoene som er definert på siden **Kontoer for automatiske transaksjoner**. Hovedkontoer må tilordnes til følgende typer transaksjon før konverteringsprosessen kjøres:

-   Gevinst ved omregning av regnskapsvaluta
-   Tap ved omregning av regnskapsvaluta
-   Øredifferanse i regnskapsvaluta
-   Øredifferanse i rapporteringsvaluta
-   Årets resultat

## <a name="posting-rounding-differences-and-sum-recalculations"></a>Postere avrundingsdifferanser og omberegninger
Følgende informasjon forklarer hvor forskjeller i avrunding kan oppstå:

-   Hvis produktpriser er omregnet til null, genereres det en rapport som viser produktnummeret, modultypen, prisen før omregningen og enheten.
-   Avrundingsdifferanser mellom merverdiavgift og finans posteres i økonomijournalen.
-   Beløp for revaluering av utenlandsk valuta blir omberegnet, og kunde- og leverandørtransaksjonsbeløp beregnes på nytt.
-   Kunde- og leverandørutligningsposter opprettes for avrundingsdifferansene for hver kunde- og leverandørtransaksjon.
-   Avrundingsdifferanser for kunder og leverandører posteres i økonomijournalen.
-   Utlignede kostnadsbeløp og kostnadsjusteringsbeløp i lukkede lagertransaksjoner omberegnes.
-   Avrundingsdifferanser i lagerstyring posteres i økonomijournalen.
-   Lagerbeholdning omberegnes.
-   Totalbeløp i finansjournaler beregnes.
-   Finansavslutningsark omberegnes.
-   Finanssaldoer omberegnes.
-   Avrundingsdifferanser i finans posteres i økonomijournalen.
-   Åpningstransaksjoner for finans omberegnes.
-   Det endelige beløpet i finanssaldoer beregnes.

Hvis du omregner til en ny regnskapsvaluta for finans og det oppstår en feil under omberegningen av totalbeløpene eller posteringen av avrundingsdifferansene, må du lukke siden **Konvertering av finansregnskapsvaluta**. De totale beløpene beregnes deretter på nytt og avrundingsdifferansene posteres.

## <a name="processing-the-currency-conversion"></a>Behandle valutaomregningen
Når du starter valutaomregningsprosessen, må alle brukere være logget av systemet. Du må definere den nye finans- eller rapporteringsvalutaen og valutakursene. Når du klikker **OK**, kjører prosessen og oppdaterer hver transaksjon i systemet. Valutaomregning er en lang prosess. Når den er fullført, vil du se at regnskaps- eller rapporteringsvalutaen er oppdatert på **Finans**-siden.

## <a name="completing-the-currency-conversion"></a>Fullføre valutaomregningen
Etter valutaomregningen må du generere alle avstemmingsrapporter på nytt for å være sikker på at alle omregnede beløp er riktige.

-   Hvis konverteringen av finansregnskapsvalutaen fører til avrundingsdifferanser, posteres ikke disse forskjellene ved hjelp av bilaget der avrundingsdifferansen oppstod. I stedet posteres forskjellene ved hjelp av bilaget som ble angitt for omregningsposteringene. Etter omregningen inkluderer alle rapporter som kontrollerer på bilag og dato, disse avrundingsdifferansene. Dette er riktig, og kan ignoreres.
-   Hvis avstemmingsrapportene for kunde og leverandør viser et differansebeløp på totallinjen, og ingen differansebeløp fantes før omregningen, må dette differansebeløpet posteres. Kontoen er sammendragskontoen for kunder og leverandører. Motkontoen er finanskontoen for omregningstap eller omregningsgevinst.

Når alle finanstransaksjonsjournaler er slettet, kan du journalføre finanstransaksjonene. Klikk **Økonomimodul** &gt; **Periodisk** &gt; **Journaler** &gt; **Journalføring**. Du kan revaluere beløp i utenlandsk valuta når etter valutakonverteringen hvis revaluering er nødvendig. Du kan revaluere beløp i utenlandsk valuta ved å velge **Standard** i **Metode**-feltet for revalueringen.




