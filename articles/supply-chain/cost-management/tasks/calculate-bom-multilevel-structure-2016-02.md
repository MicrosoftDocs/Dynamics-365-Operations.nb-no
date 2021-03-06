---
title: Beregne en stykkliste ved hjelp av en struktur med flere nivåer (februar 2016)
description: Denne fremgangsmåten viser hvordan du beregner kostnaden av ferdige produkter ved hjelp av nedbryting på flere nivåer som er basert på kostarket.
author: ShylaThompson
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: EcoResProductDetailsExtended, InventItemPrice, BOMCalcDialog, BOMCalcTrans
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: kamaybac
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 859f7b7c828dcdad1aa836044d2cc26847630f1e
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 04/01/2021
ms.locfileid: "5821423"
---
# <a name="calculate-a-bom-by-using-a-multilevel-structure-february-2016"></a>Beregne en stykkliste ved hjelp av en struktur med flere nivåer (februar 2016)

[!include [banner](../../includes/banner.md)]

Denne fremgangsmåten viser hvordan du beregner kostnaden av ferdige produkter ved hjelp av nedbryting på flere nivåer som er basert på kostarket. Det er den sjuende oppgaven i serien stykklisteberegning. Demonstrasjonsdatafirmaet USMF brukes til å opprette denne oppgaven.

1. Gå til Behandling av produktinformasjon > Produkter > Frigitte produkter.
2. Finn og velg ønsket post i listen.
    * Velg produkt BOM_1.  
3. Klikk på Styr kostnader i handlingsruten.
4. Klikk på Varepris.
5. Klikk på Beregn varekostnad.
    * Du må kanskje klikke ellipsen (...) for å se dette alternativet i den øverste menyen.  
6. Angi eller velg en verdi i Etterkalkuleringsversjon-feltet.
    * Velg Etterkalkuleringsversjon 20, fordi den planlagte kostnadstypen og nedbrytingsmodusen er Flere nivåer.   Modusen Nedbryting på flere nivåer gjelder for planlagte kostnader og simuleringer. Den brukes ikke for standardkostnad.  
7. Klikk på OK.
8. Klikk på Vis beregningsdetaljer.
    * Du må kanskje klikke ellipsen (...) for å se dette alternativet i den øverste menyen.  I dette tilfellet ser du hvordan BOM_2 er beregnet ved å ta hensyn til råvaren, prosessen og administrasjonskostnadene med totalt 29,40 i stedet for standardkostnad på 10 som ble aktivert i den første oppgaveveiledningen i denne serien.  
9. Klikk på fanen Kostark.
    * Går vi til fanen Kostark, er totaler per kostgruppe forskjellige sammenlignet med beregningen utført i den forrige oppgaveveiledningen.  
10. Velg Flere i Nivå-feltet.
    * Når du velger Flere, klassifiseres kostnadene i henhold til sammensetningen av BOM_2, der 10 er avledet fra M1-kostnadsgruppen (ITEM_C), og 15,60 er avledet fra produksjonen der kostgruppen er L2. Indirekte kostnader varierer også.  
11. Lukk siden.
12. Lukk siden.



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]