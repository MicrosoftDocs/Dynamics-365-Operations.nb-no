--- 
title: "Beregne en stykkliste ved hjelp av en struktur med flere nivåer (bare februar 2016)"
description: "Denne fremgangsmåten viser hvordan du beregner kostnaden av ferdige produkter ved hjelp av nedbryting på flere nivåer som er basert på kostarket."
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
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 7e0a5d044133b917a3eb9386773205218e5c1b40
ms.openlocfilehash: 16c2cacaf70df5455c3ed49b8dcb5756e89f8cb8
ms.contentlocale: nb-no
ms.lasthandoff: 09/29/2017

---
# <a name="calculate-a-bom-by-using-a-multilevel-structure-february-2016-only"></a>Beregne en stykkliste ved hjelp av en struktur med flere nivåer (bare februar 2016)

[!INCLUDE [task guide banner](../../includes/task-guide-banner.md)]

Denne fremgangsmåten viser hvordan du beregner kostnaden av ferdige produkter ved hjelp av nedbryting på flere nivåer som er basert på kostarket. Det er den sjuende oppgaven i serien stykklisteberegning. Demonstrasjonsdatafirmaet USMF brukes til å opprette denne oppgaven.

1. Gå til Behandling av produktinformasjon > Produkter > Frigitte produkter.
2. Finn og velg ønsket post i listen.
    * Velg produkt BOM_1.  
3. Klikk Styr kostnader i handlingsruten.
4. Klikk Varepris.
5. Klikk Beregn varekostnad.
    * Du må kanskje klikke ellipsen (...) for å se dette alternativet i den øverste menyen.  
6. Angi eller velg en verdi i Etterkalkuleringsversjon-feltet.
    * Velg Etterkalkuleringsversjon 20, fordi den planlagte kostnadstypen og nedbrytingsmodusen er Flere nivåer.   Modusen Nedbryting på flere nivåer gjelder for planlagte kostnader og simuleringer. Den brukes ikke for standardkostnad.  
7. Klikk OK.
8. Klikk Vis beregningsdetaljer.
    * Du må kanskje klikke ellipsen (...) for å se dette alternativet i den øverste menyen.  I dette tilfellet ser du hvordan BOM_2 er beregnet ved å ta hensyn til råvaren, prosessen og administrasjonskostnadene med totalt 29,40 i stedet for standardkostnad på 10 som ble aktivert i den første oppgaveveiledningen i denne serien.  
9. Klikk kategorien Kostark.
    * Går vi til kategorien Kostark, er totaler per kostgruppe forskjellige sammenlignet med beregningen utført i den forrige oppgaveveiledningen.  
10. Velg Flere i Nivå-feltet.
    * Når du velger Flere, klassifiseres kostnadene i henhold til sammensetningen av BOM_2, der 10 er avledet fra M1-kostnadsgruppen (ITEM_C), og 15,60 er avledet fra produksjonen der kostgruppen er L2. Indirekte kostnader varierer også.  
11. Lukk siden.
12. Lukk siden.


