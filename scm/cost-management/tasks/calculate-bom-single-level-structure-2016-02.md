--- 
title: "Beregne en stykkliste ved hjelp av en struktur med ett nivå (bare februar 2016)"
description: "Denne fremgangsmåten viser hvordan du beregner kostnaden av ferdige produkter ved hjelp av nedbryting på ett enkelt nivå som er basert på kostarket."
author: YuyuScheller
manager: AnnBe
ms.date: 02/07/2017
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: yuyus
ms.search.scope: Operations
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: yuyus
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 9b947a02be981155053e33a4ef20e19bf2a194a5
ms.openlocfilehash: 36096c9a0c8dde1028728ec257dfa63e7fb669af
ms.contentlocale: nb-no
ms.lasthandoff: 07/27/2017

---
# <a name="calculate-a-bom-by-using-a-single-level-structure-february-2016-only"></a>Beregne en stykkliste ved hjelp av en struktur med ett nivå (bare februar 2016)

[!include[task guide banner](../../includes/task-guide-banner.md)]

Denne fremgangsmåten viser hvordan du beregner kostnaden av ferdige produkter ved hjelp av nedbryting på ett enkelt nivå som er basert på kostarket. Dette er den sjette oppgaven i serien stykklisteberegning. Demonstrasjonsdatafirmaet USMF brukes til å opprette denne oppgaven.

1. Gå til Frigitte produkter.
2. Finn og velg ønsket post i listen.
    * Velg produkt BOM_1.  
3. Klikk Styr kostnader i handlingsruten.
4. Klikk Varepris.
5. Klikk Beregn varekostnad.
    * Du må kanskje klikke ellipsen (...) for å se dette alternativet i den øverste menyen.  
6. Klikk rullegardinknappen i feltet Etterkalkuleringsversjon for å åpne oppslaget.
    * Velg 10 for denne demonstrasjonen. Dette er den samme etterkalkuleringsversjonen som brukes til å legge til kostprisen til komponentene.  
7. Klikk OK.
8. Klikk Vis beregningsdetaljer.
    * Du må kanskje klikke ellipsen (...) for å se dette alternativet i den øverste menyen.    Her er sammensetningen av kostnaden: • 10 er avledet fra ITEM_A, 10 fra ITEM_B, 10 fra BOM_2. I dette tilfellet finnes det ingen detaljer for BOM_2 fordi det ble angitt som en standard kostnad på 10, men ikke utført gjennom beregning.  •  7 er avledet fra oppstillingstiden, som er en konstant kostnad, og ytterligere 7 er avledet fra kjøretidsoperasjonen (prosess).  •  Det finnes også andre beløp som samsvarer med indirekte kostnader.  
9. @SysTaskRecorder:_RequestClose


