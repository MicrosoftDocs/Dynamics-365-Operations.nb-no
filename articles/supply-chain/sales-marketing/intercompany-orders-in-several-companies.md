---
title: Opprette konserninterne bestillinger og salgsordrer i flere firmaer
description: Denne artikkelen beskriver hvordan du oppretter konserninterne bestillinger eller salgsordrer i flere firmaer
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
ms.openlocfilehash: 6dce419126d60199bc11d4bd3209185ad779e979
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 06/03/2022
ms.locfileid: "8873557"
---
# <a name="creating-intercompany-purchase-and-sales-orders-in-several-companies"></a>Opprette konserninterne bestillinger og salgsordrer i flere firmaer

[!include [banner](../../includes/banner.md)]

Microsoft Dynamics 365 Supply Chain Management er ikke begrenset til håndtering av ett produksjonsselskap og flere salgsselskaper. Alle selskaper i det konserninterne oppsettet kan være handelsselskaper i tillegg til produksjonsselskaper.

Hvis flere selskaper kan levere den samme varen, kan du fritt velge hvem du vil kjøpe fra, og oppdateringer behandles selv om én salgsordre blir til flere bestillinger.

På samme som du oppretter én konsernintern bestilling automatisk, kan du opprette en opprinnelig salgsordre i selskapet, og deretter få flere konserninterne leverandørselskaper til å utføre ordren ved å opprette flere konserninterne bestillinger. Microsoft Dynamics 365 Supply Chain Management oppretter automatisk konserninterne salgsordrer i leverandørselskapene.

For å gjøre dette må alle firmaene defineres som handelsforbindelser. Leverandørselskapene må være definert i Microsoft Dynamics 365 Supply Chain Management som konserninterne leverandører, og de må være hovedleverandør for den relevante varen. I salgsordren, i **Hodevisning**, må du velge feltet **Opprett konserninterne ordrer automatisk** og feltet **Direktelevering** i hurtigfanen **Konserninterne innstillinger**. Dette er standardinnstillingen.

Du oppretter salgslinjene på vanlig måte. Når du går ut av posten, vises en melding som informerer deg om at det er opprettet konserninterne bestillinger og konserninterne salgsordrer. Meldingen inneholder også koblinger til de nye ordrene. Hvis du vil vise konserninterne salgsordrer som er opprettet i leverandørselskapene, åpner du den opprinnelige salgsordren, og i **Generelt** i gruppen **Relatert informasjon** velger du **Referanser**.

Hvis du åpner de konserninterne bestillingene for leverandørene, ser du at Microsoft Dynamics 365 Supply Chain Management automatisk fyller ut det opprinnelige salgsordrenummeret og det konserninterne salgsordrenummeret for hver leverandør.

Hvis du åpner de konserninterne salgsordrene for leverandørene, ser du tilsvarende at Microsoft Dynamics 365 Supply Chain Management automatisk fyller ut det opprinnelige salgsordrenummeret og det konserninterne bestillingsnummeret for hver leverandør.

> [!NOTE]
> Hvis varene i ordre/bestilling finnes i ett av de konserninterne leverandørselskapene, men ikke ikke i de andre, oppretter Microsoft Dynamics 365 Supply Chain Management de konserninterne ordrene for leverandørselskapet der varene finnes, men stopper ordreopprettingen for det andre selskapet. En varslingsmelding vises når dette skjer.

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
