---
title: Livssyklus for partiordre fra oppretting til start
description: Denne prosedyren leder deg gjennom den første delen av livssyklusen til en partiordre.
author: johanhoffmann
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: ProdTableListPage, ProdTableCreate, ProdBOM, PmfProdCoBy, ProdParmCostEstimation, ProdCalcTrans, ProdParmRelease, ProdSchedule, ProdRouteJob, ProdParmStartUp, ProdJournalTransBOM, ProdJournalTransRoute
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: johanho
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: a7ca259ca8f176cd5bc76081836adcb7d272972b
ms.sourcegitcommit: 3b87f042a7e97f72b5aa73bef186c5426b937fec
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 09/29/2021
ms.locfileid: "7579262"
---
# <a name="batch-order-lifecycle-from-create-to-start"></a>Livssyklus for partiordre fra oppretting til start

[!include [banner](../../includes/banner.md)]

Denne prosedyren leder deg gjennom den første delen av livssyklusen til en partiordre.

Fra oppretting, kostnadsberegning og produksjonsjobbplanlegging til faktisk start av en partiordre.



Demonstrasjonsdatafirmaet USMF brukes til å opprette denne fremgangsmåten. 



Forutsetningene for å kjøre prosedyren med et annet datasett er et frigitt produkt med en aktiv formel- og ruteversjon.


## <a name="create-a-batch-order"></a>Opprette en partiordre
1. Gå til Alle produksjonsordrer.
2. Klikk på Ny partiordre.
3. Angi eller velg en verdi i Varenummer-feltet.
4. Klikk på Opprett.
5. Bruk hurtigfilteret til å filtrere på Produksjon-feltet med en verdi lik b.

## <a name="view-production-formula-and-expected-co-products"></a>Vise produksjonsformelen og forventede koprodukter
1. Klikk på Produksjonsordre i handlingsruten.
2. Klikk på Formel.
3. Lukk siden.
4. Klikk på Koprodukter.
5. Lukk siden.

## <a name="estimate-the-batch-order"></a>Beregne partiordren
1. Klikk på Estimer.
2. Klikk på OK.
3. Klikk på Styr kostnader i handlingsruten.
4. Klikk på Vis beregningsdetaljer.
5. Lukk siden.

## <a name="release-the-batch-order"></a>Frigi partiordren
1. Klikk på Produksjonsordre i handlingsruten.
2. Klikk på Frigi.
3. Klikk på OK.

## <a name="schedule-production-jobs"></a>Planlegge produksjonsjobber
1. Klikk på Planlegg i handlingsruten.
2. Klikk på Planlegg jobber.
3. Velg Nei i Begrenset kapasitet-feltet.
4. Velg Nei i Begrenset materiale-feltet.
5. Klikk på OK.
6. Klikk på Produksjonsordre i handlingsruten.
7. Klikk på Alle jobber.
8. Lukk siden.

## <a name="start-the-batch-order"></a>Starte partiordren
1. Klikk på Start.
2. Klikk på fanen Generelt.
3. Velg Nei i feltet Poster plukkliste nå.
4. Klikk på OK.
5. Klikk på Vis i handlingsruten.
6. Klikk på Plukkliste.
7. Klikk på koblingen i den valgte raden i listen.
8. Lukk siden.
9. Lukk siden.
10. Klikk på Rutekort.
11. Klikk på koblingen i den valgte raden i listen.
12. Lukk siden.
13. Lukk siden.



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]