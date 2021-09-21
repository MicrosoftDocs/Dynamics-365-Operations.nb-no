---
title: Betingelser for forretningsavtaler som ikke brukes på importerte ordrelinjer
description: Forretningsavtalepriser og -rabatter blir ikke tatt i bruk på salgs- eller bestillingslinjer som er importert via databehandling
author: kamaybac
ms.date: 05/31/2021
ms.topic: troubleshooting
ms.search.form: PurchTable, PurchTablePart, PurchRFQTable
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: yanansong
ms.search.validFrom: 2021-05-31
ms.dyn365.ops.version: 10.0.13
ms.openlocfilehash: fef38819efaff2f2a927cf09fc7f469490149574
ms.sourcegitcommit: 2d6e31648cf61abcb13362ef46a2cfb1326f0423
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 09/07/2021
ms.locfileid: "7477228"
---
# <a name="trade-agreement-conditions-arent-applied-to-imported-order-lines"></a>Betingelser for forretningsavtaler som ikke brukes på importerte ordrelinjer

## <a name="symptoms"></a>Symptomer

Forretningsavtaler som gjelder salgs- eller bestillingslinjer, brukes ikke på linjer som er importert via databehandling. De samme forretningsavtalene brukes imidlertid på salgs- eller bestillingslinjer som opprettes manuelt.

## <a name="cause"></a>Årsak

Hvis innkjøpsordrelinjer som er importert via databehandling, allerede inkluderer prisinformasjon, blir ikke forretningsavtalen evaluert på nytt for disse linjene. Hvis for eksempel **Linjerabatt i prosent** eller noen av pris- og rabattverdiene er angitt for en linje, vil det ikke bli slått opp forretningsavtaler for denne linjen.

## <a name="workaround"></a>Løsning

Denne virkemåten er forventet og er lik for både salgsordrer og bestillinger.

For å unngå dette kan du importere bestillingslinjene uten å angi prisinformasjon. Forretningsavtalene blir deretter brukt, og bestillingslinjene blir oppdatert basert på de definerte forretningsavtalene.
