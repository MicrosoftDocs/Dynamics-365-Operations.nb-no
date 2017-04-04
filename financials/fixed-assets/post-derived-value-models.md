---
title: "Postere med avledede bøker"
description: "Denne artikkelen beskriver hvordan du bruker avledede tablåer."
author: twheeloc
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
ms.search.form: AssetBookTable, LedgerJournalTransAsset
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 3421
ms.assetid: f5187c21-eec5-4148-b178-b8a5feff7f23
ms.search.region: Global
ms.author: saraschi
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
translationtype: Human Translation
ms.sourcegitcommit: 3b16ef53f9fb57a6663db0be1f7e0a57471db2fb
ms.openlocfilehash: ca077727910059878fb16a3f78c5b9133c6c741f
ms.lasthandoff: 03/31/2017


---

# <a name="post-with-derived-books"></a>Postere med avledede bøker

Denne artikkelen beskriver hvordan du bruker avledede tablåer.

Når du posterer transaksjoner for et tablå som inneholder avledede tablåer, posteres de avledede tablåtransaksjoner automatisk i journaler, bestillinger eller fritekstfakturaer. Hvis du forbereder de primære tablåtransaksjonene i anleggsmiddeljournalen, kan du imidlertid vise og endre beløpene i de avledede transaksjonene før du posterer dem.
-   Enkelt kontoer, for eksempel mva-kontoer og kunde- eller leverandørkontoer, oppdateres bare én gang ved hjelp av posteringer av det primære tablået. De avledede tablåtransaksjonene posteres til kontoene som er definert for det avledede tablået på siden Posteringsprofiler for anleggsmidler.
-   Anskaffelse brukes ofte som transaksjonstypen for de avledede tablåene. Du bruker dette når tablået og det avledede tablået skal brukes på anleggsmiddelet fra tidspunktet anleggsmiddelet ble anskaffet.
-   Andre verdier for transaksjonstypen kan også brukes. Hvis for eksempel det primære tablået og de avledede tablåene har samme intervaller når det gjelder salg eller avhending, er alle anleggsmiddeltransaksjonstyper tilgjengelige for oppsett av et avledet tablå.

> [!WARNING]
> En avskrivning som er postert i det avledede avskrivningstablået, vil ha samme beløp som det som ble postert for det primære tablået. Hvis avskrivningsmetodene er forskjellige i tablåene, bør du ikke generere avskrivningstransaksjoner ved hjelp av den avledede prosessen. |

## <a name="example"></a>Eksempel 
Informasjonen nedenfor beskriver hvordan du kan angi avskrivningsmetoder med funksjonaliteten til det avledede tablået.

1.  Opprett tablåene på Tablåer-siden.
    -   Tablået for regnskap: VM 1, gjeldende posteringslag
    -   Tablået for skatte- og avgiftsformål: VM 2, avgiftsposteringslag

2.  På VM 1 klikker du kategorien Avledede tablåer. Velg VM 2 i Tablå-feltet og Anskaffelse i Transaksjonstype-feltet.

Tablåene kan deretter knyttes til bestemte anleggsmidler. 

Når en anskaffelse posteres for et anleggsmiddel med adresseboken VM 1, posteres anskaffelsen ikke bare på VM 1, men også på den avledede boken VM 2. Statusen for begge bøker for anleggsmiddel oppdateres til åpen.

> [!NOTE]                                                                                                         
> Hvis du ikke bruker avledede tablåer, må du postere anskaffelsen av anleggsmiddelet både for tablå VM 1 og tablå VM 2.

Hvis du vil ha mer informasjon, se [avledet bøker](derived-books.md)


