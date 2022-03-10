---
title: Beregne en stykkliste ved hjelp av en struktur med ett nivå (februar 2016)
description: Denne fremgangsmåten viser hvordan du beregner kostnaden av ferdige produkter ved hjelp av nedbryting på ett enkelt nivå som er basert på kostarket.
author: AndersGirke
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: EcoResProductDetailsExtended, InventItemPrice, BOMCalcDialog
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: aevengir
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 8c5968631f5fed8a43cd63165a4ddff86e8cb4b4
ms.sourcegitcommit: 3b87f042a7e97f72b5aa73bef186c5426b937fec
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 09/29/2021
ms.locfileid: "7572103"
---
# <a name="calculate-a-bom-by-using-a-single-level-structure-february-2016"></a>Beregne en stykkliste ved hjelp av en struktur med ett nivå (februar 2016)

[!include [banner](../../includes/banner.md)]

Denne fremgangsmåten viser hvordan du beregner kostnaden av ferdige produkter ved hjelp av nedbryting på ett enkelt nivå som er basert på kostarket. Dette er den sjette oppgaven i serien stykklisteberegning. Demonstrasjonsdatafirmaet USMF brukes til å opprette denne oppgaven.

1. Gå til Frigitte produkter.
2. Finn og velg ønsket post i listen.
    * Velg produkt BOM_1.  
3. Klikk på Styr kostnader i handlingsruten.
4. Klikk på Varepris.
5. Klikk på Beregn varekostnad.
    * Du må kanskje klikke ellipsen (...) for å se dette alternativet i den øverste menyen.  
6. Klikk på rullegardinknappen i feltet Etterkalkuleringsversjon for å åpne oppslaget.
    * Velg 10 for denne demonstrasjonen. Dette er den samme etterkalkuleringsversjonen som brukes til å legge til kostprisen til komponentene.  
7. Klikk på OK.
8. Klikk på Vis beregningsdetaljer.
    * Du må kanskje klikke ellipsen (...) for å se dette alternativet i den øverste menyen.    Her er sammensetningen av kostnaden:  *    10 er avledet fra ITEM_A, 10 fra ITEM_B, 10 fra BOM_2. I dette tilfellet finnes det ingen detaljer for BOM_2 fordi det ble angitt som en standard kostnad på 10, men ikke utført gjennom beregning.  *    7 er avledet fra oppstillingstiden, som er en konstant kostnad, og ytterligere 7 er avledet fra kjøretidsoperasjonen (prosess).  *    Det finnes også andre beløp som samsvarer med indirekte kostnader.  
9. @SysTaskRecorder:_RequestClose



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]