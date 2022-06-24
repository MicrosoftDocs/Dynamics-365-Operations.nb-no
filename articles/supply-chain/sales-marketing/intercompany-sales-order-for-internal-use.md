---
title: Opprette en konsernintern salgsordre for intern bruk
description: Denne artikkelen forklarer hvordan du oppretter en konsernintern salgsordre til intern bruk
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
ms.openlocfilehash: a37b8ab1b3df10cdbd3bbb87410bc3dc70dc0ed0
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 06/03/2022
ms.locfileid: "8873528"
---
# <a name="create-an-intercompany-sales-order-for-internal-use"></a>Opprette en konsernintern salgsordre for intern bruk

[!include [banner](../../includes/banner.md)]

En konsernintern salgsordre opprettes vanligvis automatisk fra en konsernintern bestilling. Du kan også manuelt opprette en konsernintern salgsordre, som deretter genererer en konsernintern bestilling i den konserninterne kundens juridiske enhet.

![Konsernintern intern salgsprosess](media/intercompanyinternalsalesprocess.png)

## <a name="create-an-intercompany-sales-order-manually"></a>Opprette en konsernintern salgsordre manuelt

Gjør følgende i juridisk enhet B, som vist i illustrasjonen.

1. Gå til **Kunde \> Salgsordrer \> Alle salgsordrer**.
1. I handlingsruten velger du **Salgsordre** for å opprette salgsordre.
1. Velg en kundekonto på siden **Opprett salgsordre**. I hurtigfanen **Generelt** kontrollerer du at det er merket av for **Konsernintern**. Dette viser at den valgte kunden er en konsernintern kunde.
1. Angi eller endre informasjonen, og klikk deretter **OK**, og fyll ut ordrelinjene på vanlig måte.

    Verdien i **Leveringsadresse**-feltet kopieres fra det konserninterne salgsordrehodet til det konserninterne bestillingshodet. Verdien i **Varenummer**-feltet, inkludert produktdimensjoner, og verdiene i **Leveringsdato**- og **Valutakode**-feltet kopieres fra de konserninterne salgsordrelinjene til de konserninterne bestillingslinjene.

1. Velg **Konsernintern** i ordrehodet for å vise den relaterte konserninterne bestillingen.
1. Velg **Konsernintern** i ordrelinjene for å vise informasjon om lagerbeholdning for konsernintern handel.

> [!TIP]
> Du kan vise konserninterne salgsordrer på siden **Konserninterne ordrer**.

> [!NOTE]
> Når du arbeider med konserninterne kunder, anbefaler vi at du fjerner merket for **Slett ordre etter fakturering** på **Kundeparametere**-siden. Ellers slettes den tilknyttede bestillingen. Vi anbefaler også at du fjerner merket for **Slett bestilling etter fakturering** på **Leverandørparametere**-siden.

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
