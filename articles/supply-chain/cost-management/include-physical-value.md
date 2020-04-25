---
title: Ta med fysisk verdi
description: Du bruker avmerkingsboksen Ta med fysisk verdi i hurtigkategorien Lagermodell på Varemodellgrupper-siden til å angi om fysisk oppdaterte transaksjoner skal tas med i beregningen av løpende gjennomsnittlig kostpris for en vare.
author: AndersGirke
manager: tfehr
ms.date: 10/31/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: InventModelGroup
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: 79033
ms.assetid: 1928c145-bf82-436d-87ca-e7a173e31923
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: mguada
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: c6e70a40b15bf08d88958cbf3ee3e82ed63e7a48
ms.sourcegitcommit: 4f9912439ff78acf0c754d5bff972c4b85763093
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 04/02/2020
ms.locfileid: "3201738"
---
# <a name="include-physical-value"></a>Ta med fysisk verdi

[!include [banner](../includes/banner.md)]

Du bruker avmerkingsboksen Ta med fysisk verdi i hurtigkategorien Lagermodell på Varemodellgrupper-siden til å angi om fysisk oppdaterte transaksjoner skal tas med i beregningen av løpende gjennomsnittlig kostpris for en vare.

Avmerkingsboksen **Ta med fysisk verdi** har følgende verdier.

| Verdi    | Resultat                                                                                                                          |
|----------|---------------------------------------------------------------------------------------------------------------------------------|
| Valgt | Både fysisk oppdaterte transaksjoner og økonomisk oppdaterte transaksjoner brukes til å beregne løpende gjennomsnittlig kostpris. |
| Avstem  | Bare økonomisk oppdaterte transaksjoner brukes til å beregne løpende gjennomsnittlig kostpris.                                     |

Avmerkingsboksen har litt forskjellige effekter, avhengig av hvilken lagermodell du bruker.

-   Hvis du merrker av for **Ta med fysisk verdi** når du bruker lagermodellen FIFO (først inn, først ut), LIFO (sist inn, først ut) eller LIFO-dato, vil en lagerlukking også medføre justeringer i fysisk oppdaterte transaksjoner.
-   Hvis du ikke merker merket av for **Ta med fysisk verdi** når du bruker disse lagermodellene, vil lagerlukking med bare utligne transaksjoner som er økonomisk oppdatert.
-   Når du bruker lagermodellene med avveid gjennomsnitt eller avveid gjennomsnittsdato, vil lagerlukking bare utligne økonomisk oppdaterte transaksjoner, uansett om du merker av for **Ta med fysisk verdi** eller ikke.

**Eksempel 1** Du har merket av for **Ta med fysisk verdi** og mottar følgende bestillinger:

-   En bestilling av et antall på 2 og en kostpris på USD 10,00 har en oppdatert følgeseddel.
-   En bestilling av et antall på 3 og en kostpris på USD 12,00 har en oppdatert faktura.

I dette tilfellet, vil løpende gjennomsnittlig kostpris være USD 11,20 = (2x10+3x12)/(2+3), fordi både fysisk og økonomisk oppdaterte transaksjoner brukes til å beregne kostprisen. 

**Eksempel 2** Du har ikke merket av for **Ta med fysisk verdi**, og kostprisen i vareoppsettet er USD 10,00. 

-   Du mottar en bestilling av et antall på 20 og en kostpris på USD 12,00 med en oppdatert følgeseddel.

Når en salgsordre posteres, er det posterte kostbeløpet USD 10,00, fordi løpende gjennomsnittlig kostpris ikke omfatter fysisk posterte transaksjoner. 

> [!NOTE]
> For sammenligning: Hvis du merker av for **Ta med fysisk verdi** for denne varen, når en salgsordre posteres, blir det posterte kostnadsbeløpet USD 12,00.
