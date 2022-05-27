---
title: Synkronisere konsernintern kundeinformasjon
description: Dette emnet forklarer synkronisering av kundeinformasjon for konserninterne ordrer
author: Henrikan
ms.date: 09/01/2021
ms.topic: article
ms.search.form: SalesTableListPage, SalesCreateOrder, SalesTable
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: henrikan
ms.search.validFrom: 2021-09-01
ms.dyn365.ops.version: 10.0.22
ms.openlocfilehash: 1949cb69f22ade6b0e03a02c93ad78e8b7e550ae
ms.sourcegitcommit: 9166e531ae5773f5bc3bd02501b67331cf216da4
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 05/03/2022
ms.locfileid: "8672818"
---
# <a name="synchronize-intercompany-customer-information"></a>Synkronisere konsernintern kundeinformasjon

[!include [banner](../../includes/banner.md)]

Kundeinformasjon synkroniseres hvis **Kundeinformasjon**-feltet er aktivert når salgsordren opprettes, eller når kunden, leverandørreferansen eller kunderekvisjonsnummeret endres.

Du kan alltid endre verdien i disse synkroniseringsfeltene. Du kan imidlertid bare bestemme om denne verdien kopieres til de andre konserninterne ordrene ved å velge denne parameteren. Hvis du har aktivert **Kundeinformasjon**-feltet i den konserninterne salgsordren, synkroniseres endringer i den konserninterne salgsordren med den konserninterne bestillingen. Hvis du har aktivert **Kundeinformasjon**-feltet i den konserninterne bestillingen, synkroniseres den også tilbake med den originale salgsordren.

> [!NOTE]
> Hvis du har aktivert **Kundeinformasjon**-feltet i både den konserninterne salgsordren og den konserninterne bestillingen, overstyres endringer som er utført av en person i ett firma, av oppdateringer som er utført av en annen person i et annet firma i den samme ordren.

Den beste fremgangsmåte er å aktivere **Kundeinformasjon**-feltet i den konserninterne bestillingen. Dette gjør det mulig å synkronisere den originale salgsordren med den konserninterne bestillingen og den konserninterne bestillingen med den konserninterne salgsordren.

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
