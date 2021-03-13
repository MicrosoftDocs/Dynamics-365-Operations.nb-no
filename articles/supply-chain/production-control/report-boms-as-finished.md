---
title: Rapportere stykklister som ferdige
description: Denne artikkelen gir informasjon om å rapportere stykklister som ferdige.
author: johanhoffmann
manager: tfehr
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: BOMReportFinish, BOMReportFinishMax, BOMSetupReportFinish
audience: Application User
ms.reviewer: kamaybac
ms.custom: 53251
ms.assetid: 510d05a3-0073-438d-b0c4-b6a6df1882ea
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: johanho
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 0010740de764f7b9e7797cc95e2b9187cea2695b
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 01/15/2021
ms.locfileid: "5011035"
---
# <a name="report-boms-as-finished"></a>Rapportere stykklister som ferdige

[!include [banner](../includes/banner.md)]

Denne artikkelen gir informasjon om å rapportere stykklister som ferdige.

**Ferdigmeld**- og **Ferdigmeldingsmaks**-sidene brukes til å ferdigmelde stykklister. Begrepsmessig er prosessen med å rapportere en stykkliste som ferdig lik prosessen for å rapportere en produksjonsordre som ferdig. Denne prosessen kan brukes i for eksempel enkle monterings- og pakkingsprosesser der det ikke kreves mer avanserte funksjoner for produksjonsordrer. På **Ferdigmeld**-siden kan du rapportere flere stykklister som ferdige i en satsvis jobb. På **Ferdigmeldingsmaks**-siden kan du rapportere bare én stykkliste som ferdig om gangen. **Ferdigmeld**-siden er tilgjengelig fra et menyelement i Lagerstyring, og begge sidene er tilgjengelige som et menyelement på **Frigitte produkter**-siden.

## <a name="report-as-finished-page"></a>Ferdigmeld-siden
Hvis du åpner **Ferdigmeld**-siden fra et frigitt produkt, foreslår siden du kan rapportere standardantallet i standardbeholdningen som ferdigmeldt. Som standard vises den aktive stykklisteversjonen, men du kan endre stykklisteversjonen hvis det finnes andre godkjente versjoner. På siden kan du også slette poster og opprette nye poster for frigitte produkter som skal ferdigmeldes. Hvis du vil bruke en spørring til å velge produkter, klikker du **Velg**-menyelementet. Du kan manuelt bekrefte ferdigmelding for de valgte produktene ved å klikke **OK**. Du kan også angi at prosessen skal kjøres i et parti. Når ferdigmeldingsprosessen er bekreftet, genererer systemet en stykklistejournal der postering til lager behandles. Denne journalen består av ett linjeelement for det ferdige produktet og et linjeelement for hver stykklistelinje. Du kan kontrollere om journalen posteres automatisk, eller om den er åpen for flere justeringer.

## <a name="max-report-as-finished-page"></a>Maks. Ferdigmeldingsmaks-siden
På **Ferdigmeldingsmaks**-siden angir hver stykklistelinje hvor mange enheter av produktet som kan ferdigmeldes. Denne beregningen er basert på den fysisk tilgjengelige lagerbeholdningen på hver materiallinje. I eksemplet nedenfor bruker én type av varenummeret FG 2 to deler av råvare RM10 og én del av råvare RM20. Fordi det bare er 10 stykker av RM10 i beholdningen, er det maksimale antallet FG som kan ferdigmeldes, fem stykker. Denne verdien vises i **Ferdigmeldingsmaks**-feltet.

| Nivå | Varenummer | Antall | Beholdning | Maks. Ferdigmeld |
|-------|-------------|----------|---------|-------------------------|
| 0     | FG          |  1       | 0       | 5                       |
| 1     | RM10        | -2       | 10      | 5                       |
| 1     | RM20        | -1       |  8      | 8                       |

## <a name="boms-that-have-multiple-levels"></a>Stykklister med flere nivåer
Når en stykkliste har flere nivåer, kan du kontrollere hvordan materialer behandles på alle nivåer, ved å bruke **Nedbryting**-feltet. Dette feltet er tilgjengelig på både **Ferdigmeld**-siden og **Ferdigmeldingsmaks**-siden. Følgende alternativer er tilgjengelige:

-   **Aldri** – Underliggende stykklister brytes ikke ned hvis det er materialmanko.
-   **Alltid** – Alle underliggende stykklister brytes helt ned. Eventuell fri lagerbeholdning av halvferdige komponentvarer brukes derfor ikke.
-   **Manko** – Underliggende stykklister brytes bare ned hvis hele antallet av materialet du vil bruke, ikke er tilgjengelig.

### <a name="example"></a>Eksempel

I dette eksemplet kan tre deler av det ferdige produktet (varenummer FG) ferdigmeldes. Det er en stykkliste på to nivåer, som vist her.

| Nivå | Varenummer | Antall stykklistelinjer | Beholdning |
|-------|-------------|-------------------|---------|
| 0     | FG          |                   |         |
| 1     | KOMP        | 1                 | 2       |
| 1     | RM          | 1                 |         |

Følgende tabeller viser hvordan innstillingen for **Nedbryting**-feltet påvirker hvordan stykklistejournallinjer genereres. **Nedbryting: Aldri**

| Nivå | Varenummer | Antall |
|-------|-------------|----------|
| 0     | FG          | 3        |
| 1     | KOMP        | -3       |

Som tabellen ovenfor viser vurderes bare varenummeret KOMP som fratrukket i journalen. Varenummeret RM, som er en del av KOMP, brytes ikke ned til journallinjen, og de to beholdningsdelene av KOMP vurderes ikke. **Nedbryting: Alltid**

| Nivå | Varenummer | Antall |
|-------|-------------|----------|
| 0     | FG          | 3        |
| 1     | RM          | -3       |

I så fall brytes varenummer KOMP ned til råvare, varenummer RM. De to beholdningsdelene av KOMP er ikke tatt hensyn til i antallet som RM forbruker. **Nedbryting: Manko**

| Nivå | Varenummer | Antall |
|-------|-------------|----------|
| 0     | FG          | 3        |
| 1     | KOMP        | -2       |
| 1     | RM          | -1       |

I så fall vurderes de to delene for beholdning av varenummeret KOMP. Fordi det kreves tre stykk av varenummeret FG, kreves også én stykk av varenummer RM for å lage ytterligere én stykk av KOMP.



