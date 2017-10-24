---
title: Definere SEPA-avtalegiromandat
description: 
author: ShivamPandey-msft
manager: AnnBe
ms.date: 08/22/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, AX 7.0.0, Operations, UnifiedOperations
ms.custom: 59491
ms.assetid: 653a135f-c515-4ae3-9da2-82b5e1f103b5
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 7e0a5d044133b917a3eb9386773205218e5c1b40
ms.openlocfilehash: 8b50c2d585c7e0bcd8dc15aa70446cd7346ad33c
ms.contentlocale: nb-no
ms.lasthandoff: 09/29/2017

---

# <a name="set-up-sepa-direct-debit-mandate"></a>Definere SEPA-avtalegiromandat

[!include[banner](../includes/banner.md)]




Med en SEPA-avtalegiro (Single Euro Payment Area) kan kreditor kreve inn penger fra kundens bankkonto, forutsatt at kunden har gitt kreditoren et signert mandat. Mandatet som kunden signerer, tillater kreditor å kreve betaling og instruerer kundens bank om å betale purringen. Dette emnet er organisert slik at det viser prosessen med å definere SEPA-avtalegiromandater.

## <a name="prerequisites"></a>Forutsetninger
Tabellen nedenfor viser forutsetninger som må være på plass før du starter.

| Kategori       | Forutsetning                                                                                                                                              |
|----------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------|
| Land/område | Primæradressen for den juridiske enheten må være i følgende land: Østerrike, Belgia, Tyskland, Spania, Frankrike, Italia eller Nederland. |

1. Angi en nummerserie for avtalegiromandater. Hver avtalegiromandat må ha et unikt nummer. Bruk siden **Nummerserier** til å opprette en nummerserie for avtalegiromandater. Du bruker denne identifikatoren til å tilordne nummerserien til systemet for avtalegiromandat på siden **Kundeparametere**.

2. Definere kundeparametre for avtalegiromandater. Bruk siden **Kundeparametere** til å definere parametere for avtalegiromandater. For å definere parametere i kategorien **Avtalegiro** endrer du standardparameterne etter behov. I kategorien **Nummerserier** oppdaterer du feltet **ID for avtalegiromandat** med nummerserien som du tidligere definerte.

3. Definere en betalingsmåte for avtalegiromandater. Du må definere en betalingsmåte for avtalegiromandater. Du bruker denne betalingsmåten til å utføre spørringer for fakturaer du vil generere avtalegirobetaling for. Bruk siden **Betalingsmåter** til å definere betalingsmetoder. Hvis du vil definere en betalingsmåte for avtalegiromandater, må du følge disse tilleggstrinnene for en betalingsmåte:

-   I feltet **Betalingsmiddel** velger du **Elektronisk betaling**.
-   Valgfritt: Hvis du forventer at hver av kundene har flere mandater, velger du **Faktura** i **Periode**-feltet. Det blir opprettet en egen betaling for hver faktura, og hver betaling bruker mandatet som er angitt for fakturaen.
-   Velg **Krever mandat**-alternativet for å opprette betalinger ved hjelp av avtalegiromandater. **Krever mandat**-alternativet er bare tilgjengelig hvis du velger **Elektronisk betaling** i feltet **Betalingstype**.

Se også

[Oversikt over avtalegiro](sepa-direct-debit-overview.md) 

[Opprette et nytt avtalegiromandat for en kunde](tasks/create-direct-debit-mandate-customer.md) 


