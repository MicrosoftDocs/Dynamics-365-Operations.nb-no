---
title: Definere SEPA-avtalegiromandat
description: 
author: twheeloc
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
audience: Application User
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 59491
ms.assetid: 653a135f-c515-4ae3-9da2-82b5e1f103b5
ms.search.region: Global
ms.author: mfalkner
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
translationtype: Human Translation
ms.sourcegitcommit: 114dee90b0fe525f0b3efabbf651d2804a22dd7d
ms.openlocfilehash: bb835f8dad16938b56365c7b06d4a0228f9aba66
ms.lasthandoff: 03/31/2017


---

# <a name="set-up-sepa-direct-debit-mandate"></a>Definere SEPA-avtalegiromandat



Med en SEPA-avtalegiro (Single Euro Payment Area) kan kreditor kreve inn penger fra kundens bankkonto, forutsatt at kunden har gitt kreditoren et signert mandat. Mandatet som kunden signerer, tillater kreditor å kreve betaling og instruerer kundens bank om å betale purringen. Dette emnet er organisert for å vise prosessen med å definere mandates for SEPA direkte debet.

## <a name="prerequisites"></a>Forutsetninger
Tabellen nedenfor viser forutsetninger som må være på plass før du starter.

| Kategori       | Forutsetning                                                                                                                                              |
|----------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------|
| Land/område | Primæradressen for den juridiske enheten må være i følgende land: Østerrike, Belgia, Tyskland, Spania, Frankrike, Italia eller Nederland. |

1. Angi en nummerserie for direkte debet mandates mandat hver AvtaleGiro må ha et unikt nummer. Bruk siden**Nummerserier** til å opprette en nummerserie for avtalegiromandater. Du bruker denne identifikatoren til å tilordne nummerserien til systemet for avtalegiromandat på siden **Kundeparametere**.

2. Definere kundeparametere for direkte debet mandates bruk av **Kundeparametere** siden for å definere parametere for mandates for direkte debet. Til å definere parametere, på den **direkte debet** endrer parametere du trenger. På den **nummerserier** kategorien, oppdatere den **direkte debet mandat-ID** felt med nummerserien du har angitt tidligere.

3. Definere en betalingsmåte for direkte debet mandatene du må definere en betalingsmetode for mandates for direkte debet. Du bruker denne betalingsmåten til å utføre spørringer for fakturaer du vil generere avtalegirobetaling for. Bruk siden **Betalingsmåter** til å definere betalingsmetoder. Hvis du vil definere en betalingsmåte for avtalegiromandater, må du følge disse tilleggstrinnene for en betalingsmåte:

-   I feltet **Betalingsmiddel** velger du **Elektronisk betaling**.
-   Valgfritt: Hvis du forventer at hver av kundene dine har flere mandatene, i den **perioden** feltet velger du **faktura**. Det blir opprettet en egen betaling for hver faktura og hver betaling skal bruke mandat som er angitt for fakturaen.
-   Velg **Krever mandat**-alternativet for å opprette betalinger ved hjelp av avtalegiromandater. **Krever mandat**-alternativet er bare tilgjengelig hvis du velger **Elektronisk betaling** i feltet **Betalingstype**.

Se også [direkte debet-oversikt](sepa-direct-debit-overview.md) 

