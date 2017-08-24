--- 
title: Livssyklus for partiordre fra oppretting til start
description: "Denne prosedyren leder deg gjennom den første delen av livssyklusen til en partiordre."
author: YuyuScheller
manager: AnnBe
ms.date: 03/02/2016
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
ms.sourcegitcommit: 55b22d246d6bfa9e8159fb844da95f61fcf07c62
ms.openlocfilehash: dcb0814ae51f5914654736a957638f7d8be81e3f
ms.contentlocale: nb-no
ms.lasthandoff: 07/28/2017

---
# <a name="batch-order-lifecycle-from-create-to-start"></a>Livssyklus for partiordre fra oppretting til start

[!include[task guide banner](../../includes/task-guide-banner.md)]

Denne prosedyren leder deg gjennom den første delen av livssyklusen til en partiordre.

Fra oppretting, kostnadsberegning og produksjonsjobbplanlegging til faktisk start av en partiordre.



Demonstrasjonsdatafirmaet USMF brukes til å opprette denne fremgangsmåten. 



Forutsetningene for å kjøre prosedyren med et annet datasett er et frigitt produkt med en aktiv formel- og ruteversjon.


## <a name="create-a-batch-order"></a>Opprette en partiordre
1. Gå til Alle produksjonsordrer.
2. Klikk Ny partiordre.
3. Angi eller velg en verdi i Varenummer-feltet.
4. Klikk Opprett.
5. Bruk hurtigfilteret til å filtrere på Produksjon-feltet med en verdi lik b.

## <a name="view-production-formula-and-expected-co-products"></a>Vise produksjonsformelen og forventede koprodukter
1. Klikk Produksjonsordre i handlingsruten.
2. Klikk Formel.
3. Lukk siden.
4. Klikk Koprodukter.
5. Lukk siden.

## <a name="estimate-the-batch-order"></a>Beregne partiordren
1. Klikk Estimer.
2. Klikk OK.
3. Klikk Styr kostnader i handlingsruten.
4. Klikk Vis beregningsdetaljer.
5. Lukk siden.

## <a name="release-the-batch-order"></a>Frigi partiordren
1. Klikk Produksjonsordre i handlingsruten.
2. Klikk Frigi.
3. Klikk OK.

## <a name="schedule-production-jobs"></a>Planlegge produksjonsjobber
1. Klikk Planlegg i handlingsruten.
2. Klikk Planlegg jobber.
3. Velg Nei i Begrenset kapasitet-feltet.
4. Velg Nei i Begrenset materiale-feltet.
5. Klikk OK.
6. Klikk Produksjonsordre i handlingsruten.
7. Klikk Alle jobber.
8. Lukk siden.

## <a name="start-the-batch-order"></a>Starte partiordren
1. Klikk Start.
2. Klikk kategorien Generelt.
3. Velg Nei i feltet Poster plukkliste nå.
4. Klikk OK.
5. Klikk Vis i handlingsruten.
6. Klikk Plukkliste.
7. Klikk koblingen i den valgte raden i listen.
8. Lukk siden.
9. Lukk siden.
10. Klikk Rutekort.
11. Klikk koblingen i den valgte raden i listen.
12. Lukk siden.
13. Lukk siden.


