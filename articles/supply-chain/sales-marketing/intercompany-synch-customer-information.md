---
title: Synkronisere konsernintern kundeinformasjon
description: Denne artikkelen forklarer synkronisering av kundeinformasjon for konserninterne ordrer
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
ms.openlocfilehash: a3a67c9bcf93f88375d2d4d78d87175200626d50
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 06/03/2022
ms.locfileid: "8897523"
---
# <a name="synchronize-intercompany-customer-information"></a>Synkronisere konsernintern kundeinformasjon

[!include [banner](../../includes/banner.md)]

Kundeinformasjon synkroniseres hvis **Kundeinformasjon**-feltet er aktivert når salgsordren opprettes, eller når kunden, leverandørreferansen eller kunderekvisjonsnummeret endres.

Du kan alltid endre verdien i disse synkroniseringsfeltene. Du kan imidlertid bare bestemme om denne verdien kopieres til de andre konserninterne ordrene ved å velge denne parameteren. Hvis du har aktivert **Kundeinformasjon**-feltet i den konserninterne salgsordren, synkroniseres endringer i den konserninterne salgsordren med den konserninterne bestillingen. Hvis du har aktivert **Kundeinformasjon**-feltet i den konserninterne bestillingen, synkroniseres den også tilbake med den originale salgsordren.

> [!NOTE]
> Hvis du har aktivert **Kundeinformasjon**-feltet i både den konserninterne salgsordren og den konserninterne bestillingen, overstyres endringer som er utført av en person i ett firma, av oppdateringer som er utført av en annen person i et annet firma i den samme ordren.

Den beste fremgangsmåte er å aktivere **Kundeinformasjon**-feltet i den konserninterne bestillingen. Dette gjør det mulig å synkronisere den originale salgsordren med den konserninterne bestillingen og den konserninterne bestillingen med den konserninterne salgsordren.

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
