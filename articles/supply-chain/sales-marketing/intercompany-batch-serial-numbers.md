---
title: Konserninterne bunke- og serienumre
description: Dette emnet forklarer hva som vil skje når du registrerer bunkenumre og serienumre for konserninterne ordrer
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
ms.openlocfilehash: 4da936263bb57c24eeb7021ac61b3945bb2777fb
ms.sourcegitcommit: fcfd85a508c0de52cfe11d1986892219e39ef406
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 09/23/2021
ms.locfileid: "7548458"
---
# <a name="intercompany-batch-and-serial-numbers"></a>Konserninterne bunke- og serienumre

[!include [banner](../../includes/banner.md)]

Firmaer som bruker serie- og/eller partinummer til å spore varene, må også holde orden på serienumrene og partinumrene for plukkede varer. Den konserninterne funksjonen automatiserer fremskyvning/tilbakestrekking av serienumre/partinumre fra ett firma til et annet. Når du registrerer parti- og serienumrene for varene i en konsernintern salgsordre, kan du konfigurere programmet til å fremskyve serie- og partinumre automatisk til konsernintern bestilling og opprinnelig salgsordre. Du definerer de relevante parameterne på **Konsernintern**-siden for salgsordren:

- Hvis du merker av i **Partinummer**-feltet på siden **Policyer for salgsordre**, synkroniseres partinummeret med lagertransaksjoner på de konserninterne bestillingslinjene når du posterer følgeseddelen for den konserninterne salgsordren.
- Hvis du merker av i **Serienummer**-feltet, synkroniseres serienumrene med lagertransaksjonene på de konserninterne bestillingslinjene når du posterer følgeseddelen for den konserninterne salgsordren.

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
