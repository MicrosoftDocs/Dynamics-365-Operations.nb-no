---
title: Synkronisere konsernintern kundeinformasjon
description: Dette emnet forklarer synkronisering av kundeinformasjon for konserninterne ordrer
author: GalynaFedorova
ms.date: 09/01/2021
ms.topic: article
ms.search.form: SalesTableListPage, SalesCreateOrder, SalesTable
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: v-gfedorova
ms.search.validFrom: 2021-09-01
ms.dyn365.ops.version: 10.0.22
ms.openlocfilehash: c82216c8391f6c447bec74f25cd16b9db18d468d
ms.sourcegitcommit: fcfd85a508c0de52cfe11d1986892219e39ef406
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 09/23/2021
ms.locfileid: "7548451"
---
# <a name="synchronize-intercompany-customer-information"></a>Synkronisere konsernintern kundeinformasjon

[!include [banner](../../includes/banner.md)]

Kundeinformasjon synkroniseres hvis **Kundeinformasjon**-feltet er aktivert når salgsordren opprettes, eller når kunden, leverandørreferansen eller kunderekvisjonsnummeret endres.

Du kan alltid endre verdien i disse synkroniseringsfeltene. Du kan imidlertid bare bestemme om denne verdien kopieres til de andre konserninterne ordrene ved å velge denne parameteren. Hvis du har aktivert **Kundeinformasjon**-feltet i den konserninterne salgsordren, synkroniseres endringer i den konserninterne salgsordren med den konserninterne bestillingen. Hvis du har aktivert **Kundeinformasjon**-feltet i den konserninterne bestillingen, synkroniseres den også tilbake med den originale salgsordren.

> [!NOTE]
> Hvis du har aktivert **Kundeinformasjon**-feltet i både den konserninterne salgsordren og den konserninterne bestillingen, overstyres endringer som er utført av en person i ett firma, av oppdateringer som er utført av en annen person i et annet firma i den samme ordren.

Den beste fremgangsmåte er å aktivere **Kundeinformasjon**-feltet i den konserninterne bestillingen. Dette gjør det mulig å synkronisere den originale salgsordren med den konserninterne bestillingen og den konserninterne bestillingen med den konserninterne salgsordren.

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
